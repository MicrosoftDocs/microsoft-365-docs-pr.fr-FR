---
title: Notifications de courrier indésirable à l’utilisateur final dans Office 36
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
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
description: Lorsqu’un administrateur Active les notifications de courrier indésirable de l’utilisateur final dans les stratégies de blocage du courrier indésirable, les destinataires des messages reçoivent régulièrement des notifications sur leurs messages mis en quarantaine.
ms.openlocfilehash: 6cde4681d7ea3ef5795201e9a2816b7224ad36f6
ms.sourcegitcommit: fce0d5cad32ea60a08ff001b228223284710e2ed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/21/2020
ms.locfileid: "42895058"
---
# <a name="end-user-spam-notifications-in-office-365"></a><span data-ttu-id="a884d-103">Notifications de courrier indésirable à l’utilisateur final dans Office 365</span><span class="sxs-lookup"><span data-stu-id="a884d-103">End-user spam notifications in Office 365</span></span>

<span data-ttu-id="a884d-104">La quarantaine contient des messages potentiellement dangereux ou indésirables dans les organisations Office 365 avec des boîtes aux lettres dans Exchange Online ou des organisations Exchange Online Protection (EOP) autonomes sans boîtes aux lettres Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="a884d-104">Quarantine holds potentially dangerous or unwanted messages in Office 365 organizations with mailboxes in Exchange Online or standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes.</span></span> <span data-ttu-id="a884d-105">Si vous souhaitez en savoir plus, consultez l’article [La quarantaine dans Office 365](quarantine-email-messages.md).</span><span class="sxs-lookup"><span data-stu-id="a884d-105">For more information, see [Quarantine in Office 365](quarantine-email-messages.md).</span></span>

<span data-ttu-id="a884d-106">Par défaut, les notifications de courrier indésirable de l’utilisateur final sont désactivées dans les stratégies anti-courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="a884d-106">By default, end-user spam notifications are disabled in anti-spam policies.</span></span> <span data-ttu-id="a884d-107">Lorsqu’un administrateur [active les notifications de courrier indésirable de l’utilisateur final](configure-your-spam-filter-policies.md), les destinataires des messages reçoivent régulièrement des notifications sur leurs messages mis en quarantaine en tant que courrier indésirable, en masse ou (depuis avril 2020).</span><span class="sxs-lookup"><span data-stu-id="a884d-107">When an admin [enables end-user spam notifications](configure-your-spam-filter-policies.md), message recipients will receive periodic notifications about their messages that were quarantined as spam, bulk email, or (as of April, 2020) phishing.</span></span>

> [!NOTE]
> <span data-ttu-id="a884d-108">En octobre 2019, nous avons supprimé la possibilité de débloquer les messages mis en quarantaine directement à partir des notifications de courrier indésirable de l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="a884d-108">In October 2019, we removed the ability to release quarantined messages directly from end-user spam notifications.</span></span> <span data-ttu-id="a884d-109">Au lieu de cela, les utilisateurs peuvent désormais accéder au centre de conformité Office 365 Security & pour libérer leurs messages mis en quarantaine (soit directement, soit en cliquant sur **examiner** dans la notification).</span><span class="sxs-lookup"><span data-stu-id="a884d-109">Instead, users can now go to the Office 365 Security & Compliance Center to release their quarantined messages (either directly, or by clicking **Review** in the notification).</span></span> <span data-ttu-id="a884d-110">Pour plus d’informations, consultez [la rubrique Rechercher et débloquer les messages mis en quarantaine en tant qu’utilisateur dans Office 365](find-and-release-quarantined-messages-as-a-user.md).</span><span class="sxs-lookup"><span data-stu-id="a884d-110">For more information, see [Find and release quarantined messages as a user in Office 365](find-and-release-quarantined-messages-as-a-user.md).</span></span> <br/><br/> <span data-ttu-id="a884d-111">Les messages mis en quarantaine en tant que courriers indésirables de confiance élevée, programmes malveillants ou les règles de flux de messagerie (également appelées règles de transport) ne sont accessibles qu’aux administrateurs.</span><span class="sxs-lookup"><span data-stu-id="a884d-111">Messages that were quarantined as high confidence phishing, malware, or by mail flow rules (also known as transport rules) are only available to admins.</span></span> <span data-ttu-id="a884d-112">Pour plus d’informations, consultez la rubrique [gestion des messages et des fichiers mis en quarantaine en tant qu’administrateur dans Office 365](manage-quarantined-messages-and-files.md).</span><span class="sxs-lookup"><span data-stu-id="a884d-112">For more information, see [Manage quarantined messages and files as an admin in Office 365](manage-quarantined-messages-and-files.md).</span></span>

<span data-ttu-id="a884d-113">Une notification de courrier indésirable de l’utilisateur final contient les informations suivantes pour chaque message en quarantaine :</span><span class="sxs-lookup"><span data-stu-id="a884d-113">An end-user spam notification contains the following information for each quarantined message:</span></span>

- <span data-ttu-id="a884d-114">**Expéditeur**: le nom d’envoi et l’adresse de messagerie du message en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="a884d-114">**Sender**: The send name and email address of the quarantined message.</span></span>

- <span data-ttu-id="a884d-115">**Objet**: texte de la ligne d’objet du message en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="a884d-115">**Subject**: The subject line text of the quarantined message.</span></span>

- <span data-ttu-id="a884d-116">**Date**: date et heure (UTC) auxquelles le message a été mis en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="a884d-116">**Date**: The date and time (in UTC) that the message was quarantined.</span></span>

- <span data-ttu-id="a884d-117">**Bloquer l’expéditeur**: cliquez sur ce lien pour ajouter l’expéditeur à votre liste des expéditeurs bloqués.</span><span class="sxs-lookup"><span data-stu-id="a884d-117">**Block Sender**: Click this link to add the sender to your Blocked Senders list.</span></span>

- <span data-ttu-id="a884d-118">**Révision**: cliquez sur ce lien pour accéder à la mise en quarantaine dans le centre de sécurité & conformité, dans lequel vous pouvez libérer, supprimer ou signaler vos messages mis en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="a884d-118">**Review**: Click this link to go the the Quarantine in the Security & Compliance Center, where you can release, delete or report your quarantined messages.</span></span>

![Exemple de notification de courrier indésirable pour l’utilisateur final](../../media/end-user-spam-notification.png)
