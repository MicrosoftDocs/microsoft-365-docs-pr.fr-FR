---
title: Notifications de courrier indésirable pour l’utilisateur final Microsoft 365
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: Admin
ms.topic: conceptual
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
description: Les administrateurs peuvent en savoir plus sur les notifications de courrier indésirable pour les messages mis en quarantaine dans Exchange Online Protection (EOP).
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 71f2a33ad83f94895c396f92c18753bfca7f2905
ms.sourcegitcommit: ac3e9ccb7b43a42e600af8f44e6f30019533faeb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/15/2021
ms.locfileid: "52933166"
---
# <a name="use-user-spam-notifications-to-release-and-report-quarantined-messages"></a><span data-ttu-id="c0446-103">Utiliser les notifications de courrier indésirable de l’utilisateur pour libérer et signaler les messages mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="c0446-103">Use user spam notifications to release and report quarantined messages</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="c0446-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="c0446-104">**Applies to**</span></span>
- [<span data-ttu-id="c0446-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="c0446-105">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="c0446-106">Microsoft Defender pour Office 365 : offre 1 et offre 2</span><span class="sxs-lookup"><span data-stu-id="c0446-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](defender-for-office-365.md)
- [<span data-ttu-id="c0446-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="c0446-107">Microsoft 365 Defender</span></span>](../defender/microsoft-365-defender.md)

<span data-ttu-id="c0446-108">Dans les organisations Microsoft 365 avec des boîtes aux lettres dans Exchange Online ou des organisations Exchange Online Protection (EOP) autonomes sans boîtes aux lettres Exchange Online, la quarantaine contient des messages potentiellement dangereux ou indésirables.</span><span class="sxs-lookup"><span data-stu-id="c0446-108">In Microsoft 365 organizations with mailboxes in Exchange Online or standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes, quarantine holds potentially dangerous or unwanted messages.</span></span> <span data-ttu-id="c0446-109">Pour plus d’informations, [voir Messages mis en quarantaine dans EOP.](quarantine-email-messages.md)</span><span class="sxs-lookup"><span data-stu-id="c0446-109">For more information, see [Quarantined messages in EOP](quarantine-email-messages.md).</span></span>

<span data-ttu-id="c0446-110">Par défaut, les notifications de courrier indésirable de l’utilisateur final sont désactivées dans les stratégies anti-courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="c0446-110">By default, end-user spam notifications are disabled in anti-spam policies.</span></span> <span data-ttu-id="c0446-111">Lorsqu’un administrateur active les notifications de courrier indésirable pour l’utilisateur final, les [destinataires](configure-your-spam-filter-policies.md#configure-end-user-spam-notifications)(y compris les boîtes aux lettres partagées avec le mappage automatique activé) reçoivent des notifications périodiques concernant leurs messages mis en quarantaine en tant que courrier indésirable, courrier en masse ou hameçonnage (depuis avril 2020).</span><span class="sxs-lookup"><span data-stu-id="c0446-111">When an admin [enables end-user spam notifications](configure-your-spam-filter-policies.md#configure-end-user-spam-notifications), recipients (including shared mailboxes with automapping enabled) will receive periodic notifications about their messages that were quarantined as spam, bulk email, or (as of April 2020) phishing.</span></span>

<span data-ttu-id="c0446-112">Pour les boîtes aux lettres partagées, les notifications de courrier indésirable à l’utilisateur final sont uniquement pris en charge pour les utilisateurs qui ont reçu l’autorisation Autorisation totale sur la boîte aux lettres partagée.</span><span class="sxs-lookup"><span data-stu-id="c0446-112">For shared mailboxes, end-user spam notifications are only supported for users who are granted FullAccess permission to the shared mailbox.</span></span> <span data-ttu-id="c0446-113">Pour plus d’informations, voir [Utiliser le EAC pour modifier la délégation de boîte aux lettres partagée.](/Exchange/collaboration-exo/shared-mailboxes#use-the-eac-to-edit-shared-mailbox-delegation)</span><span class="sxs-lookup"><span data-stu-id="c0446-113">For more information, see [Use the EAC to edit shared mailbox delegation](/Exchange/collaboration-exo/shared-mailboxes#use-the-eac-to-edit-shared-mailbox-delegation).</span></span>

<span data-ttu-id="c0446-114">La notification de courrier indésirable de l’utilisateur final n’est pas prise en charge pour les groupes.</span><span class="sxs-lookup"><span data-stu-id="c0446-114">End User Spam notification is not supported for groups.</span></span>

> [!NOTE]
> <span data-ttu-id="c0446-115">Les messages qui ont été mis en quarantaine en tant que hameçonnage à haut niveau de confiance, programmes malveillants ou par des règles de flux de messagerie (également appelées règles de transport) ne sont disponibles que pour les administrateurs.</span><span class="sxs-lookup"><span data-stu-id="c0446-115">Messages that were quarantined as high confidence phishing, malware, or by mail flow rules (also known as transport rules) are only available to admins.</span></span> <span data-ttu-id="c0446-116">Si vous souhaitez en savoir plus, voir [Gérer les messages et les fichiers mis en quarantaine en tant qu'administrateur dans EOP](manage-quarantined-messages-and-files.md).</span><span class="sxs-lookup"><span data-stu-id="c0446-116">For more information, see [Manage quarantined messages and files as an admin in EOP](manage-quarantined-messages-and-files.md).</span></span>

<span data-ttu-id="c0446-117">Une notification de courrier indésirable à l’utilisateur final contient les informations suivantes pour chaque message mis en quarantaine :</span><span class="sxs-lookup"><span data-stu-id="c0446-117">An end-user spam notification contains the following information for each quarantined message:</span></span>

- <span data-ttu-id="c0446-118">**Expéditeur :** nom d’envoi et adresse e-mail du message mis en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="c0446-118">**Sender**: The send name and email address of the quarantined message.</span></span>
- <span data-ttu-id="c0446-119">**Objet**: texte de la ligne d’objet du message mis en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="c0446-119">**Subject**: The subject line text of the quarantined message.</span></span>
- <span data-ttu-id="c0446-120">**Date**: date et heure (au UTC) de mise en quarantaine du message.</span><span class="sxs-lookup"><span data-stu-id="c0446-120">**Date**: The date and time (in UTC) that the message was quarantined.</span></span>
- <span data-ttu-id="c0446-121">**Bloquer l’expéditeur**: cliquez sur ce lien pour ajouter l’expéditeur à la liste des expéditeurs bloqués sur votre boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="c0446-121">**Block Sender**: Click this link to add the sender to the Blocked Senders list on your mailbox.</span></span> <span data-ttu-id="c0446-122">Pour plus d'informations, consultez [Bloquer un expéditeur du courrier](https://support.microsoft.com/office/b29fd867-cac9-40d8-aed1-659e06a706e4).</span><span class="sxs-lookup"><span data-stu-id="c0446-122">For more information, see [Block a mail sender](https://support.microsoft.com/office/b29fd867-cac9-40d8-aed1-659e06a706e4).</span></span>
- <span data-ttu-id="c0446-123">**Release**: pour les messages de courrier indésirable (et non  de hameçonnage), vous pouvez libérer le message ici sans mettre en quarantaine le Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="c0446-123">**Release**: For spam (not phishing) messages, you can release the message here without going to **Quarantine** the Microsoft 365 Defender portal.</span></span>
- <span data-ttu-id="c0446-124">**Révision**: cliquez sur  ce lien pour passer en quarantaine dans le portail Microsoft 365 Defender, où vous pouvez (selon la raison de la mise en quarantaine du message) afficher, libérer, supprimer ou signaler vos messages mis en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="c0446-124">**Review**: Click this link to go to **Quarantine** in the Microsoft 365 Defender portal, where you can (depending on why the message was quarantined) view, release, delete or report your quarantined messages.</span></span> <span data-ttu-id="c0446-125">Pour plus d’informations, voir Rechercher et libérer les messages mis en quarantaine en tant [qu’utilisateur dans EOP.](find-and-release-quarantined-messages-as-a-user.md)</span><span class="sxs-lookup"><span data-stu-id="c0446-125">For more information, see [Find and release quarantined messages as a user in EOP](find-and-release-quarantined-messages-as-a-user.md).</span></span>

![Exemple de notification de courrier indésirable pour l’utilisateur final](../../media/end-user-spam-notification.png)

> [!NOTE]
> <span data-ttu-id="c0446-127">Un expéditeur bloqué peut toujours vous envoyer des messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="c0446-127">A blocked sender can still send you mail.</span></span> <span data-ttu-id="c0446-128">Tous les messages provenant de cet expéditeur qui se déplacent vers votre boîte aux lettres sont immédiatement déplacés vers le dossier Courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="c0446-128">Any messages from this sender that make it to your mailbox will be immediately moved to the Junk Email folder.</span></span> <span data-ttu-id="c0446-129">Les futurs messages de cet expéditeur seront placés dans votre dossier Courrier indésirable ou mis en quarantaine par l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="c0446-129">Future messages from this sender will go to your Junk Email folder or to the end-user quarantine.</span></span> <span data-ttu-id="c0446-130">Si vous souhaitez supprimer ces messages à l’arrivée au lieu de les mettre en quarantaine, utilisez des règles de flux de messagerie [(également](/exchange/security-and-compliance/mail-flow-rules/mail-flow-rules) appelées règles de transport) pour supprimer les messages à l’arrivée.</span><span class="sxs-lookup"><span data-stu-id="c0446-130">If you would like to delete these messages on arrival instead of quarantining them, use [mail flow Rules](/exchange/security-and-compliance/mail-flow-rules/mail-flow-rules) (also known as transport rules) to delete the messages on arrival.</span></span>
