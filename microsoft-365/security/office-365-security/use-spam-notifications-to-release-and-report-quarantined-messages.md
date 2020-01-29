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
ms.openlocfilehash: fbe8a09f7da5df2df4b3b68bd524fa3ef2ed18b8
ms.sourcegitcommit: 3f8957ddd04b8710bb5f314a0902fdee50c7c9b7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/28/2020
ms.locfileid: "41572660"
---
# <a name="use-user-spam-notifications-to-release-and-report-quarantined-messages-in-office-365"></a><span data-ttu-id="54bcc-104">Utilisation des notifications de courrier indésirable de l’utilisateur pour le déblocage et le signalement des messages de courrier indésirable mis en quarantaine dans Office 365</span><span class="sxs-lookup"><span data-stu-id="54bcc-104">Use user spam notifications to release and report quarantined messages in Office 365</span></span>

<span data-ttu-id="54bcc-105">Si votre administrateur active des notifications de courrier indésirable pour les utilisateurs, vous recevrez un message de notification répertoriant les messages adressés à votre boîte aux lettres identifiés comme courrier indésirable et mis en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="54bcc-105">If your admin enables spam notifications for users, you'll receive a notification message that lists messages addressed to your mailbox that were identified as spam and quarantined instead.</span></span>

> [!TIP]
> <span data-ttu-id="54bcc-106">Si vous êtes administrateur et que vous souhaitez activer cette fonctionnalité, vous pouvez choisir l’option lorsque vous [modifiez une stratégie de blocage du courrier indésirable par défaut](configure-your-spam-filter-policies.md).</span><span class="sxs-lookup"><span data-stu-id="54bcc-106">If you're an administrator and want to enable this feature, you can choose the option when you [modify a default anti-spam policy](configure-your-spam-filter-policies.md).</span></span>

<span data-ttu-id="54bcc-107">Le message que vous recevez inclut le nombre de messages indésirables mis en quarantaine que vous avez, ainsi que la date et l’heure (au format UTC ou UTC) du dernier message de la liste.</span><span class="sxs-lookup"><span data-stu-id="54bcc-107">The message you receive includes the number of spam-quarantined messages you have, and the date and time (in Universal Coordinated Time or UTC) of the last message in the list.</span></span> <span data-ttu-id="54bcc-108">La liste inclut les éléments suivants pour chaque message :</span><span class="sxs-lookup"><span data-stu-id="54bcc-108">The list includes the following for each message:</span></span>

- <span data-ttu-id="54bcc-109">**Expéditeur** Nom d’envoi et adresse de messagerie du message en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="54bcc-109">**Sender** The send name and email address of the quarantined message.</span></span>

- <span data-ttu-id="54bcc-110">**Objet** Texte de l'objet du message en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="54bcc-110">**Subject** The subject line text of the quarantined message.</span></span>

- <span data-ttu-id="54bcc-111">**Date** Date et heure (UTC) auxquelles le message a été mis en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="54bcc-111">**Date** The date and time (in UTC) that the message was quarantined.</span></span>

<span data-ttu-id="54bcc-112">Voici les actions que vous pouvez effectuer avec un message en quarantaine :</span><span class="sxs-lookup"><span data-stu-id="54bcc-112">These are the actions that you can take with a quarantined message:</span></span>

- <span data-ttu-id="54bcc-113">**Bloquer l’expéditeur** si vous souhaitez qu’Office 365 ajoute l’expéditeur à votre liste des expéditeurs bloqués.</span><span class="sxs-lookup"><span data-stu-id="54bcc-113">**Block Sender** if you want Office 365 to add the sender to your blocked senders list.</span></span>

- <span data-ttu-id="54bcc-114">**Release** si le message n’est pas un courrier indésirable et que vous souhaitez qu’Office 365 envoie le message à votre boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="54bcc-114">**Release** if the message isn't spam and you want Office 365 to send the message to your mailbox.</span></span>

- <span data-ttu-id="54bcc-115">**Passez en revue** pour accéder au portail de mise en quarantaine dans le centre de sécurité et conformité si vous souhaitez effectuer d’autres actions, telles que l’aperçu ou la publication.</span><span class="sxs-lookup"><span data-stu-id="54bcc-115">**Review** to navigate to the Quarantine Portal within the Security and Compliance Center if you want to take other actions, such as Preview or Release.</span></span>

<span data-ttu-id="54bcc-116">Prenez en considération ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="54bcc-116">Be aware of the following:</span></span>

- <span data-ttu-id="54bcc-117">Les messages mis en quarantaine, car ils correspondent à une règle de flux de messagerie, ne sont pas inclus dans les messages mis en quarantaine par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="54bcc-117">Messages that are quarantined because they matched a mail flow rule are not included in user quarantined messages.</span></span> <span data-ttu-id="54bcc-118">Seuls les messages mis en quarantaine car identifiés comme courrier indésirable sont répertoriés.</span><span class="sxs-lookup"><span data-stu-id="54bcc-118">Only spam-quarantined messages are listed.</span></span>

- <span data-ttu-id="54bcc-119">Vous ne pouvez libérer un message et le signaler comme faux positif (légitime) qu'une fois.</span><span class="sxs-lookup"><span data-stu-id="54bcc-119">You can only release a message and report it as a false positive (not junk) once.</span></span>
