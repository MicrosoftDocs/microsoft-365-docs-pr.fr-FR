---
title: Gérer les listes d'expéditeurs autorisés pour les vers de publipostage en bloc
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 11/17/2014
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: d48db4a3-9fbe-45e2-bbaa-1017ffdf96f8
ms.collection:
- M365-security-compliance
description: "Si vous souhaitez utiliser les listes d'expéditeurs autorisés, vous devez savoir qu'Exchange Online Protection (EOP) et Outlook gèrent différemment le traitement. Le service respecte les expéditeurs et les domaines autorisés en inspectant l'adresse RFC 5321.MailFrom, tandis qu'Outlook ajoute l'adresse RFC 5322.From à la liste des expéditeurs autorisés d'un utilisateur. (Remarque : Le service inspecte les adresses 5321.MailFrom et 5322.MailFrom pour les expéditeurs et les domaines bloqués.)"
ms.openlocfilehash: f73cc3fc88318c4f625bf5579f73d92625624fd5
ms.sourcegitcommit: 1162d676b036449ea4220de8a6642165190e3398
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/20/2019
ms.locfileid: "37080311"
---
# <a name="manage-safe-sender-lists-for-bulk-mailers"></a><span data-ttu-id="b5904-105">Gérer les listes d’expéditeurs autorisés pour les vers de publipostage en bloc</span><span class="sxs-lookup"><span data-stu-id="b5904-105">Manage safe sender lists for bulk mailers</span></span>

<span data-ttu-id="b5904-106">Si vous souhaitez utiliser les listes d'expéditeurs autorisés, vous devez savoir qu'Exchange Online Protection (EOP) et Outlook gèrent différemment le traitement.</span><span class="sxs-lookup"><span data-stu-id="b5904-106">If you want to use safe sender lists, you should know that Exchange Online Protection (EOP) and Outlook handle processing differently.</span></span> <span data-ttu-id="b5904-107">Le service Office 365 respecte les expéditeurs et les domaines approuvés en inspectant l’adresse RFC 5321. MailFrom et l’adresse RFC 5322. from, tandis qu’Outlook ajoute l’adresse RFC 5322. from à la liste des expéditeurs approuvés d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b5904-107">The Office 365 service respects safe senders and domains by inspecting the RFC 5321.MailFrom address and the RFC 5322.From address, while Outlook adds the RFC 5322.From address to a user's safe sender list.</span></span> <span data-ttu-id="b5904-108">(Remarque : Le service inspecte les adresses 5321.MailFrom et 5322.MailFrom pour les expéditeurs et les domaines bloqués.)</span><span class="sxs-lookup"><span data-stu-id="b5904-108">(Note: The service inspects both the 5321.MailFrom address and 5322.From address for blocked senders and domains.)</span></span>
  
<span data-ttu-id="b5904-p103">L'adresse SMTP MAIL FROM, aussi connue sous le nom « adresse RFC 5321.MailFrom », est l'adresse de messagerie utilisée pour effectuer les vérifications SPF. Si le courrier électronique ne peut être remis, il s'agit du chemin vers lequel le message de retour est envoyé. C'est cette adresse électronique qui est placée dans le chemin de retour des en-têtes de message par défaut, mais il est possible pour l'expéditeur de désigner une adresse de chemin de retour différente.</span><span class="sxs-lookup"><span data-stu-id="b5904-p103">The SMTP MAIL FROM address, otherwise known as the RFC 5321.MailFrom address, is the email address that's used to perform SPF checks, and if the mail can't be delivered, the path to which the bounced message is delivered. It's this email address that is placed into the Return-Path in the message headers by default, though it's possible for the sender to designate a different Return-Path address.</span></span>
  
<span data-ttu-id="b5904-111">L'adresse de l'expéditeur dans les en-têtes de message, aussi connue sous le nom « adresse RFC 5322.From », est l'adresse de messagerie affichée dans le client de messagerie, comme Outlook.</span><span class="sxs-lookup"><span data-stu-id="b5904-111">The From: address in the message headers, otherwise known as the RFC 5322.From address, is the email address that is displayed in the mail client such as Outlook.</span></span>
  
<span data-ttu-id="b5904-p104">La plupart du temps, les adresses 5321.MailFrom et 5322.From sont identiques. C'est généralement le cas pour la communication entre deux-personnes. Toutefois, lorsqu'un courrier électronique est envoyé à la place d'une autre personne, les adresses sont souvent différentes. Cela se produit généralement avec les messages de courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="b5904-p104">Much of the time, the 5321.MailFrom and 5322.From addresses are the same. This is typical for person-to-person communication. However, when email is sent on behalf of someone else, the addresses are frequently different. This usually happens most often for bulk email messages.</span></span>
  
<span data-ttu-id="b5904-116">Par exemple, supposons que la compagnie aérienne Blue Yonder Airlines ait demandé à la société Margie's Travel d'envoyer sa publicité par courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="b5904-116">For example, suppose that the airline Blue Yonder Airlines has contracted out Margie's Travel to send out its email advertising.</span></span> <span data-ttu-id="b5904-117">Vous obtenez alors un message dans votre boîte de réception provenant de l'expéditeur blueyonder@news.blueyonderairlines.com.</span><span class="sxs-lookup"><span data-stu-id="b5904-117">You then get a message in your inbox from sender blueyonder@news.blueyonderairlines.com.</span></span> <span data-ttu-id="b5904-118">Dans ce cas, l’adresse 5321. MailFrom est blueyonder.airlines@margiestravel.com et blueyonder@news.blueyonderairlines.com est l’adresse 5322. from qui est la personne, qui est affichée dans Outlook.</span><span class="sxs-lookup"><span data-stu-id="b5904-118">In this case, 5321.MailFrom address is blueyonder.airlines@margiestravel.com, and blueyonder@news.blueyonderairlines.com is the 5322.From address which is the one, you see in Outlook.</span></span> <span data-ttu-id="b5904-119">Étant donné que le service respecte l’adresse RFC 5322. from, pour empêcher le filtrage de ce message, vous pouvez ajouter l’adresse RFC 5322. from comme expéditeur approuvé dans Outlook (en tant qu’utilisateur) ou, si vous êtes administrateur, configurer une règle de flux de messagerie comme indiqué sur le [blocage du courrier indésirable. Section protection](anti-spam-protection.md) .</span><span class="sxs-lookup"><span data-stu-id="b5904-119">Because the service respects the RFC 5322.From address, to prevent this message from getting filtered, you can add the RFC 5322.From address as a safe sender in Outlook (as a user) or, if you're an administrator set up a mailflow rule as shown on the [Anti-spam Protection](anti-spam-protection.md) section.</span></span>
  

