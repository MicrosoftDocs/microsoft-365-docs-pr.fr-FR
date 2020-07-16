---
title: Notifications de courrier indésirable à l’utilisateur final dans Microsoft 365
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
ms.custom:
- seo-marvel-apr2020
description: Les administrateurs peuvent en savoir plus sur les notifications de courrier indésirable de l’utilisateur final pour les messages mis en quarantaine dans Exchange Online Protection (EOP).
ms.openlocfilehash: 14dcdfa8373e3826b23bc5574d1b5ae8ff76927b
ms.sourcegitcommit: 2acd9ec5e9d150389975e854c7883efc186a9432
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/16/2020
ms.locfileid: "44754783"
---
# <a name="use-user-spam-notifications-to-release-and-report-quarantined-messages"></a><span data-ttu-id="89102-103">Utiliser les notifications de courrier indésirable de l’utilisateur pour publier et signaler les messages mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="89102-103">Use user spam notifications to release and report quarantined messages</span></span>

<span data-ttu-id="89102-104">Dans les organisations Microsoft 365 avec des boîtes aux lettres dans Exchange Online ou des organisations Exchange Online Protection (EOP) autonomes sans boîtes aux lettres Exchange Online, la quarantaine contient des messages potentiellement dangereux ou indésirables.</span><span class="sxs-lookup"><span data-stu-id="89102-104">In Microsoft 365 organizations with mailboxes in Exchange Online or standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes, quarantine holds potentially dangerous or unwanted messages.</span></span> <span data-ttu-id="89102-105">Pour plus d’informations, consultez la rubrique [messages en quarantaine dans EOP](quarantine-email-messages.md).</span><span class="sxs-lookup"><span data-stu-id="89102-105">For more information, see [Quarantined messages in EOP](quarantine-email-messages.md).</span></span>

<span data-ttu-id="89102-106">Par défaut, les notifications de courrier indésirable de l’utilisateur final sont désactivées dans les stratégies anti-courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="89102-106">By default, end-user spam notifications are disabled in anti-spam policies.</span></span> <span data-ttu-id="89102-107">Lorsqu’un administrateur [active les notifications de courrier indésirable de l’utilisateur final](configure-your-spam-filter-policies.md#configure-end-user-spam-notifications), les destinataires (y compris les boîtes aux lettres partagées) reçoivent des notifications périodiques sur leurs messages mis en quarantaine en tant que courrier indésirable, en masse ou (depuis avril 2020).</span><span class="sxs-lookup"><span data-stu-id="89102-107">When an admin [enables end-user spam notifications](configure-your-spam-filter-policies.md#configure-end-user-spam-notifications), recipients (including shared mailboxes) will receive periodic notifications about their messages that were quarantined as spam, bulk email, or (as of April 2020) phishing.</span></span>

> [!NOTE]
> <span data-ttu-id="89102-108">Les messages mis en quarantaine en tant que courriers indésirables de confiance élevée, programmes malveillants ou les règles de flux de messagerie (également appelées règles de transport) ne sont accessibles qu’aux administrateurs.</span><span class="sxs-lookup"><span data-stu-id="89102-108">Messages that were quarantined as high confidence phishing, malware, or by mail flow rules (also known as transport rules) are only available to admins.</span></span> <span data-ttu-id="89102-109">Si vous souhaitez en savoir plus, voir [Gérer les messages et les fichiers mis en quarantaine en tant qu'administrateur dans EOP](manage-quarantined-messages-and-files.md).</span><span class="sxs-lookup"><span data-stu-id="89102-109">For more information, see [Manage quarantined messages and files as an admin in EOP](manage-quarantined-messages-and-files.md).</span></span>

<span data-ttu-id="89102-110">Une notification de courrier indésirable de l’utilisateur final contient les informations suivantes pour chaque message en quarantaine :</span><span class="sxs-lookup"><span data-stu-id="89102-110">An end-user spam notification contains the following information for each quarantined message:</span></span>

- <span data-ttu-id="89102-111">**Expéditeur**: le nom d’envoi et l’adresse de messagerie du message en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="89102-111">**Sender**: The send name and email address of the quarantined message.</span></span>

- <span data-ttu-id="89102-112">**Objet**: texte de la ligne d’objet du message en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="89102-112">**Subject**: The subject line text of the quarantined message.</span></span>

- <span data-ttu-id="89102-113">**Date**: date et heure (UTC) auxquelles le message a été mis en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="89102-113">**Date**: The date and time (in UTC) that the message was quarantined.</span></span>

- <span data-ttu-id="89102-114">**Bloquer l’expéditeur**: cliquez sur ce lien pour ajouter l’expéditeur à votre liste des expéditeurs bloqués.</span><span class="sxs-lookup"><span data-stu-id="89102-114">**Block Sender**: Click this link to add the sender to your Blocked Senders list.</span></span> <span data-ttu-id="89102-115">Pour plus d’informations, consultez [la rubrique bloquer un expéditeur de courrier](https://support.microsoft.com/office/b29fd867-cac9-40d8-aed1-659e06a706e4).</span><span class="sxs-lookup"><span data-stu-id="89102-115">For more information, see [Block a mail sender](https://support.microsoft.com/office/b29fd867-cac9-40d8-aed1-659e06a706e4).</span></span>

- <span data-ttu-id="89102-116">**Release**: pour les messages de courrier indésirable (pas de hameçonnage), vous pouvez diffuser le message sans mettre en quarantaine le centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="89102-116">**Release**: For spam (not phish) messages, you can release the message here without going to Quarantine the Security & Compliance Center.</span></span>

- <span data-ttu-id="89102-117">**Révision**: cliquez sur ce lien pour accéder à la quarantaine dans le centre de sécurité & conformité, dans lequel vous pouvez libérer, supprimer ou signaler vos messages mis en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="89102-117">**Review**: Click this link to go to Quarantine in the Security & Compliance Center, where you can release, delete or report your quarantined messages.</span></span> <span data-ttu-id="89102-118">Pour plus d’informations, consultez [la rubrique Rechercher et débloquer les messages mis en quarantaine en tant qu’utilisateur dans EOP](find-and-release-quarantined-messages-as-a-user.md).</span><span class="sxs-lookup"><span data-stu-id="89102-118">For more information, see [Find and release quarantined messages as a user in EOP](find-and-release-quarantined-messages-as-a-user.md).</span></span>

![Exemple de notification de courrier indésirable pour l’utilisateur final](../../media/end-user-spam-notification.png)
