---
title: Comment faire pour signaler les faux positifs ou les faux négatifs dans Office 365 automatisation de l’analyse et de la réponse
description: Un message a-t-il été manqué ou incorrectement détecté par Office 365 Advanced Threat Protection ? Découvrez comment soumettre des faux positifs ou faux négatifs à Microsoft pour analyse.
keywords: automatisation, analyse, alerte, déclencheur, action, correction, faux positif, faux négatif
search.appverid: met150
ms.prod: microsoft-365-enterprise
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: deniseb
author: denisebmsft
ms.date: 05/15/2020
ms.localizationpriority: medium
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
ms.topic: conceptual
ms.custom: autoir
ms.openlocfilehash: 2dd67af62a400f3e217f146e6d0ee213d74ad99a
ms.sourcegitcommit: 22e9f54d0d3ead2be91a38d49325308c70f43f90
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2020
ms.locfileid: "44262409"
---
# <a name="how-to-report-false-positivesnegatives-in-automated-investigation-and-response-capabilities"></a><span data-ttu-id="489d1-105">Comment signaler les faux positifs/négatifs dans les fonctionnalités d’analyse et de réponse automatisées</span><span class="sxs-lookup"><span data-stu-id="489d1-105">How to report false positives/negatives in automated investigation and response capabilities</span></span>

<span data-ttu-id="489d1-106">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="489d1-106">**Applies to:**</span></span>
- <span data-ttu-id="489d1-107">Office 365-Protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="489d1-107">Office 365 Advanced Threat Protection</span></span>

<span data-ttu-id="489d1-108">[Les fonctionnalités d’analyse et de réponse automatisées (air) d’Office 365](https://docs.microsoft.com/microsoft-365/security/office-365-security/automated-investigation-response-office) manquent ou détectent-elles mal ?</span><span class="sxs-lookup"><span data-stu-id="489d1-108">Did [automated investigation and response (AIR) capabilities in Office 365](https://docs.microsoft.com/microsoft-365/security/office-365-security/automated-investigation-response-office) miss or wrongly detect something?</span></span> <span data-ttu-id="489d1-109">Il existe des étapes que vous pouvez suivre pour résoudre ce problème.</span><span class="sxs-lookup"><span data-stu-id="489d1-109">There are steps you can take to fix it.</span></span> <span data-ttu-id="489d1-110">Vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="489d1-110">You can:</span></span>
- <span data-ttu-id="489d1-111">[Signaler un faux positif/négatif à Microsoft](#report-a-false-positivenegative-to-microsoft-for-analysis);</span><span class="sxs-lookup"><span data-stu-id="489d1-111">[Report a false positive/negative to Microsoft](#report-a-false-positivenegative-to-microsoft-for-analysis);</span></span>
- <span data-ttu-id="489d1-112">[Ajustez vos alertes (le](#adjust-an-alert-to-prevent-false-positives-from-recurring) cas échéant); les</span><span class="sxs-lookup"><span data-stu-id="489d1-112">[Adjust your alerts](#adjust-an-alert-to-prevent-false-positives-from-recurring) (if needed); and</span></span> 
- <span data-ttu-id="489d1-113">[Annuler les actions correctives qui ont été effectuées sur les appareils](#undo-a-remediation-action).</span><span class="sxs-lookup"><span data-stu-id="489d1-113">[Undo remediation actions that were taken on devices](#undo-a-remediation-action).</span></span> 

<span data-ttu-id="489d1-114">Utilisez cet article comme guide.</span><span class="sxs-lookup"><span data-stu-id="489d1-114">Use this article as a guide.</span></span> 

## <a name="report-a-false-positivenegative-to-microsoft-for-analysis"></a><span data-ttu-id="489d1-115">Signaler un faux positif/négatif à Microsoft pour analyse</span><span class="sxs-lookup"><span data-stu-id="489d1-115">Report a false positive/negative to Microsoft for analysis</span></span>

<span data-ttu-id="489d1-116">Si Office 365 AIR n’a pas manqué un message électronique, une pièce jointe de message électronique, une URL dans un message électronique ou une URL dans un fichier Office, vous pouvez [Envoyer des messages indésirables, hameçons, URL et fichiers suspects à Microsoft pour l’analyse d’office 365](https://docs.microsoft.com/microsoft-365/security/office-365-security/admin-submission).</span><span class="sxs-lookup"><span data-stu-id="489d1-116">If Office 365 AIR missed an email message, an email attachment, a URL in an email message, or a URL in an Office file, you can [submit suspected spam, phish, URLs, and files to Microsoft for Office 365 scanning](https://docs.microsoft.com/microsoft-365/security/office-365-security/admin-submission).</span></span>

<span data-ttu-id="489d1-117">Vous pouvez également [Envoyer un fichier à Microsoft pour analyse contre les programmes malveillants](https://www.microsoft.com/wdsi/filesubmission).</span><span class="sxs-lookup"><span data-stu-id="489d1-117">You can also [Submit a file to Microsoft for malware analysis](https://www.microsoft.com/wdsi/filesubmission).</span></span>

## <a name="adjust-an-alert-to-prevent-false-positives-from-recurring"></a><span data-ttu-id="489d1-118">Ajuster une alerte pour empêcher les faux positifs d’être périodiques</span><span class="sxs-lookup"><span data-stu-id="489d1-118">Adjust an alert to prevent false positives from recurring</span></span>

<span data-ttu-id="489d1-119">Si une alerte est déclenchée par une utilisation légitime ou si l’alerte est incorrecte, vous pouvez [gérer les alertes dans le portail de sécurité des applications Cloud](https://docs.microsoft.com/cloud-app-security/managing-alerts).</span><span class="sxs-lookup"><span data-stu-id="489d1-119">If an alert is triggered by legitimate use, or the alert is inaccurate, you can [Manage alerts in the Cloud App Security portal](https://docs.microsoft.com/cloud-app-security/managing-alerts).</span></span>

<span data-ttu-id="489d1-120">Si votre organisation utilise la [protection avancée contre les menaces Microsoft Defender](https://docs.microsoft.com/windows/security/threat-protection) en plus d’Office 365 et qu’un fichier, une adresse IP, une URL ou un domaine est traité comme un programme malveillant sur un appareil, même s’il est sûr, vous pouvez [créer un indicateur personnalisé avec une action « autoriser » pour votre appareil](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/manage-indicators).</span><span class="sxs-lookup"><span data-stu-id="489d1-120">If your organization is using [Microsoft Defender Advanced Threat Protection](https://docs.microsoft.com/windows/security/threat-protection) in addition to Office 365, and a file, IP address, URL, or domain is treated as malware on a device, even though it's safe, you can [create a custom indicator with an "Allow" action for your device](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/manage-indicators).</span></span>

## <a name="undo-a-remediation-action"></a><span data-ttu-id="489d1-121">Annuler une action de correction</span><span class="sxs-lookup"><span data-stu-id="489d1-121">Undo a remediation action</span></span>

<span data-ttu-id="489d1-122">Dans la plupart des cas, si une action de correction a été effectuée sur un message électronique, une pièce jointe de courrier électronique ou une URL, et que l’élément n’est pas une menace, votre équipe d’opérations de sécurité peut annuler l’action de correction et prendre des mesures pour empêcher le faux positif d’être périodique.</span><span class="sxs-lookup"><span data-stu-id="489d1-122">In most cases, if a remediation action was taken on an email message, email attachment, or URL, and the item is actually not a threat, your security operations team can undo the remediation action and take steps to prevent the false positive from recurring.</span></span> <span data-ttu-id="489d1-123">Vous pouvez utiliser l' [Explorateur de menaces](#undo-an-action-using-threat-explorer) ou l' [onglet actions pour effectuer une enquête](#undo-an-action-using-the-actions-tab-for-an-investigation) afin d’annuler une action.</span><span class="sxs-lookup"><span data-stu-id="489d1-123">You can either use [Threat Explorer](#undo-an-action-using-threat-explorer) or the [Actions tab for an investigation](#undo-an-action-using-the-actions-tab-for-an-investigation) to undo an action.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="489d1-124">Vérifiez que vous disposez des autorisations nécessaires avant d’effectuer les tâches suivantes.</span><span class="sxs-lookup"><span data-stu-id="489d1-124">Make sure you have the necessary permissions before attempting to perform the following tasks.</span></span>

### <a name="undo-an-action-using-threat-explorer"></a><span data-ttu-id="489d1-125">Annuler une action à l’aide de l’Explorateur de menaces</span><span class="sxs-lookup"><span data-stu-id="489d1-125">Undo an action using Threat Explorer</span></span>

<span data-ttu-id="489d1-126">Avec l’Explorateur de menaces, votre équipe des opérations de sécurité peut trouver un e-mail affecté par une action et éventuellement annuler l’action.</span><span class="sxs-lookup"><span data-stu-id="489d1-126">With Threat Explorer, your security operations team can find an email affected by an action and potentially undo the action.</span></span>

|<span data-ttu-id="489d1-127">Scénario</span><span class="sxs-lookup"><span data-stu-id="489d1-127">Scenario</span></span>  |<span data-ttu-id="489d1-128">Options d’annulation</span><span class="sxs-lookup"><span data-stu-id="489d1-128">Undo Options</span></span>  |<span data-ttu-id="489d1-129">En savoir plus</span><span class="sxs-lookup"><span data-stu-id="489d1-129">Learn more</span></span> |
|---------|---------|---------|
|<span data-ttu-id="489d1-130">Un message électronique a été acheminé vers le dossier de courrier indésirable d’un utilisateur</span><span class="sxs-lookup"><span data-stu-id="489d1-130">An email message was routed to a user's Junk Email folder</span></span>     |<span data-ttu-id="489d1-131">-Déplacer le message vers le dossier éléments supprimés de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="489d1-131">- Move the message to the user's Deleted Items folder</span></span><br/><span data-ttu-id="489d1-132">-Déplacer le message vers la boîte de réception de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="489d1-132">- Move the message to the user's Inbox</span></span> <br/><span data-ttu-id="489d1-133">-Supprimer le message</span><span class="sxs-lookup"><span data-stu-id="489d1-133">- Delete the message</span></span>          |[<span data-ttu-id="489d1-134">Rechercher et identifier les courriers électroniques malveillants remis dans Office 365</span><span class="sxs-lookup"><span data-stu-id="489d1-134">Find and investigate malicious email that was delivered in Office 365</span></span>](https://docs.microsoft.com/microsoft-365/security/office-365-security/investigate-malicious-email-that-was-delivered) |
|<span data-ttu-id="489d1-135">Un message électronique ou un fichier a été mis en quarantaine</span><span class="sxs-lookup"><span data-stu-id="489d1-135">An email message or a file was quarantined</span></span>     |<span data-ttu-id="489d1-136">-Libérer le courrier électronique ou le fichier</span><span class="sxs-lookup"><span data-stu-id="489d1-136">- Release the email or file</span></span> <br/><span data-ttu-id="489d1-137">-Supprimer le message électronique ou le fichier</span><span class="sxs-lookup"><span data-stu-id="489d1-137">- Delete the email or file</span></span>         |[<span data-ttu-id="489d1-138">Gestion des messages et des fichiers mis en quarantaine en tant qu’administrateur dans Office 365</span><span class="sxs-lookup"><span data-stu-id="489d1-138">Manage quarantined messages and files as an administrator in Office 365</span></span>](https://docs.microsoft.com/microsoft-365/security/office-365-security/manage-quarantined-messages-and-files) |


### <a name="undo-an-action-using-the-actions-tab-for-an-investigation"></a><span data-ttu-id="489d1-139">Annuler une action à l’aide de l’onglet actions pour une enquête</span><span class="sxs-lookup"><span data-stu-id="489d1-139">Undo an action using the Actions tab for an investigation</span></span>

<span data-ttu-id="489d1-140">Dans le centre de notifications, vous pouvez voir les actions de correction qui ont été prises et éventuellement annuler l’action.</span><span class="sxs-lookup"><span data-stu-id="489d1-140">In the Action center, you can see remediation actions that were taken and potentially undo the action.</span></span>

1. <span data-ttu-id="489d1-141">Accédez à [https://protection.office.com](https://protection.office.com) et connectez-vous.</span><span class="sxs-lookup"><span data-stu-id="489d1-141">Go to [https://protection.office.com](https://protection.office.com) and sign in.</span></span> <span data-ttu-id="489d1-142">Cette opération vous permet d’accéder au centre de sécurité & conformité.</span><span class="sxs-lookup"><span data-stu-id="489d1-142">This takes you to the the Security & Compliance Center.</span></span>

2. <span data-ttu-id="489d1-143">Accédez aux enquêtes de **gestion des menaces**  >  **Investigations**.</span><span class="sxs-lookup"><span data-stu-id="489d1-143">Go to **Threat management** > **Investigations**.</span></span>

3. <span data-ttu-id="489d1-144">Dans la liste des enquêtes, sélectionnez l’icône **ouvrir dans une nouvelle fenêtre** en regard de l’ID d’un élément.</span><span class="sxs-lookup"><span data-stu-id="489d1-144">In the list of investigations, select the **Open in new window** icon next to an item's ID.</span></span>

4. <span data-ttu-id="489d1-145">Sélectionnez l’onglet **actions** .</span><span class="sxs-lookup"><span data-stu-id="489d1-145">Select the **Actions** tab.</span></span>

5. <span data-ttu-id="489d1-146">Sélectionnez un élément dont le statut est **terminé**, puis recherchez un lien, tel que **approuvé**, dans la colonne **décision** .</span><span class="sxs-lookup"><span data-stu-id="489d1-146">Select an item that has status of **Completed**, and look for a link, such as **Approved**, in the **Decision** column.</span></span> <span data-ttu-id="489d1-147">Cette opération ouvre un menu volant avec plus de détails sur l’action.</span><span class="sxs-lookup"><span data-stu-id="489d1-147">This opens a flyout with more details about the action.</span></span>

6. <span data-ttu-id="489d1-148">Pour annuler l’action, sélectionnez **Supprimer la correction**.</span><span class="sxs-lookup"><span data-stu-id="489d1-148">To undo the action, select **Delete remediation**.</span></span>

## <a name="related-articles"></a><span data-ttu-id="489d1-149">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="489d1-149">Related articles</span></span>

[<span data-ttu-id="489d1-150">Protection avancée contre les menaces dans Office 365</span><span class="sxs-lookup"><span data-stu-id="489d1-150">Office 365 Advanced Threat Protection</span></span>](https://docs.microsoft.com/microsoft-365/security/office-365-security/office-365-atp)

[<span data-ttu-id="489d1-151">Prise en main de l’analyse et de la réponse automatisées (AIR) dans Office 365</span><span class="sxs-lookup"><span data-stu-id="489d1-151">Get started using Automated investigation and response (AIR) in Office 365</span></span>](office-365-air.md)