---
title: Envoyer manuellement des messages à Microsoft pour analyse
f1.keywords:
- NOCSH
ms.author: siosulli
author: siosulli
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: how-to
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: dad30e2f-93fe-4d21-9a36-21c87ced85c1
ms.collection:
- M365-security-compliance
description: Les administrateurs et les utilisateurs finaux peuvent apprendre à envoyer des messages électroniques (messages électroniques de qualité marqués comme courriers indésirables ou indésirables autorisés) à Microsoft pour analyse.
ms.custom: seo-marvel-apr2020
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 98964d17c41222fa708bdf0059c0e67151582ef1
ms.sourcegitcommit: 786f90a163d34c02b8451d09aa1efb1e1d5f543c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/18/2021
ms.locfileid: "50290368"
---
# <a name="manually-submit-messages-to-microsoft-for-analysis"></a><span data-ttu-id="cd23c-103">Envoyer manuellement des messages à Microsoft pour analyse</span><span class="sxs-lookup"><span data-stu-id="cd23c-103">Manually submit messages to Microsoft for analysis</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="cd23c-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="cd23c-104">**Applies to**</span></span>
- [<span data-ttu-id="cd23c-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="cd23c-105">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="cd23c-106">Microsoft Defender pour Office 365 Plan 1 et Plan 2</span><span class="sxs-lookup"><span data-stu-id="cd23c-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](office-365-atp.md)
- [<span data-ttu-id="cd23c-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="cd23c-107">Microsoft 365 Defender</span></span>](../mtp/microsoft-threat-protection.md)

> [!NOTE]
> <span data-ttu-id="cd23c-108">Si vous êtes un administrateur d’une organisation ayant des boîtes aux lettres Exchange Online, nous vous recommandons d’utiliser le portail Soumissions dans le Centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="cd23c-108">If you're an admin in an organization with Exchange Online mailboxes, we recommend that you use the Submissions portal in the Security & Compliance Center.</span></span> <span data-ttu-id="cd23c-109">Pour plus d’informations, voir Utiliser la soumission d’administrateur pour soumettre des messages suspects de courrier indésirable, d’hameçonnage, d’URL et [de fichiers à Microsoft.](admin-submission.md)</span><span class="sxs-lookup"><span data-stu-id="cd23c-109">For more information, see [Use Admin Submission to submit suspected spam, phish, URLs, and files to Microsoft](admin-submission.md).</span></span>

<span data-ttu-id="cd23c-110">Cela peut être frustrant lorsque les utilisateurs de votre organisation reçoivent des messages indésirables (courrier indésirable) ou de hameçonnage dans leur boîte de réception, ou s’ils ne reçoivent pas de message électronique légitime parce qu’il est marqué comme courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="cd23c-110">It can be frustrating when users in your organization receive junk messages (spam) or phishing messages in their Inbox, or if they don't receive a legitimate email message because it's marked as junk.</span></span> <span data-ttu-id="cd23c-111">Nous affinons constamment nos filtres de courrier indésirable pour être plus précis.</span><span class="sxs-lookup"><span data-stu-id="cd23c-111">We're constantly fine-tuning our spam filters to be more accurate.</span></span>

<span data-ttu-id="cd23c-112">Vous et vos utilisateurs pouvez vous aider à ce processus en envoyant des faux positifs (e-mail de qualité marqué comme faux), des faux négatifs (courrier indésirable autorisé) et des messages de hameçonnage à Microsoft pour analyse.</span><span class="sxs-lookup"><span data-stu-id="cd23c-112">You and your users can help this process by submitting false positives (good email marked as bad), false negatives (bad mail allowed) and phishing messages to Microsoft for analysis.</span></span>

> [!NOTE]
> <span data-ttu-id="cd23c-113">En raison du volume élevé de soumissions que nous recevons, nous ne pouvons peut-être pas répondre à toutes les demandes d’analyse.</span><span class="sxs-lookup"><span data-stu-id="cd23c-113">Because of the high volume of submissions that we receive, we may not be able to answer all requests for analysis.</span></span>

## <a name="submit-false-negatives-to-microsoft"></a><span data-ttu-id="cd23c-114">Envoyer des faux négatifs à Microsoft</span><span class="sxs-lookup"><span data-stu-id="cd23c-114">Submit false negatives to Microsoft</span></span>

> [!TIP]
> <span data-ttu-id="cd23c-115">Au lieu d’utiliser les procédures suivantes pour signaler les faux négatifs, les utilisateurs d’Outlook et d’Outlook sur le web (anciennement Outlook Web App) peuvent utiliser le add-in Report Message ou le add-in Report Phishing.</span><span class="sxs-lookup"><span data-stu-id="cd23c-115">Instead of using the following procedures to report false negatives, users in Outlook and Outlook on the web (formerly known as Outlook Web App) can use the Report Message add-in or the Report Phishing add-in.</span></span> <span data-ttu-id="cd23c-116">Pour plus d’informations sur l’installation et l’utilisation de ces outils, voir [Enable the Report Message add-in](enable-the-report-message-add-in.md) and Enable the Report [Phishing add-in](enable-the-report-phish-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="cd23c-116">For information about how to install and use these tools, see [Enable the Report Message add-in](enable-the-report-message-add-in.md) and [Enable the Report Phishing add-in](enable-the-report-phish-add-in.md).</span></span>

<span data-ttu-id="cd23c-117">Si vous recevez un message qui a été transmis par le biais du filtrage du courrier indésirable et qui doit avoir été identifié comme courrier indésirable ou hameçonnage, vous pouvez envoyer le message aux équipes d’analyse du courrier indésirable de Microsoft et d’analyse du hameçonnage Microsoft, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="cd23c-117">If you receive a message that passed through spam filtering that should have been identified as spam or phishing, you can submit the message to the Microsoft Spam Analysis and Microsoft Phishing Analysis teams as appropriate.</span></span> <span data-ttu-id="cd23c-118">Les analystes examinent le message et l’ajoutent aux filtres à l’échelle du service s’il répond aux critères de classification.</span><span class="sxs-lookup"><span data-stu-id="cd23c-118">The analysts will review the message and add it to the service-wide filters if it meets the classification criteria.</span></span>

1. <span data-ttu-id="cd23c-119">Créez un message électronique vide avec l’un des destinataires suivants :</span><span class="sxs-lookup"><span data-stu-id="cd23c-119">Create a new, blank email message with the one of the following recipients:</span></span>

   - <span data-ttu-id="cd23c-120">**Courrier** indésirable : `junk@office365.microsoft.com`</span><span class="sxs-lookup"><span data-stu-id="cd23c-120">**Junk**: `junk@office365.microsoft.com`</span></span>

   - <span data-ttu-id="cd23c-121">**Hameçonnage**: `phish@office365.microsoft.com`</span><span class="sxs-lookup"><span data-stu-id="cd23c-121">**Phishing**: `phish@office365.microsoft.com`</span></span>

2. <span data-ttu-id="cd23c-122">Faites glisser et déposez le message de courrier indésirable ou de hameçonnage dans le nouveau message.</span><span class="sxs-lookup"><span data-stu-id="cd23c-122">Drag and drop the junk or phishing message into the new message.</span></span> <span data-ttu-id="cd23c-123">Cela permet d’enregistrer le message de courrier indésirable ou de hameçonnage en tant que pièce jointe dans le nouveau message.</span><span class="sxs-lookup"><span data-stu-id="cd23c-123">This will save the junk or phishing message as an attachment in the new message.</span></span> <span data-ttu-id="cd23c-124">Ne copiez et collez pas le contenu du message ou ne le faites pas passer (nous avons besoin du message d’origine pour pouvoir inspecter les en-têtes du message).</span><span class="sxs-lookup"><span data-stu-id="cd23c-124">Don't copy and paste the content of the message or forward the message (we need the original message so we can inspect the message headers).</span></span>

   > [!NOTE]
   >
   > - <span data-ttu-id="cd23c-125">Vous pouvez joindre plusieurs messages dans le nouveau message.</span><span class="sxs-lookup"><span data-stu-id="cd23c-125">You can attach multiple messages in the new message.</span></span> <span data-ttu-id="cd23c-126">Assurez-vous que tous les messages sont du même type : messages de hameçonnage ou courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="cd23c-126">Make sure that all the messages are the same type: either phishing messages or junk email messages.</span></span>
   >
   > - <span data-ttu-id="cd23c-127">Laissez le corps du message vide.</span><span class="sxs-lookup"><span data-stu-id="cd23c-127">Leave the body of the new message empty.</span></span>
   >
   > - <span data-ttu-id="cd23c-128">Utilisez les formats .msg (format Outlook par défaut) ou .eml (format Outlook sur le Web par défaut) pour les messages joints.</span><span class="sxs-lookup"><span data-stu-id="cd23c-128">Use either .msg (default Outlook format) or .eml (default Outlook on the Web format) formats for the attached messages.</span></span>

3. <span data-ttu-id="cd23c-129">Lorsque vous avez terminé, cliquez sur **Envoyer.**</span><span class="sxs-lookup"><span data-stu-id="cd23c-129">When you're finished, click **Send**.</span></span>

> [!TIP]
> <span data-ttu-id="cd23c-130">Les administrateurs ont plusieurs façons de bloquer des messages spécifiques qui sont mal identifiés comme courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="cd23c-130">Admins have several different ways to block specific messages that are being misidentified as spam.</span></span> <span data-ttu-id="cd23c-131">Pour plus d’informations, voir [Créer des listes d’expéditeurs bloqués dans EOP.](create-block-sender-lists-in-office-365.md)</span><span class="sxs-lookup"><span data-stu-id="cd23c-131">For details, see [Create blocked sender lists in EOP](create-block-sender-lists-in-office-365.md).</span></span>

## <a name="submit-false-positives-to-microsoft"></a><span data-ttu-id="cd23c-132">Envoyer des faux positifs à Microsoft</span><span class="sxs-lookup"><span data-stu-id="cd23c-132">Submit false positives to Microsoft</span></span>

> [!TIP]
> <span data-ttu-id="cd23c-133">Au lieu d’utiliser les procédures suivantes pour signaler les faux positifs, les utilisateurs d’Outlook et d’Outlook sur le web (anciennement Outlook Web App) peuvent utiliser le add-in Report Message ou le add-in Report Phishing.</span><span class="sxs-lookup"><span data-stu-id="cd23c-133">Instead of using the following procedures to report false positives, users in Outlook and Outlook on the web (formerly known as Outlook Web App) can use the Report Message add-in or the Report Phishing add-in.</span></span> <span data-ttu-id="cd23c-134">Pour plus d’informations sur l’installation et l’utilisation de ces outils, voir [Enable the Report Message add-in](enable-the-report-message-add-in.md) and Enable the Report [Phishing add-in](enable-the-report-phish-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="cd23c-134">For information about how to install and use these tools, see [Enable the Report Message add-in](enable-the-report-message-add-in.md) and [Enable the Report Phishing add-in](enable-the-report-phish-add-in.md).</span></span>


<span data-ttu-id="cd23c-135">Si un message a été identifié à tort comme courrier indésirable, vous pouvez le soumettre à l’équipe d’analyse du courrier indésirable de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="cd23c-135">If a message was incorrectly identified as spam, you can submit the message to the Microsoft Spam Analysis Team.</span></span> <span data-ttu-id="cd23c-136">Les analystes évaluent le message et (en fonction des résultats de l’analyse) les filtres à l’échelle du service peuvent être ajustés pour autoriser le message.</span><span class="sxs-lookup"><span data-stu-id="cd23c-136">The analysts will evaluate the message, and (depending on the results of the analysis) the service-wide filters can be adjusted to allow the message through.</span></span>

1. <span data-ttu-id="cd23c-137">Créez un message électronique vide avec `not_junk@office365.microsoft.com` comme destinataire :</span><span class="sxs-lookup"><span data-stu-id="cd23c-137">Create a new, blank email message with `not_junk@office365.microsoft.com` as the recipient:</span></span>

2. <span data-ttu-id="cd23c-138">Faites glisser et déposez le message non identifié dans le nouveau message.</span><span class="sxs-lookup"><span data-stu-id="cd23c-138">Drag and drop the misidentified message into the new message.</span></span> <span data-ttu-id="cd23c-139">Cela permet d’enregistrer le message non identifié en tant que pièce jointe dans le nouveau message.</span><span class="sxs-lookup"><span data-stu-id="cd23c-139">This will save the misidentified message as an attachment in the new message.</span></span> <span data-ttu-id="cd23c-140">Ne copiez pas et ne collez pas le contenu du message ou ne le faites pas passer (nous avons besoin du message d’origine pour pouvoir inspecter les en-têtes du message).</span><span class="sxs-lookup"><span data-stu-id="cd23c-140">Don't copy and paste the content of the message or forward the message (we need the original message so we can inspect the message headers).</span></span>

   > [!NOTE]
   >
   > - <span data-ttu-id="cd23c-141">Vous pouvez joindre plusieurs messages dans le nouveau message.</span><span class="sxs-lookup"><span data-stu-id="cd23c-141">You can attach multiple messages in the new message.</span></span> <span data-ttu-id="cd23c-142">Assurez-vous que tous les messages sont du même type : messages de hameçonnage ou courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="cd23c-142">Make sure that all the messages are the same type: either phishing messages or junk email messages.</span></span>
   >
   > - <span data-ttu-id="cd23c-143">Laissez le corps du message vide.</span><span class="sxs-lookup"><span data-stu-id="cd23c-143">Leave the body of the new message empty.</span></span>
   >
   > - <span data-ttu-id="cd23c-144">Utilisez les formats .msg (format Outlook par défaut) ou .eml (format Outlook sur le Web par défaut) pour les messages joints.</span><span class="sxs-lookup"><span data-stu-id="cd23c-144">Use either .msg (default Outlook format) or .eml (default Outlook on the Web format) formats for the attached messages.</span></span>

3. <span data-ttu-id="cd23c-145">Lorsque vous avez terminé, cliquez sur **Envoyer.**</span><span class="sxs-lookup"><span data-stu-id="cd23c-145">When you're finished, click **Send**.</span></span>

> [!TIP]
> <span data-ttu-id="cd23c-146">Les administrateurs ont plusieurs façons d’autoriser des messages spécifiques à ignorer le filtrage du courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="cd23c-146">Admins have several different ways to allow specific messages to skip spam filtering.</span></span> <span data-ttu-id="cd23c-147">Pour plus d’informations, voir [Créer des listes d’expéditeurs sûrs dans EOP.](create-safe-sender-lists-in-office-365.md)</span><span class="sxs-lookup"><span data-stu-id="cd23c-147">For details, see [Create safe sender lists in EOP](create-safe-sender-lists-in-office-365.md).</span></span>

## <a name="where-is-the-data-from-submissions-to-microsoft-stored"></a><span data-ttu-id="cd23c-148">Où sont stockées les données des soumissions à Microsoft ?</span><span class="sxs-lookup"><span data-stu-id="cd23c-148">Where is the data from submissions to Microsoft stored?</span></span>

<span data-ttu-id="cd23c-149">Les données résident dans la limite de conformité d’Office 365 dans les centres de données d’Amérique du Nord.</span><span class="sxs-lookup"><span data-stu-id="cd23c-149">The data resides in the Office 365 compliance boundary in North American data centers.</span></span> <span data-ttu-id="cd23c-150">Les données sont examinées par les analystes de l’équipe d’ingénierie afin d’améliorer l’efficacité des filtres.</span><span class="sxs-lookup"><span data-stu-id="cd23c-150">The data is reviewed by analysts on the engineering team to help improve the effectiveness of the filters.</span></span>

## <a name="create-a-mail-flow-rule-to-receive-copies-of-messages-that-are-reported-to-microsoft"></a><span data-ttu-id="cd23c-151">Créer une règle de flux de messagerie pour recevoir des copies des messages signalés à Microsoft</span><span class="sxs-lookup"><span data-stu-id="cd23c-151">Create a mail flow rule to receive copies of messages that are reported to Microsoft</span></span>

<span data-ttu-id="cd23c-152">Pour obtenir des instructions, voir Utiliser des règles de flux de messagerie pour voir ce [que vos utilisateurs rapportent à Microsoft.](use-mail-flow-rules-to-see-what-your-users-are-reporting-to-microsoft.md)</span><span class="sxs-lookup"><span data-stu-id="cd23c-152">For instructions, see [Use mail flow rules to see what your users are reporting to Microsoft](use-mail-flow-rules-to-see-what-your-users-are-reporting-to-microsoft.md).</span></span>
