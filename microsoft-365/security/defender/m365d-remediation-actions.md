---
title: Actions de correction dans Microsoft 365 Defender
description: Obtenir une vue d’ensemble des actions de correction qui suivent des enquêtes automatisées dans Microsoft 365 Defender
keywords: automatisation, examen, alerte, déclencheur, action, correction
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: deniseb
author: denisebmsft
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
- m365initiative-m365-defender
ms.topic: conceptual
ms.custom: autoir
ms.date: 01/29/2021
ms.reviewer: evaldm, isco
ms.technology: m365d
ms.openlocfilehash: fa73756aa9f350793c00a7e4a960c215627b712f
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51064713"
---
# <a name="remediation-actions-in-microsoft-365-defender"></a><span data-ttu-id="01c73-104">Actions de correction dans Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="01c73-104">Remediation actions in Microsoft 365 Defender</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="01c73-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="01c73-105">**Applies to:**</span></span>
- <span data-ttu-id="01c73-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="01c73-106">Microsoft 365 Defender</span></span>

## <a name="remediation-actions"></a><span data-ttu-id="01c73-107">Actions de correction</span><span class="sxs-lookup"><span data-stu-id="01c73-107">Remediation actions</span></span>

<span data-ttu-id="01c73-108">Pendant et après un examen automatisé dans Microsoft 365 Defender, des actions de correction sont identifiées pour les éléments malveillants ou suspects.</span><span class="sxs-lookup"><span data-stu-id="01c73-108">During and after an automated investigation in Microsoft 365 Defender, remediation actions are identified for malicious or suspicious items.</span></span> <span data-ttu-id="01c73-109">Certains types d’actions de correction sont prises sur les appareils, également appelés points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="01c73-109">Some kinds of remediation actions are taken on devices, also referred to as endpoints.</span></span> <span data-ttu-id="01c73-110">D’autres mesures correctives sont prises sur le contenu du courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="01c73-110">Other remediation actions are taken on email content.</span></span> <span data-ttu-id="01c73-111">Les enquêtes automatisées se terminent après que des mesures correctives ont été prises, approuvées ou rejetées.</span><span class="sxs-lookup"><span data-stu-id="01c73-111">Automated investigations complete after remediation actions are taken, approved, or rejected.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="01c73-112">Le fait que des mesures correctives soient prises automatiquement ou uniquement après approbation dépend de certains paramètres, tels que la façon dont les niveaux d’automatisation sont mis en place.</span><span class="sxs-lookup"><span data-stu-id="01c73-112">Whether remediation actions are taken automatically or only upon approval depends on certain settings, such as how automation levels.</span></span> <span data-ttu-id="01c73-113">Pour en savoir plus, consultez les articles suivants :</span><span class="sxs-lookup"><span data-stu-id="01c73-113">To learn more, see the following articles:</span></span>
> - [<span data-ttu-id="01c73-114">Configurer vos fonctionnalités automatisées d’examen et de réponse dans Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="01c73-114">Configure your automated investigation and response capabilities in Microsoft 365 Defender</span></span>](m365d-configure-auto-investigation-response.md)
> - [<span data-ttu-id="01c73-115">Comment les menaces sont corrigés sur les appareils</span><span class="sxs-lookup"><span data-stu-id="01c73-115">How threats are remediated on devices</span></span>](../defender-endpoint/automated-investigations.md)
> - [<span data-ttu-id="01c73-116">Menaces et actions de correction sur le contenu de collaboration & courrier électronique</span><span class="sxs-lookup"><span data-stu-id="01c73-116">Threats and remediation actions on email & collaboration content</span></span>](../defender-365-security/air-remediation-actions.md#threats-and-remediation-actions)

<span data-ttu-id="01c73-117">Le tableau suivant récapitule les actions de correction actuellement prises en charge dans Microsoft 365 Defender :</span><span class="sxs-lookup"><span data-stu-id="01c73-117">The following table summarizes remediation actions that are currently supported in Microsoft 365 Defender:</span></span> 

|<span data-ttu-id="01c73-118">Actions de correction de l’appareil (point de terminaison)</span><span class="sxs-lookup"><span data-stu-id="01c73-118">Device (endpoint) remediation actions</span></span>  |<span data-ttu-id="01c73-119">Actions de correction des e-mails</span><span class="sxs-lookup"><span data-stu-id="01c73-119">Email remediation actions</span></span>  |
|:---------|:---------|
|<span data-ttu-id="01c73-120">- Collecter le package d’examen</span><span class="sxs-lookup"><span data-stu-id="01c73-120">- Collect investigation package</span></span> <br/><span data-ttu-id="01c73-121">- Isoler l’appareil (cette action peut être annulée)</span><span class="sxs-lookup"><span data-stu-id="01c73-121">- Isolate device (this action can be undone)</span></span><br/><span data-ttu-id="01c73-122">- Appareil hors-carte</span><span class="sxs-lookup"><span data-stu-id="01c73-122">- Offboard machine</span></span> <br/><span data-ttu-id="01c73-123">- Exécution du code de publication</span><span class="sxs-lookup"><span data-stu-id="01c73-123">- Release code execution</span></span> <br/><span data-ttu-id="01c73-124">- Sortir de la quarantaine</span><span class="sxs-lookup"><span data-stu-id="01c73-124">- Release from quarantine</span></span> <br/><span data-ttu-id="01c73-125">- Exemple de requête</span><span class="sxs-lookup"><span data-stu-id="01c73-125">- Request sample</span></span> <br/><span data-ttu-id="01c73-126">- Restreindre l’exécution du code (cette action peut être annulée)</span><span class="sxs-lookup"><span data-stu-id="01c73-126">- Restrict code execution (this action can be undone)</span></span> <br/><span data-ttu-id="01c73-127">- Exécuter une analyse antivirus</span><span class="sxs-lookup"><span data-stu-id="01c73-127">- Run antivirus scan</span></span> <br/><span data-ttu-id="01c73-128">- Arrêter et mettre en quarantaine</span><span class="sxs-lookup"><span data-stu-id="01c73-128">- Stop and quarantine</span></span>      |<span data-ttu-id="01c73-129">- Bloquer l’URL (heure du clic)</span><span class="sxs-lookup"><span data-stu-id="01c73-129">- Block URL (time-of-click)</span></span><br/><span data-ttu-id="01c73-130">- Suppression de messages électroniques ou de clusters de suppression (soft)</span><span class="sxs-lookup"><span data-stu-id="01c73-130">- Soft delete email messages or clusters</span></span><br/><span data-ttu-id="01c73-131">- E-mail de mise en quarantaine</span><span class="sxs-lookup"><span data-stu-id="01c73-131">- Quarantine email</span></span><br/><span data-ttu-id="01c73-132">- Mettre en quarantaine une pièce jointe d’un e-mail</span><span class="sxs-lookup"><span data-stu-id="01c73-132">- Quarantine an email attachment</span></span><br/><span data-ttu-id="01c73-133">- Désactiver le forwarding de courrier externe</span><span class="sxs-lookup"><span data-stu-id="01c73-133">- Turn off external mail forwarding</span></span>          |

<span data-ttu-id="01c73-134">Les actions de correction, qu’elles soient en attente d’approbation ou déjà terminées, peuvent être vues dans le centre [de correction.](m365d-action-center.md)</span><span class="sxs-lookup"><span data-stu-id="01c73-134">Remediation actions, whether pending approval or already complete, can be viewed in the [Action Center](m365d-action-center.md).</span></span>

## <a name="remediation-actions-that-follow-automated-investigations"></a><span data-ttu-id="01c73-135">Actions de correction qui suivent des enquêtes automatisées</span><span class="sxs-lookup"><span data-stu-id="01c73-135">Remediation actions that follow automated investigations</span></span>

<span data-ttu-id="01c73-136">Lorsqu’une enquête automatisée se termine, un verdict est atteint pour chaque élément de preuve impliqué.</span><span class="sxs-lookup"><span data-stu-id="01c73-136">When an automated investigation completes, a verdict is reached for every piece of evidence involved.</span></span> <span data-ttu-id="01c73-137">Selon le verdict, les actions de correction sont identifiées.</span><span class="sxs-lookup"><span data-stu-id="01c73-137">Depending on the verdict, remediation actions are identified.</span></span> <span data-ttu-id="01c73-138">Dans certains cas, des actions de correction sont effectuées automatiquement. dans d’autres cas, les actions de correction attendent une approbation.</span><span class="sxs-lookup"><span data-stu-id="01c73-138">In some cases, remediation actions are taken automatically; in other cases, remediation actions await approval.</span></span> <span data-ttu-id="01c73-139">Tout dépend de la façon dont [l’examen et la réponse automatisés sont configurés.](m365d-configure-auto-investigation-response.md)</span><span class="sxs-lookup"><span data-stu-id="01c73-139">It all depends on how [automated investigation and response is configured](m365d-configure-auto-investigation-response.md).</span></span>

<span data-ttu-id="01c73-140">Le tableau suivant répertorie les verdicts et résultats possibles :</span><span class="sxs-lookup"><span data-stu-id="01c73-140">The following table lists possible verdicts and outcomes:</span></span>

| <span data-ttu-id="01c73-141">Verdict</span><span class="sxs-lookup"><span data-stu-id="01c73-141">Verdict</span></span>    | <span data-ttu-id="01c73-142">Domaine</span><span class="sxs-lookup"><span data-stu-id="01c73-142">Area</span></span>    | <span data-ttu-id="01c73-143">Résultats</span><span class="sxs-lookup"><span data-stu-id="01c73-143">Outcomes</span></span>|
|------|------|------|
| <span data-ttu-id="01c73-144">Malveillant</span><span class="sxs-lookup"><span data-stu-id="01c73-144">Malicious</span></span>    | <span data-ttu-id="01c73-145">Appareils (points de terminaison)</span><span class="sxs-lookup"><span data-stu-id="01c73-145">Devices (endpoints)</span></span>    | <span data-ttu-id="01c73-146">Des mesures correctives sont prises automatiquement [](m365d-configure-auto-investigation-response.md#review-or-change-the-automation-level-for-device-groups) (en supposant que les groupes d’appareils de votre organisation sont entièrement corrects - corriger **les menaces automatiquement)**</span><span class="sxs-lookup"><span data-stu-id="01c73-146">Remediation actions are taken automatically (assuming your organization's [device groups](m365d-configure-auto-investigation-response.md#review-or-change-the-automation-level-for-device-groups) are set to **Full - remediate threats automatically**)</span></span>|
| <span data-ttu-id="01c73-147">Malveillant</span><span class="sxs-lookup"><span data-stu-id="01c73-147">Malicious</span></span>    | <span data-ttu-id="01c73-148">Contenu de l’e-mail (URL ou pièces jointes)</span><span class="sxs-lookup"><span data-stu-id="01c73-148">Email content (URLs or attachments)</span></span> | <span data-ttu-id="01c73-149">Les actions de correction recommandées sont en attente d’approbation</span><span class="sxs-lookup"><span data-stu-id="01c73-149">Recommended remediation actions are pending approval</span></span>|
| <span data-ttu-id="01c73-150">Suspect</span><span class="sxs-lookup"><span data-stu-id="01c73-150">Suspicious</span></span>    | <span data-ttu-id="01c73-151">Appareils ou contenu de l’e-mail</span><span class="sxs-lookup"><span data-stu-id="01c73-151">Devices or email content</span></span> | <span data-ttu-id="01c73-152">Les actions de correction recommandées sont en attente d’approbation</span><span class="sxs-lookup"><span data-stu-id="01c73-152">Recommended remediation actions are pending approval</span></span>|
| <span data-ttu-id="01c73-153">Aucune menace détectée</span><span class="sxs-lookup"><span data-stu-id="01c73-153">No threats found</span></span>    | <span data-ttu-id="01c73-154">Appareils ou contenu de l’e-mail</span><span class="sxs-lookup"><span data-stu-id="01c73-154">Devices or email content</span></span>    | <span data-ttu-id="01c73-155">Aucune action de correction n’est nécessaire</span><span class="sxs-lookup"><span data-stu-id="01c73-155">No remediation actions are needed</span></span>|


## <a name="remediation-actions-that-are-taken-manually"></a><span data-ttu-id="01c73-156">Mesures correctives prises manuellement</span><span class="sxs-lookup"><span data-stu-id="01c73-156">Remediation actions that are taken manually</span></span>

<span data-ttu-id="01c73-157">En plus des actions de correction qui suivent des enquêtes automatisées, votre équipe des opérations de sécurité peut prendre certaines mesures correctives manuellement.</span><span class="sxs-lookup"><span data-stu-id="01c73-157">In addition to remediation actions that follow automated investigations, your security operations team can take certain remediation actions manually.</span></span> <span data-ttu-id="01c73-158">Il s’agit notamment des actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="01c73-158">These include the following actions:</span></span>

- <span data-ttu-id="01c73-159">Action manuelle de l’appareil, telle que l’isolation de l’appareil ou la mise en quarantaine du fichier.</span><span class="sxs-lookup"><span data-stu-id="01c73-159">Manual device action, such as device isolation or file quarantine.</span></span>
- <span data-ttu-id="01c73-160">Action de messagerie manuelle, telle que la suppression possible des messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="01c73-160">Manual email action, such as soft-deleting email messages.</span></span> 
- <span data-ttu-id="01c73-161">[Action de recherche](../defender-endpoint/advanced-hunting-overview.md) avancée sur les appareils ou les e-mails.</span><span class="sxs-lookup"><span data-stu-id="01c73-161">[Advanced hunting](../defender-endpoint/advanced-hunting-overview.md) action on devices or email.</span></span>
- <span data-ttu-id="01c73-162">[Action de](../defender-365-security/threat-explorer.md) l’Explorateur sur le contenu du courrier électronique, telle que le déplacement du courrier électronique vers le courrier indésirable, la suppression possible ou la suppression de courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="01c73-162">[Explorer](../defender-365-security/threat-explorer.md) action on email content, such as moving email to junk, soft-deleting email, or hard-deleting email.</span></span>
- <span data-ttu-id="01c73-163">Action [de réponse en direct](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/live-response) manuelle, telle que la suppression d’un fichier, l’arrêt d’un processus et la suppression d’une tâche programmée.</span><span class="sxs-lookup"><span data-stu-id="01c73-163">Manual [live response](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/live-response) action, such as deleting a file, stopping a process, and removing a scheduled task.</span></span>
- <span data-ttu-id="01c73-164">Action de réponse en direct [avec les API microsoft Defender pour](../defender-endpoint/management-apis.md#microsoft-defender-for-endpoint-apis)les points de terminaison, telles que l’isolation d’un appareil, l’exécution d’une analyse antivirus et l’obtention d’informations sur un fichier.</span><span class="sxs-lookup"><span data-stu-id="01c73-164">Live response action with [Microsoft Defender for Endpoint APIs](../defender-endpoint/management-apis.md#microsoft-defender-for-endpoint-apis), such as isolating a device, running an antivirus scan, and getting information about a file.</span></span> 

## <a name="next-steps"></a><span data-ttu-id="01c73-165">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="01c73-165">Next steps</span></span>

- [<span data-ttu-id="01c73-166">Visiter le Centre de notifications</span><span class="sxs-lookup"><span data-stu-id="01c73-166">Visit the Action center</span></span>](m365d-action-center.md)
- [<span data-ttu-id="01c73-167">Afficher et gérer les actions de correction</span><span class="sxs-lookup"><span data-stu-id="01c73-167">View and manage remediation actions</span></span>]( m365d-autoir-actions.md)
- [<span data-ttu-id="01c73-168">Gérer les faux positifs/négatifs dans les fonctionnalités automatisées d’examen et de réponse</span><span class="sxs-lookup"><span data-stu-id="01c73-168">Handle false positives/negatives in automated investigation and response capabilities</span></span>](m365d-autoir-report-false-positives-negatives.md)
