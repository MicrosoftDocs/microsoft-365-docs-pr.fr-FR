---
title: Utilisation des notifications de courrier indésirable pour l'utilisateur final et signalement des messages de courrier indésirable mis en quarantaine
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 12/09/2016
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 4b250bc9-0056-4426-8397-7b4398f1b026
ms.collection:
- M365-security-compliance
description: 'Les utilisateurs qui voient un message de notification de courrier indésirable à l’utilisateur final de leur administrateur sur le courrier en quarantaine peuvent effectuer ces actions sur les messages. '
ms.openlocfilehash: 5c113e186a0469714829592437698ddb1185a141
ms.sourcegitcommit: 5710ce729c55d95b8b452d99ffb7ea92b5cb254a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2019
ms.locfileid: "39971412"
---
# <a name="use-end-user-spam-notifications-to-release-and-report-spam-quarantined-messages"></a><span data-ttu-id="d7273-103">Utilisation des notifications de courrier indésirable pour l'utilisateur final et signalement des messages de courrier indésirable mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="d7273-103">Use end-user spam notifications to release and report spam-quarantined messages</span></span>

<span data-ttu-id="d7273-p101">Si l'administrateur active les notifications de courrier indésirable de l'utilisateur final, vous recevez un message de notification qui répertorie les messages destinés à votre boîte aux lettres ayant été identifiés comme des courriers indésirables et mis en quarantaine. Ce message comprend le nombre de messages de courrier indésirable mis en quarantaine répertoriés, ainsi que la date et l'heure (UTC) du dernier message de la liste. Dans cette liste, vous pouvez afficher les informations suivantes concernant chaque message :</span><span class="sxs-lookup"><span data-stu-id="d7273-p101">If your administrator enables end-user spam notifications, you'll receive a notification message that lists messages intended for your mailbox that were identified as spam and quarantined instead. This message includes the number of spam-quarantined messages listed, and the date and time (in Universal Coordinated Time (UTC)) of the last message in the list. From this list, you can view the following information about each message:</span></span>

- <span data-ttu-id="d7273-107">**Sender**: nom de l’expéditeur et adresse de messagerie du message en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="d7273-107">**Sender**: The sender name and email address of the quarantined message.</span></span>

- <span data-ttu-id="d7273-108">**Objet**: texte de la ligne d’objet du message en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="d7273-108">**Subject**: The subject line text of the quarantined message.</span></span>

- <span data-ttu-id="d7273-109">**Date**: date et heure (UTC) auxquelles le message a été mis en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="d7273-109">**Date**: The date and time (in UTC) that the message was quarantined.</span></span>

- <span data-ttu-id="d7273-110">**Taille**: taille du message en quarantaine, en kilo-octets (Ko).</span><span class="sxs-lookup"><span data-stu-id="d7273-110">**Size**: The size of the quarantined message, in kilobytes (KBs).</span></span>

<span data-ttu-id="d7273-111">Vous pouvez effectuer les actions suivantes sur chaque message :</span><span class="sxs-lookup"><span data-stu-id="d7273-111">You can perform the following actions on each message:</span></span>

- <span data-ttu-id="d7273-112">**Publier dans la boîte de réception**: lorsque vous cliquez sur ce lien, le message est envoyé à votre boîte de réception, où vous pouvez l’afficher.</span><span class="sxs-lookup"><span data-stu-id="d7273-112">**Release to Inbox**: Clicking this link sends the message to your inbox where you can view it.</span></span>

- <span data-ttu-id="d7273-113">**Signaler comme légitime**: le simple clic sur ce lien envoie une copie du message à Microsoft pour analyse.</span><span class="sxs-lookup"><span data-stu-id="d7273-113">**Report as Not Junk**: Clicking this link sends a copy of the message to Microsoft for analysis.</span></span> <span data-ttu-id="d7273-114">L'équipe du courrier indésirable évalue et analyse le message, puis, selon les résultats de l'analyse, adapte les règles de filtre de courrier indésirable pour autoriser le message.</span><span class="sxs-lookup"><span data-stu-id="d7273-114">The spam team evaluates and analyzes the message, and, depending on the results of the analysis, adjusts the anti-spam filter rules to allow the message through.</span></span>

> [!NOTE]
> <span data-ttu-id="d7273-115">Les messages mis en quarantaine en raison d’une règle de flux de messagerie (également appelée a) ne sont pas inclus dans les messages de mise en quarantaine du courrier indésirable de l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="d7273-115">Messages that are quarantined due to a mail flow rule (also known as a ) match are not included in end user spam quarantined messages.</span></span> <span data-ttu-id="d7273-116">Seuls les messages mis en quarantaine car identifiés comme courrier indésirable sont répertoriés.</span><span class="sxs-lookup"><span data-stu-id="d7273-116">Only spam-quarantined messages are listed.</span></span> <br/><br/>  <span data-ttu-id="d7273-117">Vous ne pouvez libérer un message et le signaler comme faux positif (légitime) qu'une fois.</span><span class="sxs-lookup"><span data-stu-id="d7273-117">You can only release a message and report it as a false positive (not junk) once.</span></span>
