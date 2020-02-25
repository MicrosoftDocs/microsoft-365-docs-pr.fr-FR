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
ms.openlocfilehash: 76a4fe678ce0106c7345dd3bdf504673733b63b6
ms.sourcegitcommit: 59b006f8e82d1772cae2029f278a59ae8a106736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/25/2020
ms.locfileid: "42266050"
---
# <a name="remediation-actions-following-automated-investigations-in-microsoft-threat-protection"></a><span data-ttu-id="621da-104">Actions de correction suite à des enquêtes automatisées dans Microsoft Threat Protection</span><span class="sxs-lookup"><span data-stu-id="621da-104">Remediation actions following automated investigations in Microsoft Threat Protection</span></span>

<span data-ttu-id="621da-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="621da-105">**Applies to:**</span></span>
- <span data-ttu-id="621da-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="621da-106">Microsoft Threat Protection</span></span>


## <a name="remediation-actions"></a><span data-ttu-id="621da-107">Actions de correction</span><span class="sxs-lookup"><span data-stu-id="621da-107">Remediation actions</span></span>

<span data-ttu-id="621da-108">Pendant et après une enquête automatisée dans Microsoft Threat Protection, les actions de correction sont identifiées pour les éléments malveillants ou suspects.</span><span class="sxs-lookup"><span data-stu-id="621da-108">During and after an automated investigation in Microsoft Threat Protection, remediation actions are identified for malicious or suspicious items.</span></span> <span data-ttu-id="621da-109">Certains types d’actions de correction sont pris sur les appareils, également appelés points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="621da-109">Some kinds of remediation actions are taken on devices, also referred to as endpoints.</span></span> <span data-ttu-id="621da-110">D’autres actions de correction sont appliquées au contenu du courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="621da-110">Other remediation actions are taken on email content.</span></span> <span data-ttu-id="621da-111">Analyses automatiques terminées après que les actions de correction ont été effectuées, approuvées ou rejetées.</span><span class="sxs-lookup"><span data-stu-id="621da-111">Automated investigations complete after remediation actions are taken, approved, or rejected.</span></span>

<span data-ttu-id="621da-112">Le tableau suivant récapitule les actions de correction actuellement prises en charge dans Microsoft Threat Protection :</span><span class="sxs-lookup"><span data-stu-id="621da-112">The following table summarizes remediation actions that are currently supported in Microsoft Threat Protection:</span></span> 

|<span data-ttu-id="621da-113">Actions de correction du périphérique (point de terminaison)</span><span class="sxs-lookup"><span data-stu-id="621da-113">Device (endpoint) remediation actions</span></span>  |<span data-ttu-id="621da-114">Actions de correction des e-mails</span><span class="sxs-lookup"><span data-stu-id="621da-114">Email remediation actions</span></span>  |
|---------|---------|
|<span data-ttu-id="621da-115">Fichier de quarantaine</span><span class="sxs-lookup"><span data-stu-id="621da-115">Quarantine file</span></span><br/><span data-ttu-id="621da-116">Supprimer une clé de Registre</span><span class="sxs-lookup"><span data-stu-id="621da-116">Remove registry key</span></span><br/><span data-ttu-id="621da-117">Processus d’arrêt</span><span class="sxs-lookup"><span data-stu-id="621da-117">Kill process</span></span> <br/><span data-ttu-id="621da-118">Arrêter le service</span><span class="sxs-lookup"><span data-stu-id="621da-118">Stop service</span></span> <br/><span data-ttu-id="621da-119">Désactiver le pilote</span><span class="sxs-lookup"><span data-stu-id="621da-119">Disable driver</span></span> <br/><span data-ttu-id="621da-120">Supprimer une tâche planifiée.</span><span class="sxs-lookup"><span data-stu-id="621da-120">Remove scheduled task</span></span>      |<span data-ttu-id="621da-121">Supprimer (récupération possible) le courrier ou des clusters</span><span class="sxs-lookup"><span data-stu-id="621da-121">Soft delete email messages or clusters</span></span><br/><span data-ttu-id="621da-122">Bloquer l’URL (heure du clic)</span><span class="sxs-lookup"><span data-stu-id="621da-122">Block URL (time-of-click)</span></span><br/><span data-ttu-id="621da-123">Désactiver le transfert de courrier externe</span><span class="sxs-lookup"><span data-stu-id="621da-123">Turn off external mail forwarding</span></span>          |

<span data-ttu-id="621da-124">Les actions de correction, qu’elles soient en attente d’approbation ou qui sont déjà terminées, peuvent être affichées dans le [Centre de notifications](https://docs.microsoft.com/microsoft-365/security/mtp/mtp-action-center).</span><span class="sxs-lookup"><span data-stu-id="621da-124">Remediation actions, whether they're pending approval or are already complete, can be viewed in the [Action Center](https://docs.microsoft.com/microsoft-365/security/mtp/mtp-action-center).</span></span>

## <a name="verdicts-and-outcomes-following-automated-investigations"></a><span data-ttu-id="621da-125">Verdicts et résultats après des enquêtes automatisées</span><span class="sxs-lookup"><span data-stu-id="621da-125">Verdicts and outcomes following automated investigations</span></span>

<span data-ttu-id="621da-126">Lorsqu’un examen automatisé se termine, un verdict est atteint pour chaque élément de preuve impliqué et des actions de correction sont identifiées.</span><span class="sxs-lookup"><span data-stu-id="621da-126">When an automated investigation completes, a verdict is reached for every piece of evidence involved, and remediation actions are identified.</span></span> <span data-ttu-id="621da-127">Dans certains cas, des actions de correction sont effectuées automatiquement. dans d’autres cas, les actions de correction attendent une approbation.</span><span class="sxs-lookup"><span data-stu-id="621da-127">In some cases, remediation actions are taken automatically; in other cases, remediation actions await approval.</span></span> <span data-ttu-id="621da-128">Le tableau suivant répertorie les verdicts et résultats possibles :</span><span class="sxs-lookup"><span data-stu-id="621da-128">The following table lists possible verdicts and outcomes:</span></span>

|<span data-ttu-id="621da-129">Verdict</span><span class="sxs-lookup"><span data-stu-id="621da-129">Verdict</span></span>    |<span data-ttu-id="621da-130">Domaine</span><span class="sxs-lookup"><span data-stu-id="621da-130">Area</span></span>   |<span data-ttu-id="621da-131">Résultats</span><span class="sxs-lookup"><span data-stu-id="621da-131">Outcomes</span></span>|
|------|------|------|
|<span data-ttu-id="621da-132">Malveillant</span><span class="sxs-lookup"><span data-stu-id="621da-132">Malicious</span></span>  |<span data-ttu-id="621da-133">Appareils (points de terminaison)</span><span class="sxs-lookup"><span data-stu-id="621da-133">Devices (endpoints)</span></span>    |<span data-ttu-id="621da-134">Les actions d'assainissement prennent automatiquement effet</span><span class="sxs-lookup"><span data-stu-id="621da-134">Remediation actions are taken automatically</span></span>|
|<span data-ttu-id="621da-135">Malveillant</span><span class="sxs-lookup"><span data-stu-id="621da-135">Malicious</span></span>  |<span data-ttu-id="621da-136">Contenu de l’e-mail (URL ou pièces jointes)</span><span class="sxs-lookup"><span data-stu-id="621da-136">Email content (URLs or attachments)</span></span> | <span data-ttu-id="621da-137">Les actions de correction recommandées sont en attente d’approbation</span><span class="sxs-lookup"><span data-stu-id="621da-137">Recommended remediation actions are pending approval</span></span>|
|<span data-ttu-id="621da-138">Suspect</span><span class="sxs-lookup"><span data-stu-id="621da-138">Suspicious</span></span> |<span data-ttu-id="621da-139">Appareils ou contenu de l’e-mail</span><span class="sxs-lookup"><span data-stu-id="621da-139">Devices or email content</span></span> |<span data-ttu-id="621da-140">Les actions de correction recommandées sont en attente d’approbation</span><span class="sxs-lookup"><span data-stu-id="621da-140">Recommended remediation actions are pending approval</span></span>|
|<span data-ttu-id="621da-141">Nettoyer</span><span class="sxs-lookup"><span data-stu-id="621da-141">Clean</span></span>  |<span data-ttu-id="621da-142">Appareils ou contenu de l’e-mail</span><span class="sxs-lookup"><span data-stu-id="621da-142">Devices or email content</span></span>   |<span data-ttu-id="621da-143">Aucune action de correction n’est nécessaire</span><span class="sxs-lookup"><span data-stu-id="621da-143">No remediation actions are needed</span></span>|

[<span data-ttu-id="621da-144">Examiner une action en attente dans le centre de notifications</span><span class="sxs-lookup"><span data-stu-id="621da-144">Review a pending action in the Action center</span></span>](mtp-autoir-actions.md#review-a-pending-action-in-the-action-center)

> [!TIP]
> <span data-ttu-id="621da-145">Si vous pensez qu’un message a été manqué ou incorrectement détecté par les fonctionnalités d’analyse et de réponse automatiques dans Microsoft Threat Protection, faites-le nous savoir.</span><span class="sxs-lookup"><span data-stu-id="621da-145">If you think something was missed or wrongly detected by automated investigation and response features in Microsoft Threat Protection, let us know!</span></span> <span data-ttu-id="621da-146">[Signalez les faux positifs/négatifs](mtp-autoir-report-false-positives-negatives.md).</span><span class="sxs-lookup"><span data-stu-id="621da-146">[Report false positives/negatives](mtp-autoir-report-false-positives-negatives.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="621da-147">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="621da-147">Next steps</span></span>

- [<span data-ttu-id="621da-148">Approuver ou rejeter des actions</span><span class="sxs-lookup"><span data-stu-id="621da-148">Approve or reject actions</span></span>](https://docs.microsoft.com/microsoft-365/security/mtp/mtp-autoir-actions)

- <span data-ttu-id="621da-149">[En savoir plus sur le centre de notifications](https://docs.microsoft.com/microsoft-365/security/mtp/mtp-action-center).</span><span class="sxs-lookup"><span data-stu-id="621da-149">[Learn more about the Action center](https://docs.microsoft.com/microsoft-365/security/mtp/mtp-action-center)</span></span>
