---
title: Comment signaler des faux positifs ou des faux négatifs à la suite d’un examen automatisé dans Microsoft Defender pour Office 365
description: Un problème a-t-il été manqué ou détecté à tort par AIR dans Microsoft Defender pour Office 365 ? Découvrez comment soumettre des faux positifs ou des faux négatifs à Microsoft pour analyse.
keywords: automatisé, examen, alerte, déclencheur, action, correction, faux positif, faux négatif
search.appverid: met150
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: deniseb
author: denisebmsft
ms.prod: m365-security
ms.date: 01/29/2021
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
- m365initiative-defender-office365
ms.topic: how-to
ms.custom:
- autoir
ms.technology: mdo
ms.openlocfilehash: 4476578939f2ece90c638c919c7e4d134ea2d9ec
ms.sourcegitcommit: dcb97fbfdae52960ae62b6faa707a05358193ed5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2021
ms.locfileid: "51204860"
---
# <a name="how-to-report-false-positivesnegatives-in-automated-investigation-and-response-capabilities"></a><span data-ttu-id="e18ce-105">Comment signaler les faux positifs/négatifs dans les fonctionnalités automatisées d’examen et de réponse</span><span class="sxs-lookup"><span data-stu-id="e18ce-105">How to report false positives/negatives in automated investigation and response capabilities</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

<span data-ttu-id="e18ce-106">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="e18ce-106">**Applies to**</span></span>
- [<span data-ttu-id="e18ce-107">Microsoft Defender pour Office 365 Plan 2</span><span class="sxs-lookup"><span data-stu-id="e18ce-107">Microsoft Defender for Office 365 plan 2</span></span>](defender-for-office-365.md)
- [<span data-ttu-id="e18ce-108">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="e18ce-108">Microsoft 365 Defender</span></span>](../defender/microsoft-365-defender.md)

<span data-ttu-id="e18ce-109">Si des fonctionnalités d’investigation et de réponse automatisées [(AIR) dans Office 365](automated-investigation-response-office.md) ont manqué ou détecté un problème, il existe des étapes que votre équipe des opérations de sécurité peut suivre pour résoudre ce problème.</span><span class="sxs-lookup"><span data-stu-id="e18ce-109">If [automated investigation and response (AIR) capabilities in Office 365](automated-investigation-response-office.md) missed or wrongly detected something, there are steps your security operations team can take to fix it.</span></span> <span data-ttu-id="e18ce-110">Ces actions sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="e18ce-110">Such actions include:</span></span>

- <span data-ttu-id="e18ce-111">[Signalement d’un faux positif/négatif à Microsoft](#report-a-false-positivenegative-to-microsoft-for-analysis);</span><span class="sxs-lookup"><span data-stu-id="e18ce-111">[Reporting a false positive/negative to Microsoft](#report-a-false-positivenegative-to-microsoft-for-analysis);</span></span>
- <span data-ttu-id="e18ce-112">[Ajustement des alertes](#adjust-an-alert-to-prevent-false-positives-from-recurring) (si nécessaire) ; et</span><span class="sxs-lookup"><span data-stu-id="e18ce-112">[Adjusting alerts](#adjust-an-alert-to-prevent-false-positives-from-recurring) (if needed); and</span></span>
- <span data-ttu-id="e18ce-113">[Annuler les actions de correction qui ont été prises.](#undo-a-remediation-action)</span><span class="sxs-lookup"><span data-stu-id="e18ce-113">[Undoing remediation actions that were taken](#undo-a-remediation-action).</span></span>

<span data-ttu-id="e18ce-114">Utilisez cet article comme guide.</span><span class="sxs-lookup"><span data-stu-id="e18ce-114">Use this article as a guide.</span></span>

## <a name="report-a-false-positivenegative-to-microsoft-for-analysis"></a><span data-ttu-id="e18ce-115">Signaler un faux positif/négatif à Microsoft pour analyse</span><span class="sxs-lookup"><span data-stu-id="e18ce-115">Report a false positive/negative to Microsoft for analysis</span></span>

<span data-ttu-id="e18ce-116">Si AIR dans Microsoft Defender pour Office 365 a manqué un message électronique, une pièce jointe, une URL dans un message électronique ou une URL dans un fichier Office, vous pouvez soumettre des messages suspects de courrier indésirable, de hameçonnage, d’URL et de fichiers à Microsoft pour l’analyse [Office 365.](admin-submission.md)</span><span class="sxs-lookup"><span data-stu-id="e18ce-116">If AIR in Microsoft Defender for Office 365 missed an email message, an email attachment, a URL in an email message, or a URL in an Office file, you can [submit suspected spam, phish, URLs, and files to Microsoft for Office 365 scanning](admin-submission.md).</span></span>

<span data-ttu-id="e18ce-117">Vous pouvez également [soumettre un fichier à Microsoft pour analyse des programmes malveillants.](https://www.microsoft.com/wdsi/filesubmission)</span><span class="sxs-lookup"><span data-stu-id="e18ce-117">You can also [Submit a file to Microsoft for malware analysis](https://www.microsoft.com/wdsi/filesubmission).</span></span>

## <a name="adjust-an-alert-to-prevent-false-positives-from-recurring"></a><span data-ttu-id="e18ce-118">Ajuster une alerte pour éviter que les faux positifs ne se répètent</span><span class="sxs-lookup"><span data-stu-id="e18ce-118">Adjust an alert to prevent false positives from recurring</span></span>

<span data-ttu-id="e18ce-119">Si une alerte est déclenchée par un usage légitime ou si l’alerte est inexacte, vous pouvez gérer les [alertes](/cloud-app-security/managing-alerts)dans le portail Cloud App Security .</span><span class="sxs-lookup"><span data-stu-id="e18ce-119">If an alert is triggered by legitimate use, or the alert is inaccurate, you can [Manage alerts in the Cloud App Security portal](/cloud-app-security/managing-alerts).</span></span>

<span data-ttu-id="e18ce-120">Si votre organisation utilise Microsoft Defender pour [endpoint](/windows/security/threat-protection) en plus d’Office 365 et qu’un fichier, une adresse IP, une URL ou un domaine est traité comme un programme malveillant sur un appareil, même s’il est sécurisé, vous pouvez créer un indicateur personnalisé avec une [action](/windows/security/threat-protection/microsoft-defender-atp/manage-indicators)« Autoriser » pour votre appareil.</span><span class="sxs-lookup"><span data-stu-id="e18ce-120">If your organization is using [Microsoft Defender for Endpoint](/windows/security/threat-protection) in addition to Office 365, and a file, IP address, URL, or domain is treated as malware on a device, even though it's safe, you can [create a custom indicator with an "Allow" action for your device](/windows/security/threat-protection/microsoft-defender-atp/manage-indicators).</span></span>

## <a name="undo-a-remediation-action"></a><span data-ttu-id="e18ce-121">Annuler une action de correction</span><span class="sxs-lookup"><span data-stu-id="e18ce-121">Undo a remediation action</span></span>

<span data-ttu-id="e18ce-122">Dans la plupart des cas, si une action corrective a été prise sur un message électronique, une pièce jointe ou une URL, et que l’élément n’est pas une menace, votre équipe des opérations de sécurité peut annuler l’action de correction et prendre des mesures pour empêcher le faux positif de se reproduire.</span><span class="sxs-lookup"><span data-stu-id="e18ce-122">In most cases, if a remediation action was taken on an email message, email attachment, or URL, and the item is actually not a threat, your security operations team can undo the remediation action and take steps to prevent the false positive from recurring.</span></span> <span data-ttu-id="e18ce-123">Vous pouvez utiliser [l’Explorateur de](#undo-an-action-using-threat-explorer) menaces ou l’onglet Actions pour [un examen](#undo-an-action-in-the-action-center) afin d’annuler une action.</span><span class="sxs-lookup"><span data-stu-id="e18ce-123">You can either use [Threat Explorer](#undo-an-action-using-threat-explorer) or the [Actions tab for an investigation](#undo-an-action-in-the-action-center) to undo an action.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e18ce-124">Assurez-vous que vous avez les autorisations nécessaires avant d’essayer d’effectuer les tâches suivantes.</span><span class="sxs-lookup"><span data-stu-id="e18ce-124">Make sure you have the necessary permissions before attempting to perform the following tasks.</span></span>

### <a name="undo-an-action-using-threat-explorer"></a><span data-ttu-id="e18ce-125">Annuler une action à l’aide de l’Explorateur de menaces</span><span class="sxs-lookup"><span data-stu-id="e18ce-125">Undo an action using Threat Explorer</span></span>

<span data-ttu-id="e18ce-126">Avec l’Explorateur de menaces, votre équipe des opérations de sécurité peut rechercher un message électronique affecté par une action et éventuellement annuler l’action.</span><span class="sxs-lookup"><span data-stu-id="e18ce-126">With Threat Explorer, your security operations team can find an email affected by an action and potentially undo the action.</span></span>

|<span data-ttu-id="e18ce-127">Scénario</span><span class="sxs-lookup"><span data-stu-id="e18ce-127">Scenario</span></span>|<span data-ttu-id="e18ce-128">Options d’annuler</span><span class="sxs-lookup"><span data-stu-id="e18ce-128">Undo Options</span></span>|<span data-ttu-id="e18ce-129">En savoir plus</span><span class="sxs-lookup"><span data-stu-id="e18ce-129">Learn more</span></span>|
|---|---|---|
|<span data-ttu-id="e18ce-130">Un message électronique a été acheminé vers le dossier Courrier indésirable d’un utilisateur</span><span class="sxs-lookup"><span data-stu-id="e18ce-130">An email message was routed to a user's Junk Email folder</span></span>|<span data-ttu-id="e18ce-131">- Déplacer le message vers le dossier Éléments supprimés de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="e18ce-131">- Move the message to the user's Deleted Items folder</span></span><br/><span data-ttu-id="e18ce-132">- Déplacer le message vers la boîte de réception de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="e18ce-132">- Move the message to the user's Inbox</span></span><br/><span data-ttu-id="e18ce-133">- Supprimer le message</span><span class="sxs-lookup"><span data-stu-id="e18ce-133">- Delete the message</span></span>|[<span data-ttu-id="e18ce-134">Rechercher et examiner les e-mails malveillants qui ont été remis dans Office 365</span><span class="sxs-lookup"><span data-stu-id="e18ce-134">Find and investigate malicious email that was delivered in Office 365</span></span>](investigate-malicious-email-that-was-delivered.md)|
|<span data-ttu-id="e18ce-135">Un message électronique ou un fichier a été mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="e18ce-135">An email message or a file was quarantined</span></span>|<span data-ttu-id="e18ce-136">- Libérer le courrier électronique ou le fichier</span><span class="sxs-lookup"><span data-stu-id="e18ce-136">- Release the email or file</span></span><br/><span data-ttu-id="e18ce-137">- Supprimer le courrier électronique ou le fichier</span><span class="sxs-lookup"><span data-stu-id="e18ce-137">- Delete the email or file</span></span>|[<span data-ttu-id="e18ce-138">Gérer les messages mis en quarantaine en tant qu’administrateur</span><span class="sxs-lookup"><span data-stu-id="e18ce-138">Manage quarantined messages as an admin</span></span>](manage-quarantined-messages-and-files.md)|
|

### <a name="undo-an-action-in-the-action-center"></a><span data-ttu-id="e18ce-139">Annuler une action dans le centre de données</span><span class="sxs-lookup"><span data-stu-id="e18ce-139">Undo an action in the Action center</span></span>

<span data-ttu-id="e18ce-140">Dans le centre de correction, vous pouvez voir les actions de correction qui ont été prises et éventuellement annuler l’action.</span><span class="sxs-lookup"><span data-stu-id="e18ce-140">In the Action center, you can see remediation actions that were taken and potentially undo the action.</span></span>

1. <span data-ttu-id="e18ce-141">Go to the Microsoft 365 security center ( <https://security.microsoft.com> ).</span><span class="sxs-lookup"><span data-stu-id="e18ce-141">Go to the Microsoft 365 security center (<https://security.microsoft.com>).</span></span>
2. <span data-ttu-id="e18ce-142">Dans le volet de navigation, sélectionnez **Centre de l’action.**</span><span class="sxs-lookup"><span data-stu-id="e18ce-142">In the navigation pane, select **Action center**.</span></span>
3. <span data-ttu-id="e18ce-143">Sélectionnez **l’onglet** Historique pour afficher la liste des actions terminées.</span><span class="sxs-lookup"><span data-stu-id="e18ce-143">Select the **History** tab to view the list of completed actions.</span></span>
4. <span data-ttu-id="e18ce-144">Sélectionnez un élément.</span><span class="sxs-lookup"><span data-stu-id="e18ce-144">Select an item.</span></span> <span data-ttu-id="e18ce-145">Son volet volant s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="e18ce-145">Its flyout pane opens.</span></span>
5. <span data-ttu-id="e18ce-146">Dans le volet volant, sélectionnez **Annuler.**</span><span class="sxs-lookup"><span data-stu-id="e18ce-146">In the flyout pane, select **Undo**.</span></span> <span data-ttu-id="e18ce-147">(Seules les actions qui peuvent être annulées auront **un bouton Annuler.)**</span><span class="sxs-lookup"><span data-stu-id="e18ce-147">(Only actions that can be undone will have an **Undo** button.)</span></span>

## <a name="see-also"></a><span data-ttu-id="e18ce-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e18ce-148">See also</span></span>

- [<span data-ttu-id="e18ce-149">Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="e18ce-149">Microsoft Defender for Office 365</span></span>](defender-for-office-365.md)
- [<span data-ttu-id="e18ce-150">Enquêtes automatisées dans Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="e18ce-150">Automated investigations in Microsoft Defender for Office 365</span></span>](office-365-air.md)
