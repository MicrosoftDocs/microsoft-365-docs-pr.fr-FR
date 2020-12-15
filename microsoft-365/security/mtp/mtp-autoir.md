---
title: Recherche et réponse automatisées dans Microsoft 365 Defender
description: Obtenir une vue d’ensemble des fonctionnalités d’analyse et de réponse automatisées, également appelées auto-réparation, dans Microsoft 365 Defender
keywords: automatisation, examen, alerte, déclenchement, action, correction, auto-réparation
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
ms.date: 12/09/2020
ms.reviewer: evaldm, isco
ms.openlocfilehash: 7c28b7f3ac797f7402cfdb1f604fcef1e142a31b
ms.sourcegitcommit: 29eb89b8ba0628fbef350e8995d2c38369a4ffa2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/15/2020
ms.locfileid: "49683306"
---
# <a name="automated-investigation-and-response-in-microsoft-365-defender"></a><span data-ttu-id="e751d-104">Recherche et réponse automatisées dans Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="e751d-104">Automated investigation and response in Microsoft 365 Defender</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="e751d-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="e751d-105">**Applies to:**</span></span>
- <span data-ttu-id="e751d-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="e751d-106">Microsoft 365 Defender</span></span>

> <span data-ttu-id="e751d-107">Vous souhaitez découvrir Microsoft 365 Defender ?</span><span class="sxs-lookup"><span data-stu-id="e751d-107">Want to experience Microsoft 365 Defender?</span></span> <span data-ttu-id="e751d-108">Vous pouvez l' [évaluer dans un environnement de laboratoire](https://aka.ms/mtp-trial-lab) ou [exécuter votre projet pilote en production](https://aka.ms/m365d-pilotplaybook).</span><span class="sxs-lookup"><span data-stu-id="e751d-108">You can [evaluate it in a lab environment](https://aka.ms/mtp-trial-lab) or [run your pilot project in production](https://aka.ms/m365d-pilotplaybook).</span></span>
>

## <a name="how-automated-investigation-and-self-healing-works"></a><span data-ttu-id="e751d-109">Fonctionnement de l’enquête automatisée et de l’auto-réparation</span><span class="sxs-lookup"><span data-stu-id="e751d-109">How automated investigation and self-healing works</span></span>

<span data-ttu-id="e751d-110">À mesure que des alertes de sécurité sont déclenchées, c’est à votre équipe chargée des opérations de sécurité d’examiner ces alertes et de prendre des mesures pour protéger votre organisation.</span><span class="sxs-lookup"><span data-stu-id="e751d-110">As security alerts are triggered, it's up to your security operations team to look into those alerts and take steps to protect your organization.</span></span> <span data-ttu-id="e751d-111">La hiérarchisation et l’examen des alertes peuvent prendre beaucoup de temps, en particulier lorsque de nouvelles alertes continuent d’arriver pendant qu’un examen est en cours.</span><span class="sxs-lookup"><span data-stu-id="e751d-111">Prioritizing and investigating alerts can be very time consuming, especially when new alerts keep coming in while an investigation is going on.</span></span> <span data-ttu-id="e751d-112">Les équipes en charge des opérations de sécurité peuvent être submergées par le volume des menaces qu’elles doivent gérer.</span><span class="sxs-lookup"><span data-stu-id="e751d-112">Security operations teams can feel overwhelmed by the sheer volume of threats they must monitor and protect against.</span></span> <span data-ttu-id="e751d-113">Les fonctionnalités d’analyse et de réponse automatisées, avec autoréparation, dans Microsoft 365 Defender peuvent vous aider.</span><span class="sxs-lookup"><span data-stu-id="e751d-113">Automated investigation and response capabilities, with self-healing, in Microsoft 365 Defender can help.</span></span>

<span data-ttu-id="e751d-114">Regardez la vidéo suivante pour voir le fonctionnement de la réparation automatique :</span><span class="sxs-lookup"><span data-stu-id="e751d-114">Watch the following video to see how self-healing works:</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4BzwB]

<span data-ttu-id="e751d-115">Dans Microsoft 365 Defender, l’analyse et la réponse automatisées avec des fonctionnalités d’auto-réparation fonctionnent sur vos appareils, le contenu & le courrier électronique et les identités.</span><span class="sxs-lookup"><span data-stu-id="e751d-115">In Microsoft 365 Defender, automated investigation and response with self-healing capabilities works across your devices, email & content, and identities.</span></span>
 
> [!TIP]
> <span data-ttu-id="e751d-116">Cet article décrit le fonctionnement de l’instruction et de la réponse automatisées.</span><span class="sxs-lookup"><span data-stu-id="e751d-116">This article describes how automated investigation and response works.</span></span> <span data-ttu-id="e751d-117">Pour configurer ces fonctionnalités, consultez la rubrique [configure Automated State and Response Capabilities in Microsoft 365 Defender](mtp-configure-auto-investigation-response.md).</span><span class="sxs-lookup"><span data-stu-id="e751d-117">To configure these capabilities, see [Configure automated investigation and response capabilities in Microsoft 365 Defender](mtp-configure-auto-investigation-response.md).</span></span>

## <a name="your-own-virtual-analyst"></a><span data-ttu-id="e751d-118">Votre propre analyste virtuel</span><span class="sxs-lookup"><span data-stu-id="e751d-118">Your own virtual analyst</span></span>

<span data-ttu-id="e751d-119">Imaginez un analyste virtuel au sein de votre équipe de sécurité de niveau 1/2.</span><span class="sxs-lookup"><span data-stu-id="e751d-119">Imagine having a virtual analyst in your Tier 1 / Tier 2 security operations team.</span></span> <span data-ttu-id="e751d-120">L’analyste virtuel est fidèle aux étapes recommandées par les opérations de sécurité pour examiner et corriger les menaces.</span><span class="sxs-lookup"><span data-stu-id="e751d-120">The virtual analyst mimics the ideal steps that security operations would take to investigate and remediate threats.</span></span> <span data-ttu-id="e751d-121">L’assistant virtuel peut fonctionner 24h/24, 7j/7, avec une capacité illimitée et une charge considérable d’examens et de correction des menaces.</span><span class="sxs-lookup"><span data-stu-id="e751d-121">The virtual assistant could work 24x7, with unlimited capacity, and take on a significant load of investigations and threat remediation.</span></span> <span data-ttu-id="e751d-122">Un assistant virtuel pourrait considérablement réduire le temps de réponse, libérant ainsi l’équipe en charge des opérations de sécurité pour d’autres projets stratégiques importants.</span><span class="sxs-lookup"><span data-stu-id="e751d-122">Such a virtual assistant could significantly reduce the time to respond, freeing up your security operations team for other important strategic projects.</span></span> <span data-ttu-id="e751d-123">Si ce scénario ressemble à science fiction, ce n’est pas le cas.</span><span class="sxs-lookup"><span data-stu-id="e751d-123">If this scenario sounds like science fiction, it's not!</span></span> <span data-ttu-id="e751d-124">Un tel analyste virtuel fait partie de votre suite Microsoft 365 Defender, et son nom est l’analyse *et la réponse automatiques*.</span><span class="sxs-lookup"><span data-stu-id="e751d-124">Such a virtual analyst is part of your Microsoft 365 Defender suite, and its name is *automated investigation and response*.</span></span>

<span data-ttu-id="e751d-125">L’analyse et la réponse automatisées permettent à votre équipe d’opérations de sécurité d’augmenter considérablement la capacité de votre organisation à gérer les alertes et les incidents de sécurité.</span><span class="sxs-lookup"><span data-stu-id="e751d-125">Automated investigation and response enables your security operations team to dramatically increase your organization's capacity to deal with security alerts and incidents.</span></span> <span data-ttu-id="e751d-126">Grâce à l’analyse et à la réponse automatisées, vous pouvez réduire le coût de traitement des activités d’enquête et de correction et tirer le meilleur parti de votre suite de protection contre les menaces.</span><span class="sxs-lookup"><span data-stu-id="e751d-126">With automated investigation and response, you can reduce the cost of dealing with investigation and remediation activities and get the most out of your threat protection suite.</span></span> <span data-ttu-id="e751d-127">l’analyse et la réponse automatisées aident votre équipe chargée des opérations sur la sécurité à :</span><span class="sxs-lookup"><span data-stu-id="e751d-127">automated investigation and response helps your security operations team by:</span></span>

1. <span data-ttu-id="e751d-128">déterminer si une menace nécessite une action ;</span><span class="sxs-lookup"><span data-stu-id="e751d-128">Determining whether a threat requires action;</span></span>
2. <span data-ttu-id="e751d-129">effectuer (ou recommander) les actions de correction nécessaires ;</span><span class="sxs-lookup"><span data-stu-id="e751d-129">Performing (or recommending) any necessary remediation actions;</span></span>
3. <span data-ttu-id="e751d-130">déterminer des examens supplémentaires qui doivent avoir lieu ; et</span><span class="sxs-lookup"><span data-stu-id="e751d-130">Determining what additional investigations should occur; and</span></span>
4. <span data-ttu-id="e751d-131">répéter le processus autant de fois que nécessaire pour d’autres alertes.</span><span class="sxs-lookup"><span data-stu-id="e751d-131">Repeating the process as necessary for other alerts.</span></span>

## <a name="the-automated-investigation-process"></a><span data-ttu-id="e751d-132">Processus d’examen automatisé</span><span class="sxs-lookup"><span data-stu-id="e751d-132">The automated investigation process</span></span>

<span data-ttu-id="e751d-133">**Alerte** > **incident** > **examen automatisé** > **verdict** > **action de correction**</span><span class="sxs-lookup"><span data-stu-id="e751d-133">**Alert** > **incident** > **automated investigation** > **verdict** > **remediation action**</span></span>

<span data-ttu-id="e751d-134">Une alerte déclenchée crée un incident, qui peut lancer une enquête automatisée.</span><span class="sxs-lookup"><span data-stu-id="e751d-134">A triggered alert creates an incident, which can start an automated investigation.</span></span> <span data-ttu-id="e751d-135">Cet examen peut donner lieu à une ou plusieurs actions de correction.</span><span class="sxs-lookup"><span data-stu-id="e751d-135">That investigation can result in one or more remediation actions.</span></span> <span data-ttu-id="e751d-136">Dans Microsoft 365 Defender, chaque enquête automatisée établit une corrélation entre les signaux de Microsoft Defender pour l’identité, Microsoft Defender pour les points de terminaison et Defender pour Office 365, comme résumé dans le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="e751d-136">In Microsoft 365 Defender, each automated investigation correlates signals across Microsoft Defender for Identity, Microsoft Defender for Endpoint, and Defender for Office 365, as summarized in the following table:</span></span> 

|<span data-ttu-id="e751d-137">Entités</span><span class="sxs-lookup"><span data-stu-id="e751d-137">Entities</span></span> |<span data-ttu-id="e751d-138">Services de protection contre les menaces</span><span class="sxs-lookup"><span data-stu-id="e751d-138">Threat protection services</span></span>  |
|---------|---------|
|<span data-ttu-id="e751d-139">Appareils (également appelés points de terminaison)</span><span class="sxs-lookup"><span data-stu-id="e751d-139">Devices (also referred to as endpoints)</span></span>     |[<span data-ttu-id="e751d-140">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="e751d-140">Microsoft Defender for Endpoint</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/automated-investigations)<br/>[<span data-ttu-id="e751d-141">Microsoft Defender pour l’identité</span><span class="sxs-lookup"><span data-stu-id="e751d-141">Microsoft Defender for Identity</span></span>](https://docs.microsoft.com/azure-advanced-threat-protection/what-is-atp) |      
|<span data-ttu-id="e751d-142">Contenu de l’e-mail (fichiers et messages dans les boîtes aux lettres)</span><span class="sxs-lookup"><span data-stu-id="e751d-142">Email content (files and messages in mailboxes)</span></span>     |[<span data-ttu-id="e751d-143">Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="e751d-143">Microsoft Defender for Office 365</span></span>](https://docs.microsoft.com/microsoft-365/security/office-365-security/office-365-atp)         |

<span data-ttu-id="e751d-144">Chaque enquête génère des verdicts (*malveillants*, *suspects* ou *aucune menace détectée*) pour chaque preuve examinée.</span><span class="sxs-lookup"><span data-stu-id="e751d-144">Each investigation generates verdicts (*Malicious*, *Suspicious*, or *No threats found*) for each piece of evidence investigated.</span></span> <span data-ttu-id="e751d-145">Selon le type de menace et le verdict résultant, les actions de correction se produisent automatiquement ou après approbation de l’équipe des opérations de sécurité de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="e751d-145">Depending on the type of threat and resulting verdict, remediation actions occur automatically or upon approval by your organization's security operations team.</span></span> <span data-ttu-id="e751d-146">Les actions en attente et achevées sont répertoriées dans le [Centre de notifications](mtp-action-center.md).</span><span class="sxs-lookup"><span data-stu-id="e751d-146">Pending and completed actions are listed in the [Action center](mtp-action-center.md).</span></span>

<span data-ttu-id="e751d-147">Pendant l’exécution d’un examen, les autres alertes associées qui apparaissent sont ajoutées à l’examen jusqu’à la fin de l’opération.</span><span class="sxs-lookup"><span data-stu-id="e751d-147">While an investigation is running, any other related alerts that arise are added to the investigation until it completes.</span></span> <span data-ttu-id="e751d-148">Si une entité suspecte est détectée ailleurs, l’examen automatisée s’étend pour inclure cette entité, et un manuel de sécurité général s’exécute.</span><span class="sxs-lookup"><span data-stu-id="e751d-148">If an incriminated entity is seen elsewhere, the automated investigation will expand its scope to include that entity, and a general security playbook will run.</span></span> 

> [!NOTE]
> <span data-ttu-id="e751d-149">Toutes les alertes ne déclenchent pas une enquête automatisée, et toutes les recherches ne génèrent pas de mesures correctives automatisées ; tout cela dépend de la configuration de l’analyse et de la réponse automatisées pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="e751d-149">Not every alert triggers an automated investigation, and not every investigation results in automated remediation actions; this all depends on how automated investigation and response is configured for your organization.</span></span> <span data-ttu-id="e751d-150">Voir [configurer les fonctionnalités d’analyse et de réponse automatisées dans Microsoft 365 Defender](mtp-configure-auto-investigation-response.md).</span><span class="sxs-lookup"><span data-stu-id="e751d-150">See [Configure automated investigation and response capabilities in Microsoft 365 Defender](mtp-configure-auto-investigation-response.md).</span></span>


## <a name="next-steps"></a><span data-ttu-id="e751d-151">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="e751d-151">Next steps</span></span>

- [<span data-ttu-id="e751d-152">Voir la configuration requise pour l’analyse et la réponse automatisées dans Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="e751d-152">See the prerequisites for automated investigation and response in Microsoft 365 Defender</span></span>](mtp-configure-auto-investigation-response.md#prerequisites-for-automated-investigation-and-response-in-microsoft-365-defender)
- [<span data-ttu-id="e751d-153">Configurer une enquête et une réponse automatisées pour votre organisation</span><span class="sxs-lookup"><span data-stu-id="e751d-153">Configure automated investigation and response for your organization</span></span>](mtp-configure-auto-investigation-response.md)
- <span data-ttu-id="e751d-154">[En savoir plus sur le centre de notifications](mtp-action-center.md).</span><span class="sxs-lookup"><span data-stu-id="e751d-154">[Learn more about the Action center](mtp-action-center.md)</span></span>
