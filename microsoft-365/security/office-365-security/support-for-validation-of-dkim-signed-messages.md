---
title: Prise en charge de la validation des messages signés DKIM (Domain Keys Identified Mail)
f1.keywords:
- NOCSH
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
audience: ITPro
ms.topic: article
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: a4c95148-a00c-4d12-85ed-88520b547d97
ms.collection:
- M365-security-compliance
description: En savoir plus sur la validation des messages signés DKIM dans Exchange Online Protection et Exchange Online
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 8695e25000390cf6c5d58adf63db1984c873d75b
ms.sourcegitcommit: dcb97fbfdae52960ae62b6faa707a05358193ed5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2021
ms.locfileid: "51204629"
---
# <a name="support-for-validation-of-dkim-signed-messages"></a><span data-ttu-id="94a65-103">Prise en charge de la validation des messages signés DKIM</span><span class="sxs-lookup"><span data-stu-id="94a65-103">Support for validation of DKIM signed messages</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="94a65-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="94a65-104">**Applies to**</span></span>
- [<span data-ttu-id="94a65-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="94a65-105">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="94a65-106">Microsoft Defender pour Office 365 : offre 1 et offre 2</span><span class="sxs-lookup"><span data-stu-id="94a65-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](defender-for-office-365.md)
- [<span data-ttu-id="94a65-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="94a65-107">Microsoft 365 Defender</span></span>](../defender/microsoft-365-defender.md)

<span data-ttu-id="94a65-108">Exchange Online Protection (EOP) et Exchange Online la validation entrante des messages[DKIM](https://www.rfc-editor.org/rfc/rfc6376.txt)(Domain Keys Identified Mail).</span><span class="sxs-lookup"><span data-stu-id="94a65-108">Exchange Online Protection (EOP) and Exchange Online both support inbound validation of Domain Keys Identified Mail ([DKIM](https://www.rfc-editor.org/rfc/rfc6376.txt)) messages.</span></span>

<span data-ttu-id="94a65-109">DKIM confirme qu’un message  électronique n’a pas été usurpé par  une autre personne et qu’il a été envoyé à partir du domaine dont il indique qu’il est issu.</span><span class="sxs-lookup"><span data-stu-id="94a65-109">DKIM validates that an email message wasn't *spoofed* by someone else, and was sent from the domain it *says* it came from.</span></span> <span data-ttu-id="94a65-110">Il lie un message électronique à l’organisation qui l’a envoyé.</span><span class="sxs-lookup"><span data-stu-id="94a65-110">It ties an email message to the organization that sent it.</span></span> <span data-ttu-id="94a65-111">La vérification DKIM est utilisée automatiquement pour tous les messages envoyés avec IPv6.</span><span class="sxs-lookup"><span data-stu-id="94a65-111">DKIM verification is used automatically for all messages sent with IPv6.</span></span> <span data-ttu-id="94a65-112">Microsoft 365 prend également en charge DKIM lorsque le courrier est envoyé sur IPv4.</span><span class="sxs-lookup"><span data-stu-id="94a65-112">Microsoft 365 also supports DKIM when mail is sent over IPv4.</span></span> <span data-ttu-id="94a65-113">(Pour plus d'informations sur la prise en charge d'IPv6, voir [Prise en charge des messages entrants anonymes sur IPv6](support-for-anonymous-inbound-email-messages-over-ipv6.md).)</span><span class="sxs-lookup"><span data-stu-id="94a65-113">(For more information about IPv6 support, see [Support for anonymous inbound email messages over IPv6](support-for-anonymous-inbound-email-messages-over-ipv6.md).)</span></span>

<span data-ttu-id="94a65-114">DKIM valide un message signé numériquement qui apparaît dans l'DKIM-Signature'en-tête des en-têtes de message.</span><span class="sxs-lookup"><span data-stu-id="94a65-114">DKIM validates a digitally signed message that appears in the DKIM-Signature header of the message headers.</span></span> <span data-ttu-id="94a65-115">Les résultats d’une validation DKIM-Signature sont marqués dans l’en-tête Authentication-Results'un autre.</span><span class="sxs-lookup"><span data-stu-id="94a65-115">The results of a DKIM-Signature validation are stamped in the Authentication-Results header.</span></span> <span data-ttu-id="94a65-116">Le texte de l'en-tête du message ressemble à peu près à ce qui suit (où contoso.com correspond à l'expéditeur) :</span><span class="sxs-lookup"><span data-stu-id="94a65-116">The message header text appears similar to the following (where contoso.com is the sender):</span></span>

 `Authentication-Results: <contoso.com>; dkim=pass (signature was verified) header.d=example.com;`

> [!NOTE]
> <span data-ttu-id="94a65-117">Pour plus d’informations sur Authentication-Results'en-tête, voir RFC 7001 ([Message Header Field for Indicating Message Authentication Status](https://www.rfc-editor.org/rfc/rfc7001.txt).</span><span class="sxs-lookup"><span data-stu-id="94a65-117">For more information about the Authentication-Results header, see RFC 7001 ([Message Header Field for Indicating Message Authentication Status](https://www.rfc-editor.org/rfc/rfc7001.txt).</span></span> <span data-ttu-id="94a65-118">L’implémentation DKIM de Microsoft est conforme à cette RFC.</span><span class="sxs-lookup"><span data-stu-id="94a65-118">Microsoft's DKIM implementation conforms with this RFC.</span></span>

<span data-ttu-id="94a65-119">Les administrateurs peuvent créer des Exchange [de flux](/exchange/security-and-compliance/mail-flow-rules/mail-flow-rules) de messagerie (également appelées règles de transport) sur les résultats de la validation DKIM.</span><span class="sxs-lookup"><span data-stu-id="94a65-119">Admins can create Exchange [mail flow rules](/exchange/security-and-compliance/mail-flow-rules/mail-flow-rules) (also known as transport rules) on the results of DKIM validation.</span></span> <span data-ttu-id="94a65-120">Ces règles de flux de messagerie permettront aux administrateurs de filtrer ou d’router les messages selon les besoins.</span><span class="sxs-lookup"><span data-stu-id="94a65-120">These mail flow rules will allow admins to filter or route messages as needed.</span></span>