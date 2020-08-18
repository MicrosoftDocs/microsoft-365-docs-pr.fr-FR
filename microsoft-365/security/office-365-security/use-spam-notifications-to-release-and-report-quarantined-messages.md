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
ms.openlocfilehash: 2786c90f6f5fb66cbb96b0375dacf7793894f72e
ms.sourcegitcommit: 1780359234abdf081097c8064438d415da92fb85
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "46778503"
---
# <a name="use-user-spam-notifications-to-release-and-report-quarantined-messages"></a><span data-ttu-id="1f115-103">Utiliser les notifications de courrier indésirable de l’utilisateur pour publier et signaler les messages mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="1f115-103">Use user spam notifications to release and report quarantined messages</span></span>

<span data-ttu-id="1f115-104">Dans les organisations Microsoft 365 avec des boîtes aux lettres dans Exchange Online ou des organisations Exchange Online Protection (EOP) autonomes sans boîtes aux lettres Exchange Online, la quarantaine contient des messages potentiellement dangereux ou indésirables.</span><span class="sxs-lookup"><span data-stu-id="1f115-104">In Microsoft 365 organizations with mailboxes in Exchange Online or standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes, quarantine holds potentially dangerous or unwanted messages.</span></span> <span data-ttu-id="1f115-105">Pour plus d’informations, consultez la rubrique [messages en quarantaine dans EOP](quarantine-email-messages.md).</span><span class="sxs-lookup"><span data-stu-id="1f115-105">For more information, see [Quarantined messages in EOP](quarantine-email-messages.md).</span></span>

<span data-ttu-id="1f115-106">Par défaut, les notifications de courrier indésirable de l’utilisateur final sont désactivées dans les stratégies anti-courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="1f115-106">By default, end-user spam notifications are disabled in anti-spam policies.</span></span> <span data-ttu-id="1f115-107">Lorsqu’un administrateur [active les notifications de courrier indésirable de l’utilisateur final](configure-your-spam-filter-policies.md#configure-end-user-spam-notifications), les destinataires (y compris les boîtes aux lettres partagées sur lesquelles le mappage automatique est activé) reçoivent des notifications périodiques sur leurs messages mis en quarantaine en tant que courrier indésirable, en masse ou (depuis avril 2020).</span><span class="sxs-lookup"><span data-stu-id="1f115-107">When an admin [enables end-user spam notifications](configure-your-spam-filter-policies.md#configure-end-user-spam-notifications), recipients (including shared mailboxes with automapping enabled) will receive periodic notifications about their messages that were quarantined as spam, bulk email, or (as of April 2020) phishing.</span></span>

<span data-ttu-id="1f115-108">Pour les boîtes aux lettres partagées, les notifications de courrier indésirable de l’utilisateur final sont uniquement prises en charge pour les utilisateurs disposant de l’autorisation FullAccess sur la boîte aux lettres partagée.</span><span class="sxs-lookup"><span data-stu-id="1f115-108">For shared mailboxes, end-user spam notifications are only supported for users who are granted FullAccess permission to the shared mailbox.</span></span> <span data-ttu-id="1f115-109">Pour plus d’informations, consultez [la rubrique utiliser le centre d’administration Exchange pour modifier la délégation de boîtes aux lettres partagées](https://docs.microsoft.com/Exchange/collaboration-exo/shared-mailboxes#use-the-eac-to-edit-shared-mailbox-delegation).</span><span class="sxs-lookup"><span data-stu-id="1f115-109">For more information, see [Use the EAC to edit shared mailbox delegation](https://docs.microsoft.com/Exchange/collaboration-exo/shared-mailboxes#use-the-eac-to-edit-shared-mailbox-delegation).</span></span>

<span data-ttu-id="1f115-110">La notification de courrier indésirable des utilisateurs finaux n’est pas prise en charge pour les groupes.</span><span class="sxs-lookup"><span data-stu-id="1f115-110">End User Spam notification is not supported for groups.</span></span>

> [!NOTE]
> <span data-ttu-id="1f115-111">Les messages mis en quarantaine en tant que courriers indésirables de confiance élevée, programmes malveillants ou les règles de flux de messagerie (également appelées règles de transport) ne sont accessibles qu’aux administrateurs.</span><span class="sxs-lookup"><span data-stu-id="1f115-111">Messages that were quarantined as high confidence phishing, malware, or by mail flow rules (also known as transport rules) are only available to admins.</span></span> <span data-ttu-id="1f115-112">Si vous souhaitez en savoir plus, voir [Gérer les messages et les fichiers mis en quarantaine en tant qu'administrateur dans EOP](manage-quarantined-messages-and-files.md).</span><span class="sxs-lookup"><span data-stu-id="1f115-112">For more information, see [Manage quarantined messages and files as an admin in EOP](manage-quarantined-messages-and-files.md).</span></span>

<span data-ttu-id="1f115-113">Une notification de courrier indésirable de l’utilisateur final contient les informations suivantes pour chaque message en quarantaine :</span><span class="sxs-lookup"><span data-stu-id="1f115-113">An end-user spam notification contains the following information for each quarantined message:</span></span>

- <span data-ttu-id="1f115-114">**Expéditeur**: le nom d’envoi et l’adresse de messagerie du message en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="1f115-114">**Sender**: The send name and email address of the quarantined message.</span></span>

- <span data-ttu-id="1f115-115">**Objet**: texte de la ligne d’objet du message en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="1f115-115">**Subject**: The subject line text of the quarantined message.</span></span>

- <span data-ttu-id="1f115-116">**Date**: date et heure (UTC) auxquelles le message a été mis en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="1f115-116">**Date**: The date and time (in UTC) that the message was quarantined.</span></span>

- <span data-ttu-id="1f115-117">**Bloquer l’expéditeur**: cliquez sur ce lien pour ajouter l’expéditeur à votre liste des expéditeurs bloqués.</span><span class="sxs-lookup"><span data-stu-id="1f115-117">**Block Sender**: Click this link to add the sender to your Blocked Senders list.</span></span> <span data-ttu-id="1f115-118">Pour plus d’informations, consultez [la rubrique bloquer un expéditeur de courrier](https://support.microsoft.com/office/b29fd867-cac9-40d8-aed1-659e06a706e4).</span><span class="sxs-lookup"><span data-stu-id="1f115-118">For more information, see [Block a mail sender](https://support.microsoft.com/office/b29fd867-cac9-40d8-aed1-659e06a706e4).</span></span>

- <span data-ttu-id="1f115-119">**Release**: pour les messages de courrier indésirable (pas de hameçonnage), vous pouvez diffuser le message sans mettre en quarantaine le centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="1f115-119">**Release**: For spam (not phishing) messages, you can release the message here without going to Quarantine the Security & Compliance Center.</span></span>

- <span data-ttu-id="1f115-120">**Révision**: cliquez sur ce lien pour accéder à quarantaine dans le centre de sécurité & conformité, où vous pouvez (en fonction de la raison pour laquelle le message a été mis en quarantaine) afficher, publier, supprimer ou signaler vos messages mis en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="1f115-120">**Review**: Click this link to go to Quarantine in the Security & Compliance Center, where you can (depending on why the message was quarantined) view, release, delete or report your quarantined messages.</span></span> <span data-ttu-id="1f115-121">Pour plus d’informations, consultez [la rubrique Rechercher et débloquer les messages mis en quarantaine en tant qu’utilisateur dans EOP](find-and-release-quarantined-messages-as-a-user.md).</span><span class="sxs-lookup"><span data-stu-id="1f115-121">For more information, see [Find and release quarantined messages as a user in EOP](find-and-release-quarantined-messages-as-a-user.md).</span></span>

![Exemple de notification de courrier indésirable pour l’utilisateur final](../../media/end-user-spam-notification.png)
