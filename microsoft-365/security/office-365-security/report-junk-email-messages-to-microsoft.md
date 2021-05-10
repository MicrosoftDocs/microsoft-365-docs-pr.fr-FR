---
title: Signaler le courrier indésirable, le courrier non indésirable et le hameçonnage à Microsoft
f1.keywords:
- NOCSH
ms.author: siosulli
author: dansimp
manager: dansimp
ms.date: ''
audience: ITPro
ms.topic: overview
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: c31406ea-2979-4fac-9288-f835269b9d2f
ms.collection:
- M365-security-compliance
description: Les administrateurs peuvent découvrir les différentes façons de signaler les messages et fichiers bon et mauvais à Microsoft pour analyse.
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 8c87938a8716da36f027300d685f0caedcf69660
ms.sourcegitcommit: de5fce90de22ba588e75e1a1d2e87e03b9e25ec7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "52291126"
---
# <a name="report-messages-and-files-to-microsoft"></a><span data-ttu-id="45c79-103">Signaler les messages et fichiers à Microsoft</span><span class="sxs-lookup"><span data-stu-id="45c79-103">Report messages and files to Microsoft</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="45c79-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="45c79-104">**Applies to**</span></span>
- [<span data-ttu-id="45c79-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="45c79-105">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="45c79-106">Microsoft Defender pour Office 365 : offre 1 et offre 2</span><span class="sxs-lookup"><span data-stu-id="45c79-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](defender-for-office-365.md)
- [<span data-ttu-id="45c79-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="45c79-107">Microsoft 365 Defender</span></span>](../defender/microsoft-365-defender.md)

<span data-ttu-id="45c79-108">Dans Microsoft 365 organisations avec des boîtes aux lettres en Exchange Online ou des organisations Exchange Online Protection autonomes (EOP) sans boîtes aux lettres Exchange Online, les utilisateurs et les administrateurs ont plusieurs méthodes différentes pour signaler des messages électroniques et des fichiers à Microsoft.</span><span class="sxs-lookup"><span data-stu-id="45c79-108">In Microsoft 365 organizations with mailboxes in Exchange Online or standalone Exchange Online Protection (EOP) organizations without Exchange Online mailboxes, both users and admins have several different methods for reporting email messages and files to Microsoft.</span></span>

****

|<span data-ttu-id="45c79-109">Méthode</span><span class="sxs-lookup"><span data-stu-id="45c79-109">Method</span></span>|<span data-ttu-id="45c79-110">Description</span><span class="sxs-lookup"><span data-stu-id="45c79-110">Description</span></span>|
|---|---|
|[<span data-ttu-id="45c79-111">Utilisez la soumission de l’administrateur pour soumettre des courriers indésirables, l’hameçonnage, des URL et des fichiers à Microsoft</span><span class="sxs-lookup"><span data-stu-id="45c79-111">Use Admin Submission to submit suspected spam, phish, URLs, and files to Microsoft</span></span>](admin-submission.md)|<span data-ttu-id="45c79-112">La méthode de rapport recommandée pour les administrateurs dans les organisations Exchange Online boîtes aux lettres (non disponible dans EOP autonome).</span><span class="sxs-lookup"><span data-stu-id="45c79-112">The recommended reporting method for admins in organizations with Exchange Online mailboxes (not available in standalone EOP).</span></span>|
|[<span data-ttu-id="45c79-113">Activer le message de rapport ou les modules de signalement du hameçonnage</span><span class="sxs-lookup"><span data-stu-id="45c79-113">Enable the Report Message or the Report Phishing add-ins</span></span>](enable-the-report-message-add-in.md)|<span data-ttu-id="45c79-114">Fonctionne avec Outlook et Outlook sur le web (anciennement Outlook Web App).</span><span class="sxs-lookup"><span data-stu-id="45c79-114">Works with Outlook and Outlook on the web (formerly known as Outlook Web App).</span></span> <p> <span data-ttu-id="45c79-115">En fonction de votre abonnement, les messages que les utilisateurs ont signalés avec les modules sont disponibles dans le [](threat-explorer-views.md#email--submissions)portail de soumissions d’administration, les résultats de l’examen et de la réponse [automatisés (AIR),](air-view-investigation-results.md)le rapport des [messages](view-email-security-reports.md#user-reported-messages-report)signalés par l’utilisateur et l’Explorateur de [menaces.](admin-submission.md)</span><span class="sxs-lookup"><span data-stu-id="45c79-115">Depending on your subscription, messages that users reported with the add-ins are available in [the Admin Submissions portal](admin-submission.md), [Automated investigation and response (AIR) results](air-view-investigation-results.md), the [User-reported messages report](view-email-security-reports.md#user-reported-messages-report), and [Threat Explorer](threat-explorer-views.md#email--submissions).</span></span> <p> <span data-ttu-id="45c79-116">Vous pouvez configurer la copie ou la redirection des messages signalés vers une boîte aux lettres que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="45c79-116">You can configure reported messages to be copied or redirected to a mailbox that you specify.</span></span> <span data-ttu-id="45c79-117">Pour plus d’informations, voir [Stratégies d’envoi des utilisateurs.](user-submission.md)</span><span class="sxs-lookup"><span data-stu-id="45c79-117">For more information, see [User submissions policies](user-submission.md).</span></span>
|[<span data-ttu-id="45c79-118">Signaler les faux positifs et les faux négatifs à Outlook</span><span class="sxs-lookup"><span data-stu-id="45c79-118">Report false positives and false negatives to Outlook</span></span>](report-false-positives-and-false-negatives.md)|<span data-ttu-id="45c79-119">Envoyez les faux positifs (messages électroniques de qualité bloqués ou envoyés au dossier courrier indésirable) et les faux négatifs (courrier indésirable ou hameçonnage remis à la boîte de réception) à Exchange Online Protection (EOP) à l’aide de la fonctionnalité Signaler un message.</span><span class="sxs-lookup"><span data-stu-id="45c79-119">Submit false positives (good email that was blocked or sent to junk folder) and false negatives (unwanted email or phish that was delivered to the inbox) to Exchange Online Protection (EOP) using the Report Message feature.</span></span>|
|[<span data-ttu-id="45c79-120">Envoyer manuellement des messages à Microsoft pour analyse</span><span class="sxs-lookup"><span data-stu-id="45c79-120">Manually submit messages to Microsoft for analysis</span></span>](submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md)|<span data-ttu-id="45c79-121">Envoyez manuellement des messages joints à des adresses de messagerie Microsoft spécifiques pour le courrier indésirable, et non le courrier indésirable et le hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="45c79-121">Manually send attached messages to specific Microsoft email addresses for spam, not spam, and phishing.</span></span>|
|[<span data-ttu-id="45c79-122">Utiliser des règles de flux de messagerie pour voir ce que vos utilisateurs ont signalé à Microsoft</span><span class="sxs-lookup"><span data-stu-id="45c79-122">Use mail flow rules to see what your users are reporting to Microsoft</span></span>](use-mail-flow-rules-to-see-what-your-users-are-reporting-to-microsoft.md)|<span data-ttu-id="45c79-123">Découvrez comment créer une règle de flux de messagerie (également appelée règle de transport) qui vous avertit lorsque les utilisateurs signalent des messages à Microsoft pour analyse.</span><span class="sxs-lookup"><span data-stu-id="45c79-123">Learn how to create a mail flow rule (also known as a transport rule) that notifies you when users report messages to Microsoft for analysis.</span></span>|
|[<span data-ttu-id="45c79-124">Soumettre des programmes malveillants et non malveillants à Microsoft pour analyse</span><span class="sxs-lookup"><span data-stu-id="45c79-124">Submit malware and non-malware to Microsoft for analysis</span></span>](submitting-malware-and-non-malware-to-microsoft-for-analysis.md)|<span data-ttu-id="45c79-125">Utilisez le site Renseignement de sécurité Microsoft pour envoyer des pièces jointes et d’autres fichiers.</span><span class="sxs-lookup"><span data-stu-id="45c79-125">Use the Microsoft Security Intelligence site to submit attachments and other files.</span></span>|

<span data-ttu-id="45c79-126">Si le courrier indésirable ou le hameçonnage a été mis en quarantaine au lieu d’être remis, les utilisateurs peuvent signaler les messages à Microsoft à partir du portail de mise en quarantaine dans le Centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="45c79-126">If the spam or phishing messages were quarantined instead of delivered, users can report the messages to Microsoft from the Quarantine portal in the Security & Compliance Center.</span></span> <span data-ttu-id="45c79-127">Pour plus d’informations, voir Rechercher et libérer les messages mis en quarantaine en tant [qu’utilisateur dans Microsoft 365](find-and-release-quarantined-messages-as-a-user.md).</span><span class="sxs-lookup"><span data-stu-id="45c79-127">For details, see [Find and release quarantined messages as a user in Microsoft 365](find-and-release-quarantined-messages-as-a-user.md).</span></span>

> [!NOTE]
> <span data-ttu-id="45c79-128">Les données des soumissions à Microsoft résident dans la limite Office 365 conformité des centres de données d’Amérique du Nord.</span><span class="sxs-lookup"><span data-stu-id="45c79-128">Data from submissions to Microsoft resides in the Office 365 compliance boundary in North American data centers.</span></span> <span data-ttu-id="45c79-129">Les données sont examinées par les analystes de l’équipe d’ingénierie afin d’améliorer l’efficacité des filtres.</span><span class="sxs-lookup"><span data-stu-id="45c79-129">The data is reviewed by analysts on the engineering team to help improve the effectiveness of the filters.</span></span>
