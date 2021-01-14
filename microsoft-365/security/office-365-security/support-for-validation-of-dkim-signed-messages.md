---
title: Prise en charge de la validation des messages signés DKIM (Domain Keys Identified Mail)
f1.keywords:
- NOCSH
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: a4c95148-a00c-4d12-85ed-88520b547d97
ms.collection:
- M365-security-compliance
description: En savoir plus sur la validation des messages signés DKIM dans Exchange Online Protection et Exchange Online
ms.openlocfilehash: 91a01f89bb633a38d27ddd3f2945b8707643d7e9
ms.sourcegitcommit: 89097fb648987567b9493b9d94c85c5990562874
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/13/2021
ms.locfileid: "49845058"
---
# <a name="support-for-validation-of-dkim-signed-messages"></a><span data-ttu-id="2ff2e-103">Prise en charge de la validation des messages signés DKIM</span><span class="sxs-lookup"><span data-stu-id="2ff2e-103">Support for validation of DKIM signed messages</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="2ff2e-104">Exchange Online Protection (EOP) et Exchange Online peuvent tous deux assurer la validation entrante des messages[DKIM](https://www.rfc-editor.org/rfc/rfc6376.txt)(Domain Keys Identified Mail).</span><span class="sxs-lookup"><span data-stu-id="2ff2e-104">Exchange Online Protection (EOP) and Exchange Online both support inbound validation of Domain Keys Identified Mail ([DKIM](https://www.rfc-editor.org/rfc/rfc6376.txt)) messages.</span></span>

<span data-ttu-id="2ff2e-105">DKIM confirme qu’un message  électronique n’a pas été usurpé par  une autre personne et qu’il a été envoyé à partir du domaine dont il indique qu’il est issu.</span><span class="sxs-lookup"><span data-stu-id="2ff2e-105">DKIM validates that an email message wasn't *spoofed* by someone else, and was sent from the domain it *says* it came from.</span></span> <span data-ttu-id="2ff2e-106">Il lie un message électronique à l’organisation qui l’a envoyé.</span><span class="sxs-lookup"><span data-stu-id="2ff2e-106">It ties an email message to the organization that sent it.</span></span> <span data-ttu-id="2ff2e-107">La vérification DKIM est utilisée automatiquement pour tous les messages envoyés avec IPv6.</span><span class="sxs-lookup"><span data-stu-id="2ff2e-107">DKIM verification is used automatically for all messages sent with IPv6.</span></span> <span data-ttu-id="2ff2e-108">Microsoft 365 prend également en charge DKIM lorsque le courrier électronique est envoyé sur IPv4.</span><span class="sxs-lookup"><span data-stu-id="2ff2e-108">Microsoft 365 also supports DKIM when mail is sent over IPv4.</span></span> <span data-ttu-id="2ff2e-109">(Pour plus d'informations sur la prise en charge d'IPv6, voir [Prise en charge des messages entrants anonymes sur IPv6](support-for-anonymous-inbound-email-messages-over-ipv6.md).)</span><span class="sxs-lookup"><span data-stu-id="2ff2e-109">(For more information about IPv6 support, see [Support for anonymous inbound email messages over IPv6](support-for-anonymous-inbound-email-messages-over-ipv6.md).)</span></span>

<span data-ttu-id="2ff2e-110">DKIM valide un message signé numériquement qui apparaît dans l'DKIM-Signature'en-tête des en-têtes de message.</span><span class="sxs-lookup"><span data-stu-id="2ff2e-110">DKIM validates a digitally signed message that appears in the DKIM-Signature header of the message headers.</span></span> <span data-ttu-id="2ff2e-111">Les résultats d’une validation DKIM-Signature sont marqués dans l’en-tête Authentication-Results'un autre.</span><span class="sxs-lookup"><span data-stu-id="2ff2e-111">The results of a DKIM-Signature validation are stamped in the Authentication-Results header.</span></span> <span data-ttu-id="2ff2e-112">Le texte de l'en-tête du message ressemble à peu près à ce qui suit (où contoso.com correspond à l'expéditeur) :</span><span class="sxs-lookup"><span data-stu-id="2ff2e-112">The message header text appears similar to the following (where contoso.com is the sender):</span></span>

 `Authentication-Results: <contoso.com>; dkim=pass (signature was verified) header.d=example.com;`

> [!NOTE]
> <span data-ttu-id="2ff2e-113">Pour plus d’informations sur Authentication-Results'en-tête, voir RFC 7001 ([Message Header Field for Indicating Message Authentication Status](https://www.rfc-editor.org/rfc/rfc7001.txt).</span><span class="sxs-lookup"><span data-stu-id="2ff2e-113">For more information about the Authentication-Results header, see RFC 7001 ([Message Header Field for Indicating Message Authentication Status](https://www.rfc-editor.org/rfc/rfc7001.txt).</span></span> <span data-ttu-id="2ff2e-114">L’implémentation DKIM de Microsoft est conforme à cette RFC.</span><span class="sxs-lookup"><span data-stu-id="2ff2e-114">Microsoft's DKIM implementation conforms with this RFC.</span></span>

<span data-ttu-id="2ff2e-115">Les administrateurs peuvent créer des règles de [flux](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/mail-flow-rules) de messagerie Exchange (également appelées règles de transport) sur les résultats de la validation DKIM.</span><span class="sxs-lookup"><span data-stu-id="2ff2e-115">Admins can create Exchange [mail flow rules](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/mail-flow-rules) (also known as transport rules) on the results of DKIM validation.</span></span> <span data-ttu-id="2ff2e-116">Ces règles de flux de messagerie permettront aux administrateurs de filtrer ou d’router les messages selon les besoins.</span><span class="sxs-lookup"><span data-stu-id="2ff2e-116">These mail flow rules will allow admins to filter or route messages as needed.</span></span>
