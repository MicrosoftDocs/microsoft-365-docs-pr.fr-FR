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
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 47742008af9c1cd0a0a17df9e43ebc0228a825b0
ms.sourcegitcommit: 786f90a163d34c02b8451d09aa1efb1e1d5f543c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/18/2021
ms.locfileid: "50288764"
---
# <a name="quarantined-email-messages-in-eop"></a><span data-ttu-id="86ba7-103">Messages électroniques mis en quarantaine dans EOP</span><span class="sxs-lookup"><span data-stu-id="86ba7-103">Quarantined email messages in EOP</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="86ba7-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="86ba7-104">**Applies to**</span></span>
- [<span data-ttu-id="86ba7-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="86ba7-105">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="86ba7-106">Microsoft Defender pour Office 365 Plan 1 et Plan 2</span><span class="sxs-lookup"><span data-stu-id="86ba7-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](office-365-atp.md)
- [<span data-ttu-id="86ba7-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="86ba7-107">Microsoft 365 Defender</span></span>](../mtp/microsoft-threat-protection.md)

<span data-ttu-id="86ba7-108">Dans les organisations Microsoft 365 avec des boîtes aux lettres dans Exchange Online ou dans des organisations Exchange Online Protection autonomes (EOP) sans boîtes aux lettres Exchange Online, la mise en quarantaine est disponible pour contenir les messages potentiellement dangereux ou indésirables.</span><span class="sxs-lookup"><span data-stu-id="86ba7-108">In Microsoft 365 organizations with mailboxes in Exchange Online or standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes, quarantine is available to hold potentially dangerous or unwanted messages.</span></span>

<span data-ttu-id="86ba7-109">Les stratégies anti-programme malveillant met automatiquement en quarantaine un message *si* des pièces jointes contiennent des programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="86ba7-109">Anti-malware policies automatically quarantine a message if *any* attachment is found to contain malware.</span></span> <span data-ttu-id="86ba7-110">Pour plus d’informations, voir [Configurer des stratégies anti-programme malveillant dans EOP.](configure-anti-malware-policies.md)</span><span class="sxs-lookup"><span data-stu-id="86ba7-110">For more information, see [Configure anti-malware policies in EOP](configure-anti-malware-policies.md).</span></span>

<span data-ttu-id="86ba7-111">Par défaut, la protection anti-courrier indésirable met en quarantaine les messages d’hameçonnage et envoie le courrier indésirable et les messages électroniques en bloc dans le dossier Courrier indésirable de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="86ba7-111">By default, anti-spam polices quarantine phishing messages, and deliver spam and bulk email messages to the user's Junk Email folder.</span></span> <span data-ttu-id="86ba7-112">Toutefois, vous pouvez également créer et personnaliser des stratégies anti-courrier indésirable pour mettre en quarantaine le courrier indésirable et les messages électroniques en masse.</span><span class="sxs-lookup"><span data-stu-id="86ba7-112">But, you can also create and customize anti-spam policies to quarantine spam and bulk-email messages.</span></span> <span data-ttu-id="86ba7-113">Si vous souhaitez en savoir plus, consultez l’article [Configurer les stratégies anti-courrier indésirable dans EOP](configure-your-spam-filter-policies.md).</span><span class="sxs-lookup"><span data-stu-id="86ba7-113">For more information, see [Configure anti-spam policies in EOP](configure-your-spam-filter-policies.md).</span></span>

<span data-ttu-id="86ba7-114">Les utilisateurs et les administrateurs peuvent travailler avec les messages mis en quarantaine :</span><span class="sxs-lookup"><span data-stu-id="86ba7-114">Both users and admins can work with quarantined messages:</span></span>

- <span data-ttu-id="86ba7-115">Les administrateurs peuvent utiliser tous les types de messages mis en quarantaine pour tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="86ba7-115">Admins can work with all types of quarantined messages for all users.</span></span> <span data-ttu-id="86ba7-116">Seuls les administrateurs peuvent utiliser des messages mis en quarantaine en tant que programmes malveillants, hameçonnage à haut niveau de confiance ou suite à des règles de flux de messagerie (également appelées règles de transport).</span><span class="sxs-lookup"><span data-stu-id="86ba7-116">Only admins can work with messages that were quarantined as malware, high confidence phishing, or as a result of mail flow rules (also known as transport rules).</span></span> <span data-ttu-id="86ba7-117">Si vous souhaitez en savoir plus, voir [Gérer les messages et les fichiers mis en quarantaine en tant qu'administrateur dans EOP](manage-quarantined-messages-and-files.md).</span><span class="sxs-lookup"><span data-stu-id="86ba7-117">For more information, see [Manage quarantined messages and files as an admin in EOP](manage-quarantined-messages-and-files.md).</span></span>

- <span data-ttu-id="86ba7-118">Les utilisateurs peuvent utiliser des messages mis en quarantaine dont ils sont destinataires si le message a été mis en quarantaine en tant que courrier indésirable, courrier en nombre ou hameçonnage (depuis avril 2020).</span><span class="sxs-lookup"><span data-stu-id="86ba7-118">Users can work with quarantined messages where they are a recipient if the message was quarantined as spam, bulk email, or (as of April 2020) phishing.</span></span> <span data-ttu-id="86ba7-119">Pour plus d’informations, voir Rechercher et libérer les messages mis en quarantaine en tant [qu’utilisateur dans EOP.](find-and-release-quarantined-messages-as-a-user.md)</span><span class="sxs-lookup"><span data-stu-id="86ba7-119">For more information, see [Find and release quarantined messages as a user in EOP](find-and-release-quarantined-messages-as-a-user.md).</span></span>

  <span data-ttu-id="86ba7-120">Pour empêcher les utilisateurs de gérer leurs propres messages de hameçonnage  mis en quarantaine, les administrateurs peuvent configurer une action différente pour le verdict de filtrage du courrier d’hameçonnage dans les stratégies anti-courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="86ba7-120">To prevent users from managing their own quarantined phishing messages, admins can configure a different action for the **Phishing email** filtering verdict in anti-spam policies.</span></span> <span data-ttu-id="86ba7-121">Si vous souhaitez en savoir plus, consultez l’article [Configurer les stratégies anti-courrier indésirable dans EOP](configure-your-spam-filter-policies.md).</span><span class="sxs-lookup"><span data-stu-id="86ba7-121">For more information, see [Configure anti-spam policies in EOP](configure-your-spam-filter-policies.md).</span></span>

- <span data-ttu-id="86ba7-122">Les administrateurs et les utilisateurs peuvent signaler des faux positifs à Microsoft en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="86ba7-122">Admins and users can report false positives to Microsoft in quarantine.</span></span>

<span data-ttu-id="86ba7-123">Pour plus d’informations sur la mise en quarantaine, consultez [la faq sur la mise en quarantaine.](quarantine-faq.md)</span><span class="sxs-lookup"><span data-stu-id="86ba7-123">For more information about, quarantine, see [Quarantine FAQ](quarantine-faq.md).</span></span>
