---
title: Gérer les faux positifs ou les faux négatifs dans l’AIR dans la protection contre les menaces Microsoft
description: Un message a-t-il été manqué ou incorrectement détecté par AIR dans la protection contre les menaces Microsoft ? Découvrez comment soumettre des faux positifs ou faux négatifs à Microsoft pour analyse.
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
ms.date: 09/16/2020
ms.localizationpriority: medium
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
ms.topic: conceptual
ms.custom: autoir
ms.reviewer: evaldm, isco
ms.openlocfilehash: 84d2a71f715c31560f6376464bf9da25cc8d58b1
ms.sourcegitcommit: c083602dda3cdcb5b58cb8aa070d77019075f765
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/22/2020
ms.locfileid: "48198630"
---
# <a name="handle-false-positivesnegatives-in-automated-investigation-and-response-capabilities"></a><span data-ttu-id="23ed7-105">Gérer les faux positifs/négatifs dans les fonctionnalités d’analyse et de réponse automatisées</span><span class="sxs-lookup"><span data-stu-id="23ed7-105">Handle false positives/negatives in automated investigation and response capabilities</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="23ed7-106">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="23ed7-106">**Applies to:**</span></span>
- <span data-ttu-id="23ed7-107">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="23ed7-107">Microsoft Threat Protection</span></span>

<span data-ttu-id="23ed7-108">La protection contre les menaces a-t-elle permis d’effectuer des [recherches et des réponses automatiques](mtp-autoir.md) dans Microsoft Threat Protection ?</span><span class="sxs-lookup"><span data-stu-id="23ed7-108">Did [automated investigation and response capabilities](mtp-autoir.md) in Microsoft Threat Protection miss or wrongly detect something?</span></span> <span data-ttu-id="23ed7-109">Il existe des étapes que vous pouvez suivre pour résoudre ce problème.</span><span class="sxs-lookup"><span data-stu-id="23ed7-109">There are steps you can take to fix it.</span></span> <span data-ttu-id="23ed7-110">Vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="23ed7-110">You can:</span></span>

- <span data-ttu-id="23ed7-111">[Signaler un faux positif/négatif à Microsoft](#report-a-false-positivenegative-to-microsoft-for-analysis);</span><span class="sxs-lookup"><span data-stu-id="23ed7-111">[Report a false positive/negative to Microsoft](#report-a-false-positivenegative-to-microsoft-for-analysis);</span></span>

- <span data-ttu-id="23ed7-112">[Ajustez vos alertes (le](#adjust-an-alert-to-prevent-false-positives-from-recurring) cas échéant); les</span><span class="sxs-lookup"><span data-stu-id="23ed7-112">[Adjust your alerts](#adjust-an-alert-to-prevent-false-positives-from-recurring) (if needed); and</span></span> 

- <span data-ttu-id="23ed7-113">[Annuler les actions correctives qui ont été effectuées sur les appareils](#undo-a-remediation-action-that-was-taken-on-a-device).</span><span class="sxs-lookup"><span data-stu-id="23ed7-113">[Undo remediation actions that were taken on devices](#undo-a-remediation-action-that-was-taken-on-a-device).</span></span> 

<span data-ttu-id="23ed7-114">Utilisez cet article comme guide.</span><span class="sxs-lookup"><span data-stu-id="23ed7-114">Use this article as a guide.</span></span> 

## <a name="report-a-false-positivenegative-to-microsoft-for-analysis"></a><span data-ttu-id="23ed7-115">Signaler un faux positif/négatif à Microsoft pour analyse</span><span class="sxs-lookup"><span data-stu-id="23ed7-115">Report a false positive/negative to Microsoft for analysis</span></span>

|<span data-ttu-id="23ed7-116">Élément manqué ou incorrectement détecté</span><span class="sxs-lookup"><span data-stu-id="23ed7-116">Item missed or wrongly detected</span></span> |<span data-ttu-id="23ed7-117">Service</span><span class="sxs-lookup"><span data-stu-id="23ed7-117">Service</span></span>  |<span data-ttu-id="23ed7-118">Procédure</span><span class="sxs-lookup"><span data-stu-id="23ed7-118">What to do</span></span>  |
|---------|---------|---------|
|<span data-ttu-id="23ed7-119">-Message électronique</span><span class="sxs-lookup"><span data-stu-id="23ed7-119">- Email message</span></span> <br/><span data-ttu-id="23ed7-120">-Pièce jointe de courrier électronique</span><span class="sxs-lookup"><span data-stu-id="23ed7-120">- Email attachment</span></span> <br/><span data-ttu-id="23ed7-121">-URL dans un message électronique</span><span class="sxs-lookup"><span data-stu-id="23ed7-121">- URL in an email message</span></span><br/><span data-ttu-id="23ed7-122">-URL dans un fichier Office</span><span class="sxs-lookup"><span data-stu-id="23ed7-122">- URL in an Office file</span></span>      |[<span data-ttu-id="23ed7-123">Protection avancée contre les menaces dans Office 365</span><span class="sxs-lookup"><span data-stu-id="23ed7-123">Office 365 Advanced Threat Protection</span></span>](https://docs.microsoft.com/microsoft-365/security/office-365-security/office-365-atp)        |[<span data-ttu-id="23ed7-124">Soumission de courrier indésirable, hameçon, URL et fichiers suspects à Microsoft pour analyse</span><span class="sxs-lookup"><span data-stu-id="23ed7-124">Submit suspected spam, phish, URLs, and files to Microsoft for scanning</span></span>](https://docs.microsoft.com/microsoft-365/security/office-365-security/admin-submission)         |
|<span data-ttu-id="23ed7-125">Fichier ou application sur un appareil</span><span class="sxs-lookup"><span data-stu-id="23ed7-125">File or app on a device</span></span>    |[<span data-ttu-id="23ed7-126">Microsoft Defender – Protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="23ed7-126">Microsoft Defender Advanced Threat Protection</span></span>](https://docs.microsoft.com/windows/security/threat-protection)         |[<span data-ttu-id="23ed7-127">Envoi d’un fichier à Microsoft pour l’analyse des programmes malveillants</span><span class="sxs-lookup"><span data-stu-id="23ed7-127">Submit a file to Microsoft for malware analysis</span></span>](https://www.microsoft.com/wdsi/filesubmission)         |

## <a name="adjust-an-alert-to-prevent-false-positives-from-recurring"></a><span data-ttu-id="23ed7-128">Ajuster une alerte pour empêcher les faux positifs d’être périodiques</span><span class="sxs-lookup"><span data-stu-id="23ed7-128">Adjust an alert to prevent false positives from recurring</span></span>

|<span data-ttu-id="23ed7-129">Scénario</span><span class="sxs-lookup"><span data-stu-id="23ed7-129">Scenario</span></span> |<span data-ttu-id="23ed7-130">Service</span><span class="sxs-lookup"><span data-stu-id="23ed7-130">Service</span></span> |<span data-ttu-id="23ed7-131">Procédure</span><span class="sxs-lookup"><span data-stu-id="23ed7-131">What to do</span></span> |
|--------|--------|--------|
|<span data-ttu-id="23ed7-132">-Une alerte est déclenchée par une utilisation légitime</span><span class="sxs-lookup"><span data-stu-id="23ed7-132">- An alert is triggered by legitimate use</span></span> <br/><span data-ttu-id="23ed7-133">-Une alerte est incorrecte</span><span class="sxs-lookup"><span data-stu-id="23ed7-133">- An alert is inaccurate</span></span>    |[<span data-ttu-id="23ed7-134">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="23ed7-134">Microsoft Cloud App Security</span></span>](https://docs.microsoft.com/cloud-app-security)<br/> <span data-ttu-id="23ed7-135">ou</span><span class="sxs-lookup"><span data-stu-id="23ed7-135">or</span></span> <br/>[<span data-ttu-id="23ed7-136">Détection de menaces avancées Azure</span><span class="sxs-lookup"><span data-stu-id="23ed7-136">Azure Advanced Threat Detection</span></span>](https://docs.microsoft.com/azure/security/fundamentals/threat-detection)         |[<span data-ttu-id="23ed7-137">Gérer les alertes dans le portail de sécurité des applications Cloud</span><span class="sxs-lookup"><span data-stu-id="23ed7-137">Manage alerts in the Cloud App Security portal</span></span>](https://docs.microsoft.com/cloud-app-security/managing-alerts)         |
|<span data-ttu-id="23ed7-138">Un fichier, une adresse IP, une URL ou un domaine est traité comme un programme malveillant sur un appareil, même s’il est sûr.</span><span class="sxs-lookup"><span data-stu-id="23ed7-138">A file, IP address, URL, or domain is treated as malware on a device, even though it's safe</span></span>|[<span data-ttu-id="23ed7-139">Microsoft Defender – Protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="23ed7-139">Microsoft Defender Advanced Threat Protection</span></span>](https://docs.microsoft.com/windows/security/threat-protection) |[<span data-ttu-id="23ed7-140">Créer un indicateur personnalisé avec une action « autoriser »</span><span class="sxs-lookup"><span data-stu-id="23ed7-140">Create a custom indicator with an "Allow" action</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/manage-indicators) |


## <a name="undo-a-remediation-action-that-was-taken-on-a-device"></a><span data-ttu-id="23ed7-141">Annuler une action de correction effectuée sur un appareil</span><span class="sxs-lookup"><span data-stu-id="23ed7-141">Undo a remediation action that was taken on a device</span></span>

<span data-ttu-id="23ed7-142">Si une action de correction a été effectuée sur un appareil (par exemple, un appareil Windows 10) et que l’élément n’est pas une menace, votre équipe d’opérations de sécurité peut annuler l’action de correction dans le [Centre de maintenance](mtp-action-center.md).</span><span class="sxs-lookup"><span data-stu-id="23ed7-142">If a remediation action was taken on a device (such as a Windows 10 device) and the item is actually not a threat, your security operations team can undo the remediation action in the [Action center](mtp-action-center.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="23ed7-143">Vérifiez que vous disposez des [autorisations nécessaires](mtp-action-center.md#required-permissions-for-action-center-tasks) avant d’effectuer la tâche suivante.</span><span class="sxs-lookup"><span data-stu-id="23ed7-143">Make sure you have the [necessary permissions](mtp-action-center.md#required-permissions-for-action-center-tasks) before attempting to perform the following task.</span></span>

1. <span data-ttu-id="23ed7-144">Accédez à [https://security.microsoft.com](https://security.microsoft.com) et connectez-vous.</span><span class="sxs-lookup"><span data-stu-id="23ed7-144">Go to [https://security.microsoft.com](https://security.microsoft.com) and sign in.</span></span> 

2. <span data-ttu-id="23ed7-145">Dans le volet de navigation, choisissez **Centre de notifications**.</span><span class="sxs-lookup"><span data-stu-id="23ed7-145">In the navigation pane, choose **Action center**.</span></span> 

3. <span data-ttu-id="23ed7-146">Sous l’onglet **historique** , sélectionnez une action que vous souhaitez annuler.</span><span class="sxs-lookup"><span data-stu-id="23ed7-146">On the **History** tab, select an action that you want to undo.</span></span> <span data-ttu-id="23ed7-147">Une fenêtre volante s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="23ed7-147">This opens a flyout.</span></span><br/>
    > [!TIP]
    > <span data-ttu-id="23ed7-148">Utilisez des filtres pour limiter la liste des résultats.</span><span class="sxs-lookup"><span data-stu-id="23ed7-148">Use filters to narrow down the list of results.</span></span> 

4. <span data-ttu-id="23ed7-149">Dans le menu volant de l’élément sélectionné, sélectionnez **ouvrir la page d’enquête**.</span><span class="sxs-lookup"><span data-stu-id="23ed7-149">In the flyout for the selected item, select **Open investigation page**.</span></span>

5. <span data-ttu-id="23ed7-150">Dans la vue Détails de l’enquête, sélectionnez l’onglet **actions** .</span><span class="sxs-lookup"><span data-stu-id="23ed7-150">In the investigation details view, select the **Actions** tab.</span></span>

6. <span data-ttu-id="23ed7-151">Sélectionnez un élément dont le statut est **terminé**, puis recherchez un lien, tel que **approuvé**, dans la colonne **décisions** .</span><span class="sxs-lookup"><span data-stu-id="23ed7-151">Select an item that has status of **Completed**, and look for a link, such as **Approved**, in the **Decisions** column.</span></span> <span data-ttu-id="23ed7-152">Cette opération ouvre un menu volant avec plus de détails sur l’action.</span><span class="sxs-lookup"><span data-stu-id="23ed7-152">This opens a flyout with more details about the action.</span></span>

7. <span data-ttu-id="23ed7-153">Pour annuler l’action, sélectionnez **Supprimer la correction**.</span><span class="sxs-lookup"><span data-stu-id="23ed7-153">To undo the action, select **Delete remediation**.</span></span>

## <a name="see-also"></a><span data-ttu-id="23ed7-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="23ed7-154">See also</span></span>

- [<span data-ttu-id="23ed7-155">Consulter les détails et les résultats d'un examen automatisé</span><span class="sxs-lookup"><span data-stu-id="23ed7-155">View the details and results of an automated investigation</span></span>](mtp-autoir-results.md)
- [<span data-ttu-id="23ed7-156">Repérage proactive de menaces avec repérage avancé dans la Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="23ed7-156">Proactively hunt for threats with advanced hunting in Microsoft Threat Protection</span></span>](advanced-hunting-overview.md)
