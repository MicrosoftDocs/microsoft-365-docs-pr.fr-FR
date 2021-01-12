---
title: Messages électroniques mis en quarantaine
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: 4c234874-015e-4768-8495-98fcccfc639b
ms.collection:
- M365-security-compliance
- m365initiative-defender-office365
ms.custom:
- seo-marvel-apr2020
description: Les administrateurs peuvent en savoir plus sur la mise en quarantaine dans Exchange Online Protection (EOP) qui contient des messages potentiellement dangereux ou indésirables.
ms.openlocfilehash: 8a978ece029de06bcb7b434de730b0baea33a5e1
ms.sourcegitcommit: 9833f95ab6ab95aea20d68a277246dca2223f93d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/11/2021
ms.locfileid: "49794327"
---
# <a name="quarantined-email-messages-in-eop"></a><span data-ttu-id="cfb88-103">Messages électroniques mis en quarantaine dans EOP</span><span class="sxs-lookup"><span data-stu-id="cfb88-103">Quarantined email messages in EOP</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


<span data-ttu-id="cfb88-104">Dans les organisations Microsoft 365 avec des boîtes aux lettres dans Exchange Online ou dans des organisations Exchange Online Protection autonomes (EOP) sans boîtes aux lettres Exchange Online, la mise en quarantaine est disponible pour contenir les messages potentiellement dangereux ou indésirables.</span><span class="sxs-lookup"><span data-stu-id="cfb88-104">In Microsoft 365 organizations with mailboxes in Exchange Online or standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes, quarantine is available to hold potentially dangerous or unwanted messages.</span></span>

<span data-ttu-id="cfb88-105">Les stratégies anti-programme malveillant met automatiquement en quarantaine un message *si* des pièces jointes contiennent des programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="cfb88-105">Anti-malware policies automatically quarantine a message if *any* attachment is found to contain malware.</span></span> <span data-ttu-id="cfb88-106">Pour plus d’informations, voir [Configurer des stratégies anti-programme malveillant dans EOP.](configure-anti-malware-policies.md)</span><span class="sxs-lookup"><span data-stu-id="cfb88-106">For more information, see [Configure anti-malware policies in EOP](configure-anti-malware-policies.md).</span></span>

<span data-ttu-id="cfb88-107">Par défaut, la protection anti-courrier indésirable met en quarantaine les messages d’hameçonnage et envoie le courrier indésirable et les messages électroniques en bloc dans le dossier Courrier indésirable de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cfb88-107">By default, anti-spam polices quarantine phishing messages, and deliver spam and bulk email messages to the user's Junk Email folder.</span></span> <span data-ttu-id="cfb88-108">Toutefois, vous pouvez également créer et personnaliser des stratégies anti-courrier indésirable pour mettre en quarantaine le courrier indésirable et les messages électroniques en bloc.</span><span class="sxs-lookup"><span data-stu-id="cfb88-108">But, you can also create and customize anti-spam policies to quarantine spam and bulk-email messages.</span></span> <span data-ttu-id="cfb88-109">Si vous souhaitez en savoir plus, consultez l’article [Configurer les stratégies anti-courrier indésirable dans EOP](configure-your-spam-filter-policies.md).</span><span class="sxs-lookup"><span data-stu-id="cfb88-109">For more information, see [Configure anti-spam policies in EOP](configure-your-spam-filter-policies.md).</span></span>

<span data-ttu-id="cfb88-110">Les utilisateurs et les administrateurs peuvent travailler avec les messages mis en quarantaine :</span><span class="sxs-lookup"><span data-stu-id="cfb88-110">Both users and admins can work with quarantined messages:</span></span>

- <span data-ttu-id="cfb88-111">Les administrateurs peuvent utiliser tous les types de messages mis en quarantaine pour tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="cfb88-111">Admins can work with all types of quarantined messages for all users.</span></span> <span data-ttu-id="cfb88-112">Seuls les administrateurs peuvent utiliser des messages mis en quarantaine en tant que programmes malveillants, hameçonnage à haut niveau de confiance ou suite à des règles de flux de messagerie (également appelées règles de transport).</span><span class="sxs-lookup"><span data-stu-id="cfb88-112">Only admins can work with messages that were quarantined as malware, high confidence phishing, or as a result of mail flow rules (also known as transport rules).</span></span> <span data-ttu-id="cfb88-113">Si vous souhaitez en savoir plus, voir [Gérer les messages et les fichiers mis en quarantaine en tant qu'administrateur dans EOP](manage-quarantined-messages-and-files.md).</span><span class="sxs-lookup"><span data-stu-id="cfb88-113">For more information, see [Manage quarantined messages and files as an admin in EOP](manage-quarantined-messages-and-files.md).</span></span>

- <span data-ttu-id="cfb88-114">Les utilisateurs peuvent utiliser des messages mis en quarantaine lorsqu’ils sont destinataires si le message a été mis en quarantaine en tant que courrier indésirable, courrier en nombre ou hameçonnage (depuis avril 2020).</span><span class="sxs-lookup"><span data-stu-id="cfb88-114">Users can work with quarantined messages where they are a recipient if the message was quarantined as spam, bulk email, or (as of April 2020) phishing.</span></span> <span data-ttu-id="cfb88-115">Pour plus d’informations, voir Rechercher et libérer les messages mis en quarantaine en tant [qu’utilisateur dans EOP.](find-and-release-quarantined-messages-as-a-user.md)</span><span class="sxs-lookup"><span data-stu-id="cfb88-115">For more information, see [Find and release quarantined messages as a user in EOP](find-and-release-quarantined-messages-as-a-user.md).</span></span>

  <span data-ttu-id="cfb88-116">Pour empêcher les utilisateurs de gérer leurs propres messages de hameçonnage  mis en quarantaine, les administrateurs peuvent configurer une action différente pour le verdict de filtrage du courrier d’hameçonnage dans les stratégies anti-courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="cfb88-116">To prevent users from managing their own quarantined phishing messages, admins can configure a different action for the **Phishing email** filtering verdict in anti-spam policies.</span></span> <span data-ttu-id="cfb88-117">Si vous souhaitez en savoir plus, consultez l’article [Configurer les stratégies anti-courrier indésirable dans EOP](configure-your-spam-filter-policies.md).</span><span class="sxs-lookup"><span data-stu-id="cfb88-117">For more information, see [Configure anti-spam policies in EOP](configure-your-spam-filter-policies.md).</span></span>

- <span data-ttu-id="cfb88-118">Les administrateurs et les utilisateurs peuvent signaler des faux positifs à Microsoft en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="cfb88-118">Admins and users can report false positives to Microsoft in quarantine.</span></span>

<span data-ttu-id="cfb88-119">Pour plus d’informations sur la mise en quarantaine, consultez [la faq sur la mise en quarantaine.](quarantine-faq.md)</span><span class="sxs-lookup"><span data-stu-id="cfb88-119">For more information about, quarantine, see [Quarantine FAQ](quarantine-faq.md).</span></span>
