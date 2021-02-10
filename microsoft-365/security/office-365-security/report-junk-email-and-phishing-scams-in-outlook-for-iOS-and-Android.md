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
description: Les administrateurs peuvent en savoir plus sur les options intégrées de signalement du courrier indésirable, et non du courrier indésirable et du hameçonnage dans Outlook pour iOS et Android.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 58027f7589280b1266cddc8cfbf44db9e4f0ece4
ms.sourcegitcommit: a1846b1ee2e4fa397e39c1271c997fc4cf6d5619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2021
ms.locfileid: "50166818"
---
# <a name="report-junk-and-phishing-email-in-outlook-for-ios-and-android-in-exchange-online"></a><span data-ttu-id="b9558-103">Signaler le courrier indésirable et le hameçonnage dans Outlook pour iOS et Android dans Exchange Online</span><span class="sxs-lookup"><span data-stu-id="b9558-103">Report junk and phishing email in Outlook for iOS and Android in Exchange Online</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="b9558-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="b9558-104">**Applies to**</span></span>
- [<span data-ttu-id="b9558-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="b9558-105">Exchange Online Protection</span></span>](https://go.microsoft.com/fwlink/?linkid=2148611)
- [<span data-ttu-id="b9558-106">Microsoft Defender pour Office 365 plan 1 et plan 2</span><span class="sxs-lookup"><span data-stu-id="b9558-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](https://go.microsoft.com/fwlink/?linkid=2148715)
- [<span data-ttu-id="b9558-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="b9558-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

<span data-ttu-id="b9558-108">Dans les organisations Microsoft 365 avec des boîtes aux lettres dans Exchange Online ou locales utilisant l’authentification moderne [hybride,](https://docs.microsoft.com/microsoft-365/enterprise/hybrid-modern-auth-overview)vous pouvez utiliser les options de rapport intégrées dans Outlook pour iOS et Android pour envoyer des faux positifs (courrier électronique de qualité marqué comme courrier indésirable), des faux négatifs (courrier indésirable autorisé) et des messages de hameçonnage à Exchange Online Protection (EOP).</span><span class="sxs-lookup"><span data-stu-id="b9558-108">In Microsoft 365 organizations with mailboxes in Exchange Online or on-premises mailboxes using [hybrid modern authentication](https://docs.microsoft.com/microsoft-365/enterprise/hybrid-modern-auth-overview), you can use the built-in reporting options in Outlook for iOS and Android to submit false positives (good email marked as spam), false negatives (bad email allowed), and phishing messages to Exchange Online Protection (EOP).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="b9558-109">Ce que vous devez savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="b9558-109">What do you need to know before you begin</span></span>

- <span data-ttu-id="b9558-110">Si vous êtes un administrateur d’une organisation ayant des boîtes aux lettres Exchange Online, nous vous recommandons d’utiliser le portail Soumissions dans le Centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="b9558-110">If you're an admin in an organization with Exchange Online mailboxes, we recommend that you use the Submissions portal in the Security & Compliance Center.</span></span> <span data-ttu-id="b9558-111">Pour plus d’informations, voir Utiliser la soumission d’administrateur pour soumettre des messages suspects de courrier indésirable, d’hameçonnage, d’URL et [de fichiers à Microsoft.](admin-submission.md)</span><span class="sxs-lookup"><span data-stu-id="b9558-111">For more information, see [Use Admin Submission to submit suspected spam, phish, URLs, and files to Microsoft](admin-submission.md).</span></span>

- <span data-ttu-id="b9558-112">Vous pouvez configurer la copie ou la redirection des messages signalés vers une boîte aux lettres que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="b9558-112">You can configure reported messages to be copied or redirected to a mailbox that you specify.</span></span> <span data-ttu-id="b9558-113">Pour plus d’informations, [voir stratégies de soumission d’utilisateurs.](user-submission.md)</span><span class="sxs-lookup"><span data-stu-id="b9558-113">For more information, see [User Submissions policies](user-submission.md).</span></span>

- <span data-ttu-id="b9558-114">Pour plus d’informations sur la notification des messages à Microsoft, voir [Signaler des messages et des fichiers à Microsoft.](report-junk-email-messages-to-microsoft.md)</span><span class="sxs-lookup"><span data-stu-id="b9558-114">For more information about reporting messages to Microsoft, see [Report messages and files to Microsoft](report-junk-email-messages-to-microsoft.md).</span></span>

  > [!NOTE]
  > <span data-ttu-id="b9558-115">Si le signalement du courrier indésirable est désactivé pour Outlook dans la stratégie de soumission de l’utilisateur, les messages de courrier indésirable ou de hameçonnage sont déplacés vers le dossier Courrier indésirable et ne sont pas signalés à votre administrateur ou Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b9558-115">If junk email reporting is disabled for Outlook in the user submission policy, junk or phishing messages will be moved to the Junk folder and not reported to your admin or Microsoft.</span></span>

## <a name="report-spam-and-phishing-messages-in-outlook-for-ios-and-android"></a><span data-ttu-id="b9558-116">Signaler le courrier indésirable et les messages de hameçonnage dans Outlook pour iOS et Android</span><span class="sxs-lookup"><span data-stu-id="b9558-116">Report spam and phishing messages in Outlook for iOS and Android</span></span>

<span data-ttu-id="b9558-117">Pour les messages dans la boîte de réception ou tout autre dossier de courrier électronique à l’exception du courrier indésirable, utilisez les étapes suivantes pour signaler le courrier indésirable et les messages de hameçonnage pour iOS et Android :</span><span class="sxs-lookup"><span data-stu-id="b9558-117">For messages in the Inbox, or any other email folder except Junk Email, use the following steps to report spam and phishing messages for iOS and Android:</span></span>

1. <span data-ttu-id="b9558-118">Sélectionnez un ou plusieurs messages.</span><span class="sxs-lookup"><span data-stu-id="b9558-118">Select one or more messages.</span></span>
2. <span data-ttu-id="b9558-119">Dans le coin supérieur droit, appuyez sur les trois points verticaux.</span><span class="sxs-lookup"><span data-stu-id="b9558-119">In the top-right corner tap on the three vertical dots.</span></span> <span data-ttu-id="b9558-120">Le menu Action s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="b9558-120">The action menu opens.</span></span>

   ![Signaler le courrier indésirable ou le hameçonnage à partir du menu Action](../../media/Android-report-as-junk-dialog.png)

3. <span data-ttu-id="b9558-122">Appuyez **sur Signaler le courrier** indésirable, puis **sélectionnez Courrier** indésirable ou **Hameçonnage.**</span><span class="sxs-lookup"><span data-stu-id="b9558-122">Tap **Report junk** and then select **Junk** or **Phishing**.</span></span>

   ![Signaler le courrier indésirable ou le hameçonnage](../../media/Android-report-junk-or-phishing.png)

4. <span data-ttu-id="b9558-124">Dans la boîte de dialogue qui s’affiche, vous pouvez choisir **Rapport** ou **Non merci.**</span><span class="sxs-lookup"><span data-stu-id="b9558-124">In the dialog that appears, you can choose **Report** or **No Thanks**.</span></span> <span data-ttu-id="b9558-125">Lorsque vous sélectionnez Non **merci,** si vous avez tapé Courrier indésirable, le message se déplace vers le dossier Courrier indésirable, si vous avez tapé Hameçonnage, le message est envoyé vers le dossier Éléments supprimés.  </span><span class="sxs-lookup"><span data-stu-id="b9558-125">On selecting **No Thanks**, if you tapped **Junk** the message moves to the Junk Email folder, if you tapped **Phishing** the message moves to the Deleted Items folder.</span></span> <span data-ttu-id="b9558-126">Sélectionnez **Rapport** pour envoyer également une copie du message à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b9558-126">Select **Report** to also send a copy of the message to Microsoft.</span></span>

   ![Signaler les options de signalement de courrier indésirable ou de hameçonnage](../../media/Android-junk-email-reporting-options.png)

<span data-ttu-id="b9558-128">Si vous changez d’avis, **sélectionnez Annuler** dans la notification toast qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="b9558-128">If you change your mind, select **Undo** on the toast notification that appears.</span></span> <span data-ttu-id="b9558-129">Le message reste dans le dossier Boîte de réception.</span><span class="sxs-lookup"><span data-stu-id="b9558-129">The message remains in the Inbox folder.</span></span>

## <a name="report-non-spam-messages-from-the-junk-folder-in-outlook-for-ios-and-android"></a><span data-ttu-id="b9558-130">Signaler les messages non indésirables à partir du dossier Courrier indésirable dans Outlook pour iOS et Android</span><span class="sxs-lookup"><span data-stu-id="b9558-130">Report non-spam messages from the Junk folder in Outlook for iOS and Android</span></span>

<span data-ttu-id="b9558-131">Dans le dossier Courrier indésirable, utilisez les étapes suivantes pour signaler les faux positifs du courrier indésirable :</span><span class="sxs-lookup"><span data-stu-id="b9558-131">In the Junk folder, use the following steps to report spam false positives:</span></span>

1. <span data-ttu-id="b9558-132">Sélectionnez un ou plusieurs messages.</span><span class="sxs-lookup"><span data-stu-id="b9558-132">Select one or more messages.</span></span>
2. <span data-ttu-id="b9558-133">Dans le coin supérieur droit, appuyez sur les trois points verticaux.</span><span class="sxs-lookup"><span data-stu-id="b9558-133">In the top-right corner tap on the three vertical dots.</span></span> <span data-ttu-id="b9558-134">Le menu Action s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="b9558-134">The action menu opens.</span></span>

   ![Signaler le courrier non indésirable à partir du menu Action](../../media/Android-not-junk-email.png)

3. <span data-ttu-id="b9558-136">Appuyez **sur Pas de courrier indésirable**.</span><span class="sxs-lookup"><span data-stu-id="b9558-136">Tap **Not junk**.</span></span>

<span data-ttu-id="b9558-137">Une notification toast s’affiche pour vous faire savoir que l’e-mail a été déplacé vers votre boîte de réception.</span><span class="sxs-lookup"><span data-stu-id="b9558-137">A toast notification appears that the email has moved to your Inbox.</span></span> <span data-ttu-id="b9558-138">Si vous changez d’avis, sélectionnez **Annuler** dans la notification toast.</span><span class="sxs-lookup"><span data-stu-id="b9558-138">If you change your mind, select **Undo** on the toast notification.</span></span> <span data-ttu-id="b9558-139">Le courrier électronique reste dans le dossier Courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="b9558-139">The email remains in the Junk folder.</span></span>
