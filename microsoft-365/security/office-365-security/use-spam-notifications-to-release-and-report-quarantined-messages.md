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
ms.openlocfilehash: 4cf592f0aec948c3c8f6383cf288fb32ac644cd6
ms.sourcegitcommit: 5710ce729c55d95b8b452d99ffb7ea92b5cb254a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2019
ms.locfileid: "39971362"
---
# <a name="use-user-spam-notifications-to-release-and-report-quarantined-messages-in-office-365"></a><span data-ttu-id="b0ff9-104">Utilisation des notifications de courrier indésirable de l’utilisateur pour le déblocage et le signalement des messages de courrier indésirable mis en quarantaine dans Office 365</span><span class="sxs-lookup"><span data-stu-id="b0ff9-104">Use user spam notifications to release and report quarantined messages in Office 365</span></span>

<span data-ttu-id="b0ff9-105">Si votre administrateur active des notifications de courrier indésirable pour les utilisateurs, vous recevrez un message de notification répertoriant les messages adressés à votre boîte aux lettres identifiés comme courrier indésirable et mis en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="b0ff9-105">If your admin enables spam notifications for users, you'll receive a notification message that lists messages addressed to your mailbox that were identified as spam and quarantined instead.</span></span>

> [!TIP]
> <span data-ttu-id="b0ff9-106">Si vous êtes administrateur et que vous souhaitez activer cette fonctionnalité, vous pouvez choisir l’option lorsque vous [modifiez une stratégie de blocage du courrier indésirable par défaut](configure-your-spam-filter-policies.md).</span><span class="sxs-lookup"><span data-stu-id="b0ff9-106">If you're an administrator and want to enable this feature, you can choose the option when you [modify a default anti-spam policy](configure-your-spam-filter-policies.md).</span></span>

<span data-ttu-id="b0ff9-107">Le message que vous recevez inclut le nombre de messages indésirables mis en quarantaine que vous avez, ainsi que la date et l’heure (au format UTC ou UTC) du dernier message de la liste.</span><span class="sxs-lookup"><span data-stu-id="b0ff9-107">The message you receive includes the number of spam-quarantined messages you have, and the date and time (in Universal Coordinated Time or UTC) of the last message in the list.</span></span> <span data-ttu-id="b0ff9-108">La liste inclut les éléments suivants pour chaque message :</span><span class="sxs-lookup"><span data-stu-id="b0ff9-108">The list includes the following for each message:</span></span>

- <span data-ttu-id="b0ff9-109">**Expéditeur** Nom d’envoi et adresse de messagerie du message en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="b0ff9-109">**Sender** The send name and email address of the quarantined message.</span></span>

- <span data-ttu-id="b0ff9-110">**Objet** Texte de l'objet du message en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="b0ff9-110">**Subject** The subject line text of the quarantined message.</span></span>

- <span data-ttu-id="b0ff9-111">**Date** Date et heure (UTC) auxquelles le message a été mis en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="b0ff9-111">**Date** The date and time (in UTC) that the message was quarantined.</span></span>

<span data-ttu-id="b0ff9-112">Voici les actions que vous pouvez effectuer avec un message en quarantaine :</span><span class="sxs-lookup"><span data-stu-id="b0ff9-112">These are the actions that you can take with a quarantined message:</span></span>

- <span data-ttu-id="b0ff9-113">**Bloquer l’expéditeur** si vous souhaitez qu’Office 365 ajoute l’expéditeur à votre liste des expéditeurs bloqués.</span><span class="sxs-lookup"><span data-stu-id="b0ff9-113">**Block Sender** if you want Office 365 to add the sender to your blocked senders list.</span></span>

- <span data-ttu-id="b0ff9-114">**Passez en revue** pour accéder au portail de mise en quarantaine dans le centre de sécurité et conformité si vous souhaitez effectuer d’autres actions, telles que l’aperçu ou la publication.</span><span class="sxs-lookup"><span data-stu-id="b0ff9-114">**Review** to navigate to the Quarantine Portal within the Security and Compliance Center if you want to take other actions, such as Preview or Release.</span></span>

<span data-ttu-id="b0ff9-115">Prenez en considération ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="b0ff9-115">Be aware of the following:</span></span>

- <span data-ttu-id="b0ff9-116">Les messages mis en quarantaine, car ils correspondent à une règle de flux de messagerie, ne sont pas inclus dans les messages mis en quarantaine par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b0ff9-116">Messages that are quarantined because they matched a mail flow rule are not included in user quarantined messages.</span></span> <span data-ttu-id="b0ff9-117">Seuls les messages mis en quarantaine car identifiés comme courrier indésirable sont répertoriés.</span><span class="sxs-lookup"><span data-stu-id="b0ff9-117">Only spam-quarantined messages are listed.</span></span>

- <span data-ttu-id="b0ff9-118">Vous ne pouvez libérer un message et le signaler comme faux positif (légitime) qu'une fois.</span><span class="sxs-lookup"><span data-stu-id="b0ff9-118">You can only release a message and report it as a false positive (not junk) once.</span></span>
