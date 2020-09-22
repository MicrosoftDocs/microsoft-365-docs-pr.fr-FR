---
title: FAQ sur les messages mis en quarantaine
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: troubleshooting
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: c440b2ac-cafa-4be5-ba4c-14278a7990ae
ms.collection:
- M365-security-compliance
description: Les administrateurs peuvent consulter les réponses et les questions fréquemment posées sur les messages mis en quarantaine dans Exchange Online Protection (EOP).
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: d52aa8b6d86421bbc03e03191d0e0ccd074ce782
ms.sourcegitcommit: c083602dda3cdcb5b58cb8aa070d77019075f765
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/22/2020
ms.locfileid: "48202458"
---
# <a name="quarantined-messages-faq"></a><span data-ttu-id="bb733-103">FAQ sur les messages mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="bb733-103">Quarantined messages FAQ</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


<span data-ttu-id="bb733-104">Cette rubrique fournit des questions fréquemment posées et des réponses sur les messages électroniques mis en quarantaine pour les organisations Microsoft 365 avec des boîtes aux lettres dans Exchange Online ou des organisations Exchange Online (EOP) autonomes sans boîte aux lettres Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="bb733-104">This topic provides frequently asked questions and answers about quarantined email messages for Microsoft 365 organizations with mailboxes in Exchange Online, or standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes.</span></span>

<span data-ttu-id="bb733-105">Pour obtenir des questions et des réponses sur la protection contre le courrier indésirable, consultez la rubrique [protection contre le courrier indésirable](anti-spam-protection-faq.md).</span><span class="sxs-lookup"><span data-stu-id="bb733-105">For questions and answers about anti-spam protection, see [Anti-spam protection FAQ](anti-spam-protection-faq.md).</span></span>

<span data-ttu-id="bb733-106">Pour obtenir des questions et des réponses sur la protection contre les programmes malveillants, consultez la rubrique [anti-malware protection FAQ](anti-malware-protection-faq-eop.md).</span><span class="sxs-lookup"><span data-stu-id="bb733-106">For questions and answers about anti-malware protection, see [Anti-malware protection FAQ](anti-malware-protection-faq-eop.md).</span></span>

<span data-ttu-id="bb733-107">Pour obtenir des questions et des réponses sur la protection contre l’usurpation d’identité, consultez la rubrique [anti-spoofing protection FAQ](anti-spoofing-protection-faq.md).</span><span class="sxs-lookup"><span data-stu-id="bb733-107">For questions and answers about anti-spoofing protection, see [Anti-spoofing protection FAQ](anti-spoofing-protection-faq.md).</span></span>

## <a name="how-do-i-manage-messages-that-were-quarantined-for-malware"></a><span data-ttu-id="bb733-108">Comment puis-je gérer les messages qui ont été mis en quarantaine pour les programmes malveillants ?</span><span class="sxs-lookup"><span data-stu-id="bb733-108">How do I manage messages that were quarantined for malware?</span></span>

<span data-ttu-id="bb733-109">Seuls les administrateurs peuvent gérer les messages mis en quarantaine pour les programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="bb733-109">Only admins can manage messages that were quarantined for malware.</span></span> <span data-ttu-id="bb733-110">Pour plus d’informations, consultez la rubrique [gestion des messages et des fichiers mis en quarantaine en tant qu’administrateur](manage-quarantined-messages-and-files.md).</span><span class="sxs-lookup"><span data-stu-id="bb733-110">For more information, see [Manage quarantined messages and files as an admin](manage-quarantined-messages-and-files.md).</span></span>

## <a name="how-do-i-quarantine-spam"></a><span data-ttu-id="bb733-111">Comment mettre en quarantaine le courrier indésirable ?</span><span class="sxs-lookup"><span data-stu-id="bb733-111">How do I quarantine spam?</span></span>

<span data-ttu-id="bb733-112">Par défaut, les messages classés comme courriers indésirables ou en masse par filtrage du courrier indésirable sont remis à la boîte aux lettres de l’utilisateur et sont déplacés vers le dossier courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="bb733-112">By default, messages that are classified as spam or bulk email by spam filtering are delivered to the user's mailbox, and are moved to the Junk Email folder.</span></span> <span data-ttu-id="bb733-113">Toutefois, vous pouvez créer et configurer des stratégies de blocage du courrier indésirable pour mettre en quarantaine les messages électroniques en masse ou le courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="bb733-113">But you can create and configure anti-spam policies to quarantine spam or bulk email messages instead.</span></span> <span data-ttu-id="bb733-114">Si vous souhaitez en savoir plus, consultez l’article [Configurer les stratégies anti-courrier indésirable dans EOP](configure-your-spam-filter-policies.md).</span><span class="sxs-lookup"><span data-stu-id="bb733-114">For more information, see [Configure anti-spam policies in EOP](configure-your-spam-filter-policies.md).</span></span>

## <a name="how-do-i-give-users-access-to-the-quarantine"></a><span data-ttu-id="bb733-115">Comment accorder aux utilisateurs l’accès à la mise en quarantaine ?</span><span class="sxs-lookup"><span data-stu-id="bb733-115">How do I give users access to the quarantine?</span></span>

<span data-ttu-id="bb733-116">Un utilisateur doit disposer d’un compte valide pour accéder à ses propres messages en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="bb733-116">A user must have a valid account to access their own messages in quarantine.</span></span> <span data-ttu-id="bb733-117">La fonctionnalité EOP autonome nécessite que les utilisateurs soient représentés en tant qu’utilisateurs de messagerie dans EOP (création manuelle ou création via la synchronisation d’annuaires).</span><span class="sxs-lookup"><span data-stu-id="bb733-117">Standalone EOP requires that users are represented as mail users in EOP (manually created or created via directory synchronization).</span></span> <span data-ttu-id="bb733-118">Pour plus d’informations sur la gestion des utilisateurs dans les environnements autonomes EOP, consultez la rubrique [gestion des utilisateurs de messagerie dans EOP](manage-mail-users-in-eop.md).</span><span class="sxs-lookup"><span data-stu-id="bb733-118">For more information about managing users in standalone EOP environments, see [Manage mail users in EOP](manage-mail-users-in-eop.md).</span></span>

## <a name="what-messages-can-end-users-access-in-quarantine"></a><span data-ttu-id="bb733-119">Quels messages les utilisateurs finaux peuvent-ils accéder en quarantaine ?</span><span class="sxs-lookup"><span data-stu-id="bb733-119">What messages can end users access in quarantine?</span></span>

<span data-ttu-id="bb733-120">Les utilisateurs peuvent accéder aux messages de courrier indésirable, de courrier en nombre et (à partir d’avril 2020) lorsqu’ils sont destinataires.</span><span class="sxs-lookup"><span data-stu-id="bb733-120">Users can access spam, bulk email, and (as of April 2020) phishing messages where they are a recipient.</span></span> <span data-ttu-id="bb733-121">Les utilisateurs finaux ne peuvent pas accéder aux programmes malveillants mis en quarantaine, à la confiance élevée ou aux messages mis en quarantaine en raison de la **remise du message à l’action de mise en quarantaine hébergée dans les** règles de flux de messagerie (également appelées règles de transport).</span><span class="sxs-lookup"><span data-stu-id="bb733-121">End users can't access quarantined malware, high confidence phishing or messages that were quarantined because of the **Deliver the message to the hosted quarantine** action in mail flow rules (also known as transport rules).</span></span> <span data-ttu-id="bb733-122">Pour plus d’informations sur les utilisateurs qui accèdent aux messages mis en quarantaine, consultez [la rubrique Rechercher et débloquer les messages mis en quarantaine en tant qu’utilisateur](find-and-release-quarantined-messages-as-a-user.md).</span><span class="sxs-lookup"><span data-stu-id="bb733-122">For more information about users accessing quarantined messages, see [Find and release quarantined messages as a user](find-and-release-quarantined-messages-as-a-user.md).</span></span>

## <a name="how-long-are-messages-kept-in-the-quarantine"></a><span data-ttu-id="bb733-123">Combien de temps les messages sont-ils conservés en quarantaine ?</span><span class="sxs-lookup"><span data-stu-id="bb733-123">How long are messages kept in the quarantine?</span></span>

<span data-ttu-id="bb733-124">Vous configurez la durée pendant laquelle les courriers indésirables, les messages hameçons et les messages électroniques en masse sont conservés en quarantaine à l’aide de stratégies de blocage du courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="bb733-124">You configure how long spam, phishing, and bulk email messages are kept in the quarantine by using anti-spam policies.</span></span> <span data-ttu-id="bb733-125">La valeur par défaut est 30 jours, ce qui est également le maximum.</span><span class="sxs-lookup"><span data-stu-id="bb733-125">The default is 30 days, which is also the maximum.</span></span> <span data-ttu-id="bb733-126">Pour plus d’informations, consultez la rubrique [configurer des stratégies anti-courrier indésirable dans EOP](configure-your-spam-filter-policies.md)</span><span class="sxs-lookup"><span data-stu-id="bb733-126">For more information, see [Configure anti-spam policies in EOP](configure-your-spam-filter-policies.md)</span></span>

<span data-ttu-id="bb733-127">Pour les messages mis en quarantaine par l’action de règle de flux de messagerie, **remet le message à la quarantaine hébergée**, les messages sont conservés en quarantaine pendant 30 jours.</span><span class="sxs-lookup"><span data-stu-id="bb733-127">For messages that were quarantined by the mail flow rule action **Deliver the message to the hosted quarantine**, the messages are kept in quarantine for 30 days.</span></span> <span data-ttu-id="bb733-128">Vous ne pouvez pas configurer cette durée.</span><span class="sxs-lookup"><span data-stu-id="bb733-128">You can't configure this duration.</span></span>

<span data-ttu-id="bb733-129">Une fois la période expirée, les messages sont supprimés et ne sont pas récupérables.</span><span class="sxs-lookup"><span data-stu-id="bb733-129">After the time period expires, the messages are deleted and are not recoverable.</span></span>

## <a name="can-i-release-or-report-more-than-one-quarantined-message-at-a-time"></a><span data-ttu-id="bb733-130">Est-ce que je peux libérer ou signaler plusieurs messages mis en quarantaine à la fois ?</span><span class="sxs-lookup"><span data-stu-id="bb733-130">Can I release or report more than one quarantined message at a time?</span></span>

<span data-ttu-id="bb733-131">Dans le centre de sécurité & conformité, vous pouvez sélectionner et publier jusqu’à 100 messages à la fois.</span><span class="sxs-lookup"><span data-stu-id="bb733-131">In the Security & Compliance Center, you can select and release up to 100 messages at a time.</span></span>

<span data-ttu-id="bb733-132">Les administrateurs peuvent utiliser les cmdlets [Get-QuarantineMessage](https://docs.microsoft.com/powershell/module/exchange/get-quarantinemessage) et [Release-QuarantineMessage](https://docs.microsoft.com/powershell/module/exchange/release-quarantinemessage) dans Exchange Online PowerShell ou autonome EOP PowerShell pour rechercher et débloquer les messages mis en quarantaine en bloc, et pour signaler les faux positifs en bloc.</span><span class="sxs-lookup"><span data-stu-id="bb733-132">Admins can use the the [Get-QuarantineMessage](https://docs.microsoft.com/powershell/module/exchange/get-quarantinemessage) and [Release-QuarantineMessage](https://docs.microsoft.com/powershell/module/exchange/release-quarantinemessage) cmdlets in Exchange Online PowerShell or standalone EOP PowerShell to find and release quarantined messages in bulk, and to report false positives in bulk.</span></span>

## <a name="are-wildcards-supported-when-searching-for-quarantined-messages-can-i-search-for-quarantined-messages-for-a-specific-domain"></a><span data-ttu-id="bb733-133">Les caractères génériques sont-ils pris en charge lors de la recherche de messages mis en quarantaine ?</span><span class="sxs-lookup"><span data-stu-id="bb733-133">Are wildcards supported when searching for quarantined messages?</span></span> <span data-ttu-id="bb733-134">Puis-je rechercher des messages mis en quarantaine pour un domaine spécifique ?</span><span class="sxs-lookup"><span data-stu-id="bb733-134">Can I search for quarantined messages for a specific domain?</span></span>

<span data-ttu-id="bb733-135">Les caractères génériques ne sont pas pris en charge dans le centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="bb733-135">Wildcards aren't supported in the Security & Compliance Center.</span></span> <span data-ttu-id="bb733-136">Par exemple, lors de la recherche d’un expéditeur, vous devez spécifier l’adresse de messagerie complète.</span><span class="sxs-lookup"><span data-stu-id="bb733-136">For example, when searching for a sender, you need to specify the full email address.</span></span> <span data-ttu-id="bb733-137">Toutefois, vous pouvez utiliser des caractères génériques dans Exchange Online PowerShell ou autonome EOP PowerShell.</span><span class="sxs-lookup"><span data-stu-id="bb733-137">But, you can use wildcards in Exchange Online PowerShell or standalone EOP PowerShell.</span></span>

<span data-ttu-id="bb733-138">Par exemple, exécutez la commande suivante pour rechercher les messages de courrier indésirable mis en quarantaine à partir de tous les expéditeurs dans le domaine contoso.com :</span><span class="sxs-lookup"><span data-stu-id="bb733-138">For example, run the following command to find spam quarantined messages from all senders in the domain contoso.com:</span></span>

```powershell
$CQ = Get-QuarantineMessage -Type Spam | where {$_.SenderAddress -like "*@contoso.com"}
```

<span data-ttu-id="bb733-139">Ensuite, exécutez la commande suivante pour libérer ces messages à tous les destinataires d’origine :</span><span class="sxs-lookup"><span data-stu-id="bb733-139">Then, run the following command to release those messages to all original recipients:</span></span>

```powershell
$CQ | foreach {Release-QuarantineMessage -Identity $_.Identity -ReleaseToAll}
```

<span data-ttu-id="bb733-140">Une fois que vous avez publié un message, vous ne pouvez plus le libérer.</span><span class="sxs-lookup"><span data-stu-id="bb733-140">After you release a message, you can't release it again.</span></span>
