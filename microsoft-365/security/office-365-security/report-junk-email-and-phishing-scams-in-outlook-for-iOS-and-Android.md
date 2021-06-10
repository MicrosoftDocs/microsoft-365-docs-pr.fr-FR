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
ms.openlocfilehash: 2c95f7b32d0d395e164d218c994b1608d36018d5
ms.sourcegitcommit: dcb97fbfdae52960ae62b6faa707a05358193ed5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2021
ms.locfileid: "51204719"
---
# <a name="report-junk-and-phishing-email-in-outlook-for-ios-and-android-in-exchange-online"></a><span data-ttu-id="acee3-103">Signaler le courrier indésirable et le hameçonnage dans Outlook pour iOS et Android dans Exchange Online</span><span class="sxs-lookup"><span data-stu-id="acee3-103">Report junk and phishing email in Outlook for iOS and Android in Exchange Online</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="acee3-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="acee3-104">**Applies to**</span></span>
- [<span data-ttu-id="acee3-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="acee3-105">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="acee3-106">Microsoft Defender pour Office 365 : offre 1 et offre 2</span><span class="sxs-lookup"><span data-stu-id="acee3-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](defender-for-office-365.md)
- [<span data-ttu-id="acee3-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="acee3-107">Microsoft 365 Defender</span></span>](../defender/microsoft-365-defender.md)

<span data-ttu-id="acee3-108">Dans Microsoft 365 organisations avec des boîtes aux lettres dans Exchange Online ou locales utilisant l’authentification moderne [hybride,](../../enterprise/hybrid-modern-auth-overview.md)vous pouvez soumettre des faux positifs (courrier électronique de qualité marqué comme courrier indésirable), des faux négatifs (courrier indésirable autorisé) et des messages de hameçonnage à Exchange Online Protection (EOP).</span><span class="sxs-lookup"><span data-stu-id="acee3-108">In Microsoft 365 organizations with mailboxes in Exchange Online or on-premises mailboxes using [hybrid modern authentication](../../enterprise/hybrid-modern-auth-overview.md), you can submit false positives (good email marked as spam), false negatives (bad email allowed), and phishing messages to Exchange Online Protection (EOP).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="acee3-109">Ce que vous devez savoir avant de commencer</span><span class="sxs-lookup"><span data-stu-id="acee3-109">What do you need to know before you begin</span></span>

- <span data-ttu-id="acee3-110">Pour une expérience de soumission d’utilisateurs de premier choix, nous vous recommandons d’utiliser les add-ins Message de rapport et Hameçonnage de rapport. Pour [plus d’informations,](./enable-the-report-message-add-in.md) voir Activer le add-in Message de rapport et Activer le module [de](./enable-the-report-phish-add-in.md) signalement de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="acee3-110">For the best user submission experience we recommend using the Report Message and the Report Phishing add-ins. See [Enable the Report Message add-in](./enable-the-report-message-add-in.md) and [Enable the Report Phishing add-in](./enable-the-report-phish-add-in.md) for more information.</span></span>

- <span data-ttu-id="acee3-111">Si vous êtes un administrateur d’une organisation Exchange Online boîtes aux lettres, nous vous recommandons d’utiliser le portail Soumissions dans le Centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="acee3-111">If you're an admin in an organization with Exchange Online mailboxes, we recommend that you use the Submissions portal in the Security & Compliance Center.</span></span> <span data-ttu-id="acee3-112">Pour plus d’informations, voir Utiliser la soumission d’administrateur pour soumettre des messages suspects de courrier indésirable, d’hameçonnage, d’URL et [de fichiers à Microsoft.](admin-submission.md)</span><span class="sxs-lookup"><span data-stu-id="acee3-112">For more information, see [Use Admin Submission to submit suspected spam, phish, URLs, and files to Microsoft](admin-submission.md).</span></span>

- <span data-ttu-id="acee3-113">Vous pouvez configurer la copie ou la redirection des messages signalés vers une boîte aux lettres que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="acee3-113">You can configure reported messages to be copied or redirected to a mailbox that you specify.</span></span> <span data-ttu-id="acee3-114">Pour plus d’informations, [voir stratégies de soumission d’utilisateurs.](user-submission.md)</span><span class="sxs-lookup"><span data-stu-id="acee3-114">For more information, see [User Submissions policies](user-submission.md).</span></span>

- <span data-ttu-id="acee3-115">Pour plus d’informations sur la notification des messages à Microsoft, voir [Signaler des messages et des fichiers à Microsoft.](report-junk-email-messages-to-microsoft.md)</span><span class="sxs-lookup"><span data-stu-id="acee3-115">For more information about reporting messages to Microsoft, see [Report messages and files to Microsoft](report-junk-email-messages-to-microsoft.md).</span></span>

  > [!NOTE]
  > <span data-ttu-id="acee3-116">Si le signalement du courrier indésirable est désactivé pour les Outlook dans la stratégie de soumission de l’utilisateur, les messages de courrier indésirable ou de hameçonnage sont déplacés vers le dossier Courrier indésirable et ne sont pas signalés à votre administrateur ou Microsoft.</span><span class="sxs-lookup"><span data-stu-id="acee3-116">If junk email reporting is disabled for Outlook in the user submission policy, junk or phishing messages will be moved to the Junk folder and not reported to your admin or Microsoft.</span></span>