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
ms.openlocfilehash: ca0c557de24320692d903a1136fc434d635f0507
ms.sourcegitcommit: 58c1b4208a5e231463091573e40696d08fc39b8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2020
ms.locfileid: "42955590"
---
# <a name="remediation-actions-following-automated-investigations-in-microsoft-threat-protection"></a><span data-ttu-id="efa72-104">Actions de correction suite à des enquêtes automatisées dans Microsoft Threat Protection</span><span class="sxs-lookup"><span data-stu-id="efa72-104">Remediation actions following automated investigations in Microsoft Threat Protection</span></span>

<span data-ttu-id="efa72-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="efa72-105">**Applies to:**</span></span>
- <span data-ttu-id="efa72-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="efa72-106">Microsoft Threat Protection</span></span>


## <a name="remediation-actions"></a><span data-ttu-id="efa72-107">Actions de correction</span><span class="sxs-lookup"><span data-stu-id="efa72-107">Remediation actions</span></span>

<span data-ttu-id="efa72-108">Pendant et après une enquête automatisée dans Microsoft Threat Protection, les actions de correction sont identifiées pour les éléments malveillants ou suspects.</span><span class="sxs-lookup"><span data-stu-id="efa72-108">During and after an automated investigation in Microsoft Threat Protection, remediation actions are identified for malicious or suspicious items.</span></span> <span data-ttu-id="efa72-109">Certains types d’actions de correction sont pris sur les appareils, également appelés points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="efa72-109">Some kinds of remediation actions are taken on devices, also referred to as endpoints.</span></span> <span data-ttu-id="efa72-110">D’autres actions de correction sont appliquées au contenu du courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="efa72-110">Other remediation actions are taken on email content.</span></span> <span data-ttu-id="efa72-111">Analyses automatiques terminées après que les actions de correction ont été effectuées, approuvées ou rejetées.</span><span class="sxs-lookup"><span data-stu-id="efa72-111">Automated investigations complete after remediation actions are taken, approved, or rejected.</span></span>

<span data-ttu-id="efa72-112">Le tableau suivant récapitule les actions de correction actuellement prises en charge dans Microsoft Threat Protection :</span><span class="sxs-lookup"><span data-stu-id="efa72-112">The following table summarizes remediation actions that are currently supported in Microsoft Threat Protection:</span></span> 

|<span data-ttu-id="efa72-113">Actions de correction du périphérique (point de terminaison)</span><span class="sxs-lookup"><span data-stu-id="efa72-113">Device (endpoint) remediation actions</span></span>  |<span data-ttu-id="efa72-114">Actions de correction des e-mails</span><span class="sxs-lookup"><span data-stu-id="efa72-114">Email remediation actions</span></span>  |
|---------|---------|
|<span data-ttu-id="efa72-115">Fichier de quarantaine</span><span class="sxs-lookup"><span data-stu-id="efa72-115">Quarantine file</span></span><br/><span data-ttu-id="efa72-116">Supprimer une clé de Registre</span><span class="sxs-lookup"><span data-stu-id="efa72-116">Remove registry key</span></span><br/><span data-ttu-id="efa72-117">Processus d’arrêt</span><span class="sxs-lookup"><span data-stu-id="efa72-117">Kill process</span></span> <br/><span data-ttu-id="efa72-118">Arrêter le service</span><span class="sxs-lookup"><span data-stu-id="efa72-118">Stop service</span></span> <br/><span data-ttu-id="efa72-119">Désactiver le pilote</span><span class="sxs-lookup"><span data-stu-id="efa72-119">Disable driver</span></span> <br/><span data-ttu-id="efa72-120">Supprimer une tâche planifiée.</span><span class="sxs-lookup"><span data-stu-id="efa72-120">Remove scheduled task</span></span>      |<span data-ttu-id="efa72-121">Supprimer (récupération possible) le courrier ou des clusters</span><span class="sxs-lookup"><span data-stu-id="efa72-121">Soft delete email messages or clusters</span></span><br/><span data-ttu-id="efa72-122">Bloquer l’URL (heure du clic)</span><span class="sxs-lookup"><span data-stu-id="efa72-122">Block URL (time-of-click)</span></span><br/><span data-ttu-id="efa72-123">Désactiver le transfert de courrier externe</span><span class="sxs-lookup"><span data-stu-id="efa72-123">Turn off external mail forwarding</span></span>          |

<span data-ttu-id="efa72-124">Les actions de correction, qu’elles soient en attente d’approbation ou qui sont déjà terminées, peuvent être affichées dans le [Centre de notifications](https://docs.microsoft.com/microsoft-365/security/mtp/mtp-action-center).</span><span class="sxs-lookup"><span data-stu-id="efa72-124">Remediation actions, whether they're pending approval or are already complete, can be viewed in the [Action Center](https://docs.microsoft.com/microsoft-365/security/mtp/mtp-action-center).</span></span>

## <a name="remediation-actions-follow-automated-investigations"></a><span data-ttu-id="efa72-125">Les actions de correction suivent les enquêtes automatiques</span><span class="sxs-lookup"><span data-stu-id="efa72-125">Remediation actions follow automated investigations</span></span>

<span data-ttu-id="efa72-126">Lorsqu’un examen automatisé se termine, un verdict est atteint pour chaque élément de preuve impliqué et des actions de correction sont identifiées.</span><span class="sxs-lookup"><span data-stu-id="efa72-126">When an automated investigation completes, a verdict is reached for every piece of evidence involved, and remediation actions are identified.</span></span> <span data-ttu-id="efa72-127">Dans certains cas, des actions de correction sont effectuées automatiquement. dans d’autres cas, les actions de correction attendent une approbation.</span><span class="sxs-lookup"><span data-stu-id="efa72-127">In some cases, remediation actions are taken automatically; in other cases, remediation actions await approval.</span></span> <span data-ttu-id="efa72-128">Le tableau suivant répertorie les verdicts et résultats possibles :</span><span class="sxs-lookup"><span data-stu-id="efa72-128">The following table lists possible verdicts and outcomes:</span></span>

|<span data-ttu-id="efa72-129">Verdict</span><span class="sxs-lookup"><span data-stu-id="efa72-129">Verdict</span></span>    |<span data-ttu-id="efa72-130">Domaine</span><span class="sxs-lookup"><span data-stu-id="efa72-130">Area</span></span>    |<span data-ttu-id="efa72-131">Résultats</span><span class="sxs-lookup"><span data-stu-id="efa72-131">Outcomes</span></span>|
|------|------|------|
|<span data-ttu-id="efa72-132">Malveillant</span><span class="sxs-lookup"><span data-stu-id="efa72-132">Malicious</span></span>    |<span data-ttu-id="efa72-133">Appareils (points de terminaison)</span><span class="sxs-lookup"><span data-stu-id="efa72-133">Devices (endpoints)</span></span>    |<span data-ttu-id="efa72-134">Les actions d'assainissement prennent automatiquement effet</span><span class="sxs-lookup"><span data-stu-id="efa72-134">Remediation actions are taken automatically</span></span>|
|<span data-ttu-id="efa72-135">Malveillant</span><span class="sxs-lookup"><span data-stu-id="efa72-135">Malicious</span></span>    |<span data-ttu-id="efa72-136">Contenu de l’e-mail (URL ou pièces jointes)</span><span class="sxs-lookup"><span data-stu-id="efa72-136">Email content (URLs or attachments)</span></span> | <span data-ttu-id="efa72-137">Les actions de correction recommandées sont en attente d’approbation</span><span class="sxs-lookup"><span data-stu-id="efa72-137">Recommended remediation actions are pending approval</span></span>|
|<span data-ttu-id="efa72-138">Suspect</span><span class="sxs-lookup"><span data-stu-id="efa72-138">Suspicious</span></span>    |<span data-ttu-id="efa72-139">Appareils ou contenu de l’e-mail</span><span class="sxs-lookup"><span data-stu-id="efa72-139">Devices or email content</span></span> |<span data-ttu-id="efa72-140">Les actions de correction recommandées sont en attente d’approbation</span><span class="sxs-lookup"><span data-stu-id="efa72-140">Recommended remediation actions are pending approval</span></span>|
|<span data-ttu-id="efa72-141">Aucune menace détectée</span><span class="sxs-lookup"><span data-stu-id="efa72-141">No threats found</span></span>    |<span data-ttu-id="efa72-142">Appareils ou contenu de l’e-mail</span><span class="sxs-lookup"><span data-stu-id="efa72-142">Devices or email content</span></span>    |<span data-ttu-id="efa72-143">Aucune action de correction n’est nécessaire</span><span class="sxs-lookup"><span data-stu-id="efa72-143">No remediation actions are needed</span></span>|

[<span data-ttu-id="efa72-144">Examiner une action en attente dans le centre de notifications</span><span class="sxs-lookup"><span data-stu-id="efa72-144">Review a pending action in the Action center</span></span>](mtp-autoir-actions.md#review-a-pending-action-in-the-action-center)

> [!TIP]
> <span data-ttu-id="efa72-145">Si vous pensez qu’un message a été manqué ou incorrectement détecté par les fonctionnalités d’analyse et de réponse automatiques dans Microsoft Threat Protection, faites-le nous savoir.</span><span class="sxs-lookup"><span data-stu-id="efa72-145">If you think something was missed or wrongly detected by automated investigation and response features in Microsoft Threat Protection, let us know!</span></span> <span data-ttu-id="efa72-146">[Signalez les faux positifs/négatifs](mtp-autoir-report-false-positives-negatives.md).</span><span class="sxs-lookup"><span data-stu-id="efa72-146">[Report false positives/negatives](mtp-autoir-report-false-positives-negatives.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="efa72-147">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="efa72-147">Next steps</span></span>

- [<span data-ttu-id="efa72-148">Approuver ou rejeter des actions</span><span class="sxs-lookup"><span data-stu-id="efa72-148">Approve or reject actions</span></span>](https://docs.microsoft.com/microsoft-365/security/mtp/mtp-autoir-actions)

- <span data-ttu-id="efa72-149">[En savoir plus sur le centre de notifications](https://docs.microsoft.com/microsoft-365/security/mtp/mtp-action-center).</span><span class="sxs-lookup"><span data-stu-id="efa72-149">[Learn more about the Action center](https://docs.microsoft.com/microsoft-365/security/mtp/mtp-action-center)</span></span>
