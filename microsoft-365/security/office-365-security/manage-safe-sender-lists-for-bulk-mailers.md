---
title: Gérer les listes d'expéditeurs autorisés pour les vers de publipostage en bloc
f1.keywords:
- NOCSH
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
ms.openlocfilehash: aaede7cab2e640603c20804f4015e19f61b6c2f3
ms.sourcegitcommit: 1c91b7b24537d0e54d484c3379043db53c1aea65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2020
ms.locfileid: "41598941"
---
# <a name="manage-safe-sender-lists-for-bulk-mailers"></a><span data-ttu-id="44bb4-105">Gérer les listes d’expéditeurs autorisés pour les vers de publipostage en bloc</span><span class="sxs-lookup"><span data-stu-id="44bb4-105">Manage safe sender lists for bulk mailers</span></span>

<span data-ttu-id="44bb4-106">Si vous souhaitez utiliser les listes d'expéditeurs autorisés, vous devez savoir qu'Exchange Online Protection (EOP) et Outlook gèrent différemment le traitement.</span><span class="sxs-lookup"><span data-stu-id="44bb4-106">If you want to use safe sender lists, you should know that Exchange Online Protection (EOP) and Outlook handle processing differently.</span></span> <span data-ttu-id="44bb4-107">Le service Office 365 respecte les expéditeurs et les domaines approuvés en inspectant l' `RFC 5321.MailFrom` adresse `RFC 5322.From` et l’adresse, tandis `RFC 5322.From` qu’Outlook ajoute l’adresse à la liste des expéditeurs approuvés d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="44bb4-107">The Office 365 service respects safe senders and domains by inspecting the `RFC 5321.MailFrom` address and the `RFC 5322.From` address, while Outlook adds the `RFC 5322.From` address to a user's safe sender list.</span></span> <span data-ttu-id="44bb4-108">(Remarque : le service inspecte l’adresse `5321.MailFrom` et `5322.From` l’adresse pour les expéditeurs et les domaines bloqués.)</span><span class="sxs-lookup"><span data-stu-id="44bb4-108">(Note: The service inspects both the `5321.MailFrom` address and `5322.From` address for blocked senders and domains.)</span></span>

<span data-ttu-id="44bb4-109">L' `SMTP MAIL FROM` adresse, appelée `RFC 5321.MailFrom address`,, est l’adresse de messagerie utilisée pour effectuer des vérifications SPF, et si le courrier ne peut pas être remis, le chemin d’accès vers lequel le message retourné est remis.</span><span class="sxs-lookup"><span data-stu-id="44bb4-109">The `SMTP MAIL FROM` address, otherwise known as the `RFC 5321.MailFrom address`, is the email address that's used to perform SPF checks, and if the mail can't be delivered, the path to which the bounced message is delivered.</span></span> <span data-ttu-id="44bb4-110">Il s’agit de cette adresse de messagerie qui est `Return-Path` placée dans le dans les en-têtes de message par défaut, bien qu’il soit possible pour l' `Return-Path` expéditeur de désigner une autre adresse.</span><span class="sxs-lookup"><span data-stu-id="44bb4-110">It's this email address that is placed into the `Return-Path` in the message headers by default, though it's possible for the sender to designate a different `Return-Path` address.</span></span>

<span data-ttu-id="44bb4-111">L' `From:` adresse dans les en-têtes de message, également appelée `RFC 5322.From` adresse, est l’adresse de messagerie qui est affichée dans le client de messagerie, tel qu’Outlook.</span><span class="sxs-lookup"><span data-stu-id="44bb4-111">The `From:` address in the message headers, otherwise known as the `RFC 5322.From` address, is the email address that is displayed in the mail client such as Outlook.</span></span>

<span data-ttu-id="44bb4-112">La plupart du temps, les `5321.MailFrom` adresses `5322.From` et sont identiques.</span><span class="sxs-lookup"><span data-stu-id="44bb4-112">Much of the time, the `5321.MailFrom` and `5322.From` addresses are the same.</span></span> <span data-ttu-id="44bb4-113">C'est généralement le cas pour la communication entre deux-personnes.</span><span class="sxs-lookup"><span data-stu-id="44bb4-113">This is typical for person-to-person communication.</span></span> <span data-ttu-id="44bb4-114">Toutefois, lorsqu'un courrier électronique est envoyé à la place d'une autre personne, les adresses sont souvent différentes.</span><span class="sxs-lookup"><span data-stu-id="44bb4-114">However, when email is sent on behalf of someone else, the addresses are frequently different.</span></span> <span data-ttu-id="44bb4-115">Cela se produit généralement avec les messages de courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="44bb4-115">This usually happens most often for bulk email messages.</span></span>

<span data-ttu-id="44bb4-116">Par exemple, supposons que Blue Yonder Airlines a embauché Margie’s Travel pour envoyer sa publicité par courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="44bb4-116">For example, suppose that Blue Yonder Airlines has hired Margie's Travel to send out its email advertising.</span></span> <span data-ttu-id="44bb4-117">Vous obtenez alors un message dans votre boîte de réception provenant de l'expéditeur blueyonder@news.blueyonderairlines.com.</span><span class="sxs-lookup"><span data-stu-id="44bb4-117">You then get a message in your inbox from sender blueyonder@news.blueyonderairlines.com.</span></span> <span data-ttu-id="44bb4-118">Dans cet exemple :</span><span class="sxs-lookup"><span data-stu-id="44bb4-118">In this example:</span></span>

- <span data-ttu-id="44bb4-119">L' `5321.MailFrom` adresse est blueyonder.Airlines@margiestravel.com.</span><span class="sxs-lookup"><span data-stu-id="44bb4-119">The `5321.MailFrom` address is blueyonder.airlines@margiestravel.com.</span></span>

- <span data-ttu-id="44bb4-120">L' `5322.From` adresse est blueyonder@news.blueyonderairlines.com, ce que vous verrez dans Outlook.</span><span class="sxs-lookup"><span data-stu-id="44bb4-120">The `5322.From` address is blueyonder@news.blueyonderairlines.com, which is what you'll see in Outlook.</span></span>

<span data-ttu-id="44bb4-121">Pour empêcher le filtrage de ce message, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="44bb4-121">To prevent this message from being filtered, you can:</span></span>

- <span data-ttu-id="44bb4-122">**En tant qu’utilisateur**: ajouter `RFC 5322.From` l’adresse en tant qu’expéditeur approuvé dans Outlook.</span><span class="sxs-lookup"><span data-stu-id="44bb4-122">**As a user**: Add the `RFC 5322.From` address as a Safe Sender in Outlook.</span></span>

- <span data-ttu-id="44bb4-123">**En tant qu’administrateur**: configurez une [règle de flux de messagerie](anti-spam-protection.md#beyond-the-basics-more-ways-to-prevent-spam-in-office-365) (également appelée règle de transport).</span><span class="sxs-lookup"><span data-stu-id="44bb4-123">**As an admin**: Set up a [mail flow rule](anti-spam-protection.md#beyond-the-basics-more-ways-to-prevent-spam-in-office-365) (also known as a transport rule).</span></span>
