---
title: Signaler les messages de courrier indésirable et de hameçonnage dans Outlook pour iOS et Android
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
ms.assetid: 758822b5-0126-463a-9d08-7366bb2a807d
ms.collection:
- M365-security-compliance
description: Les administrateurs peuvent découvrir les options de notification de courrier indésirable, non de courrier indésirable et de hameçonnage dans Outlook pour iOS et Android.
ms.openlocfilehash: 216f60eb168190603c7c9aba58cef27c2bf15b01
ms.sourcegitcommit: 787b198765565d54ee73972f664bdbd5023d666b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/24/2020
ms.locfileid: "46867404"
---
# <a name="report-junk-and-phishing-email-in-outlook-for-ios-and-android-in-exchange-online"></a><span data-ttu-id="887f3-103">Signaler le courrier indésirable et le hameçonnage dans Outlook pour iOS et Android dans Exchange Online</span><span class="sxs-lookup"><span data-stu-id="887f3-103">Report junk and phishing email in Outlook for iOS and Android in Exchange Online</span></span>

<span data-ttu-id="887f3-104">Dans les organisations Microsoft 365 avec des boîtes aux lettres dans Exchange Online ou des boîtes aux lettres locales qui utilisent l' [authentification moderne hybride](https://docs.microsoft.com/microsoft-365/enterprise/hybrid-modern-auth-overview?view=o365-worldwide), vous pouvez utiliser les options de création de rapports intégrées dans Outlook pour iOS et Android pour soumettre des faux positifs (courrier marqué comme courrier indésirable), des faux négatifs (courrier indésirable autorisé) et des messages de hameçonnage à Exchange Online Protection (EoP)</span><span class="sxs-lookup"><span data-stu-id="887f3-104">In Microsoft 365 organizations with mailboxes in Exchange Online or on-premises mailboxes using [hybrid modern authentication](https://docs.microsoft.com/microsoft-365/enterprise/hybrid-modern-auth-overview?view=o365-worldwide), you can use the built-in reporting options in Outlook for iOS and Android to submit false positives (good email marked as spam), false negatives (bad email allowed), and phishing messages to Exchange Online Protection (EOP).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="887f3-105">Ce qu’il faut savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="887f3-105">What do you need to know before you begin</span></span>

- <span data-ttu-id="887f3-106">Si vous êtes administrateur d’une organisation avec des boîtes aux lettres Exchange Online, nous vous recommandons d’utiliser le portail d’envoi du centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="887f3-106">If you're an admin in an organization with Exchange Online mailboxes, we recommend that you use the Submissions portal in the Security & Compliance Center.</span></span> <span data-ttu-id="887f3-107">Pour plus d’informations, consultez la rubrique [utiliser la soumission de l’administrateur pour envoyer des courriers indésirables, des hameçons, des URL et des fichiers à Microsoft](admin-submission.md).</span><span class="sxs-lookup"><span data-stu-id="887f3-107">For more information, see [Use Admin Submission to submit suspected spam, phish, URLs, and files to Microsoft](admin-submission.md).</span></span>

- <span data-ttu-id="887f3-108">Vous pouvez configurer la copie ou la redirection des messages signalés vers une boîte aux lettres que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="887f3-108">You can configure reported messages to be copied or redirected to a mailbox that you specify.</span></span> <span data-ttu-id="887f3-109">Pour plus d’informations, consultez [la rubrique spécifier une boîte aux lettres pour les soumissions utilisateur de messages de courrier indésirable et de hameçonnage dans Exchange Online](user-submission.md).</span><span class="sxs-lookup"><span data-stu-id="887f3-109">For more information, see [Specify a mailbox for user submissions of spam and phishing messages in Exchange Online](user-submission.md).</span></span>

- <span data-ttu-id="887f3-110">Pour plus d’informations sur la création de rapports de messages à Microsoft, consultez la rubrique [signaler des messages et des fichiers à Microsoft](report-junk-email-messages-to-microsoft.md).</span><span class="sxs-lookup"><span data-stu-id="887f3-110">For more information about reporting messages to Microsoft, see [Report messages and files to Microsoft](report-junk-email-messages-to-microsoft.md).</span></span>

  > [!NOTE]
  > <span data-ttu-id="887f3-111">Si la création de rapports de courrier indésirable est désactivée pour Outlook dans la stratégie d’envoi, les messages de courrier indésirable ou de hameçonnage sont déplacés vers le dossier courrier indésirable et ne sont pas envoyés à votre administrateur ou Microsoft.</span><span class="sxs-lookup"><span data-stu-id="887f3-111">If junk email reporting is disabled for Outlook in the user submission policy, junk or phishing messages will be moved to the Junk folder and not reported to your admin or Microsoft.</span></span>

## <a name="report-spam-and-phishing-messages-in-outlook-for-ios-and-android"></a><span data-ttu-id="887f3-112">Signaler les messages de courrier indésirable et de hameçonnage dans Outlook pour iOS et Android</span><span class="sxs-lookup"><span data-stu-id="887f3-112">Report spam and phishing messages in Outlook for iOS and Android</span></span>

<span data-ttu-id="887f3-113">Pour les messages de la boîte de réception ou de tout autre dossier de messagerie, à l’exception du courrier indésirable, procédez comme suit pour signaler les messages de courrier indésirable et de hameçonnage pour iOS et Android :</span><span class="sxs-lookup"><span data-stu-id="887f3-113">For messages in the Inbox, or any other email folder except Junk Email, use the following steps to report spam and phishing messages for iOS and Android:</span></span>

1. <span data-ttu-id="887f3-114">Sélectionnez un ou plusieurs messages.</span><span class="sxs-lookup"><span data-stu-id="887f3-114">Select one or more messages.</span></span>
2. <span data-ttu-id="887f3-115">Dans le coin supérieur droit, appuyez sur les trois points verticaux.</span><span class="sxs-lookup"><span data-stu-id="887f3-115">In the top-right corner tap on the three vertical dots.</span></span> <span data-ttu-id="887f3-116">Le menu action s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="887f3-116">The action menu opens.</span></span>

   ![Signaler le courrier indésirable ou de hameçonnage dans le menu Action](../../media/Android-report-as-junk-dialog.png)

3. <span data-ttu-id="887f3-118">Appuyez sur **signaler le courrier indésirable** , puis sélectionnez **courrier indésirable** ou **hameçonnage**.</span><span class="sxs-lookup"><span data-stu-id="887f3-118">Tap **Report junk** and then select **Junk** or **Phishing**.</span></span>

   ![Signaler le courrier indésirable ou de hameçonnage](../../media/Android-report-junk-or-phishing.png)

4. <span data-ttu-id="887f3-120">Dans la boîte de dialogue qui s’affiche, vous pouvez choisir **rapport** ou **non**.</span><span class="sxs-lookup"><span data-stu-id="887f3-120">In the dialog that appears, you can choose **Report** or **No Thanks**.</span></span> <span data-ttu-id="887f3-121">En sélectionnant **non merci**, si vous avez cliqué sur **courrier indésirable** , le message est déplacé dans le dossier courrier indésirable si vous avez cliqué sur **hameçonnage** le message est déplacé vers le dossier éléments supprimés.</span><span class="sxs-lookup"><span data-stu-id="887f3-121">On selecting **No Thanks**, if you tapped **Junk** the message moves to the Junk Email folder, if you tapped **Phishing** the message moves to the Deleted Items folder.</span></span> <span data-ttu-id="887f3-122">Sélectionnez **rapport** pour envoyer une copie du message à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="887f3-122">Select **Report** to also send a copy of the message to Microsoft.</span></span>

   ![Signaler les options de signalement de courrier indésirable ou de hameçonnage](../../media/Android-junk-email-reporting-options.png)

<span data-ttu-id="887f3-124">Si vous changez d’avis, sélectionnez **Annuler** dans la notification Toast qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="887f3-124">If you change your mind, select **Undo** on the toast notification that appears.</span></span> <span data-ttu-id="887f3-125">Le message reste dans le dossier boîte de réception.</span><span class="sxs-lookup"><span data-stu-id="887f3-125">The message remains in the Inbox folder.</span></span>

## <a name="report-non-spam-messages-from-the-junk-folder-in-outlook-for-ios-and-android"></a><span data-ttu-id="887f3-126">Signaler des messages non de courrier indésirable dans le dossier courrier indésirable dans Outlook pour iOS et Android</span><span class="sxs-lookup"><span data-stu-id="887f3-126">Report non-spam messages from the Junk folder in Outlook for iOS and Android</span></span>

<span data-ttu-id="887f3-127">Dans le dossier courrier indésirable, procédez comme suit pour signaler les faux positifs du courrier indésirable :</span><span class="sxs-lookup"><span data-stu-id="887f3-127">In the Junk folder, use the following steps to report spam false positives:</span></span>

1. <span data-ttu-id="887f3-128">Sélectionnez un ou plusieurs messages.</span><span class="sxs-lookup"><span data-stu-id="887f3-128">Select one or more messages.</span></span>
2. <span data-ttu-id="887f3-129">Dans le coin supérieur droit, appuyez sur les trois points verticaux.</span><span class="sxs-lookup"><span data-stu-id="887f3-129">In the top-right corner tap on the three vertical dots.</span></span> <span data-ttu-id="887f3-130">Le menu action s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="887f3-130">The action menu opens.</span></span>

   ![Signaler le courrier indésirable dans le menu Action](../../media/Android-not-junk-email.png)

3. <span data-ttu-id="887f3-132">Appuyez sur **légitime**.</span><span class="sxs-lookup"><span data-stu-id="887f3-132">Tap **Not junk**.</span></span>

<span data-ttu-id="887f3-133">Une notification Toast apparaît que le message a été déplacé vers votre boîte de réception.</span><span class="sxs-lookup"><span data-stu-id="887f3-133">A toast notification appears that the email has moved to your Inbox.</span></span> <span data-ttu-id="887f3-134">Si vous changez d’avis, sélectionnez **Annuler** dans la notification Toast.</span><span class="sxs-lookup"><span data-stu-id="887f3-134">If you change your mind, select **Undo** on the toast notification.</span></span> <span data-ttu-id="887f3-135">Le courrier électronique reste dans le dossier de courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="887f3-135">The email remains in the Junk folder.</span></span>
