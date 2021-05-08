---
title: Corriger les faux positifs ou les faux négatifs dans Microsoft 365 Defender
description: Un problème a-t-il été manqué ou détecté à tort par AIR dans Microsoft 365 Defender ? Découvrez comment soumettre des faux positifs ou des faux négatifs à Microsoft pour analyse.
keywords: automatisé, examen, alerte, correction, faux positif, faux négatif
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: josephd
author: JoeDavies-MSFT
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
- m365initiative-m365-defender
ms.topic: how-to
ms.custom: autoir
ms.reviewer: evaldm, isco
ms.technology: m365d
ms.openlocfilehash: 3cffa97d26b2b28de8d9e45d7030e0931a7ba072
ms.sourcegitcommit: 51b316c23e070ab402a687f927e8fa01cb719c74
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2021
ms.locfileid: "52269576"
---
# <a name="address-false-positives-or-false-negatives-in-microsoft-365-defender"></a><span data-ttu-id="5aa39-105">Corriger les faux positifs ou les faux négatifs dans Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="5aa39-105">Address false positives or false negatives in Microsoft 365 Defender</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

<span data-ttu-id="5aa39-106">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="5aa39-106">**Applies to:**</span></span>
- <span data-ttu-id="5aa39-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="5aa39-107">Microsoft 365 Defender</span></span>

<span data-ttu-id="5aa39-108">Les faux positifs ou négatifs peuvent parfois se produire avec n’importe quelle solution de protection contre les menaces.</span><span class="sxs-lookup"><span data-stu-id="5aa39-108">False positives or negatives can occasionally occur with any threat protection solution.</span></span> <span data-ttu-id="5aa39-109">Si [des fonctionnalités](m365d-autoir.md) automatisées d’examen et de réponse dans Microsoft 365 Defender ont manqué ou détecté un problème, votre équipe des opérations de sécurité peut suivre les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="5aa39-109">If [automated investigation and response capabilities](m365d-autoir.md) in Microsoft 365 Defender missed or wrongly detected something, there are steps your security operations team can take:</span></span>

- [<span data-ttu-id="5aa39-110">Signaler un faux positif/négatif à Microsoft</span><span class="sxs-lookup"><span data-stu-id="5aa39-110">Report a false positive/negative to Microsoft</span></span>](#report-a-false-positivenegative-to-microsoft-for-analysis)
- <span data-ttu-id="5aa39-111">[Ajuster vos alertes](#adjust-an-alert-to-prevent-false-positives-from-recurring) (si nécessaire)</span><span class="sxs-lookup"><span data-stu-id="5aa39-111">[Adjust your alerts](#adjust-an-alert-to-prevent-false-positives-from-recurring) (if needed)</span></span>
- [<span data-ttu-id="5aa39-112">Annuler les actions de correction qui ont été prises sur les appareils</span><span class="sxs-lookup"><span data-stu-id="5aa39-112">Undo remediation actions that were taken on devices</span></span>](#undo-a-remediation-action-that-was-taken-on-a-device)

<span data-ttu-id="5aa39-113">Les sections suivantes décrivent comment effectuer ces tâches.</span><span class="sxs-lookup"><span data-stu-id="5aa39-113">The following sections describe how to perform these tasks.</span></span>

## <a name="report-a-false-positivenegative-to-microsoft-for-analysis"></a><span data-ttu-id="5aa39-114">Signaler un faux positif/négatif à Microsoft pour analyse</span><span class="sxs-lookup"><span data-stu-id="5aa39-114">Report a false positive/negative to Microsoft for analysis</span></span>

|<span data-ttu-id="5aa39-115">Élément manqué ou détecté de manière erronée</span><span class="sxs-lookup"><span data-stu-id="5aa39-115">Item missed or wrongly detected</span></span> |<span data-ttu-id="5aa39-116">Service</span><span class="sxs-lookup"><span data-stu-id="5aa39-116">Service</span></span>  |<span data-ttu-id="5aa39-117">Procédure</span><span class="sxs-lookup"><span data-stu-id="5aa39-117">What to do</span></span>  |
|---------|---------|---------|
|<span data-ttu-id="5aa39-118">- Message électronique</span><span class="sxs-lookup"><span data-stu-id="5aa39-118">- Email message</span></span> <br/><span data-ttu-id="5aa39-119">- Pièce jointe d’un e-mail</span><span class="sxs-lookup"><span data-stu-id="5aa39-119">- Email attachment</span></span> <br/><span data-ttu-id="5aa39-120">- URL dans un message électronique</span><span class="sxs-lookup"><span data-stu-id="5aa39-120">- URL in an email message</span></span><br/><span data-ttu-id="5aa39-121">- URL dans un fichier Office</span><span class="sxs-lookup"><span data-stu-id="5aa39-121">- URL in an Office file</span></span>      |[<span data-ttu-id="5aa39-122">Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="5aa39-122">Microsoft Defender for Office 365</span></span>](/microsoft-365/security/office-365-security/defender-for-office-365)        |[<span data-ttu-id="5aa39-123">Soumettre des messages suspects de courrier indésirable, d’hameçonnage, d’URL et de fichiers à Microsoft pour analyse</span><span class="sxs-lookup"><span data-stu-id="5aa39-123">Submit suspected spam, phish, URLs, and files to Microsoft for scanning</span></span>](../office-365-security/admin-submission.md)         |
|<span data-ttu-id="5aa39-124">Fichier ou application sur un appareil</span><span class="sxs-lookup"><span data-stu-id="5aa39-124">File or app on a device</span></span>    |[<span data-ttu-id="5aa39-125">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="5aa39-125">Microsoft Defender for Endpoint</span></span>](/windows/security/threat-protection)         |[<span data-ttu-id="5aa39-126">Envoyer un fichier à Microsoft pour analyse des programmes malveillants</span><span class="sxs-lookup"><span data-stu-id="5aa39-126">Submit a file to Microsoft for malware analysis</span></span>](https://www.microsoft.com/wdsi/filesubmission)         |

## <a name="adjust-an-alert-to-prevent-false-positives-from-recurring"></a><span data-ttu-id="5aa39-127">Ajuster une alerte pour éviter que les faux positifs ne se répètent</span><span class="sxs-lookup"><span data-stu-id="5aa39-127">Adjust an alert to prevent false positives from recurring</span></span>

|<span data-ttu-id="5aa39-128">Scénario</span><span class="sxs-lookup"><span data-stu-id="5aa39-128">Scenario</span></span> |<span data-ttu-id="5aa39-129">Service</span><span class="sxs-lookup"><span data-stu-id="5aa39-129">Service</span></span> |<span data-ttu-id="5aa39-130">Procédure</span><span class="sxs-lookup"><span data-stu-id="5aa39-130">What to do</span></span> |
|--------|--------|--------|
|<span data-ttu-id="5aa39-131">- Une alerte est déclenchée par un usage légitime</span><span class="sxs-lookup"><span data-stu-id="5aa39-131">- An alert is triggered by legitimate use</span></span> <br/><span data-ttu-id="5aa39-132">- Une alerte est inexacte</span><span class="sxs-lookup"><span data-stu-id="5aa39-132">- An alert is inaccurate</span></span>    |[<span data-ttu-id="5aa39-133">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="5aa39-133">Microsoft Cloud App Security</span></span>](/cloud-app-security)<br/> <span data-ttu-id="5aa39-134">ou</span><span class="sxs-lookup"><span data-stu-id="5aa39-134">or</span></span> <br/>[<span data-ttu-id="5aa39-135">Protection Azure contre les menaces</span><span class="sxs-lookup"><span data-stu-id="5aa39-135">Azure threat protection</span></span>](/azure/security/fundamentals/threat-detection)         |[<span data-ttu-id="5aa39-136">Gérer les alertes dans le portail Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="5aa39-136">Manage alerts in the Cloud App Security portal</span></span>](/cloud-app-security/managing-alerts)         |
|<span data-ttu-id="5aa39-137">Un fichier, une adresse IP, une URL ou un domaine est traité comme un programme malveillant sur un appareil, même s’il est sécurisé</span><span class="sxs-lookup"><span data-stu-id="5aa39-137">A file, IP address, URL, or domain is treated as malware on a device, even though it's safe</span></span>|[<span data-ttu-id="5aa39-138">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="5aa39-138">Microsoft Defender for Endpoint</span></span>](/windows/security/threat-protection) |[<span data-ttu-id="5aa39-139">Créer un indicateur personnalisé avec une action « Autoriser »</span><span class="sxs-lookup"><span data-stu-id="5aa39-139">Create a custom indicator with an "Allow" action</span></span>](/windows/security/threat-protection/microsoft-defender-atp/manage-indicators) |

## <a name="undo-a-remediation-action-that-was-taken-on-a-device"></a><span data-ttu-id="5aa39-140">Annuler une action de correction qui a été prise sur un appareil</span><span class="sxs-lookup"><span data-stu-id="5aa39-140">Undo a remediation action that was taken on a device</span></span>

<span data-ttu-id="5aa39-141">Si une action de correction a été entreprise sur une entité (par exemple, un appareil ou un message électronique) et que l’entité concernée n’est pas réellement une menace, votre équipe des opérations de sécurité peut annuler l’action de correction dans le centre de [correction.](m365d-action-center.md)</span><span class="sxs-lookup"><span data-stu-id="5aa39-141">If a remediation action was taken on an entity (such as a device or an email message) and the affected entity is not actually a threat, your security operations team can undo the remediation action in the [Action center](m365d-action-center.md).</span></span>

1. <span data-ttu-id="5aa39-142">Accédez à [https://security.microsoft.com](https://security.microsoft.com) et connectez-vous.</span><span class="sxs-lookup"><span data-stu-id="5aa39-142">Go to [https://security.microsoft.com](https://security.microsoft.com) and sign in.</span></span> 
2. <span data-ttu-id="5aa39-143">Dans le volet de navigation, choisissez **Centre de notifications**.</span><span class="sxs-lookup"><span data-stu-id="5aa39-143">In the navigation pane, choose **Action center**.</span></span> 
3. <span data-ttu-id="5aa39-144">Sous **l’onglet** Historique, sélectionnez une action à annuler.</span><span class="sxs-lookup"><span data-stu-id="5aa39-144">On the **History** tab, select an action that you want to undo.</span></span> <span data-ttu-id="5aa39-145">Son volet volant s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="5aa39-145">Its flyout pane opens.</span></span>
4. <span data-ttu-id="5aa39-146">Dans le volet volant, sélectionnez **Annuler.**</span><span class="sxs-lookup"><span data-stu-id="5aa39-146">In the flyout pane, select **Undo**.</span></span>

> [!TIP]
> <span data-ttu-id="5aa39-147">Voir [Annuler les actions terminées.](m365d-autoir-actions.md#undo-completed-actions)</span><span class="sxs-lookup"><span data-stu-id="5aa39-147">See [Undo completed actions](m365d-autoir-actions.md#undo-completed-actions).</span></span>

## <a name="see-also"></a><span data-ttu-id="5aa39-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5aa39-148">See also</span></span>

- [<span data-ttu-id="5aa39-149">Consulter les détails et les résultats d'un examen automatisé</span><span class="sxs-lookup"><span data-stu-id="5aa39-149">View the details and results of an automated investigation</span></span>](m365d-autoir-results.md)
- [<span data-ttu-id="5aa39-150">Recherche proactive des menaces avec le hunting avancé dans Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="5aa39-150">Proactively hunt for threats with advanced hunting in Microsoft 365 Defender</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="5aa39-151">Résoudre des faux négatifs/positifs dans Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="5aa39-151">Address false positives/negatives in Microsoft Defender for Endpoint</span></span>](/windows/security/threat-protection/microsoft-defender-atp/defender-endpoint-false-positives-negatives)