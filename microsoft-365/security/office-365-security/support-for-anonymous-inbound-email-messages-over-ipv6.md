---
title: Prise en charge des messages entrants anonymes sur IPv6
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: b68df621-0a5f-4824-8abc-41e0c4fd1398
ms.collection:
- M365-security-compliance
description: Découvrez comment configurer la prise en charge des messages anonymes provenant de sources IPv6 pour Exchange Online Protection et Exchange Online.
ms.openlocfilehash: c29c1fa450ca2a2e213930c4f4a394aaf462e31d
ms.sourcegitcommit: 70e920f76526f47fc849df615de4569e0ac2f4be
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/07/2019
ms.locfileid: "38031989"
---
# <a name="support-for-anonymous-inbound-email-messages-over-ipv6"></a><span data-ttu-id="08a01-103">Prise en charge des messages entrants anonymes sur IPv6</span><span class="sxs-lookup"><span data-stu-id="08a01-103">Support for anonymous inbound email messages over IPv6</span></span>

<span data-ttu-id="08a01-104">Exchange Online Protection (EOP) et Exchange Online prennent en charge la réception de messages électroniques entrants anonymes dans le cadre de communications IPv6 provenant d'expéditeurs qui n'envoient pas de messages via le protocole TLS (Transport Layer Security).</span><span class="sxs-lookup"><span data-stu-id="08a01-104">Exchange Online Protection (EOP) and Exchange Online support receiving anonymous inbound email messages over IPv6 communications from senders who don't send messages over Transport Layer Security (TLS).</span></span> <span data-ttu-id="08a01-105">Vous pouvez vous abonner pour recevoir des messages via IPv6 en demandant cette fonctionnalité au support Microsoft en ouvrant le centre d’administration Microsoft [https://admin.microsoft.com/adminportal/home](https://admin.microsoft.com/adminportal/home)365 à l’adresse, en cliquant sur **support**, puis en cliquant sur **nouvelle demande de service**).</span><span class="sxs-lookup"><span data-stu-id="08a01-105">You can opt-in to receive messages over IPv6 by requesting this functionality from Microsoft Support by opening the Microsoft 365 admin center at [https://admin.microsoft.com/adminportal/home](https://admin.microsoft.com/adminportal/home), clicking **Support**, and then clicking **New service request**).</span></span> <span data-ttu-id="08a01-106">Si vous refusez les communications IPv6, vous continuerez à recevoir vos messages via le protocole IPv4.</span><span class="sxs-lookup"><span data-stu-id="08a01-106">If you don't opt-in to IPv6 you'll continue to receive messages over IPv4.</span></span>
  
<span data-ttu-id="08a01-107">Les expéditeurs qui transmettent des messages au service sur IPv6 doivent respecter les deux conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="08a01-107">Senders who transmit messages to the service over IPv6 must comply with the following two requirements:</span></span>
  
1. <span data-ttu-id="08a01-108">L'adresse IPv6 d'envoi doit posséder un enregistrement PTR valide ([enregistrement DNS inversé](https://en.wikipedia.org/wiki/Reverse_DNS_lookup) de l'adresse IPv6 d'envoi).</span><span class="sxs-lookup"><span data-stu-id="08a01-108">The sending IPv6 address must have a valid PTR record ([reverse DNS record](https://en.wikipedia.org/wiki/Reverse_DNS_lookup) of the sending IPv6 address).</span></span> 
    
2. <span data-ttu-id="08a01-109">L'expéditeur doit répondre aux exigences de l'étape de vérification SPF (définie dans le fichier [RFC 7208](https://tools.ietf.org/html/rfc7208)) ou de l'étape de [vérification DKIM](https://dkim.org/) (définie dans le fichier [RFC 6376](https://www.rfc-editor.org/rfc/rfc6376.txt)).</span><span class="sxs-lookup"><span data-stu-id="08a01-109">The sender must pass either SPF verification (defined in [RFC 7208](https://tools.ietf.org/html/rfc7208)) or [DKIM verification](https://dkim.org/) (defined in [RFC 6376](https://www.rfc-editor.org/rfc/rfc6376.txt)).</span></span>
    
<span data-ttu-id="08a01-p102">Quelle que soit votre configuration, vous devez remplir ces conditions pour utiliser IPv6. Si ces deux conditions sont remplies, le message est traité par le processus normal de filtrage des courriers électroniques proposé par le service. Si l'une ou l'autre de ces conditions n'est pas remplie, le message est rejeté et l'une des réponses 450 suivantes apparaît :</span><span class="sxs-lookup"><span data-stu-id="08a01-p102">Meeting these requirements is mandatory regardless of your configuration prior to opting-in to IPv6. If both requirements are met, the message will go through normal email message filtering provided by the service. If one or the other isn't met, the message will be rejected with one of the following 450 responses:</span></span>
  
-  `450 4.7.25 Service unavailable, sending IPv6 address [2a01:111:f200:2004::240] must have reverse DNS record.`
    
-  `450 4.7.26 Service unavailable, message sent over IPv6 [2a01:111:f200:2004::240] must pass either SPF or DKIM validation.`
    
<span data-ttu-id="08a01-113">Si vous n'avez pas accepté de recevoir des messages sur IPv6 et que l'expéditeur tente de forcer l'envoi d'un message sur IPv6 en se connectant manuellement au serveur de messagerie, le message sera rejeté et une réponse 550 de ce type apparaîtra :</span><span class="sxs-lookup"><span data-stu-id="08a01-113">If you aren't opted in to receive messages over IPv6 and the sender tries to force a message over IPv6 by manually connecting to the mail server, the message will be rejected with a 550 response that looks similar to the following:</span></span>
  
 `550 5.2.1 Service unavailable, [contoso.com] does not accept email over IPv6.`
  
## <a name="for-more-information"></a><span data-ttu-id="08a01-114">Pour plus d'informations</span><span class="sxs-lookup"><span data-stu-id="08a01-114">For more information</span></span>

[<span data-ttu-id="08a01-115">Prise en charge de la validation des messages signés DKIM</span><span class="sxs-lookup"><span data-stu-id="08a01-115">Support for validation of DKIM signed messages</span></span>](support-for-validation-of-dkim-signed-messages.md)
  

