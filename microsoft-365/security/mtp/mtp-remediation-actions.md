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
- m365initiative-m365-defender
ms.topic: conceptual
ms.custom: autoir
ms.date: 09/16/2020
ms.reviewer: evaldm, isco
ms.openlocfilehash: 5106ef34f11cb43d74fa993fcdb820d6a5dce86f
ms.sourcegitcommit: de600339b08951d6dd3933288a8da2327a4b6ef3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/13/2020
ms.locfileid: "48429472"
---
# <a name="remediation-actions-following-automated-investigations-in-microsoft-threat-protection"></a><span data-ttu-id="22797-104">Actions de correction suite à des enquêtes automatisées dans Microsoft Threat Protection</span><span class="sxs-lookup"><span data-stu-id="22797-104">Remediation actions following automated investigations in Microsoft Threat Protection</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="22797-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="22797-105">**Applies to:**</span></span>
- <span data-ttu-id="22797-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="22797-106">Microsoft Threat Protection</span></span>


## <a name="remediation-actions"></a><span data-ttu-id="22797-107">Actions de correction</span><span class="sxs-lookup"><span data-stu-id="22797-107">Remediation actions</span></span>

<span data-ttu-id="22797-108">Pendant et après une enquête automatisée dans Microsoft Threat Protection, les actions de correction sont identifiées pour les éléments malveillants ou suspects.</span><span class="sxs-lookup"><span data-stu-id="22797-108">During and after an automated investigation in Microsoft Threat Protection, remediation actions are identified for malicious or suspicious items.</span></span> <span data-ttu-id="22797-109">Certains types d’actions de correction sont pris sur les appareils, également appelés points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="22797-109">Some kinds of remediation actions are taken on devices, also referred to as endpoints.</span></span> <span data-ttu-id="22797-110">D’autres actions de correction sont appliquées au contenu du courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="22797-110">Other remediation actions are taken on email content.</span></span> <span data-ttu-id="22797-111">Analyses automatiques terminées après que les actions de correction ont été effectuées, approuvées ou rejetées.</span><span class="sxs-lookup"><span data-stu-id="22797-111">Automated investigations complete after remediation actions are taken, approved, or rejected.</span></span>

<span data-ttu-id="22797-112">Le tableau suivant récapitule les actions de correction actuellement prises en charge dans Microsoft Threat Protection :</span><span class="sxs-lookup"><span data-stu-id="22797-112">The following table summarizes remediation actions that are currently supported in Microsoft Threat Protection:</span></span> 

|<span data-ttu-id="22797-113">Actions de correction du périphérique (point de terminaison)</span><span class="sxs-lookup"><span data-stu-id="22797-113">Device (endpoint) remediation actions</span></span>  |<span data-ttu-id="22797-114">Actions de correction des e-mails</span><span class="sxs-lookup"><span data-stu-id="22797-114">Email remediation actions</span></span>  |
|---------|---------|
|<span data-ttu-id="22797-115">-Créer un package d’enquête</span><span class="sxs-lookup"><span data-stu-id="22797-115">- Collect investigation package</span></span> <br/><span data-ttu-id="22797-116">-Isoler le périphérique (cette action peut être inachevée)</span><span class="sxs-lookup"><span data-stu-id="22797-116">- Isolate device (this action can be undone)</span></span><br/><span data-ttu-id="22797-117">-Ordinateur débarquement</span><span class="sxs-lookup"><span data-stu-id="22797-117">- Offboard machine</span></span> <br/><span data-ttu-id="22797-118">-Exécution du code de la version</span><span class="sxs-lookup"><span data-stu-id="22797-118">- Release code execution</span></span> <br/><span data-ttu-id="22797-119">-Libérer de la quarantaine</span><span class="sxs-lookup"><span data-stu-id="22797-119">- Release from quarantine</span></span> <br/><span data-ttu-id="22797-120">-Exemple de requête</span><span class="sxs-lookup"><span data-stu-id="22797-120">- Request sample</span></span> <br/><span data-ttu-id="22797-121">-Restreindre l’exécution du code (cette action peut être terminée)</span><span class="sxs-lookup"><span data-stu-id="22797-121">- Restrict code execution (this action can be undone)</span></span> <br/><span data-ttu-id="22797-122">-Exécuter l’analyse antivirus</span><span class="sxs-lookup"><span data-stu-id="22797-122">- Run antivirus scan</span></span> <br/><span data-ttu-id="22797-123">-Arrêter et mettre en quarantaine</span><span class="sxs-lookup"><span data-stu-id="22797-123">- Stop and quarantine</span></span>      |<span data-ttu-id="22797-124">-Bloquer l’URL (temps de clic)</span><span class="sxs-lookup"><span data-stu-id="22797-124">- Block URL (time-of-click)</span></span><br/><span data-ttu-id="22797-125">-Supprimer les messages électroniques ou les clusters par suppression douce</span><span class="sxs-lookup"><span data-stu-id="22797-125">- Soft delete email messages or clusters</span></span><br/><span data-ttu-id="22797-126">-Courrier en quarantaine</span><span class="sxs-lookup"><span data-stu-id="22797-126">- Quarantine email</span></span><br/><span data-ttu-id="22797-127">-Mettre en quarantaine une pièce jointe de courrier électronique</span><span class="sxs-lookup"><span data-stu-id="22797-127">- Quarantine an email attachment</span></span><br/><span data-ttu-id="22797-128">-Désactiver le transfert de courrier externe</span><span class="sxs-lookup"><span data-stu-id="22797-128">- Turn off external mail forwarding</span></span>          |

<span data-ttu-id="22797-129">Les actions de correction, qu’elles soient en attente d’approbation ou déjà terminées, peuvent être affichées dans le [Centre de notifications](https://docs.microsoft.com/microsoft-365/security/mtp/mtp-action-center).</span><span class="sxs-lookup"><span data-stu-id="22797-129">Remediation actions, whether pending approval or already complete, can be viewed in the [Action Center](https://docs.microsoft.com/microsoft-365/security/mtp/mtp-action-center).</span></span>

## <a name="remediation-actions-follow-automated-investigations"></a><span data-ttu-id="22797-130">Les actions de correction suivent les enquêtes automatiques</span><span class="sxs-lookup"><span data-stu-id="22797-130">Remediation actions follow automated investigations</span></span>

<span data-ttu-id="22797-131">Lorsqu’une enquête automatisée se termine, un verdict est atteint pour chaque élément de preuve impliqué.</span><span class="sxs-lookup"><span data-stu-id="22797-131">When an automated investigation completes, a verdict is reached for every piece of evidence involved.</span></span> <span data-ttu-id="22797-132">Selon le verdict, les actions de correction sont identifiées.</span><span class="sxs-lookup"><span data-stu-id="22797-132">Depending on the verdict, remediation actions are identified.</span></span> <span data-ttu-id="22797-133">Dans certains cas, des actions de correction sont effectuées automatiquement. dans d’autres cas, les actions de correction attendent une approbation.</span><span class="sxs-lookup"><span data-stu-id="22797-133">In some cases, remediation actions are taken automatically; in other cases, remediation actions await approval.</span></span> <span data-ttu-id="22797-134">Tout dépend de la configuration de l’analyse [et de la réponse automatisées](mtp-configure-auto-investigation-response.md).</span><span class="sxs-lookup"><span data-stu-id="22797-134">It all depends on how [automated investigation and response is configured](mtp-configure-auto-investigation-response.md).</span></span>

<span data-ttu-id="22797-135">Le tableau suivant répertorie les verdicts et résultats possibles :</span><span class="sxs-lookup"><span data-stu-id="22797-135">The following table lists possible verdicts and outcomes:</span></span>

|<span data-ttu-id="22797-136">Verdict</span><span class="sxs-lookup"><span data-stu-id="22797-136">Verdict</span></span>    |<span data-ttu-id="22797-137">Domaine</span><span class="sxs-lookup"><span data-stu-id="22797-137">Area</span></span>    |<span data-ttu-id="22797-138">Résultats</span><span class="sxs-lookup"><span data-stu-id="22797-138">Outcomes</span></span>|
|------|------|------|
|<span data-ttu-id="22797-139">Malveillant</span><span class="sxs-lookup"><span data-stu-id="22797-139">Malicious</span></span>    |<span data-ttu-id="22797-140">Appareils (points de terminaison)</span><span class="sxs-lookup"><span data-stu-id="22797-140">Devices (endpoints)</span></span>    |<span data-ttu-id="22797-141">Les actions de correction sont prises automatiquement (en supposant que les [groupes d’appareils](mtp-configure-auto-investigation-response.md#review-or-change-the-automation-level-for-device-groups) de votre organisation sont configurés pour effectuer **automatiquement des**corrections de menace).</span><span class="sxs-lookup"><span data-stu-id="22797-141">Remediation actions are taken automatically (assuming your organization's [device groups](mtp-configure-auto-investigation-response.md#review-or-change-the-automation-level-for-device-groups) are set to **Full - remediate threats automatically**)</span></span>|
|<span data-ttu-id="22797-142">Malveillant</span><span class="sxs-lookup"><span data-stu-id="22797-142">Malicious</span></span>    |<span data-ttu-id="22797-143">Contenu de l’e-mail (URL ou pièces jointes)</span><span class="sxs-lookup"><span data-stu-id="22797-143">Email content (URLs or attachments)</span></span> | <span data-ttu-id="22797-144">Les actions de correction recommandées sont en attente d’approbation</span><span class="sxs-lookup"><span data-stu-id="22797-144">Recommended remediation actions are pending approval</span></span>|
|<span data-ttu-id="22797-145">Suspect</span><span class="sxs-lookup"><span data-stu-id="22797-145">Suspicious</span></span>    |<span data-ttu-id="22797-146">Appareils ou contenu de l’e-mail</span><span class="sxs-lookup"><span data-stu-id="22797-146">Devices or email content</span></span> |<span data-ttu-id="22797-147">Les actions de correction recommandées sont en attente d’approbation</span><span class="sxs-lookup"><span data-stu-id="22797-147">Recommended remediation actions are pending approval</span></span>|
|<span data-ttu-id="22797-148">Aucune menace détectée</span><span class="sxs-lookup"><span data-stu-id="22797-148">No threats found</span></span>    |<span data-ttu-id="22797-149">Appareils ou contenu de l’e-mail</span><span class="sxs-lookup"><span data-stu-id="22797-149">Devices or email content</span></span>    |<span data-ttu-id="22797-150">Aucune action de correction n’est nécessaire</span><span class="sxs-lookup"><span data-stu-id="22797-150">No remediation actions are needed</span></span>|

> [!IMPORTANT]
> <span data-ttu-id="22797-151">La prise automatique ou non des actions de correction dépend de certains paramètres, tels que les stratégies de groupe d’appareils de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="22797-151">Whether remediation actions are taken automatically or only upon approval depends on certain settings, such as your organization's device group policies.</span></span> <span data-ttu-id="22797-152">Pour en savoir plus, consultez les articles suivants :</span><span class="sxs-lookup"><span data-stu-id="22797-152">To learn more, see the following articles:</span></span>
> - [<span data-ttu-id="22797-153">Configurer les fonctionnalités d’analyse et de réponse automatisées dans Microsoft Threat Protection</span><span class="sxs-lookup"><span data-stu-id="22797-153">Configure automated investigation and response capabilities in Microsoft Threat Protection</span></span>](mtp-configure-auto-investigation-response.md)
> - [<span data-ttu-id="22797-154">Comment les menaces sont corrigées sur les appareils</span><span class="sxs-lookup"><span data-stu-id="22797-154">How threats are remediated on devices</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/automated-investigations)

## <a name="next-steps"></a><span data-ttu-id="22797-155">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="22797-155">Next steps</span></span>

- [<span data-ttu-id="22797-156">Visiter le Centre de notifications</span><span class="sxs-lookup"><span data-stu-id="22797-156">Visit the Action center</span></span>](https://docs.microsoft.com/microsoft-365/security/mtp/mtp-action-center)
- [<span data-ttu-id="22797-157">Approuver ou refuser des actions en attente</span><span class="sxs-lookup"><span data-stu-id="22797-157">Approve or reject pending actions</span></span>](https://docs.microsoft.com/microsoft-365/security/mtp/mtp-autoir-actions)
- [<span data-ttu-id="22797-158">Gérer les faux positifs/négatifs dans les fonctionnalités d’analyse et de réponse automatisées</span><span class="sxs-lookup"><span data-stu-id="22797-158">Handle false positives/negatives in automated investigation and response capabilities</span></span>](mtp-autoir-report-false-positives-negatives.md)
