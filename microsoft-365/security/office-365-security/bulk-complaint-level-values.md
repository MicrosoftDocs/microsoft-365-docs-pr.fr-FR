---
title: Valeurs de niveau de réclamation en bloc
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: conceptual
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: a5b03b3c-37dd-429e-8e9b-2c1b25031794
ms.collection:
- M365-security-compliance
description: Les administrateurs peuvent en savoir plus sur les valeurs BCL (bulk complaint level) utilisées dans Exchange Online Protection (EOP).
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 11f884ec6b32795deba09c0f1ba88055a6422e9b
ms.sourcegitcommit: f780de91bc00caeb1598781e0076106c76234bad
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2021
ms.locfileid: "52537942"
---
# <a name="bulk-complaint-level-bcl-in-eop"></a><span data-ttu-id="f9cc4-103">Niveau de réclamation en bloc (BCL) dans EOP</span><span class="sxs-lookup"><span data-stu-id="f9cc4-103">Bulk complaint level (BCL) in EOP</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="f9cc4-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="f9cc4-104">**Applies to**</span></span>
- [<span data-ttu-id="f9cc4-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="f9cc4-105">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="f9cc4-106">Microsoft Defender pour Office 365 : offre 1 et offre 2</span><span class="sxs-lookup"><span data-stu-id="f9cc4-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](defender-for-office-365.md)
- [<span data-ttu-id="f9cc4-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="f9cc4-107">Microsoft 365 Defender</span></span>](../defender/microsoft-365-defender.md)

<span data-ttu-id="f9cc4-108">Dans Microsoft 365 organisations avec des boîtes aux lettres en Exchange Online ou des organisations Exchange Online Protection autonomes (EOP) sans boîtes aux lettres Exchange Online, EOP affecte un niveau de réclamation en bloc (BCL) aux messages entrants provenant de publipostages en masse.</span><span class="sxs-lookup"><span data-stu-id="f9cc4-108">In Microsoft 365 organizations with mailboxes in Exchange Online or standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes, EOP assigns a bulk complaint level (BCL) to inbound messages from bulk mailers.</span></span> <span data-ttu-id="f9cc4-109">Le bcl est ajouté au message dans un en-tête X et est similaire au niveau de confiance du courrier indésirable [(SCL)](spam-confidence-levels.md) utilisé pour identifier les messages comme courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="f9cc4-109">The BCL is added to the message in an X-header and is similar to the [spam confidence level (SCL)](spam-confidence-levels.md) that's used to identify messages as spam.</span></span> <span data-ttu-id="f9cc4-110">Une valeur BCL supérieure indique qu’un message en nombre est plus susceptible de générer des réclamations (et est donc plus susceptible d’être du courrier indésirable).</span><span class="sxs-lookup"><span data-stu-id="f9cc4-110">A higher BCL indicates a bulk message is more likely to generate complaints (and is therefore more likely to be spam).</span></span> <span data-ttu-id="f9cc4-111">Microsoft utilise des sources internes et tierces pour identifier le courrier en nombre et déterminer le bcl approprié.</span><span class="sxs-lookup"><span data-stu-id="f9cc4-111">Microsoft uses both internal and third party sources to identify bulk mail and determine the appropriate BCL.</span></span>

<span data-ttu-id="f9cc4-112">Les publipostages en nombre varient selon les modèles d’envoi, la création de contenu et les pratiques d’acquisition des destinataires.</span><span class="sxs-lookup"><span data-stu-id="f9cc4-112">Bulk mailers vary in their sending patterns, content creation, and recipient acquisition practices.</span></span> <span data-ttu-id="f9cc4-113">Les expéditeurs de courrier en nombre de bonne qualité envoient les messages souhaités avec du contenu pertinent à leurs abonnés.</span><span class="sxs-lookup"><span data-stu-id="f9cc4-113">Good bulk mailers send desired messages with relevant content to their subscribers.</span></span> <span data-ttu-id="f9cc4-114">Ces messages entraînent peu de réclamations de la part des destinataires.</span><span class="sxs-lookup"><span data-stu-id="f9cc4-114">These messages generate few complaints from recipients.</span></span> <span data-ttu-id="f9cc4-115">D'autres vers de publipostage en bloc envoient des messages non sollicités qui s'apparentent fortement à du courrier indésirable et entraînent de nombreuses réclamations de la part des destinataires.</span><span class="sxs-lookup"><span data-stu-id="f9cc4-115">Other bulk mailers send unsolicited messages that closely resemble spam and generate many complaints from recipients.</span></span> <span data-ttu-id="f9cc4-116">Les messages provenant d’un publipostage en masse sont appelés courriers en masse ou gris.</span><span class="sxs-lookup"><span data-stu-id="f9cc4-116">Messages from a bulk mailer are known as bulk mail or gray mail.</span></span>

 <span data-ttu-id="f9cc4-117">Le filtrage du  courrier indésirable marque les messages en tant que messages électroniques en bloc en fonction du seuil BCL (valeur par défaut ou valeur que vous spécifiez) et prend l’action spécifiée sur le message (l’action par défaut consiste à remettre le message dans le dossier Courrier indésirable du destinataire).</span><span class="sxs-lookup"><span data-stu-id="f9cc4-117">Spam filtering marks messages as **Bulk email** based on the BCL threshold (the default value or a value you specify) and takes the specified action on the message (the default action is deliver the message to the recipient's Junk Email folder).</span></span> <span data-ttu-id="f9cc4-118">Pour plus d’informations, voir Configurer des [stratégies anti-courrier](configure-your-spam-filter-policies.md) indésirable et quelle est la différence entre le courrier indésirable et le [courrier en masse ?](what-s-the-difference-between-junk-email-and-bulk-email.md)</span><span class="sxs-lookup"><span data-stu-id="f9cc4-118">For more information, see [Configure anti-spam policies](configure-your-spam-filter-policies.md) and [What's the difference between junk email and bulk email?](what-s-the-difference-between-junk-email-and-bulk-email.md)</span></span>

<span data-ttu-id="f9cc4-119">Vous pouvez utiliser la liste d’adresses client autoriser/bloquer pour configurer des exceptions pour le filtrage du courrier en bloc.</span><span class="sxs-lookup"><span data-stu-id="f9cc4-119">You can use the Tenant Allow/Block List to configure exceptions for bulk mail filtering.</span></span> <span data-ttu-id="f9cc4-120">Les messages provenant d’expéditeurs dans les domaines spécifiés ne reçoivent pas l’action du verdict de filtrage du courrier indésirable en bloc dans les stratégies anti-courrier indésirable. </span><span class="sxs-lookup"><span data-stu-id="f9cc4-120">Messages from senders in the specified domains don't receive the action for the **Bulk email** spam filtering verdict in anti-spam policies.</span></span> <span data-ttu-id="f9cc4-121">Pour plus d’informations, [voir Manage the Tenant Allow/Block List](tenant-allow-block-list.md).</span><span class="sxs-lookup"><span data-stu-id="f9cc4-121">For more information, see [Manage the Tenant Allow/Block List](tenant-allow-block-list.md).</span></span>

<span data-ttu-id="f9cc4-122">Les seuils BCL sont décrits dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="f9cc4-122">The BCL thresholds are described in the following table.</span></span>

****

|<span data-ttu-id="f9cc4-123">BCL</span><span class="sxs-lookup"><span data-stu-id="f9cc4-123">BCL</span></span>|<span data-ttu-id="f9cc4-124">Description</span><span class="sxs-lookup"><span data-stu-id="f9cc4-124">Description</span></span>|
|:---:|---|
|<span data-ttu-id="f9cc4-125">0</span><span class="sxs-lookup"><span data-stu-id="f9cc4-125">0</span></span>|<span data-ttu-id="f9cc4-126">Le message ne provient pas d'un expéditeur en bloc.</span><span class="sxs-lookup"><span data-stu-id="f9cc4-126">The message isn't from a bulk sender.</span></span>|
|<span data-ttu-id="f9cc4-127">1, 2, 3</span><span class="sxs-lookup"><span data-stu-id="f9cc4-127">1, 2, 3</span></span>|<span data-ttu-id="f9cc4-128">Le message provient d'un expéditeur en bloc qui génère peu de réclamations.</span><span class="sxs-lookup"><span data-stu-id="f9cc4-128">The message is from a bulk sender that generates few complaints.</span></span>|
|<span data-ttu-id="f9cc4-129">4, 5, 6, 7<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="f9cc4-129">4, 5, 6, 7<sup>\*</sup></span></span>|<span data-ttu-id="f9cc4-130">Le message provient d'un expéditeur en bloc qui génère un nombre moyen de réclamations.</span><span class="sxs-lookup"><span data-stu-id="f9cc4-130">The message is from a bulk sender that generates a mixed number of complaints.</span></span>|
|<span data-ttu-id="f9cc4-131">8, 9</span><span class="sxs-lookup"><span data-stu-id="f9cc4-131">8, 9</span></span>|<span data-ttu-id="f9cc4-132">Le message est provenant d’un expéditeur en bloc qui génère un nombre élevé de réclamations.</span><span class="sxs-lookup"><span data-stu-id="f9cc4-132">The message is from a bulk sender that generates a high number of complaints.</span></span>|
|

<span data-ttu-id="f9cc4-133"><sup>\*</sup> Il s’agit de la valeur de seuil par défaut utilisée dans les stratégies anti-courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="f9cc4-133"><sup>\*</sup> This is the default threshold value that's used in anti-spam policies.</span></span>
