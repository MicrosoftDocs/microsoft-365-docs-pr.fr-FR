---
title: Vue du flux de messagerie sortant et entrant dans le tableau de bord de flux de messagerie
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: f2738dec-41b0-43c4-b814-84c0a4e45c6d
description: Les administrateurs peuvent en savoir plus sur le flux de messages entrants et sortants dans le tableau de bord de flux de messagerie dans le centre de sécurité & conformité.
ms.openlocfilehash: 33bfe3882c274fa655d17c80aba007e8d246b250
ms.sourcegitcommit: c083602dda3cdcb5b58cb8aa070d77019075f765
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/22/2020
ms.locfileid: "48199300"
---
# <a name="outbound-and-inbound-mail-flow-insight-in-the-security--compliance-center"></a><span data-ttu-id="d8e7a-103">Vue du flux de messagerie sortant et entrant dans le centre de sécurité & conformité</span><span class="sxs-lookup"><span data-stu-id="d8e7a-103">Outbound and inbound mail flow insight in the Security & Compliance Center</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


<span data-ttu-id="d8e7a-104">L’analyse du **flux de messagerie sortant et entrant** dans le [tableau de bord de flux de messagerie](mail-flow-insights-v2.md) dans le centre de [sécurité & conformité](https://protection.office.com) combine les informations du [rapport de connecteur](view-mail-flow-reports.md#connector-report) et de l’ancien **rapport de vue d’ensemble TLS** à un seul emplacement.</span><span class="sxs-lookup"><span data-stu-id="d8e7a-104">The **Outbound and inbound mail flow** insight in the [Mail flow dashboard](mail-flow-insights-v2.md) in the [Security & Compliance Center](https://protection.office.com) combines the information from the [Connector report](view-mail-flow-reports.md#connector-report) and the former **TLS overview report** in one place.</span></span>

<span data-ttu-id="d8e7a-105">Le widget affiche le chiffrement TLS utilisé pour la connexion lors de la remise de messages à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="d8e7a-105">The widget displays the TLS encryption that's used for the connection when messages are delivered to and from your organization.</span></span> <span data-ttu-id="d8e7a-106">Les connexions établies avec d’autres services de messagerie sont chiffrées par TLS lorsque TLS est offert par les deux côtés.</span><span class="sxs-lookup"><span data-stu-id="d8e7a-106">The connections that are established with other email services are encrypted by TLS when TLS is offered by both sides.</span></span> <span data-ttu-id="d8e7a-107">Le widget offre un instantané de la dernière semaine du flux de messagerie.</span><span class="sxs-lookup"><span data-stu-id="d8e7a-107">The widget offers a snapshot of the last week of mail flow.</span></span>

![Widget flux de messagerie sortant et entrant dans le tableau de bord de flux de messagerie dans le centre de sécurité & conformité](../../media/mfi-outbound-and-inbound-mail-flow-report-widget.png)

<span data-ttu-id="d8e7a-109">Les informations contenues dans le widget sont liées aux connecteurs et à la protection des messages TLS dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="d8e7a-109">The information in the widget is related to connectors and TLS message protection in Microsoft 365.</span></span> <span data-ttu-id="d8e7a-110">Pour plus d'informations, voir les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="d8e7a-110">For more information, see these topics:</span></span>

- [<span data-ttu-id="d8e7a-111">Configurer le flux de messagerie à l’aide des connecteurs</span><span class="sxs-lookup"><span data-stu-id="d8e7a-111">Configure mail flow using connectors</span></span>](https://docs.microsoft.com/exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/use-connectors-to-configure-mail-flow)
- [<span data-ttu-id="d8e7a-112">Utilisation de TLS par Exchange Online pour sécuriser les connexions de messagerie</span><span class="sxs-lookup"><span data-stu-id="d8e7a-112">How Exchange Online uses TLS to secure email connections</span></span>](https://docs.microsoft.com/microsoft-365/compliance/exchange-online-uses-tls-to-secure-email-connections)
- [<span data-ttu-id="d8e7a-113">Informations de référence technique sur le chiffrement dans Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="d8e7a-113">Technical reference details about encryption in Microsoft 365</span></span>](https://docs.microsoft.com/microsoft-365/compliance/technical-reference-details-about-encryption)

## <a name="message-protected-in-transit-by-tls"></a><span data-ttu-id="d8e7a-114">Message protégé en transit (par TLS)</span><span class="sxs-lookup"><span data-stu-id="d8e7a-114">Message protected in transit (by TLS)</span></span>

<span data-ttu-id="d8e7a-115">Lorsque vous cliquez sur **afficher les détails** dans le widget, le menu volant **message protégé en transit (par TLS)** vous indique la protection TLS pour les messages entrants et sortants de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="d8e7a-115">When you click **View Details** on the widget, the **Message protected in transit (by TLS)** flyout shows you the TLS protection for messages entering and leaving your organization.</span></span>

![Messages de la fenêtre mobile protected in transit (par TLS) qui s’affiche une fois que vous avez cliqué sur Afficher les détails dans le widget courrier électronique entrant et sortant](../../media/mfi-outbound-and-inbound-mail-flow-report-details.png)

<span data-ttu-id="d8e7a-117">Actuellement, TLS 1,2 est la version la plus sécurisée de TLS offerte par Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="d8e7a-117">Currently, TLS 1.2 is the most secure version of TLS that's offered by Microsoft 365.</span></span> <span data-ttu-id="d8e7a-118">En règle générale, vous devez déterminer le chiffrement TLS utilisé pour les audits de conformité.</span><span class="sxs-lookup"><span data-stu-id="d8e7a-118">Often, you'll need to know the TLS encryption that's being used for compliance audits.</span></span> <span data-ttu-id="d8e7a-119">Vous n’avez probablement pas de relation directe avec la plupart des serveurs de messagerie source et de destination (vous n’êtes pas propriétaire, ni Microsoft), de sorte que vous n’avez pas de nombreuses options pour améliorer le chiffrement TLS utilisé par ces serveurs.</span><span class="sxs-lookup"><span data-stu-id="d8e7a-119">You probably don't have a direct relationship with most of the source and destination email servers (you don't own them, and neither does Microsoft), so you don't have many options to improve the TLS encryption that's used by those servers.</span></span>

<span data-ttu-id="d8e7a-120">Toutefois, vous pouvez utiliser des [connecteurs](https://docs.microsoft.com/exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/use-connectors-to-configure-mail-flow) pour garantir la meilleure protection TLS disponible pour les messages échangés entre vos serveurs de messagerie et Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="d8e7a-120">But, you can use [connectors](https://docs.microsoft.com/exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/use-connectors-to-configure-mail-flow) to ensure the best available TLS protection for messages that are sent between your email servers and Microsoft 365.</span></span> <span data-ttu-id="d8e7a-121">Le flux de messagerie entre Microsoft 365 et vos propres serveurs de messagerie ou serveurs qui appartiennent à vos partenaires est souvent plus important et plus sensible que les messages normaux, de sorte que vous souhaitez appliquer une sécurité supplémentaire et la vigilance de ces messages.</span><span class="sxs-lookup"><span data-stu-id="d8e7a-121">Mail flow between Microsoft 365 and your own email servers or servers that belong to your partners is often more important and sensitive than regular messages, so you'll want to apply extra security and vigilance to those messages.</span></span>

<span data-ttu-id="d8e7a-122">Vous pouvez mettre à niveau ou réparer vos propres serveurs de messagerie pour améliorer le chiffrement TLS utilisé ou contacter vos partenaires pour qu’ils effectuent la même opération.</span><span class="sxs-lookup"><span data-stu-id="d8e7a-122">You can upgrade or fix your own email servers to improve the TLS encryption that's being used, or reach out to your partners to do the same.</span></span> <span data-ttu-id="d8e7a-123">Le **rapport de connecteur** affiche le volume de flux de messagerie et le chiffrement TLS pour les messages qui utilisent vos connecteurs Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="d8e7a-123">The **Connector Report** displays both mail flow volume and TLS encryption for messages that use your Microsoft 365 connectors.</span></span>

<span data-ttu-id="d8e7a-124">Vous pouvez cliquer sur le lien du **rapport de connecteur** pour accéder au [rapport du connecteur](view-mail-flow-reports.md#connector-report).</span><span class="sxs-lookup"><span data-stu-id="d8e7a-124">You can click the **Connector report** link to go to the [Connector report](view-mail-flow-reports.md#connector-report).</span></span> <span data-ttu-id="d8e7a-125">Les informations suivantes peuvent être disponibles sur la page de **rapport du connecteur** si la condition associée a été détectée :</span><span class="sxs-lookup"><span data-stu-id="d8e7a-125">The following insights might be available on the **Connector report** page if the associated condition has been detected:</span></span>

- <span data-ttu-id="d8e7a-126">**Le connecteur de partenaire entrant voit un flux de messagerie TLS 1.0 important**</span><span class="sxs-lookup"><span data-stu-id="d8e7a-126">**Inbound Partner connector seeing significant TLS1.0 mail flow**</span></span>
- <span data-ttu-id="d8e7a-127">**Connecteur OnPremises entrant présentant un flux de messagerie TLS 1.0 important**</span><span class="sxs-lookup"><span data-stu-id="d8e7a-127">**Inbound OnPremises connector seeing significant TLS1.0 mail flow**</span></span>

<span data-ttu-id="d8e7a-128">Pour les connexions 1,0 TLS, vous devez vraiment obtenir votre serveur de messagerie ou le serveur de votre partenaire mis à niveau ou résolu afin d’éviter tout problème lorsque la prise en charge de TLS 1,0 est finalement déconseillée dans Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="d8e7a-128">For TLS 1.0 connections, you really need to get your email server or your partner's server upgraded or fixed to avoid any issues when TLS 1.0 support is eventually deprecated in Microsoft 365.</span></span>

## <a name="see-also"></a><span data-ttu-id="d8e7a-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8e7a-129">See also</span></span>

<span data-ttu-id="d8e7a-130">Pour plus d’informations sur les autres informations du tableau de bord de flux de messagerie, consultez [la rubrique mail Flow Insights in the Security & Compliance Center](mail-flow-insights-v2.md).</span><span class="sxs-lookup"><span data-stu-id="d8e7a-130">For information about other insights in the Mail flow dashboard, see [Mail flow insights in the Security & Compliance Center](mail-flow-insights-v2.md).</span></span>
