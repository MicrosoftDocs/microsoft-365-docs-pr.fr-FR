---
title: Rétrodiffusion et EOP
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 6f64f2de-d626-48ed-8084-03cc72301aa4
ms.collection:
- M365-security-compliance
description: Rétrodiffusion est un message de retour automatique qui est envoyé aux adresses e-mail falsifiées. Le BACKSCATTERER d’envoi d’un nuage identifie les serveurs qui envoient des messages rétrodiffusion (qui peuvent inclure de nombreuses sources de messagerie légitimes). Étant donné qu’il ne s’agit pas d’une liste de spammeurs, nous n’essayons pas de nous retirer du BACKSCATTERER.
ms.openlocfilehash: 22eeec29722cf1742e096234aad95b9f6ee407e2
ms.sourcegitcommit: fce0d5cad32ea60a08ff001b228223284710e2ed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/21/2020
ms.locfileid: "42895404"
---
# <a name="backscatter-and-eop"></a><span data-ttu-id="ef1f6-105">Rétrodiffusion et EOP</span><span class="sxs-lookup"><span data-stu-id="ef1f6-105">Backscatter and EOP</span></span>

<span data-ttu-id="ef1f6-106">*Rétrodiffusion* est des notifications d’échec de remise (également appelées notifications de non-remise) que vous recevez pour les messages que vous n’avez pas envoyés.</span><span class="sxs-lookup"><span data-stu-id="ef1f6-106">*Backscatter* is non-delivery reports (also known as NDRs or bounce messages) you receive for messages that you didn't send.</span></span> <span data-ttu-id="ef1f6-107">Les expéditeurs de courrier indésirable falsifient (usurpent) l’adresse de provenance de leurs messages et utilisent souvent des adresses de messagerie réelles pour prêter une crédibilité à leurs messages.</span><span class="sxs-lookup"><span data-stu-id="ef1f6-107">Spammers forge (spoof) the From: address of their messages, and they often use real email addresses to lend credibility to their messages.</span></span> <span data-ttu-id="ef1f6-108">Par conséquent, lorsque des expéditeurs de courrier indésirable envoient inévitablement des messages à des destinataires inexistants (le courrier indésirable est une opération à fort volume), le serveur de messagerie de destination est essentiellement amené à renvoyer le message non remis dans une notification d’échec de remise à l’expéditeur falsifié dans l’adresse de :.</span><span class="sxs-lookup"><span data-stu-id="ef1f6-108">So, when spammers inevitably send messages to non-existent recipients (spam is a high-volume operation), the destination email server is essentially tricked into returning the undeliverable message in an NDR to the forged sender in the From: address.</span></span>

<span data-ttu-id="ef1f6-109">Exchange Online Protection (EOP) permet d’identifier et de supprimer silencieusement les messages provenant de sources douteuse sans générer de notification d’inversion.</span><span class="sxs-lookup"><span data-stu-id="ef1f6-109">Exchange Online Protection (EOP) makes every effort to identify and silently drop messages from dubious sources without generating an NDR.</span></span> <span data-ttu-id="ef1f6-110">Toutefois, en fonction de la quantité de courrier électronique qui transite par le service, il y a toujours la possibilité qu’EOP envoie involontairement rétrodiffusion.</span><span class="sxs-lookup"><span data-stu-id="ef1f6-110">But, based on the sheer volume email flowing through the service, there's always the possibility that EOP will unintentionally send backscatter.</span></span>

<span data-ttu-id="ef1f6-111">Backscatterer.org gère une liste rouge (également appelée liste de blocage DNS ou BACKSCATTERER) des serveurs de messagerie qui étaient responsables de l’envoi de rétrodiffusion, et les serveurs EOP peuvent apparaître dans cette liste.</span><span class="sxs-lookup"><span data-stu-id="ef1f6-111">Backscatterer.org maintains a block list (also known as a DNS block list or DNSBL) of email servers that were responsible for sending backscatter, and EOP servers might appear on this list.</span></span> <span data-ttu-id="ef1f6-112">Mais nous n’essayons pas de nous supprimer de la liste rouge Backscatterer.org, car il ne s’agit pas d’une liste de spammers (par leur propre admission).</span><span class="sxs-lookup"><span data-stu-id="ef1f6-112">But, we don't try to remove ourselves from the Backscatterer.org block list because it isn't a list of spammers (by their own admission).</span></span>

> [!TIP]
> <span data-ttu-id="ef1f6-113">Le site Web Backscatter.org<http://www.backscatterer.org/?target=usage>() recommande l’utilisation de son service pour vérifier le courrier électronique entrant en mode sans échec au lieu d’un mode de rejet (les services de messagerie volumineux envoient presque toujours des rétrodiffusion).</span><span class="sxs-lookup"><span data-stu-id="ef1f6-113">The Backscatter.org website (<http://www.backscatterer.org/?target=usage>) recommends using their service to check incoming email in Safe mode instead of Reject mode (large email services almost always send some backscatter).</span></span>
