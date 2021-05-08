---
title: Examen et réponse automatisés dans Microsoft 365 Defender
description: Obtenir une vue d’ensemble des fonctionnalités d’examen et de réponse automatisées, également appelées auto-ressource, dans Microsoft 365 Defender
keywords: automatisé, examen, alerte, déclencheur, action, correction, réparation automatique
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
ms.topic: conceptual
ms.custom: autoir
ms.reviewer: evaldm, isco
ms.technology: m365d
ms.openlocfilehash: fcb7283faed6fe8c5af59cedeeb90577b557ab34
ms.sourcegitcommit: 5a1cb7d95070eef47d401a4693cc137a90550a5e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/06/2021
ms.locfileid: "52259534"
---
# <a name="automated-investigation-and-response-in-microsoft-365-defender"></a><span data-ttu-id="808e5-104">Examen et réponse automatisés dans Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="808e5-104">Automated investigation and response in Microsoft 365 Defender</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

<span data-ttu-id="808e5-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="808e5-105">**Applies to:**</span></span>
- <span data-ttu-id="808e5-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="808e5-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="808e5-107">Si votre organisation utilise [Microsoft 365 Defender,](microsoft-365-defender.md)votre équipe des opérations de sécurité reçoit une alerte dans le centre de sécurité Microsoft 365 chaque fois qu’une activité ou un artefact malveillant ou suspect est détecté.</span><span class="sxs-lookup"><span data-stu-id="808e5-107">If your organization is using [Microsoft 365 Defender](microsoft-365-defender.md), your security operations team receives an alert within the Microsoft 365 security center whenever a malicious or suspicious activity or artifact is detected.</span></span> <span data-ttu-id="808e5-108">Étant donné le flux sans fin des menaces qui peuvent survenir, les équipes de sécurité doivent souvent relever le défi de traiter le volume élevé d’alertes.</span><span class="sxs-lookup"><span data-stu-id="808e5-108">Given the seemingly never-ending flow of threats that can come in, security teams often face the challenge of addressing the high volume of alerts.</span></span> <span data-ttu-id="808e5-109">Heureusement, Microsoft 365 Defender inclut des fonctionnalités d’investigation et de correction automatisées (AIR) qui peuvent aider votre équipe des opérations de sécurité à gérer les menaces plus efficacement et efficacement.</span><span class="sxs-lookup"><span data-stu-id="808e5-109">Fortunately, Microsoft 365 Defender includes automated investigation and remediation (AIR) capabilities that can help your security operations team address threats more efficiently and effectively.</span></span>

<span data-ttu-id="808e5-110">Cet article fournit une vue d’ensemble d’AIR et inclut des liens vers les étapes suivantes et des ressources supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="808e5-110">This article provides an overview of AIR and includes links to next steps and additional resources.</span></span>

> [!TIP]
> <span data-ttu-id="808e5-111">Vous voulez essayer Microsoft 365 Defender ?</span><span class="sxs-lookup"><span data-stu-id="808e5-111">Want to experience Microsoft 365 Defender?</span></span> <span data-ttu-id="808e5-112">Vous pouvez [l’évaluer dans un environnement de laboratoire](m365d-evaluation.md?ocid=cx-docs-MTPtriallab) ou [exécuter votre projet pilote en production](m365d-pilot.md?ocid=cx-evalpilot).</span><span class="sxs-lookup"><span data-stu-id="808e5-112">You can [evaluate it in a lab environment](m365d-evaluation.md?ocid=cx-docs-MTPtriallab) or [run your pilot project in production](m365d-pilot.md?ocid=cx-evalpilot).</span></span>

## <a name="how-automated-investigation-and-self-healing-works"></a><span data-ttu-id="808e5-113">Fonctionnement de l’examen automatisé et de la auto-ressource</span><span class="sxs-lookup"><span data-stu-id="808e5-113">How automated investigation and self-healing works</span></span>

<span data-ttu-id="808e5-114">Lorsque des alertes de sécurité sont déclenchées, c’est à votre équipe des opérations de sécurité d’examiner ces alertes et de prendre les mesures nécessaires pour protéger votre organisation.</span><span class="sxs-lookup"><span data-stu-id="808e5-114">As security alerts are triggered, it's up to your security operations team to look into those alerts and take steps to protect your organization.</span></span> <span data-ttu-id="808e5-115">La hiérarchisation et l’examen des alertes peuvent prendre beaucoup de temps, en particulier lorsque de nouvelles alertes continuent d’arriver pendant qu’un examen est en cours.</span><span class="sxs-lookup"><span data-stu-id="808e5-115">Prioritizing and investigating alerts can be very time consuming, especially when new alerts keep coming in while an investigation is going on.</span></span> <span data-ttu-id="808e5-116">Les équipes en charge des opérations de sécurité peuvent être submergées par le volume des menaces qu’elles doivent gérer.</span><span class="sxs-lookup"><span data-stu-id="808e5-116">Security operations teams can feel overwhelmed by the sheer volume of threats they must monitor and protect against.</span></span> <span data-ttu-id="808e5-117">Les fonctionnalités automatisées d’examen et de réponse, avec auto-Microsoft 365 Defender peuvent vous aider.</span><span class="sxs-lookup"><span data-stu-id="808e5-117">Automated investigation and response capabilities, with self-healing, in Microsoft 365 Defender can help.</span></span>

<span data-ttu-id="808e5-118">Regardez la vidéo suivante pour voir comment fonctionne la auto-ressource :</span><span class="sxs-lookup"><span data-stu-id="808e5-118">Watch the following video to see how self-healing works:</span></span> <p>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4BzwB]

<span data-ttu-id="808e5-119">Dans Microsoft 365 Defender, l’examen et la réponse automatisés avec des fonctionnalités de auto-cicatrisation fonctionnent sur vos appareils, vos & de messagerie et vos identités.</span><span class="sxs-lookup"><span data-stu-id="808e5-119">In Microsoft 365 Defender, automated investigation and response with self-healing capabilities works across your devices, email & content, and identities.</span></span>
 
> [!TIP]
> <span data-ttu-id="808e5-120">Cet article décrit le fonctionnement de l’examen et de la réponse automatisés.</span><span class="sxs-lookup"><span data-stu-id="808e5-120">This article describes how automated investigation and response works.</span></span> <span data-ttu-id="808e5-121">Pour configurer ces fonctionnalités, voir [Configurer des fonctionnalités d’investigation](m365d-configure-auto-investigation-response.md)et de réponse automatisées dans Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="808e5-121">To configure these capabilities, see [Configure automated investigation and response capabilities in Microsoft 365 Defender](m365d-configure-auto-investigation-response.md).</span></span>

## <a name="your-own-virtual-analyst"></a><span data-ttu-id="808e5-122">Votre propre analyste virtuel</span><span class="sxs-lookup"><span data-stu-id="808e5-122">Your own virtual analyst</span></span>

<span data-ttu-id="808e5-123">Imagine un analyste virtuel dans votre équipe des opérations de sécurité de niveau 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="808e5-123">Imagine having a virtual analyst in your Tier 1 or Tier 2 security operations team.</span></span> <span data-ttu-id="808e5-124">L’analyste virtuel est fidèle aux étapes recommandées par les opérations de sécurité pour examiner et corriger les menaces.</span><span class="sxs-lookup"><span data-stu-id="808e5-124">The virtual analyst mimics the ideal steps that security operations would take to investigate and remediate threats.</span></span> <span data-ttu-id="808e5-125">L’analyste virtuel peut travailler 24 heures sur 24, 7 jours sur 7, avec une capacité illimitée et prendre en charge une charge importante d’enquêtes et de correction des menaces.</span><span class="sxs-lookup"><span data-stu-id="808e5-125">The virtual analyst could work 24x7, with unlimited capacity, and take on a significant load of investigations and threat remediation.</span></span> <span data-ttu-id="808e5-126">Un tel analyste virtuel pourrait réduire considérablement le temps de réponse, libérant ainsi votre équipe des opérations de sécurité pour d’autres menaces importantes ou des projets stratégiques.</span><span class="sxs-lookup"><span data-stu-id="808e5-126">Such a virtual analyst could significantly reduce the time to respond, freeing up your security operations team for other important threats or strategic projects.</span></span> <span data-ttu-id="808e5-127">Si ce scénario ressemble à une science fictive, ce n’est pas le cas !</span><span class="sxs-lookup"><span data-stu-id="808e5-127">If this scenario sounds like science fiction, it's not!</span></span> <span data-ttu-id="808e5-128">Cet analyste virtuel fait partie de votre suite Microsoft 365 Defender, et son nom est examen *et réponse automatisés.*</span><span class="sxs-lookup"><span data-stu-id="808e5-128">Such a virtual analyst is part of your Microsoft 365 Defender suite, and its name is *automated investigation and response*.</span></span>

<span data-ttu-id="808e5-129">Les fonctionnalités d’examen et de réponse automatisées permettent à votre équipe en charge des opérations de sécurité d’augmenter considérablement la capacité de votre organisation à gérer les alertes et les incidents de sécurité.</span><span class="sxs-lookup"><span data-stu-id="808e5-129">Automated investigation and response capabilities enable your security operations team to dramatically increase your organization's capacity to deal with security alerts and incidents.</span></span> <span data-ttu-id="808e5-130">Grâce à l’examen et à la réponse automatisés, vous pouvez réduire le coût de traitement des activités d’examen et de correction et utiliser au mieux votre suite de protection contre les menaces.</span><span class="sxs-lookup"><span data-stu-id="808e5-130">With automated investigation and response, you can reduce the cost of dealing with investigation and remediation activities and get the most out of your threat protection suite.</span></span> <span data-ttu-id="808e5-131">Les fonctionnalités d’examen et de réponse automatisées aident votre équipe en matière d’opérations de sécurité en :</span><span class="sxs-lookup"><span data-stu-id="808e5-131">Automated investigation and response capabilities help your security operations team by:</span></span>

1. <span data-ttu-id="808e5-132">Déterminer si une menace nécessite une action.</span><span class="sxs-lookup"><span data-stu-id="808e5-132">Determining whether a threat requires action.</span></span>
2. <span data-ttu-id="808e5-133">Prendre (ou recommander) toutes les actions de correction nécessaires.</span><span class="sxs-lookup"><span data-stu-id="808e5-133">Taking (or recommending) any necessary remediation actions.</span></span>
3. <span data-ttu-id="808e5-134">Déterminer si et quelles autres enquêtes doivent se produire.</span><span class="sxs-lookup"><span data-stu-id="808e5-134">Determining whether and what other investigations should occur.</span></span>
4. <span data-ttu-id="808e5-135">répéter le processus autant de fois que nécessaire pour d’autres alertes.</span><span class="sxs-lookup"><span data-stu-id="808e5-135">Repeating the process as necessary for other alerts.</span></span>

## <a name="the-automated-investigation-process"></a><span data-ttu-id="808e5-136">Processus d’examen automatisé</span><span class="sxs-lookup"><span data-stu-id="808e5-136">The automated investigation process</span></span>

<span data-ttu-id="808e5-137">Une alerte crée un incident, qui peut démarrer une enquête automatisée.</span><span class="sxs-lookup"><span data-stu-id="808e5-137">An alert creates an incident, which can start an automated investigation.</span></span> <span data-ttu-id="808e5-138">L’enquête automatisée entraîne un verdict pour chaque élément de preuve.</span><span class="sxs-lookup"><span data-stu-id="808e5-138">The automated investigation results in a verdict for each piece of evidence.</span></span> <span data-ttu-id="808e5-139">Les verdicts peuvent être :</span><span class="sxs-lookup"><span data-stu-id="808e5-139">Verdicts can be:</span></span>
- <span data-ttu-id="808e5-140">*Malveillant*</span><span class="sxs-lookup"><span data-stu-id="808e5-140">*Malicious*</span></span>
- <span data-ttu-id="808e5-141">*Suspect*</span><span class="sxs-lookup"><span data-stu-id="808e5-141">*Suspicious*</span></span> 
- <span data-ttu-id="808e5-142">*Aucune menace détectée*</span><span class="sxs-lookup"><span data-stu-id="808e5-142">*No threats found*</span></span> 

<span data-ttu-id="808e5-143">Les actions de correction pour les entités malveillantes ou suspectes sont identifiées.</span><span class="sxs-lookup"><span data-stu-id="808e5-143">Remediation actions for malicious or suspicious entities are identified.</span></span> <span data-ttu-id="808e5-144">Voici quelques exemples d’actions de correction :</span><span class="sxs-lookup"><span data-stu-id="808e5-144">Examples of remediation actions include:</span></span>

- <span data-ttu-id="808e5-145">Envoi d’un fichier en quarantaine</span><span class="sxs-lookup"><span data-stu-id="808e5-145">Sending a file to quarantine</span></span>
- <span data-ttu-id="808e5-146">Arrêt d’un processus</span><span class="sxs-lookup"><span data-stu-id="808e5-146">Stopping a process</span></span>
- <span data-ttu-id="808e5-147">Isolation d’un appareil</span><span class="sxs-lookup"><span data-stu-id="808e5-147">Isolating a device</span></span>
- <span data-ttu-id="808e5-148">Blocage d’une URL</span><span class="sxs-lookup"><span data-stu-id="808e5-148">Blocking a URL</span></span> 
- <span data-ttu-id="808e5-149">Autres actions</span><span class="sxs-lookup"><span data-stu-id="808e5-149">Other actions</span></span>

<span data-ttu-id="808e5-150">Pour plus d’informations, voir [actions de correction dans Microsoft 365 Defender](m365d-remediation-actions.md).</span><span class="sxs-lookup"><span data-stu-id="808e5-150">For more information, see See [Remediation actions in Microsoft 365 Defender](m365d-remediation-actions.md).</span></span>

<span data-ttu-id="808e5-151">Selon la [façon dont les](m365d-configure-auto-investigation-response.md) fonctionnalités d’examen et de réponse automatisées sont configurées pour votre organisation, des mesures correctives sont prises automatiquement ou uniquement après approbation par votre équipe des opérations de sécurité.</span><span class="sxs-lookup"><span data-stu-id="808e5-151">Depending on [how automated investigation and response capabilities are configured](m365d-configure-auto-investigation-response.md) for your organization, remediation actions are taken automatically or only upon approval by your security operations team.</span></span> <span data-ttu-id="808e5-152">Toutes les actions, en attente ou terminées, sont répertoriées dans le centre [de actions.](m365d-action-center.md)</span><span class="sxs-lookup"><span data-stu-id="808e5-152">All actions, whether pending or completed, are listed in the [Action center](m365d-action-center.md).</span></span>

<span data-ttu-id="808e5-153">Pendant l’exécution d’un examen, les autres alertes associées qui apparaissent sont ajoutées à l’examen jusqu’à la fin de l’opération.</span><span class="sxs-lookup"><span data-stu-id="808e5-153">While an investigation is running, any other related alerts that arise are added to the investigation until it completes.</span></span> <span data-ttu-id="808e5-154">Si une entité affectée est vue ailleurs, l’enquête automatisée étend son étendue pour inclure cette entité, et le processus d’examen se répète.</span><span class="sxs-lookup"><span data-stu-id="808e5-154">If an affected entity is seen elsewhere, the automated investigation expands its scope to include that entity, and the investigation process repeats.</span></span> 

<span data-ttu-id="808e5-155">Dans Microsoft 365 Defender, chaque enquête automatisée met en corrélation les signaux entre Microsoft Defender pour l’identité, Microsoft Defender pour point de terminaison et Microsoft Defender pour Office 365, comme résumé dans le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="808e5-155">In Microsoft 365 Defender, each automated investigation correlates signals across Microsoft Defender for Identity, Microsoft Defender for Endpoint, and Microsoft Defender for Office 365, as summarized in the following table:</span></span> 

|<span data-ttu-id="808e5-156">Entités</span><span class="sxs-lookup"><span data-stu-id="808e5-156">Entities</span></span> |<span data-ttu-id="808e5-157">Services de protection contre les menaces</span><span class="sxs-lookup"><span data-stu-id="808e5-157">Threat protection services</span></span>  |
|:---------|:---------|
|<span data-ttu-id="808e5-158">Appareils (également appelés points de terminaison ou ordinateurs)</span><span class="sxs-lookup"><span data-stu-id="808e5-158">Devices (also referred to as endpoints or machines)</span></span> |[<span data-ttu-id="808e5-159">Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="808e5-159">Defender for Endpoint</span></span>](../defender-endpoint/automated-investigations.md) |      
|<span data-ttu-id="808e5-160">Utilisateurs Active Directory locaux, comportement des entités et activités</span><span class="sxs-lookup"><span data-stu-id="808e5-160">On-premises Active Directory users, entity behavior, and activities</span></span>     |[<span data-ttu-id="808e5-161">Defender pour l’identité</span><span class="sxs-lookup"><span data-stu-id="808e5-161">Defender for Identity</span></span>](/azure-advanced-threat-protection/what-is-atp) |      
|<span data-ttu-id="808e5-162">Contenu du courrier électronique (messages électroniques qui peuvent contenir des fichiers et des URL)</span><span class="sxs-lookup"><span data-stu-id="808e5-162">Email content (email messages that can contain files and URLs)</span></span>     |[<span data-ttu-id="808e5-163">Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="808e5-163">Defender for Office 365</span></span>](../office-365-security/defender-for-office-365.md) |

> [!NOTE]
> <span data-ttu-id="808e5-164">Toutes les alertes ne déclenchent pas une enquête automatisée, et toutes les enquêtes n’entraînent pas des actions de correction automatisées.</span><span class="sxs-lookup"><span data-stu-id="808e5-164">Not every alert triggers an automated investigation, and not every investigation results in automated remediation actions.</span></span> <span data-ttu-id="808e5-165">Cela dépend de la façon dont l’examen et la réponse automatisés sont configurés pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="808e5-165">It depends on how automated investigation and response is configured for your organization.</span></span> <span data-ttu-id="808e5-166">Voir [Configurer les fonctionnalités d’examen et de réponse automatisées.](m365d-configure-auto-investigation-response.md)</span><span class="sxs-lookup"><span data-stu-id="808e5-166">See [Configure automated investigation and response capabilities](m365d-configure-auto-investigation-response.md).</span></span>

## <a name="viewing-a-list-of-investigations"></a><span data-ttu-id="808e5-167">Affichage d’une liste d’enquêtes</span><span class="sxs-lookup"><span data-stu-id="808e5-167">Viewing a list of investigations</span></span>

<span data-ttu-id="808e5-168">Pour afficher les enquêtes, consultez la page **Incidents.**</span><span class="sxs-lookup"><span data-stu-id="808e5-168">To view investigations, go to the **Incidents** page.</span></span> <span data-ttu-id="808e5-169">Sélectionnez un incident, puis l’onglet **Enquêtes.** Pour en savoir plus, consultez [les détails et les résultats d’une enquête automatisée.](m365d-autoir-results.md)</span><span class="sxs-lookup"><span data-stu-id="808e5-169">Select an incident, and then select the **Investigations** tab. To learn more, see [Details and results of an automated investigation](m365d-autoir-results.md).</span></span>


## <a name="next-steps"></a><span data-ttu-id="808e5-170">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="808e5-170">Next steps</span></span>

- [<span data-ttu-id="808e5-171">Voir les conditions préalables à l’examen et à la réponse automatisés</span><span class="sxs-lookup"><span data-stu-id="808e5-171">See the prerequisites for automated investigation and response</span></span>](m365d-configure-auto-investigation-response.md#prerequisites-for-automated-investigation-and-response-in-microsoft-365-defender)
- [<span data-ttu-id="808e5-172">Configurer l’examen et la réponse automatisés pour votre organisation</span><span class="sxs-lookup"><span data-stu-id="808e5-172">Configure automated investigation and response for your organization</span></span>](m365d-configure-auto-investigation-response.md)
- <span data-ttu-id="808e5-173">[En savoir plus sur le centre de notifications](m365d-action-center.md).</span><span class="sxs-lookup"><span data-stu-id="808e5-173">[Learn more about the Action center](m365d-action-center.md)</span></span>
