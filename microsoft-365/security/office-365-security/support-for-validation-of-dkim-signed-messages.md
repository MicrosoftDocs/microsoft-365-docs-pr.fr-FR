---
title: Prise en charge de la validation des messages signés DKIM
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
ms.openlocfilehash: bb02e558c7aaf07a7b13ec0bdb237a9ab84220f4
ms.sourcegitcommit: 2468bcb01625f97a322459814d81b9faad717859
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/05/2019
ms.locfileid: "39871230"
---
# <a name="support-for-validation-of-dkim-signed-messages"></a><span data-ttu-id="f72dd-103">Prise en charge de la validation des messages signés DKIM</span><span class="sxs-lookup"><span data-stu-id="f72dd-103">Support for validation of DKIM signed messages</span></span>

<span data-ttu-id="f72dd-104">Exchange Online Protection (EOP) et Exchange Online prennent en charge la validation entrante des messages DKIM ([Domain Keys Identified Mail](https://www.rfc-editor.org/rfc/rfc6376.txt)).</span><span class="sxs-lookup"><span data-stu-id="f72dd-104">Exchange Online Protection (EOP) and Exchange Online support inbound validation of Domain Keys Identified Mail ([DKIM](https://www.rfc-editor.org/rfc/rfc6376.txt)) messages.</span></span> <span data-ttu-id="f72dd-105">Il s'agit d'une méthode de validation des messages envoyés depuis le domaine dont ils indiquent provenir et qui n'ont pas été usurpés par un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f72dd-105">DKIM is a method for validating that a message was sent from the domain it says it originated from and that it was not spoofed by someone else.</span></span> <span data-ttu-id="f72dd-106">Elle associe un message électronique à l'organisation responsable de son envoi.</span><span class="sxs-lookup"><span data-stu-id="f72dd-106">It ties an email message to the organization responsible for sending it.</span></span> <span data-ttu-id="f72dd-107">La vérification DKIM est automatiquement utilisée pour tous les messages envoyés dans le cadre de communications IPv6.</span><span class="sxs-lookup"><span data-stu-id="f72dd-107">DKIM verification is automatically used for all messages sent over IPv6 communications.</span></span> <span data-ttu-id="f72dd-108">Office 365 prend également en charge DKIM lorsque le courrier électronique est envoyé via IPv4.</span><span class="sxs-lookup"><span data-stu-id="f72dd-108">Office 365 also now supports DKIM when mail is sent over IPv4.</span></span> <span data-ttu-id="f72dd-109">(Pour plus d'informations sur la prise en charge d'IPv6, voir [Prise en charge des messages entrants anonymes sur IPv6](support-for-anonymous-inbound-email-messages-over-ipv6.md).)</span><span class="sxs-lookup"><span data-stu-id="f72dd-109">(For more information about IPv6 support, see [Support for anonymous inbound email messages over IPv6](support-for-anonymous-inbound-email-messages-over-ipv6.md).)</span></span>

<span data-ttu-id="f72dd-p102">La technologie DKIM valide un message signé numériquement qui apparaît dans l'en-tête réservé à la signature DKIM au niveau des en-têtes de message. Les résultats d'une validation par signature DKIM sont intégrés à l'en-tête des résultats d'authentification, conformément à la norme RFC 7001 ([champ de l'en-tête du message permettant d'indiquer le statut d'authentification du message](https://www.rfc-editor.org/rfc/rfc7001.txt)). Le texte de l'en-tête du message ressemble à peu près à ce qui suit (où contoso.com correspond à l'expéditeur) :</span><span class="sxs-lookup"><span data-stu-id="f72dd-p102">DKIM validates a digitally signed message that appears in the DKIM-Signature header in the message headers. The results of a DKIM-Signature validation is stamped in the Authentication-Results header which conforms with RFC 7001 ([Message Header Field for Indicating Message Authentication Status](https://www.rfc-editor.org/rfc/rfc7001.txt)). The message header text appears similar to the following (where contoso.com is the sender):</span></span>

 `Authentication-Results: <contoso.com>; dkim=pass (signature was verified) header.d=example.com;`

<span data-ttu-id="f72dd-113">Les administrateurs peuvent créer des [règles de flux de messagerie](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/mail-flow-rules) Exchange (également appelées règles de transport) sur les résultats d’une validation DKIM pour filtrer ou acheminer les messages selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="f72dd-113">Admins can create Exchange [mail flow rules](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/mail-flow-rules) (also known as transport rules) on the results of a DKIM validation to filter or route messages as needed.</span></span>
