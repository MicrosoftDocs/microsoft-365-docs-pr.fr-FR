---
title: FAQ sur la mise en quarantaine
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: c440b2ac-cafa-4be5-ba4c-14278a7990ae
ms.collection:
- M365-security-compliance
description: Réponses aux questions fréquemment posées sur la mise en quarantaine dans Office 365.
ms.openlocfilehash: 58800d5645241c2115356bc9899ce53302d1e37e
ms.sourcegitcommit: fe4beef350ef9f39b1098755cff46fa2b8e7dc4d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2020
ms.locfileid: "42856904"
---
# <a name="quarantine-faq-in-office-365"></a><span data-ttu-id="d3d0c-103">FAQ sur la mise en quarantaine dans Office 365</span><span class="sxs-lookup"><span data-stu-id="d3d0c-103">Quarantine FAQ in Office 365</span></span>

<span data-ttu-id="d3d0c-104">Cette rubrique fournit des questions fréquemment posées et des réponses sur la mise en quarantaine pour les clients Office 365 avec des boîtes aux lettres dans Exchange Online ou des clients Exchange Online Protection (EOP) autonomes sans boîtes aux lettres Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="d3d0c-104">This topic provides frequently asked questions and answers about quarantine for Office 365 customers with mailboxes in Exchange Online or standalone Exchange Online Protection (EOP) customers without Exchange Online mailboxes.</span></span>

## <a name="q-how-do-i-manage-messages-that-were-quarantined-for-malware"></a><span data-ttu-id="d3d0c-105">Q : Comment puis-je gérer les messages mis en quarantaine pour les programmes malveillants ?</span><span class="sxs-lookup"><span data-stu-id="d3d0c-105">Q: How do I manage messages that were quarantined for malware?</span></span>

<span data-ttu-id="d3d0c-106">Seuls les administrateurs peuvent gérer les messages mis en quarantaine pour les programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="d3d0c-106">Only admins can manage messages that were quarantined for malware.</span></span> <span data-ttu-id="d3d0c-107">Pour plus d’informations, consultez la rubrique [gestion des messages et des fichiers mis en quarantaine en tant qu’administrateur dans Office 365](manage-quarantined-messages-and-files.md).</span><span class="sxs-lookup"><span data-stu-id="d3d0c-107">For more information, see [Manage quarantined messages and files as an admin in Office 365](manage-quarantined-messages-and-files.md).</span></span>

## <a name="q-how-do-i-quarantine-spam"></a><span data-ttu-id="d3d0c-108">Q : comment mettre en quarantaine le courrier indésirable ?</span><span class="sxs-lookup"><span data-stu-id="d3d0c-108">Q: How do I quarantine spam?</span></span>

<span data-ttu-id="d3d0c-109">A.</span><span class="sxs-lookup"><span data-stu-id="d3d0c-109">A.</span></span> <span data-ttu-id="d3d0c-110">Par défaut, les messages classés comme courriers indésirables ou en masse par filtrage du courrier indésirable sont remis à la boîte aux lettres de l’utilisateur et sont déplacés vers le dossier courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="d3d0c-110">By default, messages that are classified as spam or bulk email by spam filtering are delivered to the user's mailbox, and are moved to the Junk Email folder.</span></span> <span data-ttu-id="d3d0c-111">Toutefois, vous pouvez créer et configurer des stratégies de blocage du courrier indésirable pour mettre en quarantaine les messages électroniques en masse ou le courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="d3d0c-111">But you can create and configure anti-spam policies to quarantine spam or bulk email messages instead.</span></span> <span data-ttu-id="d3d0c-112">Pour plus d’informations, consultez la rubrique [configurer des stratégies de blocage du courrier indésirable dans Office 365](configure-your-spam-filter-policies.md).</span><span class="sxs-lookup"><span data-stu-id="d3d0c-112">For more information, see [Configure anti-spam policies in Office 365](configure-your-spam-filter-policies.md).</span></span>

## <a name="q-how-do-i-give-users-access-to-the-quarantine"></a><span data-ttu-id="d3d0c-113">Q : comment accorder aux utilisateurs l’accès à la mise en quarantaine ?</span><span class="sxs-lookup"><span data-stu-id="d3d0c-113">Q: How do I give users access to the quarantine?</span></span>

<span data-ttu-id="d3d0c-114">A.</span><span class="sxs-lookup"><span data-stu-id="d3d0c-114">A.</span></span> <span data-ttu-id="d3d0c-115">Un utilisateur doit disposer d’un compte valide pour accéder à ses propres messages en quarantaine.</span><span class="sxs-lookup"><span data-stu-id="d3d0c-115">A user must have a valid account to access their own messages in quarantine.</span></span> <span data-ttu-id="d3d0c-116">La fonctionnalité EOP autonome nécessite que les utilisateurs soient représentés en tant qu’utilisateurs de messagerie dans EOP (création manuelle ou création via la synchronisation d’annuaires).</span><span class="sxs-lookup"><span data-stu-id="d3d0c-116">Standalone EOP requires that users are represented as mail users in EOP (manually created or created via directory synchronization).</span></span> <span data-ttu-id="d3d0c-117">Pour plus d’informations sur la gestion des utilisateurs dans les environnements autonomes EOP, consultez la rubrique [gestion des utilisateurs de messagerie dans EOP](manage-mail-users-in-eop.md).</span><span class="sxs-lookup"><span data-stu-id="d3d0c-117">For more information about managing users in standalone EOP environments, see [Manage mail users in EOP](manage-mail-users-in-eop.md).</span></span>

## <a name="q-what-messages-can-end-users-access-in-quarantine"></a><span data-ttu-id="d3d0c-118">Q : quels messages les utilisateurs finaux peuvent-ils accéder en quarantaine ?</span><span class="sxs-lookup"><span data-stu-id="d3d0c-118">Q: What messages can end users access in quarantine?</span></span>

<span data-ttu-id="d3d0c-119">A.</span><span class="sxs-lookup"><span data-stu-id="d3d0c-119">A.</span></span> <span data-ttu-id="d3d0c-120">Les utilisateurs peuvent accéder aux messages de courrier indésirable, de courrier en nombre et (à partir d’avril, 2020) dans lesquels ils sont destinataires.</span><span class="sxs-lookup"><span data-stu-id="d3d0c-120">Users can access spam, bulk email, and (as of April, 2020) phishing messages where they are a recipient.</span></span> <span data-ttu-id="d3d0c-121">Les utilisateurs finaux ne peuvent pas accéder aux programmes malveillants mis en quarantaine, à la confiance élevée ou aux messages mis en quarantaine en raison de la **remise du message à l’action de mise en quarantaine hébergée dans les** règles de flux de messagerie (également appelées règles de transport).</span><span class="sxs-lookup"><span data-stu-id="d3d0c-121">End users can't access quarantined malware, high confidence phishing or messages that were quarantined because of the **Deliver the message to the hosted quarantine** action in mail flow rules (also known as transport rules).</span></span> <span data-ttu-id="d3d0c-122">Pour plus d’informations sur les utilisateurs qui accèdent aux messages mis en quarantaine, consultez [la rubrique Rechercher et débloquer les messages mis en quarantaine en tant qu’utilisateur dans Office 365](find-and-release-quarantined-messages-as-a-user.md).</span><span class="sxs-lookup"><span data-stu-id="d3d0c-122">For more information about users accessing quarantined messages, see [Find and release quarantined messages as a user in Office 365](find-and-release-quarantined-messages-as-a-user.md).</span></span>

## <a name="q-how-long-are-messages-kept-in-the-quarantine"></a><span data-ttu-id="d3d0c-123">Q : combien de temps les messages sont-ils conservés en quarantaine ?</span><span class="sxs-lookup"><span data-stu-id="d3d0c-123">Q: How long are messages kept in the quarantine?</span></span>

<span data-ttu-id="d3d0c-124">A.</span><span class="sxs-lookup"><span data-stu-id="d3d0c-124">A.</span></span> <span data-ttu-id="d3d0c-125">Vous configurez la durée pendant laquelle les courriers indésirables, les messages hameçons et les messages électroniques en masse sont conservés en quarantaine à l’aide de stratégies de blocage du courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="d3d0c-125">You configure how long spam, phishing, and bulk email messages are kept in the quarantine by using anti-spam policies.</span></span> <span data-ttu-id="d3d0c-126">La valeur par défaut est 30 jours, ce qui est également le maximum.</span><span class="sxs-lookup"><span data-stu-id="d3d0c-126">The default is 30 days, which is also the maximum.</span></span> <span data-ttu-id="d3d0c-127">Pour plus d’informations, consultez la rubrique [Configuration des stratégies de blocage du courrier indésirable dans Office 365](configure-your-spam-filter-policies.md)</span><span class="sxs-lookup"><span data-stu-id="d3d0c-127">For more information, see [Configure anti-spam policies in Office 365](configure-your-spam-filter-policies.md)</span></span>

<span data-ttu-id="d3d0c-128">Pour les messages mis en quarantaine par l’action de règle de flux de messagerie, **remet le message à la quarantaine hébergée**, les messages sont conservés en quarantaine pendant 30 jours.</span><span class="sxs-lookup"><span data-stu-id="d3d0c-128">For messages that were quarantined by the mail flow rule action **Deliver the message to the hosted quarantine**, the messages are kept in quarantine for 30 days.</span></span> <span data-ttu-id="d3d0c-129">Vous ne pouvez pas configurer cette durée.</span><span class="sxs-lookup"><span data-stu-id="d3d0c-129">You can't configure this duration.</span></span>

<span data-ttu-id="d3d0c-130">Une fois la période expirée, les messages sont supprimés et ne sont pas récupérables.</span><span class="sxs-lookup"><span data-stu-id="d3d0c-130">After the time period expires, the messages are deleted and are not recoverable.</span></span>

## <a name="q-can-i-release-or-report-more-than-one-quarantined-message-at-a-time"></a><span data-ttu-id="d3d0c-131">Q : puis-je publier ou signaler plusieurs messages en quarantaine à la fois ?</span><span class="sxs-lookup"><span data-stu-id="d3d0c-131">Q: Can I release or report more than one quarantined message at a time?</span></span>

<span data-ttu-id="d3d0c-132">A.</span><span class="sxs-lookup"><span data-stu-id="d3d0c-132">A.</span></span> <span data-ttu-id="d3d0c-133">Dans le centre de sécurité & conformité, vous pouvez sélectionner et publier jusqu’à 100 messages à la fois.</span><span class="sxs-lookup"><span data-stu-id="d3d0c-133">In the Security & Compliance Center, you can select and release up to 100 messages at a time.</span></span>

<span data-ttu-id="d3d0c-134">Les administrateurs peuvent utiliser les cmdlets [Get-QuarantineMessage](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/get-quarantinemessage) et [Release-QuarantineMessage](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/release-quarantinemessage) dans Exchange Online PowerShell ou un environnement autonome Exchange Online Protection PowerShell pour rechercher et débloquer des messages mis en quarantaine en bloc, et pour signaler des faux positifs en bloc.</span><span class="sxs-lookup"><span data-stu-id="d3d0c-134">Admins can use the the [Get-QuarantineMessage](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/get-quarantinemessage) and [Release-QuarantineMessage](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/release-quarantinemessage) cmdlets in Exchange Online PowerShell or standalone Exchange Online Protection PowerShell to find and release quarantined messages in bulk, and to report false positives in bulk.</span></span>

## <a name="q-are-wildcards-supported-when-searching-for-quarantined-messages-can-i-search-for-quarantined-messages-for-a-specific-domain"></a><span data-ttu-id="d3d0c-135">Q : est-ce que les caractères génériques sont pris en charge lors de la recherche de messages mis en quarantaine ?</span><span class="sxs-lookup"><span data-stu-id="d3d0c-135">Q: Are wildcards supported when searching for quarantined messages?</span></span> <span data-ttu-id="d3d0c-136">Puis-je rechercher des messages mis en quarantaine pour un domaine spécifique ?</span><span class="sxs-lookup"><span data-stu-id="d3d0c-136">Can I search for quarantined messages for a specific domain?</span></span>

<span data-ttu-id="d3d0c-137">A.</span><span class="sxs-lookup"><span data-stu-id="d3d0c-137">A.</span></span> <span data-ttu-id="d3d0c-138">Les caractères génériques ne sont pas pris en charge dans le centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="d3d0c-138">Wildcards aren't supported in the Security & Compliance Center.</span></span> <span data-ttu-id="d3d0c-139">Par exemple, lors de la recherche d’un expéditeur, vous devez spécifier l’adresse de messagerie complète.</span><span class="sxs-lookup"><span data-stu-id="d3d0c-139">For example, when searching for a sender, you need to specify the full email address.</span></span> <span data-ttu-id="d3d0c-140">Toutefois, vous pouvez utiliser des caractères génériques dans Exchange Online PowerShell ou Exchange Online Protection PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d3d0c-140">But, you can use wildcards in Exchange Online PowerShell or Exchange Online Protection PowerShell.</span></span>

<span data-ttu-id="d3d0c-141">Par exemple, exécutez la commande suivante pour rechercher les messages de courrier indésirable mis en quarantaine à partir de tous les expéditeurs dans le domaine contoso.com :</span><span class="sxs-lookup"><span data-stu-id="d3d0c-141">For example, run the following command to find spam quarantined messages from all senders in the domain contoso.com:</span></span>

```powershell
$CQ = Get-QuarantineMessage -Type Spam | where {$_.SenderAddress -like "*@contoso.com"}
```

<span data-ttu-id="d3d0c-142">Ensuite, exécutez la commande suivante pour libérer ces messages à tous les destinataires d’origine :</span><span class="sxs-lookup"><span data-stu-id="d3d0c-142">Then, run the following command to release those messages to all original recipients:</span></span>

```powershell
$CQ | foreach {Release-QuarantineMessage -Identity $CQ.Identity -ReleaseToAll}
```

<span data-ttu-id="d3d0c-143">Une fois que vous avez publié un message, vous ne pouvez plus le libérer.</span><span class="sxs-lookup"><span data-stu-id="d3d0c-143">After you release a message, you can't release it again.</span></span>
