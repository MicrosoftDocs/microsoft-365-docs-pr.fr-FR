---
title: Actions de correction suite à des enquêtes automatisées dans Microsoft Threat Protection
description: Obtenir une vue d’ensemble des actions de correction qui suivent des enquêtes automatisées dans Microsoft Threat Protection
keywords: automatisation, examen, alerte, déclencheur, action, correction
search.appverid: met150
ms.prod: microsoft-365-enterprise
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: deniseb
author: denisebmsft
ms.localizationpriority: medium
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
ms.topic: conceptual
ms.custom: autoir
ms.openlocfilehash: e0f76f6a232edeac350d08eeeb47188535ffe688
ms.sourcegitcommit: 1b83b6bcacb997324bc4be355deba6daf319591d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/28/2020
ms.locfileid: "46502936"
---
# <a name="remediation-actions-following-automated-investigations-in-microsoft-threat-protection"></a><span data-ttu-id="ec601-104">Actions de correction suite à des enquêtes automatisées dans Microsoft Threat Protection</span><span class="sxs-lookup"><span data-stu-id="ec601-104">Remediation actions following automated investigations in Microsoft Threat Protection</span></span>

<span data-ttu-id="ec601-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="ec601-105">**Applies to:**</span></span>
- <span data-ttu-id="ec601-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="ec601-106">Microsoft Threat Protection</span></span>


## <a name="remediation-actions"></a><span data-ttu-id="ec601-107">Actions de correction</span><span class="sxs-lookup"><span data-stu-id="ec601-107">Remediation actions</span></span>

<span data-ttu-id="ec601-108">Pendant et après une enquête automatisée dans Microsoft Threat Protection, les actions de correction sont identifiées pour les éléments malveillants ou suspects.</span><span class="sxs-lookup"><span data-stu-id="ec601-108">During and after an automated investigation in Microsoft Threat Protection, remediation actions are identified for malicious or suspicious items.</span></span> <span data-ttu-id="ec601-109">Certains types d’actions de correction sont pris sur les appareils, également appelés points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="ec601-109">Some kinds of remediation actions are taken on devices, also referred to as endpoints.</span></span> <span data-ttu-id="ec601-110">D’autres actions de correction sont appliquées au contenu du courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="ec601-110">Other remediation actions are taken on email content.</span></span> <span data-ttu-id="ec601-111">Analyses automatiques terminées après que les actions de correction ont été effectuées, approuvées ou rejetées.</span><span class="sxs-lookup"><span data-stu-id="ec601-111">Automated investigations complete after remediation actions are taken, approved, or rejected.</span></span>

<span data-ttu-id="ec601-112">Le tableau suivant récapitule les actions de correction actuellement prises en charge dans Microsoft Threat Protection :</span><span class="sxs-lookup"><span data-stu-id="ec601-112">The following table summarizes remediation actions that are currently supported in Microsoft Threat Protection:</span></span> 

|<span data-ttu-id="ec601-113">Actions de correction du périphérique (point de terminaison)</span><span class="sxs-lookup"><span data-stu-id="ec601-113">Device (endpoint) remediation actions</span></span>  |<span data-ttu-id="ec601-114">Actions de correction des e-mails</span><span class="sxs-lookup"><span data-stu-id="ec601-114">Email remediation actions</span></span>  |
|---------|---------|
|<span data-ttu-id="ec601-115">-Créer un package d’enquête</span><span class="sxs-lookup"><span data-stu-id="ec601-115">- Collect investigation package</span></span> <br/><span data-ttu-id="ec601-116">-Isoler le périphérique (cette action peut être inachevée)</span><span class="sxs-lookup"><span data-stu-id="ec601-116">- Isolate device (this action can be undone)</span></span><br/><span data-ttu-id="ec601-117">-Ordinateur débarquement</span><span class="sxs-lookup"><span data-stu-id="ec601-117">- Offboard machine</span></span> <br/><span data-ttu-id="ec601-118">-Exécution du code de la version</span><span class="sxs-lookup"><span data-stu-id="ec601-118">- Release code execution</span></span> <br/><span data-ttu-id="ec601-119">-Libérer de la quarantaine</span><span class="sxs-lookup"><span data-stu-id="ec601-119">- Release from quarantine</span></span> <br/><span data-ttu-id="ec601-120">-Exemple de requête</span><span class="sxs-lookup"><span data-stu-id="ec601-120">- Request sample</span></span> <br/><span data-ttu-id="ec601-121">-Restreindre l’exécution du code (cette action peut être terminée)</span><span class="sxs-lookup"><span data-stu-id="ec601-121">- Restrict code execution (this action can be undone)</span></span> <br/><span data-ttu-id="ec601-122">-Exécuter l’analyse antivirus</span><span class="sxs-lookup"><span data-stu-id="ec601-122">- Run antivirus scan</span></span> <br/><span data-ttu-id="ec601-123">-Arrêter et mettre en quarantaine</span><span class="sxs-lookup"><span data-stu-id="ec601-123">- Stop and quarantine</span></span>      |<span data-ttu-id="ec601-124">-Bloquer l’URL (temps de clic)</span><span class="sxs-lookup"><span data-stu-id="ec601-124">- Block URL (time-of-click)</span></span><br/><span data-ttu-id="ec601-125">-Supprimer les messages électroniques ou les clusters par suppression douce</span><span class="sxs-lookup"><span data-stu-id="ec601-125">- Soft delete email messages or clusters</span></span><br/><span data-ttu-id="ec601-126">-Courrier en quarantaine</span><span class="sxs-lookup"><span data-stu-id="ec601-126">- Quarantine email</span></span><br/><span data-ttu-id="ec601-127">-Mettre en quarantaine une pièce jointe de courrier électronique</span><span class="sxs-lookup"><span data-stu-id="ec601-127">- Quarantine an email attachment</span></span><br/><span data-ttu-id="ec601-128">-Désactiver le transfert de courrier externe</span><span class="sxs-lookup"><span data-stu-id="ec601-128">- Turn off external mail forwarding</span></span>          |

<span data-ttu-id="ec601-129">Les actions de correction, qu’elles soient en attente d’approbation ou qui sont déjà terminées, peuvent être affichées dans le [Centre de notifications](https://docs.microsoft.com/microsoft-365/security/mtp/mtp-action-center).</span><span class="sxs-lookup"><span data-stu-id="ec601-129">Remediation actions, whether they're pending approval or are already complete, can be viewed in the [Action Center](https://docs.microsoft.com/microsoft-365/security/mtp/mtp-action-center).</span></span>

## <a name="remediation-actions-follow-automated-investigations"></a><span data-ttu-id="ec601-130">Les actions de correction suivent les enquêtes automatiques</span><span class="sxs-lookup"><span data-stu-id="ec601-130">Remediation actions follow automated investigations</span></span>

<span data-ttu-id="ec601-131">Lorsqu’un examen automatisé se termine, un verdict est atteint pour chaque élément de preuve impliqué et des actions de correction sont identifiées.</span><span class="sxs-lookup"><span data-stu-id="ec601-131">When an automated investigation completes, a verdict is reached for every piece of evidence involved, and remediation actions are identified.</span></span> <span data-ttu-id="ec601-132">Dans certains cas, des actions de correction sont effectuées automatiquement. dans d’autres cas, les actions de correction attendent une approbation.</span><span class="sxs-lookup"><span data-stu-id="ec601-132">In some cases, remediation actions are taken automatically; in other cases, remediation actions await approval.</span></span> <span data-ttu-id="ec601-133">Le tableau suivant répertorie les verdicts et résultats possibles :</span><span class="sxs-lookup"><span data-stu-id="ec601-133">The following table lists possible verdicts and outcomes:</span></span>

|<span data-ttu-id="ec601-134">Verdict</span><span class="sxs-lookup"><span data-stu-id="ec601-134">Verdict</span></span>    |<span data-ttu-id="ec601-135">Domaine</span><span class="sxs-lookup"><span data-stu-id="ec601-135">Area</span></span>    |<span data-ttu-id="ec601-136">Résultats</span><span class="sxs-lookup"><span data-stu-id="ec601-136">Outcomes</span></span>|
|------|------|------|
|<span data-ttu-id="ec601-137">Malveillant</span><span class="sxs-lookup"><span data-stu-id="ec601-137">Malicious</span></span>    |<span data-ttu-id="ec601-138">Appareils (points de terminaison)</span><span class="sxs-lookup"><span data-stu-id="ec601-138">Devices (endpoints)</span></span>    |<span data-ttu-id="ec601-139">Les actions d'assainissement prennent automatiquement effet</span><span class="sxs-lookup"><span data-stu-id="ec601-139">Remediation actions are taken automatically</span></span>|
|<span data-ttu-id="ec601-140">Malveillant</span><span class="sxs-lookup"><span data-stu-id="ec601-140">Malicious</span></span>    |<span data-ttu-id="ec601-141">Contenu de l’e-mail (URL ou pièces jointes)</span><span class="sxs-lookup"><span data-stu-id="ec601-141">Email content (URLs or attachments)</span></span> | <span data-ttu-id="ec601-142">Les actions de correction recommandées sont en attente d’approbation</span><span class="sxs-lookup"><span data-stu-id="ec601-142">Recommended remediation actions are pending approval</span></span>|
|<span data-ttu-id="ec601-143">Suspect</span><span class="sxs-lookup"><span data-stu-id="ec601-143">Suspicious</span></span>    |<span data-ttu-id="ec601-144">Appareils ou contenu de l’e-mail</span><span class="sxs-lookup"><span data-stu-id="ec601-144">Devices or email content</span></span> |<span data-ttu-id="ec601-145">Les actions de correction recommandées sont en attente d’approbation</span><span class="sxs-lookup"><span data-stu-id="ec601-145">Recommended remediation actions are pending approval</span></span>|
|<span data-ttu-id="ec601-146">Aucune menace détectée</span><span class="sxs-lookup"><span data-stu-id="ec601-146">No threats found</span></span>    |<span data-ttu-id="ec601-147">Appareils ou contenu de l’e-mail</span><span class="sxs-lookup"><span data-stu-id="ec601-147">Devices or email content</span></span>    |<span data-ttu-id="ec601-148">Aucune action de correction n’est nécessaire</span><span class="sxs-lookup"><span data-stu-id="ec601-148">No remediation actions are needed</span></span>|

[<span data-ttu-id="ec601-149">Examiner une action en attente dans le centre de notifications</span><span class="sxs-lookup"><span data-stu-id="ec601-149">Review a pending action in the Action center</span></span>](mtp-autoir-actions.md#review-a-pending-action-in-the-action-center)

> [!TIP]
> <span data-ttu-id="ec601-150">Si vous pensez qu’un message a été manqué ou incorrectement détecté par les fonctionnalités d’analyse et de réponse automatiques dans Microsoft Threat Protection, faites-le nous savoir.</span><span class="sxs-lookup"><span data-stu-id="ec601-150">If you think something was missed or wrongly detected by automated investigation and response features in Microsoft Threat Protection, let us know!</span></span> <span data-ttu-id="ec601-151">[Signalez les faux positifs/négatifs](mtp-autoir-report-false-positives-negatives.md).</span><span class="sxs-lookup"><span data-stu-id="ec601-151">[Report false positives/negatives](mtp-autoir-report-false-positives-negatives.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="ec601-152">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="ec601-152">Next steps</span></span>

- [<span data-ttu-id="ec601-153">Approuver ou rejeter des actions</span><span class="sxs-lookup"><span data-stu-id="ec601-153">Approve or reject actions</span></span>](https://docs.microsoft.com/microsoft-365/security/mtp/mtp-autoir-actions)

- <span data-ttu-id="ec601-154">[En savoir plus sur le centre de notifications](https://docs.microsoft.com/microsoft-365/security/mtp/mtp-action-center).</span><span class="sxs-lookup"><span data-stu-id="ec601-154">[Learn more about the Action center](https://docs.microsoft.com/microsoft-365/security/mtp/mtp-action-center)</span></span>
