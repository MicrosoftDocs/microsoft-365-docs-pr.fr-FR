---
title: Messages de rétrodiffusion et EOP
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
description: Les messages rétrodiffusion sont des messages de retour automatique qui sont envoyés à des adresses de messagerie falsifiées. Le BACKSCATTERER d’envoi d’un nuage identifie les serveurs qui envoient des messages rétrodiffusion (qui peuvent inclure de nombreuses sources de messagerie légitimes). Étant donné qu’il ne s’agit pas d’une liste de spammeurs, nous n’essayons pas de nous retirer du BACKSCATTERER.
ms.openlocfilehash: 3dc83c303e861c8762f2276de521e1b550ae2e59
ms.sourcegitcommit: 1c91b7b24537d0e54d484c3379043db53c1aea65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2020
ms.locfileid: "41599731"
---
# <a name="backscatter-messages-and-eop"></a><span data-ttu-id="fd47d-105">Messages de rétrodiffusion et EOP</span><span class="sxs-lookup"><span data-stu-id="fd47d-105">Backscatter messages and EOP</span></span>

<span data-ttu-id="fd47d-106">Les *messages rétrodiffusion* sont des notifications d’échec de remise (également appelées notifications de non-remise) que vous recevez pour les messages que vous n’avez pas envoyés.</span><span class="sxs-lookup"><span data-stu-id="fd47d-106">*Backscatter messages* are non-delivery reports (also known as NDRs or bounce messages) you receive for messages that you didn't send.</span></span> <span data-ttu-id="fd47d-107">Les expéditeurs de courrier indésirable falsifient (usurpent) l’adresse de provenance de leurs messages et utilisent souvent des adresses de messagerie réelles pour prêter une crédibilité à leurs messages.</span><span class="sxs-lookup"><span data-stu-id="fd47d-107">Spammers forge (spoof) the From: address of their messages, and they often use real email addresses to lend credibility to their messages.</span></span> <span data-ttu-id="fd47d-108">Par conséquent, lorsqu’ils envoient inévitablement des messages à des destinataires qui ne sont pas existants (le courrier indésirable est une opération à fort volume), le serveur de messagerie de destination peut faire face à une notification d’échec de remise, qui est envoyée à l’expéditeur falsifié dans l’adresse de :.</span><span class="sxs-lookup"><span data-stu-id="fd47d-108">So, when they inevitably send messages to non-existent recipients (spam is a high-volume operation), the destination email server might dutifully respond with an NDR, which is sent to the forged sender in the From: address.</span></span>

<span data-ttu-id="fd47d-109">Exchange Online Protection (EOP) permet d’identifier et de supprimer silencieusement les messages provenant de sources douteuse sans générer de notification d’inversion.</span><span class="sxs-lookup"><span data-stu-id="fd47d-109">Exchange Online Protection (EOP) makes every effort to identify and silently drop messages from dubious sources without generating an NDR.</span></span> <span data-ttu-id="fd47d-110">Toutefois, en fonction de la quantité de courrier électronique qui transite par le service, il y a toujours la possibilité qu’EOP envoie involontairement des messages rétrodiffusion.</span><span class="sxs-lookup"><span data-stu-id="fd47d-110">But, based on the sheer volume email flowing through the service, there's always the possibility that EOP will unintentionally send backscatter messages.</span></span>

<span data-ttu-id="fd47d-111">Backscatterer.org gère une liste rouge (également appelée liste de blocage DNS ou BACKSCATTERER) des serveurs de messagerie qui étaient responsables de l’envoi de messages rétrodiffusion, et des serveurs EOP peuvent apparaître dans cette liste.</span><span class="sxs-lookup"><span data-stu-id="fd47d-111">Backscatterer.org maintains a block list (also known as a DNS block list or DNSBL) of email servers that were responsible for sending backscatter messages, and EOP servers might appear on this list.</span></span> <span data-ttu-id="fd47d-112">Mais nous n’essayons pas de nous supprimer de la liste rouge Backscatterer.org, car il ne s’agit pas d’une liste de spammers (par leur propre admission).</span><span class="sxs-lookup"><span data-stu-id="fd47d-112">But, we don't try to remove ourselves from the Backscatterer.org block list because it isn't a list of spammers (by their own admission).</span></span>

> [!TIP]
> <span data-ttu-id="fd47d-113">En fonction du rétrodiffusion. ou du site`http://www.backscatterer.org/?target=usage`Web (), il est recommandé d’utiliser son service pour vérifier le courrier entrant en mode sans échec au lieu du mode de rejet (les services de messagerie volumineux envoient presque toujours des messages rétrodiffusion).</span><span class="sxs-lookup"><span data-stu-id="fd47d-113">According to the Backscatter.or website (`http://www.backscatterer.org/?target=usage`), they recommend using their service to check incoming email in Safe mode instead of Reject mode (large email services almost always send some backscatter messages).</span></span>
