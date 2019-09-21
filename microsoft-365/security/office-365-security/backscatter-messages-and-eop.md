---
title: Messages de rétrodiffusion et EOP
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 12/9/2016
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 6f64f2de-d626-48ed-8084-03cc72301aa4
ms.collection:
- M365-security-compliance
description: La rétrodiffusion désigne l’envoi automatisé de messages non remis par des serveurs de messagerie, généralement à la suite de la détection d’un courrier indésirable entrant. La liste rouge DNS Backscatterer est une liste d'adresses IP qui envoient des messages de rétrodiffusion. Il ne s'agit pas d'une liste d'expéditeurs de courriers indésirables et nous n'essayons pas de retirer nos serveurs de la liste rouge DNS Backscatterer.
ms.openlocfilehash: e8a8f98045d111976078b09797a1078d0fbb6a6b
ms.sourcegitcommit: 1162d676b036449ea4220de8a6642165190e3398
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/20/2019
ms.locfileid: "37079475"
---
# <a name="backscatter-messages-and-eop"></a><span data-ttu-id="b9ae7-105">Messages de rétrodiffusion et EOP</span><span class="sxs-lookup"><span data-stu-id="b9ae7-105">Backscatter messages and EOP</span></span>

<span data-ttu-id="b9ae7-p102">La rétrodiffusion désigne l'envoi automatisé de messages non remis par des serveurs de messagerie, généralement à la suite de la détection d'un courrier indésirable entrant. Comme Exchange Online Protection (EOP) est un service de filtrage de courriers indésirables, les messages électroniques envoyés à des destinataires inexistants et vers d'autres destinations suspectes sont rejetés par notre service. Dans ce cas, EOP génère un rapport de non-remise (NDR), qu'il renvoie à l'« émetteur ». Étant donné que les expéditeurs de courriers indésirables utilisent souvent une adresse « De » factice ou non valide dans leurs messages, il est possible que l'adresse de l'expéditeur à qui le rapport NDR est envoyé génère un message de rétrodiffusion. Dans ce cas, les serveurs sortants associés au réseau EOP peuvent être répertoriés sur la liste rouge DNS Backscatterer (DNSBL). La liste rouge DNS Backscatterer est une liste d'adresses IP qui envoient des messages de rétrodiffusion. Il ne s'agit pas d'une liste d'expéditeurs de courriers indésirables et nous n'essayons pas de retirer nos serveurs de la liste rouge DNS Backscatterer.</span><span class="sxs-lookup"><span data-stu-id="b9ae7-p102">Backscatter messages are the automated bounce messages that are sent by mail servers, typically as a result of incoming spam. Because Exchange Online Protection (EOP) is a spam filtering service, email messages sent to nonexistent recipients and to other suspicious destinations are rejected by our service. When this happens, EOP generates a non-delivery report (NDR) message and delivers it back to the "sender." Because spammers frequently use a forged or invalid "From" address in their messages, the sender address to which the NDR is sent may result in a backscatter message. When this happens, outgoing servers that are associated with the EOP network may be listed on the Backscatterer DNS Block List (DNSBL). The Backscatterer DNSBL is a list of IP addresses that send backscatter messages. It isn't a spammer list, and we don't try to remove our servers from the Backscatterer DNSBL.</span></span> 
  
> [!TIP]
> <span data-ttu-id="b9ae7-p103">Selon les instructions figurant sur le site web Backscatterer, l'utilisation du mode de rejet pour tous les messages entrants n'est pas une configuration ou une utilisation recommandée de ce service. Il doit plutôt être utilisé en mode sécurisé. Pour plus d'informations sur la mise en œuvre de la configuration de rétrodiffusion appropriée, consultez le site web [Backscatterer.org](http://www.backscatterer.org/?target=usage).</span><span class="sxs-lookup"><span data-stu-id="b9ae7-p103">According to the instructions on the Backscatterer website, the use of reject mode for all incoming mail isn't a recommended configuration or use of that service. It should be used in safe mode instead. For more information about implementing the correct backscatter configuration, visit the [Backscatterer.org website](http://www.backscatterer.org/?target=usage).</span></span> 
  
## <a name="related-topics"></a><span data-ttu-id="b9ae7-116">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="b9ae7-116">Related topics</span></span>
  
[<span data-ttu-id="b9ae7-117">Options de filtrage avancé du courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="b9ae7-117">Advanced spam filtering  options</span></span>](advanced-spam-filtering-asf-options.md)
  

