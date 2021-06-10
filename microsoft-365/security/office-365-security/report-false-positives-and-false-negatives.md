---
title: Signaler les faux positifs et les faux négatifs dans Outlook
f1.keywords:
- NOCSH
ms.author: dansimp
author: dansimp
manager: dansimp
audience: Admin
ms.topic: how-to
localization_priority: Normal
ms.collection:
- M365-security-compliance
description: Découvrez comment signaler les faux positifs et les faux négatifs dans Outlook à l’aide de la fonctionnalité Signaler un message.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 84a5b697f8a4b46cf79c542485bfafb396328f5c
ms.sourcegitcommit: b09aee96a1e2266b33ba81dfe497f24c5300bb56
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/06/2021
ms.locfileid: "52789242"
---
# <a name="report-false-positives-and-false-negatives-in-outlook"></a><span data-ttu-id="b7eb5-103">Signaler les faux positifs et les faux négatifs dans Outlook</span><span class="sxs-lookup"><span data-stu-id="b7eb5-103">Report false positives and false negatives in Outlook</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="b7eb5-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="b7eb5-104">**Applies to**</span></span>
- [<span data-ttu-id="b7eb5-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="b7eb5-105">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="b7eb5-106">Microsoft Defender pour Office 365 : offre 1 et offre 2</span><span class="sxs-lookup"><span data-stu-id="b7eb5-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](defender-for-office-365.md)
- [<span data-ttu-id="b7eb5-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="b7eb5-107">Microsoft 365 Defender</span></span>](../defender/microsoft-365-defender.md)

> [!NOTE]
> <span data-ttu-id="b7eb5-108">Si vous êtes un administrateur d’une organisation Microsoft 365 avec des boîtes aux lettres Exchange Online, nous vous recommandons d’utiliser le portail Soumissions dans le Centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="b7eb5-108">If you're an admin in a Microsoft 365 organization with Exchange Online mailboxes, we recommend that you use the Submissions portal in the Security & Compliance Center.</span></span> <span data-ttu-id="b7eb5-109">Pour plus d’informations, voir Utiliser la soumission d’administrateur pour soumettre des messages suspects de courrier indésirable, d’hameçonnage, d’URL et [de fichiers à Microsoft.](admin-submission.md)</span><span class="sxs-lookup"><span data-stu-id="b7eb5-109">For more information, see [Use Admin Submission to submit suspected spam, phish, URLs, and files to Microsoft](admin-submission.md).</span></span>

<span data-ttu-id="b7eb5-110">Dans Microsoft 365 organisations avec des boîtes aux lettres dans Exchange Online ou locales utilisant l’authentification moderne hybride, vous pouvez envoyer des faux positifs (messages électroniques de qualité bloqués ou envoyés à un dossier de courrier indésirable) et des faux négatifs (courrier indésirable ou hameçonnage qui a été remis à la boîte de réception) à Exchange Online Protection (EOP).</span><span class="sxs-lookup"><span data-stu-id="b7eb5-110">In Microsoft 365 organizations with mailboxes in Exchange Online or on-premises mailboxes using hybrid modern authentication, you can submit false positives (good email that was blocked or sent to junk folder) and false negatives (unwanted email or phish that was delivered to the inbox) to Exchange Online Protection (EOP).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="b7eb5-111">Ce qu'il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="b7eb5-111">What do you need to know before you begin?</span></span>

- <span data-ttu-id="b7eb5-112">Pour une meilleure expérience de soumission d’utilisateurs, utilisez le add-in Report Message ou report Phishing.</span><span class="sxs-lookup"><span data-stu-id="b7eb5-112">For the best user submission experience, use the Report Message add-in or the Report Phishing add-in.</span></span>

  > [!IMPORTANT]
  > <span data-ttu-id="b7eb5-113">L’expérience intégrée pour signaler le courrier indésirable ou le hameçonnage dans Outlook ne peut pas utiliser la stratégie [de soumission d’utilisateur.](./user-submission.md)</span><span class="sxs-lookup"><span data-stu-id="b7eb5-113">The built-in experience for reporting junk or phishing in Outlook can't use the [user submission policy](./user-submission.md).</span></span> <span data-ttu-id="b7eb5-114">Nous vous recommandons plutôt d’utiliser le add-in Report Message ou report Phishing.</span><span class="sxs-lookup"><span data-stu-id="b7eb5-114">We recommend using the Report Message add-in or the Report Phishing add-in instead.</span></span>

- <span data-ttu-id="b7eb5-115">Le add-in Report Message et le add-in Report Phishing fonctionnent pour Outlook sur toutes les plateformes (Outlook sur le web, iOS, Android et Bureau).</span><span class="sxs-lookup"><span data-stu-id="b7eb5-115">The the Report Message add-in and the Report Phishing add-in work for Outlook in all platforms (Outlook on the web, iOS, Android, and Desktop).</span></span>

- <span data-ttu-id="b7eb5-116">Si vous êtes un administrateur d’une organisation Exchange Online boîtes aux lettres, utilisez le portail Soumissions dans le Centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="b7eb5-116">If you're an admin in an organization with Exchange Online mailboxes, use the Submissions portal in the Security & Compliance Center.</span></span> <span data-ttu-id="b7eb5-117">Pour plus d’informations, voir Utiliser la soumission d’administrateur pour soumettre des messages suspects de courrier indésirable, d’hameçonnage, d’URL et [de fichiers à Microsoft.](admin-submission.md)</span><span class="sxs-lookup"><span data-stu-id="b7eb5-117">For more information, see [Use Admin Submission to submit suspected spam, phish, URLs, and files to Microsoft](admin-submission.md).</span></span>

- <span data-ttu-id="b7eb5-118">Vous pouvez configurer pour envoyer des messages directement à Microsoft, une boîte aux lettres que vous spécifiez, ou les deux.</span><span class="sxs-lookup"><span data-stu-id="b7eb5-118">You can configure to send messages directly to Microsoft, a mailbox you specify, or both.</span></span> <span data-ttu-id="b7eb5-119">Pour plus d’informations, voir [Stratégies d’envoi des utilisateurs.](user-submission.md)</span><span class="sxs-lookup"><span data-stu-id="b7eb5-119">For more information, see [User submissions policies](user-submission.md).</span></span>

- <span data-ttu-id="b7eb5-120">Pour plus d’informations sur la façon d’obtenir et d’activer le message de rapport ou les add-ins De hameçonnage de rapport, voir Activer le [message](enable-the-report-message-add-in.md)de rapport ou les rapports de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="b7eb5-120">For more information on how to get and enable the Report Message or the Report Phishing add-ins, see [Enable the Report Message or the Report Phishing add-ins](enable-the-report-message-add-in.md).</span></span>

- <span data-ttu-id="b7eb5-121">Pour plus d’informations sur la notification des messages à Microsoft, voir [Signaler des messages et des fichiers à Microsoft.](report-junk-email-messages-to-microsoft.md)</span><span class="sxs-lookup"><span data-stu-id="b7eb5-121">For more information about reporting messages to Microsoft, see [Report messages and files to Microsoft](report-junk-email-messages-to-microsoft.md).</span></span>

## <a name="use-the-report-message-feature"></a><span data-ttu-id="b7eb5-122">Utiliser la fonctionnalité Message de rapport</span><span class="sxs-lookup"><span data-stu-id="b7eb5-122">Use the Report Message feature</span></span>

### <a name="report-junk-and-phishing-messages"></a><span data-ttu-id="b7eb5-123">Signaler les messages de courrier indésirable et de hameçonnage</span><span class="sxs-lookup"><span data-stu-id="b7eb5-123">Report junk and phishing messages</span></span>

<span data-ttu-id="b7eb5-124">Pour les messages dans la boîte de réception ou tout autre dossier de courrier électronique à l’exception du courrier indésirable, utilisez la méthode suivante pour signaler le courrier indésirable et les messages de hameçonnage :</span><span class="sxs-lookup"><span data-stu-id="b7eb5-124">For messages in the Inbox or any other email folder except Junk Email, use the following method to report spam and phishing messages:</span></span>

1. <span data-ttu-id="b7eb5-125">Sélectionnez les ellipses Autres **actions** dans le coin supérieur droit du message sélectionné, sélectionnez Signaler **le message** dans le menu déroulant, puis sélectionnez Courrier indésirable ou **Hameçonnage.** </span><span class="sxs-lookup"><span data-stu-id="b7eb5-125">Select the **More actions** ellipses on the top-right corner of the selected message, select **Report message** from the dropdown menu, and then select **Junk** or **Phishing**.</span></span>

   ![Message de rapport - Plus d’actions](../../media/report-message-more-actions.png)
   
   ![Message de rapport : courrier indésirable et hameçonnage](../../media/report-message-junk-phishing.png)

2. <span data-ttu-id="b7eb5-128">Les messages sélectionnés sont envoyés à Microsoft pour analyse et :</span><span class="sxs-lookup"><span data-stu-id="b7eb5-128">The selected messages will be sent to Microsoft for analysis and:</span></span>
   - <span data-ttu-id="b7eb5-129">Déplacé vers le dossier Courrier indésirable s’ils ont été signalés comme courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="b7eb5-129">Moved to the Junk Email folder if they were reported as spam.</span></span>
   - <span data-ttu-id="b7eb5-130">Supprimé s’ils ont été signalés comme hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="b7eb5-130">Deleted if they were reported as phishing.</span></span>

### <a name="report-messages-that-are-not-junk"></a><span data-ttu-id="b7eb5-131">Signaler les messages qui ne sont pas indésirables</span><span class="sxs-lookup"><span data-stu-id="b7eb5-131">Report messages that are not junk</span></span>

1. <span data-ttu-id="b7eb5-132">Sélectionnez les ellipses Autres **actions** dans le coin supérieur droit du message sélectionné, sélectionnez Signaler **le message** dans le menu déroulant, puis sélectionnez Non indésirable **.**</span><span class="sxs-lookup"><span data-stu-id="b7eb5-132">Select the **More actions** ellipses on the top-right corner of the selected message, select **Report message** from the dropdown menu, and then select **Not Junk**.</span></span>

   ![Message de rapport - Plus d’actions](../../media/report-message-more-actions.png)
   
   ![Message de rapport - Courrier non indésirable](../../media/report-message-not-junk.png)

2. <span data-ttu-id="b7eb5-135">Le message sélectionné est envoyé à Microsoft pour analyse et déplacé vers la boîte de réception ou tout autre dossier spécifié.</span><span class="sxs-lookup"><span data-stu-id="b7eb5-135">The selected message will be sent to Microsoft for analysis and moved to Inbox or any other specified folder.</span></span>

## <a name="view-and-review-reported-messages"></a><span data-ttu-id="b7eb5-136">Afficher et examiner les messages signalés</span><span class="sxs-lookup"><span data-stu-id="b7eb5-136">View and review reported messages</span></span>

<span data-ttu-id="b7eb5-137">Pour passer en revue les messages que les utilisateurs signalent à Microsoft, vous avez les options ci-après :</span><span class="sxs-lookup"><span data-stu-id="b7eb5-137">To review messages that users report to Microsoft, you have these options:</span></span>

- <span data-ttu-id="b7eb5-138">Utilisez le portail Soumissions d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="b7eb5-138">Use the Admin Submissions portal.</span></span> <span data-ttu-id="b7eb5-139">Pour plus d’informations, voir [Afficher les soumissions d’utilisateurs à Microsoft.](admin-submission.md#view-user-submissions-to-microsoft)</span><span class="sxs-lookup"><span data-stu-id="b7eb5-139">For more information, see [View user submissions to Microsoft](admin-submission.md#view-user-submissions-to-microsoft).</span></span>
- <span data-ttu-id="b7eb5-140">Créez une règle de flux de messagerie (également appelée règle de transport) pour envoyer des copies des messages signalés.</span><span class="sxs-lookup"><span data-stu-id="b7eb5-140">Create a mail flow rule (also known as a transport rule) to send copies of reported messages.</span></span> <span data-ttu-id="b7eb5-141">Pour obtenir des instructions, voir Utiliser des règles de flux de messagerie pour voir [quels utilisateurs font des rapports à Microsoft.](/exchange/security-and-compliance/mail-flow-rules/use-rules-to-see-what-users-are-reporting-to-microsoft)</span><span class="sxs-lookup"><span data-stu-id="b7eb5-141">For instructions, see [Use mail flow rules to see what users are reporting to Microsoft](/exchange/security-and-compliance/mail-flow-rules/use-rules-to-see-what-users-are-reporting-to-microsoft).</span></span>
