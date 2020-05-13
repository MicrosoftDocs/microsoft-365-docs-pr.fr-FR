---
title: Envoi manuel de messages à Microsoft pour analyse
f1.keywords:
- NOCSH
ms.author: chrisda
author: chrisda
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: dad30e2f-93fe-4d21-9a36-21c87ced85c1
ms.collection:
- M365-security-compliance
description: Les administrateurs et les utilisateurs peuvent découvrir comment envoyer des messages électroniques (courrier marqué comme incorrect ou courrier incorrect) à Microsoft pour analyse.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: ed605d88f025996646c928200c20945df9c9871f
ms.sourcegitcommit: 93c0088d272cd45f1632a1dcaf04159f234abccd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2020
ms.locfileid: "44208608"
---
# <a name="manually-submit-messages-to-microsoft-for-analysis"></a><span data-ttu-id="b3697-103">Envoi manuel de messages à Microsoft pour analyse</span><span class="sxs-lookup"><span data-stu-id="b3697-103">Manually submit messages to Microsoft for analysis</span></span>

> [!NOTE]
> <span data-ttu-id="b3697-104">Si vous êtes administrateur d’une organisation avec des boîtes aux lettres Exchange Online, nous vous recommandons d’utiliser le portail d’envoi du centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="b3697-104">If you're an admin in an organization with Exchange Online mailboxes, we recommend that you use the Submissions portal in the Security & Compliance Center.</span></span> <span data-ttu-id="b3697-105">Pour plus d’informations, consultez la rubrique [utiliser la soumission de l’administrateur pour envoyer des courriers indésirables, des hameçons, des URL et des fichiers à Microsoft](admin-submission.md).</span><span class="sxs-lookup"><span data-stu-id="b3697-105">For more information, see [Use Admin Submission to submit suspected spam, phish, URLs, and files to Microsoft](admin-submission.md).</span></span>

<span data-ttu-id="b3697-106">Il peut être frustrant lorsque les utilisateurs de votre organisation reçoivent des courriers indésirables (spam) ou des messages de hameçonnage dans leur boîte de réception, ou s’ils ne reçoivent pas de message électronique légitime, car il est marqué comme courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="b3697-106">It can be frustrating when users in your organization receive junk messages (spam) or phishing messages in their Inbox, or if they don't receive a legitimate email message because it's marked as junk.</span></span> <span data-ttu-id="b3697-107">Nous ajustons constamment les filtres de courrier indésirable pour qu’ils soient plus précis.</span><span class="sxs-lookup"><span data-stu-id="b3697-107">We're constantly fine-tuning our spam filters to be more accurate.</span></span>

<span data-ttu-id="b3697-108">Vous et vos utilisateurs pouvez aider ce processus en soumettant des faux positifs (courrier électronique marqué comme incorrect), des faux négatifs (courrier incorrect) et des messages de hameçonnage à Microsoft pour analyse.</span><span class="sxs-lookup"><span data-stu-id="b3697-108">You and your users can help this process by submitting false positives (good email marked as bad), false negatives (bad mail allowed) and phishing messages to Microsoft for analysis.</span></span>

> [!NOTE]
> <span data-ttu-id="b3697-109">En raison du volume élevé des envois que nous recevons, il se peut que nous ne parvenons pas à répondre à toutes les demandes d’analyse.</span><span class="sxs-lookup"><span data-stu-id="b3697-109">Because of the high volume of submissions that we receive, we may not be able to answer all requests for analysis.</span></span>

## <a name="submit-false-negatives-to-microsoft"></a><span data-ttu-id="b3697-110">Soumettre des faux négatifs à Microsoft</span><span class="sxs-lookup"><span data-stu-id="b3697-110">Submit false negatives to Microsoft</span></span>

> [!TIP]
> <span data-ttu-id="b3697-111">Au lieu d’utiliser les procédures suivantes pour signaler les faux négatifs, les utilisateurs dans Outlook et Outlook sur le Web (anciennement appelé Outlook Web App) peuvent utiliser le complément de message de rapport pour Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="b3697-111">Instead of using the following procedures to report false negatives, users in Outlook and Outlook on the web (formerly known as Outlook Web App) can use the Report Message Add-in for Microsoft Outlook.</span></span> <span data-ttu-id="b3697-112">Pour plus d’informations sur l’installation et l’utilisation de cet outil, voir [activer le complément de message de rapport](enable-the-report-message-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="b3697-112">For information about how to install and use this tool, see [Enable the Report Message add-in](enable-the-report-message-add-in.md).</span></span>

<span data-ttu-id="b3697-113">Si vous recevez un message transmis par le biais du filtrage du courrier indésirable qui aurait dû être identifié comme courrier indésirable ou hameçonnage, vous pouvez envoyer le message aux équipes analyse du courrier indésirable et Microsoft Phishing Analysis, selon le cas.</span><span class="sxs-lookup"><span data-stu-id="b3697-113">If you receive a message that passed through spam filtering that should have been identified as spam or phishing, you can submit the message to the Microsoft Spam Analysis and Microsoft Phishing Analysis teams as appropriate.</span></span> <span data-ttu-id="b3697-114">Les analystes examineront le message et l’ajouteront aux filtres à l’échelle du service s’il répond aux critères de classification.</span><span class="sxs-lookup"><span data-stu-id="b3697-114">The analysts will review the message and add it to the service-wide filters if it meets the classification criteria.</span></span>

1. <span data-ttu-id="b3697-115">Créez un message électronique vide avec l’un des destinataires suivants :</span><span class="sxs-lookup"><span data-stu-id="b3697-115">Create a new, blank email message with the one of the following recipients:</span></span>

   - <span data-ttu-id="b3697-116">**Courrier indésirable**:`junk@office365.microsoft.com`</span><span class="sxs-lookup"><span data-stu-id="b3697-116">**Junk**: `junk@office365.microsoft.com`</span></span>

   - <span data-ttu-id="b3697-117">**Hameçonnage**:`phish@office365.microsoft.com`</span><span class="sxs-lookup"><span data-stu-id="b3697-117">**Phishing**: `phish@office365.microsoft.com`</span></span>

2. <span data-ttu-id="b3697-118">Faites glisser et déposez le message de courrier indésirable dans le nouveau message.</span><span class="sxs-lookup"><span data-stu-id="b3697-118">Drag and drop the junk or phishing message into the new message.</span></span> <span data-ttu-id="b3697-119">Cette opération permet d’enregistrer le message de courrier indésirable ou de hameçonnage en tant que pièce jointe dans le nouveau message.</span><span class="sxs-lookup"><span data-stu-id="b3697-119">This will save the junk or phishing message as an attachment in the new message.</span></span> <span data-ttu-id="b3697-120">Ne copiez pas et ne collez pas le contenu du message ou transférez le message (nous avons besoin du message d’origine pour pouvoir inspecter les en-têtes des messages).</span><span class="sxs-lookup"><span data-stu-id="b3697-120">Don't copy and paste the content of the message or forward the message (we need the original message so we can inspect the message headers).</span></span>

   > [!NOTE]
   > <ul><li><span data-ttu-id="b3697-121">Vous pouvez joindre plusieurs messages dans le nouveau message.</span><span class="sxs-lookup"><span data-stu-id="b3697-121">You can attach multiple messages in the new message.</span></span> <span data-ttu-id="b3697-122">Assurez-vous que tous les messages sont du même type : les messages de hameçonnage ou les messages électroniques de courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="b3697-122">Make sure that all the messages are the same type: either phishing scam messages or junk email messages.</span></span></li><li><span data-ttu-id="b3697-123">Laissez le corps du message vide.</span><span class="sxs-lookup"><span data-stu-id="b3697-123">Leave the body of the new message empty.</span></span></li><li><span data-ttu-id="b3697-124">Utilisez les formats. MSG (format Outlook par défaut) ou. eml (Outlook sur le format Web par défaut) pour les messages joints.</span><span class="sxs-lookup"><span data-stu-id="b3697-124">Use either .msg (default Outlook format) or .eml (default Outlook on the Web format) formats for the attached messages.</span></span></li></ul>

3. <span data-ttu-id="b3697-125">Lorsque vous avez terminé, cliquez sur **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="b3697-125">When you're finished, click **Send**.</span></span>

> [!TIP]
> <span data-ttu-id="b3697-126">Les administrateurs disposent de différentes manières de bloquer des messages spécifiques identifiés comme courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="b3697-126">Admins have several different ways to block specific messages that are being misidentified as spam.</span></span> <span data-ttu-id="b3697-127">Pour plus d’informations, consultez la rubrique [créer des listes d’expéditeurs bloqués dans EOP](create-block-sender-lists-in-office-365.md).</span><span class="sxs-lookup"><span data-stu-id="b3697-127">For details, see [Create blocked sender lists in EOP](create-block-sender-lists-in-office-365.md).</span></span>

## <a name="submit-false-positives-to-microsoft"></a><span data-ttu-id="b3697-128">Soumettre des faux positifs à Microsoft</span><span class="sxs-lookup"><span data-stu-id="b3697-128">Submit false positives to Microsoft</span></span>

> [!TIP]
> <span data-ttu-id="b3697-129">Au lieu d’utiliser les procédures suivantes pour signaler les faux positifs, les utilisateurs dans Outlook et Outlook sur le Web peuvent utiliser le complément de message de rapport pour Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="b3697-129">Instead of using the following procedures to report false positives, users in Outlook and Outlook on the web can use the Report Message Add-in for Microsoft Outlook.</span></span> <span data-ttu-id="b3697-130">Pour plus d’informations sur l’installation et l’utilisation de cet outil, voir [activer le complément de message de rapport](enable-the-report-message-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="b3697-130">For information about how to install and use this tool, see [Enable the Report Message add-in](enable-the-report-message-add-in.md).</span></span>

<span data-ttu-id="b3697-131">Si un message a été identifié de manière incorrecte comme courrier indésirable, vous pouvez envoyer le message à l’équipe d’analyse du courrier indésirable de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b3697-131">If a message was incorrectly identified as spam, you can submit the message to the Microsoft Spam Analysis Team.</span></span> <span data-ttu-id="b3697-132">Les analystes évaluent le message et (en fonction des résultats de l’analyse) les filtres à l’échelle du service peuvent être ajustés pour autoriser le message.</span><span class="sxs-lookup"><span data-stu-id="b3697-132">The analysts will evaluate the message, and (depending on the results of the analysis) the service-wide filters can be adjusted to allow the message through.</span></span>

1. <span data-ttu-id="b3697-133">Créez un message électronique vide avec `not_junk@office365.microsoft.com` comme destinataire :</span><span class="sxs-lookup"><span data-stu-id="b3697-133">Create a new, blank email message with `not_junk@office365.microsoft.com` as the recipient:</span></span>

2. <span data-ttu-id="b3697-134">Faites glisser et déposez le message qui a été identifié dans le nouveau message.</span><span class="sxs-lookup"><span data-stu-id="b3697-134">Drag and drop the misidentified message into the new message.</span></span> <span data-ttu-id="b3697-135">Cette opération permet d’enregistrer le message identifié de manière indéterminée en tant que pièce jointe dans le nouveau message.</span><span class="sxs-lookup"><span data-stu-id="b3697-135">This will save the misidentified message as an attachment in the new message.</span></span> <span data-ttu-id="b3697-136">Ne copiez pas et ne collez pas le contenu du message ou transférez le message (nous avons besoin du message d’origine pour pouvoir inspecter les en-têtes des messages).</span><span class="sxs-lookup"><span data-stu-id="b3697-136">Don't copy and paste the content of the message or forward the message (we need the original message so we can inspect the message headers).</span></span>

   > [!NOTE]
   > <ul><li><span data-ttu-id="b3697-137">Vous pouvez joindre plusieurs messages dans le nouveau message.</span><span class="sxs-lookup"><span data-stu-id="b3697-137">You can attach multiple messages in the new message.</span></span> <span data-ttu-id="b3697-138">Assurez-vous que tous les messages sont du même type : les messages de hameçonnage ou les messages électroniques de courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="b3697-138">Make sure that all the messages are the same type: either phishing messages or junk email messages.</span></span></li><li><span data-ttu-id="b3697-139">Laissez le corps du message vide.</span><span class="sxs-lookup"><span data-stu-id="b3697-139">Leave the body of the new message empty.</span></span></li><li><span data-ttu-id="b3697-140">Utilisez les formats. MSG (format Outlook par défaut) ou. eml (Outlook sur le format Web par défaut) pour les messages joints.</span><span class="sxs-lookup"><span data-stu-id="b3697-140">Use either .msg (default Outlook format) or .eml (default Outlook on the Web format) formats for the attached messages.</span></span></li></ul>

3. <span data-ttu-id="b3697-141">Lorsque vous avez terminé, cliquez sur **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="b3697-141">When you're finished, click **Send**.</span></span>

> [!TIP]
> <span data-ttu-id="b3697-142">Les administrateurs disposent de différentes manières d’autoriser des messages spécifiques à ignorer le filtrage du courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="b3697-142">Admins have several different ways to allow specific messages to skip spam filtering.</span></span> <span data-ttu-id="b3697-143">Pour plus d’informations, consultez la rubrique [créer des listes d’expéditeurs approuvés dans EOP](create-safe-sender-lists-in-office-365.md).</span><span class="sxs-lookup"><span data-stu-id="b3697-143">For details, see [Create safe sender lists in EOP](create-safe-sender-lists-in-office-365.md).</span></span>

## <a name="create-a-mail-flow-rule-to-receive-copies-of-messages-that-are-reported-to-microsoft"></a><span data-ttu-id="b3697-144">Créer une règle de flux de messagerie pour recevoir des copies des messages signalés à Microsoft</span><span class="sxs-lookup"><span data-stu-id="b3697-144">Create a mail flow rule to receive copies of messages that are reported to Microsoft</span></span>

<span data-ttu-id="b3697-145">Pour obtenir des instructions, consultez [la rubrique utiliser des règles de flux de messagerie pour voir ce que vos utilisateurs signalent à Microsoft](use-mail-flow-rules-to-see-what-your-users-are-reporting-to-microsoft.md).</span><span class="sxs-lookup"><span data-stu-id="b3697-145">For instructions, see [Use mail flow rules to see what your users are reporting to Microsoft](use-mail-flow-rules-to-see-what-your-users-are-reporting-to-microsoft.md).</span></span>
