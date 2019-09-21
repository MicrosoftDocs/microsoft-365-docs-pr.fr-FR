---
title: Utilisation des notifications de courrier indésirable de l’utilisateur pour le déblocage et le signalement des messages de courrier indésirable mis en quarantaine dans Office 365
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 03/14/2019
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: 56de4ed5-b0aa-4195-9f46-033d7cc086bc
ms.collection:
- M365-security-compliance
description: Si votre administrateur Active les notifications pour les utilisateurs, vous recevrez un message de notification répertoriant les messages envoyés à votre boîte aux lettres identifiés comme courriers indésirables, en masse ou par hameçonnage. Vous pouvez publier ou signaler des messages après leur notification.
ms.openlocfilehash: 499af3ae2934eed19e421918af07a45b72fe2518
ms.sourcegitcommit: 1162d676b036449ea4220de8a6642165190e3398
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/20/2019
ms.locfileid: "37079936"
---
# <a name="use-user-spam-notifications-to-release-and-report-quarantined-messages-in-office-365"></a><span data-ttu-id="6157a-104">Utilisation des notifications de courrier indésirable de l’utilisateur pour le déblocage et le signalement des messages de courrier indésirable mis en quarantaine dans Office 365</span><span class="sxs-lookup"><span data-stu-id="6157a-104">Use user spam notifications to release and report quarantined messages in Office 365</span></span>

<span data-ttu-id="6157a-105">Si votre administrateur active des notifications de courrier indésirable pour les utilisateurs, vous recevrez un message de notification répertoriant les messages adressés à votre boîte aux lettres identifiés comme courrier indésirable et mis en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="6157a-105">If your admin enables spam notifications for users, you'll receive a notification message that lists messages addressed to your mailbox that were identified as spam and quarantined instead.</span></span>
  
> [!TIP]
> <span data-ttu-id="6157a-106">Si vous êtes administrateur et que vous souhaitez activer cette fonctionnalité, vous pouvez choisir l’option lorsque vous [modifiez une stratégie de blocage du courrier indésirable par défaut](https://go.microsoft.com/fwlink/?LinkId=800313).</span><span class="sxs-lookup"><span data-stu-id="6157a-106">If you're an administrator and want to enable this feature, you can choose the option when you [modify a default anti-spam policy](https://go.microsoft.com/fwlink/?LinkId=800313).</span></span> 
  
<span data-ttu-id="6157a-107">Le message que vous recevez inclut le nombre de messages indésirables mis en quarantaine que vous avez, ainsi que la date et l’heure (au format UTC ou UTC) du dernier message de la liste.</span><span class="sxs-lookup"><span data-stu-id="6157a-107">The message you receive includes the number of spam-quarantined messages you have, and the date and time (in Universal Coordinated Time or UTC) of the last message in the list.</span></span> <span data-ttu-id="6157a-108">La liste inclut les éléments suivants pour chaque message :</span><span class="sxs-lookup"><span data-stu-id="6157a-108">The list includes the following for each message:</span></span>
  
- <span data-ttu-id="6157a-109">**Expéditeur** Nom d’envoi et adresse de messagerie du message en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="6157a-109">**Sender** The send name and email address of the quarantined message.</span></span> 
    
- <span data-ttu-id="6157a-110">**Objet** Texte de l'objet du message en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="6157a-110">**Subject** The subject line text of the quarantined message.</span></span> 
    
- <span data-ttu-id="6157a-111">**Date** Date et heure (UTC) auxquelles le message a été mis en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="6157a-111">**Date** The date and time (in UTC) that the message was quarantined.</span></span> 
    
- <span data-ttu-id="6157a-112">**Taille** Taille du message, en kilo-octets (Ko).</span><span class="sxs-lookup"><span data-stu-id="6157a-112">**Size** The size of the message, in kilobytes (KBs).</span></span> 
    
<span data-ttu-id="6157a-113">Voici les actions que vous pouvez effectuer avec un message en quarantaine :</span><span class="sxs-lookup"><span data-stu-id="6157a-113">These are the actions that you can take with a quarantined message:</span></span>

- <span data-ttu-id="6157a-114">**Affichez un aperçu** du message si vous souhaitez afficher un aperçu du contenu ou de l’en-tête avant de prendre une mesure.</span><span class="sxs-lookup"><span data-stu-id="6157a-114">**Preview** the message if you would like to preview the content or header prior to taking action.</span></span>

- <span data-ttu-id="6157a-115">**Téléchargez** le message si vous souhaitez consulter le message et les pièces jointes (le cas échéant) sur votre appareil avant de prendre une mesure.</span><span class="sxs-lookup"><span data-stu-id="6157a-115">**Download** the message if you would like to review the message and attachments (if any) on your device prior to taking action.</span></span>

- <span data-ttu-id="6157a-116">**Release** si le message n’est pas un courrier indésirable et que vous souhaitez qu’Office 365 envoie le message à votre boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="6157a-116">**Release** if the message isn’t spam and you want Office 365 to send the message to your mailbox.</span></span>

- <span data-ttu-id="6157a-117">**Release & autoriser l’expéditeur** si le message n’est pas un courrier indésirable et que vous souhaitez qu’Office 365 ajoute l’expéditeur à votre liste des expéditeurs et destinataires approuvés pour les futurs courriers électroniques.</span><span class="sxs-lookup"><span data-stu-id="6157a-117">**Release & Allow Sender** if the message isn’t spam and you want Office 365 to add the sender to your safe senders and recipients list for future emails.</span></span> <span data-ttu-id="6157a-118">Gardez à l’esprit que votre administrateur peut avoir d’autres configurations autoriser/bloquer des organisations qui remplacent votre liste d’expéditeurs autorisés.</span><span class="sxs-lookup"><span data-stu-id="6157a-118">Keep in mind that your admin may have other organization wide allow/block configurations that override your safe sender list.</span></span>

- <span data-ttu-id="6157a-119">**Release & Report**, si le message n’est pas indésirable et que vous voulez envoyer le message à votre boîte aux lettres et le signaler à Microsoft pour analyse.</span><span class="sxs-lookup"><span data-stu-id="6157a-119">**Release & Report**, if the message isn’t spam and you want to send the message to your mailbox and report it to Microsoft for analysis.</span></span>

- <span data-ttu-id="6157a-120">**Bloquer l’expéditeur** si vous souhaitez qu’Office 365 ajoute l’expéditeur à votre liste des expéditeurs bloqués.</span><span class="sxs-lookup"><span data-stu-id="6157a-120">**Block Sender** if you want Office 365 to add the sender to your blocked senders list.</span></span>

<span data-ttu-id="6157a-121">Prenez en considération ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="6157a-121">Be aware of the following:</span></span>
  
- <span data-ttu-id="6157a-122">Les messages mis en quarantaine, car ils correspondent à une règle de flux de messagerie, ne sont pas inclus dans les messages mis en quarantaine par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6157a-122">Messages that are quarantined because they matched a mail flow rule are not included in user quarantined messages.</span></span> <span data-ttu-id="6157a-123">Seuls les messages mis en quarantaine car identifiés comme courrier indésirable sont répertoriés.</span><span class="sxs-lookup"><span data-stu-id="6157a-123">Only spam-quarantined messages are listed.</span></span>
    
- <span data-ttu-id="6157a-124">Vous ne pouvez libérer un message et le signaler comme faux positif (légitime) qu'une fois.</span><span class="sxs-lookup"><span data-stu-id="6157a-124">You can only release a message and report it as a false positive (not junk) once.</span></span>
    

