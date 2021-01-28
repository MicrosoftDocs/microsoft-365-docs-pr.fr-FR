---
title: Signaler le courrier indésirable et le hameçonnage dans Outlook pour iOS et Android
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
ms.assetid: 758822b5-0126-463a-9d08-7366bb2a807d
ms.collection:
- M365-security-compliance
description: Les administrateurs peuvent en savoir plus sur les options intégrées de signalement de courrier indésirable, non indésirable et de hameçonnage dans Outlook pour iOS et Android.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: d702ab1d97c07c3e38430a9a7beff5f14db7b60a
ms.sourcegitcommit: 537e513a4a232a01e44ecbc76d86a8bcaf142482
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/27/2021
ms.locfileid: "50029279"
---
# <a name="report-junk-and-phishing-email-in-outlook-for-ios-and-android-in-exchange-online"></a><span data-ttu-id="aadfb-103">Signaler le courrier indésirable et le hameçonnage dans Outlook pour iOS et Android dans Exchange Online</span><span class="sxs-lookup"><span data-stu-id="aadfb-103">Report junk and phishing email in Outlook for iOS and Android in Exchange Online</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


<span data-ttu-id="aadfb-104">Dans les organisations Microsoft 365 avec des boîtes aux lettres dans Exchange Online ou locales utilisant l’authentification moderne [hybride,](https://docs.microsoft.com/microsoft-365/enterprise/hybrid-modern-auth-overview)vous pouvez utiliser les options de rapport intégrées dans Outlook pour iOS et Android pour envoyer des faux positifs (courrier électronique de qualité marqué comme courrier indésirable), des faux négatifs (courrier indésirable autorisé) et des messages de hameçonnage à Exchange Online Protection (EOP).</span><span class="sxs-lookup"><span data-stu-id="aadfb-104">In Microsoft 365 organizations with mailboxes in Exchange Online or on-premises mailboxes using [hybrid modern authentication](https://docs.microsoft.com/microsoft-365/enterprise/hybrid-modern-auth-overview), you can use the built-in reporting options in Outlook for iOS and Android to submit false positives (good email marked as spam), false negatives (bad email allowed), and phishing messages to Exchange Online Protection (EOP).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="aadfb-105">Ce que vous devez savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="aadfb-105">What do you need to know before you begin</span></span>

- <span data-ttu-id="aadfb-106">Si vous êtes un administrateur d’une organisation ayant des boîtes aux lettres Exchange Online, nous vous recommandons d’utiliser le portail Soumissions dans le Centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="aadfb-106">If you're an admin in an organization with Exchange Online mailboxes, we recommend that you use the Submissions portal in the Security & Compliance Center.</span></span> <span data-ttu-id="aadfb-107">Pour plus d’informations, voir Utiliser la soumission d’administrateur pour soumettre des messages suspects de courrier indésirable, d’hameçonnage, d’URL et [de fichiers à Microsoft.](admin-submission.md)</span><span class="sxs-lookup"><span data-stu-id="aadfb-107">For more information, see [Use Admin Submission to submit suspected spam, phish, URLs, and files to Microsoft](admin-submission.md).</span></span>

- <span data-ttu-id="aadfb-108">Vous pouvez configurer la copie ou la redirection des messages signalés vers une boîte aux lettres que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="aadfb-108">You can configure reported messages to be copied or redirected to a mailbox that you specify.</span></span> <span data-ttu-id="aadfb-109">Pour plus d’informations, [voir stratégies de soumission d’utilisateurs.](user-submission.md)</span><span class="sxs-lookup"><span data-stu-id="aadfb-109">For more information, see [User Submissions policies](user-submission.md).</span></span>

- <span data-ttu-id="aadfb-110">Pour plus d’informations sur la notification des messages à Microsoft, voir [Signaler des messages et des fichiers à Microsoft.](report-junk-email-messages-to-microsoft.md)</span><span class="sxs-lookup"><span data-stu-id="aadfb-110">For more information about reporting messages to Microsoft, see [Report messages and files to Microsoft](report-junk-email-messages-to-microsoft.md).</span></span>

  > [!NOTE]
  > <span data-ttu-id="aadfb-111">Si le signalement du courrier indésirable est désactivé pour Outlook dans la stratégie de soumission de l’utilisateur, les messages de courrier indésirable ou de hameçonnage sont déplacés vers le dossier Courrier indésirable et ne sont pas signalés à votre administrateur ou Microsoft.</span><span class="sxs-lookup"><span data-stu-id="aadfb-111">If junk email reporting is disabled for Outlook in the user submission policy, junk or phishing messages will be moved to the Junk folder and not reported to your admin or Microsoft.</span></span>

## <a name="report-spam-and-phishing-messages-in-outlook-for-ios-and-android"></a><span data-ttu-id="aadfb-112">Signaler le courrier indésirable et les messages de hameçonnage dans Outlook pour iOS et Android</span><span class="sxs-lookup"><span data-stu-id="aadfb-112">Report spam and phishing messages in Outlook for iOS and Android</span></span>

<span data-ttu-id="aadfb-113">Pour les messages dans la boîte de réception ou tout autre dossier de courrier électronique à l’exception du courrier indésirable, utilisez les étapes suivantes pour signaler le courrier indésirable et les messages de hameçonnage pour iOS et Android :</span><span class="sxs-lookup"><span data-stu-id="aadfb-113">For messages in the Inbox, or any other email folder except Junk Email, use the following steps to report spam and phishing messages for iOS and Android:</span></span>

1. <span data-ttu-id="aadfb-114">Sélectionnez un ou plusieurs messages.</span><span class="sxs-lookup"><span data-stu-id="aadfb-114">Select one or more messages.</span></span>
2. <span data-ttu-id="aadfb-115">Dans le coin supérieur droit, appuyez sur les trois points verticaux.</span><span class="sxs-lookup"><span data-stu-id="aadfb-115">In the top-right corner tap on the three vertical dots.</span></span> <span data-ttu-id="aadfb-116">Le menu Action s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="aadfb-116">The action menu opens.</span></span>

   ![Signaler le courrier indésirable ou le hameçonnage à partir du menu Action](../../media/Android-report-as-junk-dialog.png)

3. <span data-ttu-id="aadfb-118">Appuyez **sur Signaler le courrier** indésirable, puis **sélectionnez Courrier** indésirable ou **Hameçonnage.**</span><span class="sxs-lookup"><span data-stu-id="aadfb-118">Tap **Report junk** and then select **Junk** or **Phishing**.</span></span>

   ![Signaler le courrier indésirable ou le hameçonnage](../../media/Android-report-junk-or-phishing.png)

4. <span data-ttu-id="aadfb-120">Dans la boîte de dialogue qui s’affiche, vous pouvez choisir **Rapport** ou **Non merci.**</span><span class="sxs-lookup"><span data-stu-id="aadfb-120">In the dialog that appears, you can choose **Report** or **No Thanks**.</span></span> <span data-ttu-id="aadfb-121">Lorsque vous sélectionnez Non **merci,** si vous avez tapé Courrier indésirable, le message se déplace vers le dossier Courrier indésirable, si vous avez tapé Hameçonnage, le message est envoyé vers le dossier Éléments supprimés.  </span><span class="sxs-lookup"><span data-stu-id="aadfb-121">On selecting **No Thanks**, if you tapped **Junk** the message moves to the Junk Email folder, if you tapped **Phishing** the message moves to the Deleted Items folder.</span></span> <span data-ttu-id="aadfb-122">Sélectionnez **Rapport** pour envoyer également une copie du message à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="aadfb-122">Select **Report** to also send a copy of the message to Microsoft.</span></span>

   ![Signaler les options de signalement de courrier indésirable ou de hameçonnage](../../media/Android-junk-email-reporting-options.png)

<span data-ttu-id="aadfb-124">Si vous changez d’avis, **sélectionnez Annuler** dans la notification toast qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="aadfb-124">If you change your mind, select **Undo** on the toast notification that appears.</span></span> <span data-ttu-id="aadfb-125">Le message reste dans le dossier Boîte de réception.</span><span class="sxs-lookup"><span data-stu-id="aadfb-125">The message remains in the Inbox folder.</span></span>

## <a name="report-non-spam-messages-from-the-junk-folder-in-outlook-for-ios-and-android"></a><span data-ttu-id="aadfb-126">Signaler les messages non indésirables à partir du dossier Courrier indésirable dans Outlook pour iOS et Android</span><span class="sxs-lookup"><span data-stu-id="aadfb-126">Report non-spam messages from the Junk folder in Outlook for iOS and Android</span></span>

<span data-ttu-id="aadfb-127">Dans le dossier Courrier indésirable, utilisez les étapes suivantes pour signaler les faux positifs du courrier indésirable :</span><span class="sxs-lookup"><span data-stu-id="aadfb-127">In the Junk folder, use the following steps to report spam false positives:</span></span>

1. <span data-ttu-id="aadfb-128">Sélectionnez un ou plusieurs messages.</span><span class="sxs-lookup"><span data-stu-id="aadfb-128">Select one or more messages.</span></span>
2. <span data-ttu-id="aadfb-129">Dans le coin supérieur droit, appuyez sur les trois points verticaux.</span><span class="sxs-lookup"><span data-stu-id="aadfb-129">In the top-right corner tap on the three vertical dots.</span></span> <span data-ttu-id="aadfb-130">Le menu Action s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="aadfb-130">The action menu opens.</span></span>

   ![Signaler le courrier non indésirable à partir du menu Action](../../media/Android-not-junk-email.png)

3. <span data-ttu-id="aadfb-132">Appuyez **sur Pas de courrier indésirable**.</span><span class="sxs-lookup"><span data-stu-id="aadfb-132">Tap **Not junk**.</span></span>

<span data-ttu-id="aadfb-133">Une notification toast apparaît que l’e-mail a été déplacé vers votre boîte de réception.</span><span class="sxs-lookup"><span data-stu-id="aadfb-133">A toast notification appears that the email has moved to your Inbox.</span></span> <span data-ttu-id="aadfb-134">Si vous changez d’avis, **sélectionnez Annuler** dans la notification toast.</span><span class="sxs-lookup"><span data-stu-id="aadfb-134">If you change your mind, select **Undo** on the toast notification.</span></span> <span data-ttu-id="aadfb-135">Le courrier électronique reste dans le dossier Courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="aadfb-135">The email remains in the Junk folder.</span></span>
