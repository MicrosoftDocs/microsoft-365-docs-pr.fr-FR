---
title: Gérer les faux positifs ou les faux négatifs dans AIR dans Microsoft 365 Defender
description: Un problème a-t-il été manqué ou détecté à tort par AIR dans Microsoft 365 Defender ? Découvrez comment soumettre des faux positifs ou des faux négatifs à Microsoft pour analyse.
keywords: automatisé, examen, alerte, déclencheur, action, correction, faux positif, faux négatif
search.appverid: met150
ms.prod: m365-security
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
- m365initiative-m365-defender
ms.topic: conceptual
ms.custom: autoir
ms.reviewer: evaldm, isco
ms.technology: m365d
ms.openlocfilehash: dbef240e28258d1ac4000c05538d0ce073a9d910
ms.sourcegitcommit: 855719ee21017cf87dfa98cbe62806763bcb78ac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/22/2021
ms.locfileid: "49930353"
---
# <a name="handle-false-positivesnegatives-in-automated-investigation-and-response-capabilities"></a><span data-ttu-id="63fd0-105">Gérer les faux positifs/négatifs dans les fonctionnalités automatisées d’examen et de réponse</span><span class="sxs-lookup"><span data-stu-id="63fd0-105">Handle false positives/negatives in automated investigation and response capabilities</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="63fd0-106">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="63fd0-106">**Applies to:**</span></span>
- <span data-ttu-id="63fd0-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="63fd0-107">Microsoft 365 Defender</span></span>

<span data-ttu-id="63fd0-108">Les [fonctionnalités d’investigation](mtp-autoir.md) et de réponse automatisées dans Microsoft 365 Defender ont-elle manqué ou détecté un problème ?</span><span class="sxs-lookup"><span data-stu-id="63fd0-108">Did [automated investigation and response capabilities](mtp-autoir.md) in Microsoft 365 Defender miss or wrongly detect something?</span></span> <span data-ttu-id="63fd0-109">Vous pouvez suivre certaines étapes pour y remédier.</span><span class="sxs-lookup"><span data-stu-id="63fd0-109">There are steps you can take to fix it.</span></span> <span data-ttu-id="63fd0-110">Vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="63fd0-110">You can:</span></span>

- <span data-ttu-id="63fd0-111">[Signaler un faux positif/négatif à Microsoft](#report-a-false-positivenegative-to-microsoft-for-analysis);</span><span class="sxs-lookup"><span data-stu-id="63fd0-111">[Report a false positive/negative to Microsoft](#report-a-false-positivenegative-to-microsoft-for-analysis);</span></span>

- <span data-ttu-id="63fd0-112">[Ajuster vos alertes](#adjust-an-alert-to-prevent-false-positives-from-recurring) (si nécessaire) ; et</span><span class="sxs-lookup"><span data-stu-id="63fd0-112">[Adjust your alerts](#adjust-an-alert-to-prevent-false-positives-from-recurring) (if needed); and</span></span> 

- <span data-ttu-id="63fd0-113">[Annuler les actions de correction qui ont été prises sur les appareils.](#undo-a-remediation-action-that-was-taken-on-a-device)</span><span class="sxs-lookup"><span data-stu-id="63fd0-113">[Undo remediation actions that were taken on devices](#undo-a-remediation-action-that-was-taken-on-a-device).</span></span> 

<span data-ttu-id="63fd0-114">Utilisez cet article comme guide.</span><span class="sxs-lookup"><span data-stu-id="63fd0-114">Use this article as a guide.</span></span> 

## <a name="report-a-false-positivenegative-to-microsoft-for-analysis"></a><span data-ttu-id="63fd0-115">Signaler un faux positif/négatif à Microsoft pour analyse</span><span class="sxs-lookup"><span data-stu-id="63fd0-115">Report a false positive/negative to Microsoft for analysis</span></span>

|<span data-ttu-id="63fd0-116">Élément manqué ou détecté de manière erronée</span><span class="sxs-lookup"><span data-stu-id="63fd0-116">Item missed or wrongly detected</span></span> |<span data-ttu-id="63fd0-117">Service</span><span class="sxs-lookup"><span data-stu-id="63fd0-117">Service</span></span>  |<span data-ttu-id="63fd0-118">Procédure</span><span class="sxs-lookup"><span data-stu-id="63fd0-118">What to do</span></span>  |
|---------|---------|---------|
|<span data-ttu-id="63fd0-119">- Message électronique</span><span class="sxs-lookup"><span data-stu-id="63fd0-119">- Email message</span></span> <br/><span data-ttu-id="63fd0-120">- Pièce jointe d’un e-mail</span><span class="sxs-lookup"><span data-stu-id="63fd0-120">- Email attachment</span></span> <br/><span data-ttu-id="63fd0-121">- URL dans un message électronique</span><span class="sxs-lookup"><span data-stu-id="63fd0-121">- URL in an email message</span></span><br/><span data-ttu-id="63fd0-122">- URL dans un fichier Office</span><span class="sxs-lookup"><span data-stu-id="63fd0-122">- URL in an Office file</span></span>      |[<span data-ttu-id="63fd0-123">Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="63fd0-123">Microsoft Defender for Office 365</span></span>](https://docs.microsoft.com/microsoft-365/security/office-365-security/office-365-atp)        |[<span data-ttu-id="63fd0-124">Soumettre des messages suspects de courrier indésirable, d’hameçonnage, d’URL et de fichiers à Microsoft pour analyse</span><span class="sxs-lookup"><span data-stu-id="63fd0-124">Submit suspected spam, phish, URLs, and files to Microsoft for scanning</span></span>](https://docs.microsoft.com/microsoft-365/security/office-365-security/admin-submission)         |
|<span data-ttu-id="63fd0-125">Fichier ou application sur un appareil</span><span class="sxs-lookup"><span data-stu-id="63fd0-125">File or app on a device</span></span>    |[<span data-ttu-id="63fd0-126">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="63fd0-126">Microsoft Defender for Endpoint</span></span>](https://docs.microsoft.com/windows/security/threat-protection)         |[<span data-ttu-id="63fd0-127">Envoyer un fichier à Microsoft pour analyse des programmes malveillants</span><span class="sxs-lookup"><span data-stu-id="63fd0-127">Submit a file to Microsoft for malware analysis</span></span>](https://www.microsoft.com/wdsi/filesubmission)         |

## <a name="adjust-an-alert-to-prevent-false-positives-from-recurring"></a><span data-ttu-id="63fd0-128">Ajuster une alerte pour éviter que les faux positifs ne se répètent</span><span class="sxs-lookup"><span data-stu-id="63fd0-128">Adjust an alert to prevent false positives from recurring</span></span>

|<span data-ttu-id="63fd0-129">Scénario</span><span class="sxs-lookup"><span data-stu-id="63fd0-129">Scenario</span></span> |<span data-ttu-id="63fd0-130">Service</span><span class="sxs-lookup"><span data-stu-id="63fd0-130">Service</span></span> |<span data-ttu-id="63fd0-131">Procédure</span><span class="sxs-lookup"><span data-stu-id="63fd0-131">What to do</span></span> |
|--------|--------|--------|
|<span data-ttu-id="63fd0-132">- Une alerte est déclenchée par un usage légitime</span><span class="sxs-lookup"><span data-stu-id="63fd0-132">- An alert is triggered by legitimate use</span></span> <br/><span data-ttu-id="63fd0-133">- Une alerte est inexacte</span><span class="sxs-lookup"><span data-stu-id="63fd0-133">- An alert is inaccurate</span></span>    |[<span data-ttu-id="63fd0-134">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="63fd0-134">Microsoft Cloud App Security</span></span>](https://docs.microsoft.com/cloud-app-security)<br/> <span data-ttu-id="63fd0-135">ou</span><span class="sxs-lookup"><span data-stu-id="63fd0-135">or</span></span> <br/>[<span data-ttu-id="63fd0-136">Azure Advanced Threat Detection</span><span class="sxs-lookup"><span data-stu-id="63fd0-136">Azure Advanced Threat Detection</span></span>](https://docs.microsoft.com/azure/security/fundamentals/threat-detection)         |[<span data-ttu-id="63fd0-137">Gérer les alertes dans le portail Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="63fd0-137">Manage alerts in the Cloud App Security portal</span></span>](https://docs.microsoft.com/cloud-app-security/managing-alerts)         |
|<span data-ttu-id="63fd0-138">Un fichier, une adresse IP, une URL ou un domaine est traité comme un programme malveillant sur un appareil, même s’il est sécurisé</span><span class="sxs-lookup"><span data-stu-id="63fd0-138">A file, IP address, URL, or domain is treated as malware on a device, even though it's safe</span></span>|[<span data-ttu-id="63fd0-139">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="63fd0-139">Microsoft Defender for Endpoint</span></span>](https://docs.microsoft.com/windows/security/threat-protection) |[<span data-ttu-id="63fd0-140">Créer un indicateur personnalisé avec une action « Autoriser »</span><span class="sxs-lookup"><span data-stu-id="63fd0-140">Create a custom indicator with an "Allow" action</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/manage-indicators) |


## <a name="undo-a-remediation-action-that-was-taken-on-a-device"></a><span data-ttu-id="63fd0-141">Annuler une action de correction qui a été prise sur un appareil</span><span class="sxs-lookup"><span data-stu-id="63fd0-141">Undo a remediation action that was taken on a device</span></span>

<span data-ttu-id="63fd0-142">Si une action de correction a été entreprise sur un appareil (tel qu’un appareil Windows 10) et que l’élément n’est pas une menace, votre équipe des opérations de sécurité peut annuler l’action de correction dans le centre de [correction.](mtp-action-center.md)</span><span class="sxs-lookup"><span data-stu-id="63fd0-142">If a remediation action was taken on a device (such as a Windows 10 device) and the item is actually not a threat, your security operations team can undo the remediation action in the [Action center](mtp-action-center.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="63fd0-143">Assurez-vous que vous avez les [autorisations nécessaires](mtp-action-center.md#required-permissions-for-action-center-tasks) avant d’essayer d’effectuer la tâche suivante.</span><span class="sxs-lookup"><span data-stu-id="63fd0-143">Make sure you have the [necessary permissions](mtp-action-center.md#required-permissions-for-action-center-tasks) before attempting to perform the following task.</span></span>

1. <span data-ttu-id="63fd0-144">Accédez à [https://security.microsoft.com](https://security.microsoft.com) et connectez-vous.</span><span class="sxs-lookup"><span data-stu-id="63fd0-144">Go to [https://security.microsoft.com](https://security.microsoft.com) and sign in.</span></span> 

2. <span data-ttu-id="63fd0-145">Dans le volet de navigation, choisissez **Centre de notifications**.</span><span class="sxs-lookup"><span data-stu-id="63fd0-145">In the navigation pane, choose **Action center**.</span></span> 

3. <span data-ttu-id="63fd0-146">Sous **l’onglet** Historique, sélectionnez une action à annuler.</span><span class="sxs-lookup"><span data-stu-id="63fd0-146">On the **History** tab, select an action that you want to undo.</span></span> <span data-ttu-id="63fd0-147">Cela ouvre un volant.</span><span class="sxs-lookup"><span data-stu-id="63fd0-147">This opens a flyout.</span></span><br/>
    > [!TIP]
    > <span data-ttu-id="63fd0-148">Utilisez des filtres pour affiner la liste des résultats.</span><span class="sxs-lookup"><span data-stu-id="63fd0-148">Use filters to narrow down the list of results.</span></span> 

4. <span data-ttu-id="63fd0-149">Dans le volant de l’élément sélectionné, sélectionnez **Ouvrir la page Ouvrir l’examen.**</span><span class="sxs-lookup"><span data-stu-id="63fd0-149">In the flyout for the selected item, select **Open investigation page**.</span></span>

5. <span data-ttu-id="63fd0-150">Dans l’affichage Détails de l’examen, sélectionnez **l’onglet Actions.**</span><span class="sxs-lookup"><span data-stu-id="63fd0-150">In the investigation details view, select the **Actions** tab.</span></span>

6. <span data-ttu-id="63fd0-151">Sélectionnez un élément dont l’état est **Terminé** et recherchez un lien, tel que **Approuvé,** dans la colonne **Décisions.**</span><span class="sxs-lookup"><span data-stu-id="63fd0-151">Select an item that has status of **Completed**, and look for a link, such as **Approved**, in the **Decisions** column.</span></span> <span data-ttu-id="63fd0-152">Cela ouvre un volant avec plus de détails sur l’action.</span><span class="sxs-lookup"><span data-stu-id="63fd0-152">This opens a flyout with more details about the action.</span></span>

7. <span data-ttu-id="63fd0-153">Pour annuler l’action, sélectionnez **Supprimer la correction.**</span><span class="sxs-lookup"><span data-stu-id="63fd0-153">To undo the action, select **Delete remediation**.</span></span>

## <a name="see-also"></a><span data-ttu-id="63fd0-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63fd0-154">See also</span></span>

- [<span data-ttu-id="63fd0-155">Consulter les détails et les résultats d'un examen automatisé</span><span class="sxs-lookup"><span data-stu-id="63fd0-155">View the details and results of an automated investigation</span></span>](mtp-autoir-results.md)
- [<span data-ttu-id="63fd0-156">Recherche proactive des menaces avec le hunting avancé dans Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="63fd0-156">Proactively hunt for threats with advanced hunting in Microsoft 365 Defender</span></span>](advanced-hunting-overview.md)
