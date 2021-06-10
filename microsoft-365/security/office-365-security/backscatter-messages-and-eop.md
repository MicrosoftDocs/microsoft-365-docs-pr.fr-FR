---
title: Rétrodiffusion dans EOP
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: conceptual
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 6f64f2de-d626-48ed-8084-03cc72301aa4
ms.collection:
- M365-security-compliance
ms.custom:
- seo-marvel-apr2020
description: Dans cet article, vous allez découvrir la protection contre la Microsoft Exchange Online (EOP)
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: e5882f611c3feec9a22760e696973cd0713649b2
ms.sourcegitcommit: dcb97fbfdae52960ae62b6faa707a05358193ed5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2021
ms.locfileid: "51204025"
---
# <a name="backscatter-in-eop"></a><span data-ttu-id="84133-103">Rétrodiffusion dans EOP</span><span class="sxs-lookup"><span data-stu-id="84133-103">Backscatter in EOP</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="84133-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="84133-104">**Applies to**</span></span>
- [<span data-ttu-id="84133-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="84133-105">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="84133-106">Microsoft Defender pour Office 365 : offre 1 et offre 2</span><span class="sxs-lookup"><span data-stu-id="84133-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](defender-for-office-365.md)
- [<span data-ttu-id="84133-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="84133-107">Microsoft 365 Defender</span></span>](../defender/microsoft-365-defender.md)

<span data-ttu-id="84133-108">*La backscatter* est une non-remise (également appelées rapports de non-remise ou messages de non-remise) que vous recevez pour les messages que vous n’avez pas envoyés.</span><span class="sxs-lookup"><span data-stu-id="84133-108">*Backscatter* is non-delivery reports (also known as NDRs or bounce messages) you receive for messages that you didn't send.</span></span> <span data-ttu-id="84133-109">Les expéditeurs de courrier indésirable falsifient (usurpent) l’adresse De : de leurs messages. Ils utilisent souvent des adresses de messagerie réelles pour donner de la crédibilité à leurs messages.</span><span class="sxs-lookup"><span data-stu-id="84133-109">Spammers forge (spoof) the From: address of their messages, and they often use real email addresses to lend credibility to their messages.</span></span> <span data-ttu-id="84133-110">Ainsi, lorsque les expéditeurs de courrier indésirable envoient inévitablement des messages à des destinataires inexistants (le courrier indésirable est une opération à volume élevé), le serveur de messagerie de destination est essentiellement dupliqué pour renvoyer le message non remettre dans une NDR à l’expéditeur falsifié dans l’adresse De: .</span><span class="sxs-lookup"><span data-stu-id="84133-110">So, when spammers inevitably send messages to non-existent recipients (spam is a high-volume operation), the destination email server is essentially tricked into returning the undeliverable message in an NDR to the forged sender in the From: address.</span></span>

<span data-ttu-id="84133-111">Dans Microsoft 365 organisations avec des boîtes aux lettres dans Exchange Online ou des organisations Exchange Online Protection autonomes (EOP) sans boîtes aux lettres Exchange Online, EOP s’évouille d’identifier et de déposer silencieusement des messages à partir de sources fictives sans générer de rapport de non-réception.</span><span class="sxs-lookup"><span data-stu-id="84133-111">In Microsoft 365 organizations with mailboxes in Exchange Online or standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes, EOP makes every effort to identify and silently drop messages from dubious sources without generating an NDR.</span></span> <span data-ttu-id="84133-112">Toutefois, en fonction de la quantité de messages électroniques en volume qui circulent dans le service, il est toujours possible qu’EOP envoie involontairement une copie d’erreur.</span><span class="sxs-lookup"><span data-stu-id="84133-112">But, based on the sheer volume email flowing through the service, there's always the possibility that EOP will unintentionally send backscatter.</span></span>

<span data-ttu-id="84133-113">Backscatterer.org conserve une liste d’adresses (également appelée liste d’adresses DNS bloqués ou DNSBL) des serveurs de messagerie qui étaient chargés de l’envoi de la backscatter, et les serveurs EOP peuvent apparaître dans cette liste.</span><span class="sxs-lookup"><span data-stu-id="84133-113">Backscatterer.org maintains a block list (also known as a DNS block list or DNSBL) of email servers that were responsible for sending backscatter, and EOP servers might appear on this list.</span></span> <span data-ttu-id="84133-114">Toutefois, nous n’essayons pas de nous supprimer de la liste d’Backscatterer.org bloqués, car il ne s’agit pas d’une liste d’expéditeurs de courrier indésirable (de leur propre admission).</span><span class="sxs-lookup"><span data-stu-id="84133-114">But, we don't try to remove ourselves from the Backscatterer.org block list because it isn't a list of spammers (by their own admission).</span></span>

> [!TIP]
> <span data-ttu-id="84133-115">Le Backscatter.org web () recommande d’utiliser son service pour vérifier le courrier entrant en mode sans échec plutôt qu’en mode de rejet (les services de courrier de grande taille envoient presque toujours des <http://www.backscatterer.org/?target=usage> retours).</span><span class="sxs-lookup"><span data-stu-id="84133-115">The Backscatter.org website (<http://www.backscatterer.org/?target=usage>) recommends using their service to check incoming email in Safe mode instead of Reject mode (large email services almost always send some backscatter).</span></span>
