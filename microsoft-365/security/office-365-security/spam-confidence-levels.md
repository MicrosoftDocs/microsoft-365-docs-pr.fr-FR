---
title: Spam confidence level
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
ms.assetid: 34681000-0022-4b92-b38a-e32b3ed96bf6
ms.collection:
- M365-security-compliance
ms.custom:
- seo-marvel-apr2020
description: Les administrateurs peuvent en savoir plus sur le niveau de confiance du courrier indésirable (SCL) appliqué aux messages dans Exchange Online Protection (EOP).
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: e4fc20b7d7db5b85b5bdde02ab720fa26af2a4b5
ms.sourcegitcommit: a1846b1ee2e4fa397e39c1271c997fc4cf6d5619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2021
ms.locfileid: "50167154"
---
# <a name="spam-confidence-level-scl-in-eop"></a><span data-ttu-id="18865-103">Niveau de confiance du courrier indésirable (SCL) dans EOP</span><span class="sxs-lookup"><span data-stu-id="18865-103">Spam confidence level (SCL) in EOP</span></span>

<span data-ttu-id="18865-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="18865-104">**Applies to**</span></span>
- [<span data-ttu-id="18865-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="18865-105">Exchange Online Protection</span></span>](https://go.microsoft.com/fwlink/?linkid=2148611)
- [<span data-ttu-id="18865-106">Microsoft Defender pour Office 365 plan 1 et plan 2</span><span class="sxs-lookup"><span data-stu-id="18865-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](https://go.microsoft.com/fwlink/?linkid=2148715)
- [<span data-ttu-id="18865-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="18865-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="18865-108">Dans les organisations Microsoft 365 avec des boîtes aux lettres dans Exchange Online ou des organisations Exchange Online Protection autonomes (EOP) sans boîtes aux lettres Exchange Online, les messages entrants sont filtrés par le filtrage du courrier indésirable dans EOP et un score de courrier indésirable leur est attribué.</span><span class="sxs-lookup"><span data-stu-id="18865-108">In Microsoft 365 organizations with mailboxes in Exchange Online or standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes, inbound messages go through spam filtering in EOP and are assigned a spam score.</span></span> <span data-ttu-id="18865-109">Ce score est mappé à un niveau de confiance de courrier indésirable (SCL) individuel qui est ajouté au message dans un en-tête X.</span><span class="sxs-lookup"><span data-stu-id="18865-109">That score is mapped to an individual spam confidence level (SCL) that's added to the message in an X-header.</span></span> <span data-ttu-id="18865-110">Un SCL plus élevé indique qu’un message est plus susceptible d’être du courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="18865-110">A higher SCL indicates a message is more likely to be spam.</span></span> <span data-ttu-id="18865-111">EOP prend des mesures sur le message en fonction du SCL.</span><span class="sxs-lookup"><span data-stu-id="18865-111">EOP takes action on the message based on the SCL.</span></span>

<span data-ttu-id="18865-112">Ce que signifie le SCL et les actions par défaut qui sont prises sur les messages sont décrits dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="18865-112">What the SCL means and the default actions that are taken on messages are described in the following table.</span></span> <span data-ttu-id="18865-113">Pour plus d’informations sur les actions que vous pouvez prendre sur les messages en fonction du verdict de filtrage du courrier indésirable, voir Configurer des stratégies [anti-courrier indésirable dans EOP.](configure-your-spam-filter-policies.md)</span><span class="sxs-lookup"><span data-stu-id="18865-113">For more information about actions you can take on messages based on the spam filtering verdict, see [Configure anti-spam policies in EOP](configure-your-spam-filter-policies.md).</span></span>

****

|<span data-ttu-id="18865-114">SCL</span><span class="sxs-lookup"><span data-stu-id="18865-114">SCL</span></span>|<span data-ttu-id="18865-115">Définition</span><span class="sxs-lookup"><span data-stu-id="18865-115">Definition</span></span>|<span data-ttu-id="18865-116">Action par défaut</span><span class="sxs-lookup"><span data-stu-id="18865-116">Default action</span></span>|
|:---:|---|---|
|<span data-ttu-id="18865-117">-1</span><span class="sxs-lookup"><span data-stu-id="18865-117">-1</span></span>|<span data-ttu-id="18865-118">Le message a ignoré le filtrage du courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="18865-118">The message skipped spam filtering.</span></span> <span data-ttu-id="18865-119">Par exemple, le message est provenant d’un expéditeur fiable, a été envoyé à un destinataire fiable ou à partir d’un serveur source de messagerie sur la liste d’adresses IP permises.</span><span class="sxs-lookup"><span data-stu-id="18865-119">For example, the message is from a safe sender, was sent to a safe recipient, or is from an email source server on the IP Allow List.</span></span> <span data-ttu-id="18865-120">Pour plus d’informations, voir [Créer des listes d’expéditeurs sûrs dans EOP.](create-safe-sender-lists-in-office-365.md)</span><span class="sxs-lookup"><span data-stu-id="18865-120">For more information, see [Create safe sender lists in EOP](create-safe-sender-lists-in-office-365.md).</span></span>|<span data-ttu-id="18865-121">Le message est remis dans la boîte aux lettres des destinataires.</span><span class="sxs-lookup"><span data-stu-id="18865-121">Deliver the message to the recipients' inbox.</span></span>|
|<span data-ttu-id="18865-122">0, 1</span><span class="sxs-lookup"><span data-stu-id="18865-122">0, 1</span></span>|<span data-ttu-id="18865-123">Le filtrage du courrier indésirable a déterminé que le message n’était pas du courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="18865-123">Spam filtering determined the message was not spam.</span></span>|<span data-ttu-id="18865-124">Le message est remis dans la boîte aux lettres des destinataires.</span><span class="sxs-lookup"><span data-stu-id="18865-124">Deliver the message to the recipients' inbox.</span></span>|
|<span data-ttu-id="18865-125">5, 6</span><span class="sxs-lookup"><span data-stu-id="18865-125">5, 6</span></span>|<span data-ttu-id="18865-126">Le filtrage du courrier indésirable a marqué le message comme **courrier indésirable**</span><span class="sxs-lookup"><span data-stu-id="18865-126">Spam filtering marked the message as **Spam**</span></span>|<span data-ttu-id="18865-127">Le message est envoyé vers le dossier Courrier indésirable des destinataires.</span><span class="sxs-lookup"><span data-stu-id="18865-127">Deliver the message to the recipients' Junk Email folder.</span></span>|
|<span data-ttu-id="18865-128">9 </span><span class="sxs-lookup"><span data-stu-id="18865-128">9</span></span>|<span data-ttu-id="18865-129">Le filtrage du courrier indésirable a marqué le message comme courrier **indésirable à niveau de confiance élevé**</span><span class="sxs-lookup"><span data-stu-id="18865-129">Spam filtering marked the message as **High confidence spam**</span></span>|<span data-ttu-id="18865-130">Le message est envoyé vers le dossier Courrier indésirable des destinataires.</span><span class="sxs-lookup"><span data-stu-id="18865-130">Deliver the message to the recipients' Junk Email folder.</span></span>|
|

<span data-ttu-id="18865-131">Vous remarquerez que les SCL 2, 3, 4, 7 et 8 ne sont pas utilisés par le filtrage du courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="18865-131">You'll notice that SCL 2, 3, 4, 7, and 8 aren't used by spam filtering.</span></span>

<span data-ttu-id="18865-132">Vous pouvez utiliser des règles de flux de messagerie (également appelées règles de transport) pour marquer le SCL sur les messages.</span><span class="sxs-lookup"><span data-stu-id="18865-132">You can use mail flow rules (also known as transport rules) to stamp the SCL on messages.</span></span> <span data-ttu-id="18865-133">Si vous utilisez une règle de flux de messagerie pour définir le SCL, les valeurs 5 ou 6 déclenchent l’action de filtrage du courrier indésirable **et** les valeurs 7, 8 ou 9 déclenchent l’action de filtrage du courrier indésirable pour le courrier indésirable à niveau de confiance **élevé.**</span><span class="sxs-lookup"><span data-stu-id="18865-133">If you use a mail flow rule to set the SCL, the values 5 or 6 trigger the spam filtering action for **Spam**, and the values 7, 8, or 9 trigger the spam filtering action for **High confidence spam**.</span></span> <span data-ttu-id="18865-134">Pour plus d’informations, voir Utiliser des règles de flux de messagerie pour définir le niveau de confiance du courrier indésirable [(SCL) dans les messages.](use-mail-flow-rules-to-set-the-spam-confidence-level-scl-in-messages.md)</span><span class="sxs-lookup"><span data-stu-id="18865-134">For more information, see [Use mail flow rules to set the spam confidence level (SCL) in messages](use-mail-flow-rules-to-set-the-spam-confidence-level-scl-in-messages.md).</span></span>

<span data-ttu-id="18865-135">Comme pour le SCL, le niveau de réclamation en bloc (BCL) identifie les messages électroniques en masse (également appelés _messages gris)._</span><span class="sxs-lookup"><span data-stu-id="18865-135">Similar to the SCL, the bulk complaint level (BCL) identifies bad bulk email (also known as _gray mail_).</span></span> <span data-ttu-id="18865-136">Un niveau BCL supérieur indique qu’un courrier en nombre est susceptible de générer des plaintes (et par conséquent plus susceptible d’être du courrier indésirable).</span><span class="sxs-lookup"><span data-stu-id="18865-136">A higher BCL indicates a bulk mail message is more likely to generate complaints (and is therefore more likely to be spam).</span></span> <span data-ttu-id="18865-137">Vous configurez le seuil BCL dans les stratégies anti-courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="18865-137">You configure the BCL threshold in anti-spam policies.</span></span> <span data-ttu-id="18865-138">Pour plus d’informations, voir [Configure anti-spam policies in EOP](configure-your-spam-filter-policies.md), [Bulk complaint level (BCL) in EOP)](bulk-complaint-level-values.md)et [What’s the difference between junk email and bulk email?](what-s-the-difference-between-junk-email-and-bulk-email.md).</span><span class="sxs-lookup"><span data-stu-id="18865-138">For more information, see [Configure anti-spam policies in EOP](configure-your-spam-filter-policies.md), [Bulk complaint level (BCL) in EOP)](bulk-complaint-level-values.md), and [What's the difference between junk email and bulk email?](what-s-the-difference-between-junk-email-and-bulk-email.md).</span></span>

****

<span data-ttu-id="18865-139">![L’icône courte pour LinkedIn Learning ](../../media/eac8a413-9498-4220-8544-1e37d1aaea13.png) **New to Microsoft 365 ?**</span><span class="sxs-lookup"><span data-stu-id="18865-139">![The short icon for LinkedIn Learning](../../media/eac8a413-9498-4220-8544-1e37d1aaea13.png) **New to Microsoft 365?**</span></span> <span data-ttu-id="18865-140">Découvrez les cours vidéo gratuits pour les **administrateurs Microsoft 365** et les professionnels de l’informatique, présentés par LinkedIn Learning.</span><span class="sxs-lookup"><span data-stu-id="18865-140">Discover free video courses for **Microsoft 365 admins and IT pros**, brought to you by LinkedIn Learning.</span></span>
