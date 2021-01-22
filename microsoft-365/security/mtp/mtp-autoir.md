---
title: Examen et réponse automatisés dans Microsoft 365 Defender
description: Obtenir une vue d’ensemble des fonctionnalités d’examen et de réponse automatisées, également appelées auto-ressource, dans Microsoft 365 Defender
keywords: automatisé, examen, alerte, déclencheur, action, correction, auto-réparation
search.appverid: met150
ms.prod: m365-security
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
ms.technology: m365d
ms.openlocfilehash: 905455e4cd70485e099f8005b5f8876b1a5d9caf
ms.sourcegitcommit: 855719ee21017cf87dfa98cbe62806763bcb78ac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/22/2021
ms.locfileid: "49930329"
---
# <a name="automated-investigation-and-response-in-microsoft-365-defender"></a><span data-ttu-id="8773f-104">Examen et réponse automatisés dans Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="8773f-104">Automated investigation and response in Microsoft 365 Defender</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="8773f-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="8773f-105">**Applies to:**</span></span>
- <span data-ttu-id="8773f-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="8773f-106">Microsoft 365 Defender</span></span>

> <span data-ttu-id="8773f-107">Vous souhaitez découvrir Microsoft 365 Defender ?</span><span class="sxs-lookup"><span data-stu-id="8773f-107">Want to experience Microsoft 365 Defender?</span></span> <span data-ttu-id="8773f-108">Vous pouvez [l’évaluer dans un environnement de laboratoire](https://aka.ms/mtp-trial-lab) ou exécuter votre projet pilote en [production.](https://aka.ms/m365d-pilotplaybook)</span><span class="sxs-lookup"><span data-stu-id="8773f-108">You can [evaluate it in a lab environment](https://aka.ms/mtp-trial-lab) or [run your pilot project in production](https://aka.ms/m365d-pilotplaybook).</span></span>
>

## <a name="how-automated-investigation-and-self-healing-works"></a><span data-ttu-id="8773f-109">Fonctionnement de l’examen automatisé et de la auto-ressource</span><span class="sxs-lookup"><span data-stu-id="8773f-109">How automated investigation and self-healing works</span></span>

<span data-ttu-id="8773f-110">Lorsque des alertes de sécurité sont déclenchées, c’est à votre équipe des opérations de sécurité d’examiner ces alertes et de prendre les mesures nécessaires pour protéger votre organisation.</span><span class="sxs-lookup"><span data-stu-id="8773f-110">As security alerts are triggered, it's up to your security operations team to look into those alerts and take steps to protect your organization.</span></span> <span data-ttu-id="8773f-111">La hiérarchisation et l’examen des alertes peuvent prendre beaucoup de temps, en particulier lorsque de nouvelles alertes continuent d’arriver pendant qu’un examen est en cours.</span><span class="sxs-lookup"><span data-stu-id="8773f-111">Prioritizing and investigating alerts can be very time consuming, especially when new alerts keep coming in while an investigation is going on.</span></span> <span data-ttu-id="8773f-112">Les équipes en charge des opérations de sécurité peuvent être submergées par le volume des menaces qu’elles doivent gérer.</span><span class="sxs-lookup"><span data-stu-id="8773f-112">Security operations teams can feel overwhelmed by the sheer volume of threats they must monitor and protect against.</span></span> <span data-ttu-id="8773f-113">Les fonctionnalités automatisées d’examen et de réponse, avec auto-ressource, dans Microsoft 365 Defender peuvent vous aider.</span><span class="sxs-lookup"><span data-stu-id="8773f-113">Automated investigation and response capabilities, with self-healing, in Microsoft 365 Defender can help.</span></span>

<span data-ttu-id="8773f-114">Regardez la vidéo suivante pour voir comment fonctionne la auto-ressource :</span><span class="sxs-lookup"><span data-stu-id="8773f-114">Watch the following video to see how self-healing works:</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4BzwB]

<span data-ttu-id="8773f-115">Dans Microsoft 365 Defender, l’examen et la réponse automatisés grâce à des fonctionnalités de auto-ressource fonctionnent sur vos appareils, vos & de messagerie et vos identités.</span><span class="sxs-lookup"><span data-stu-id="8773f-115">In Microsoft 365 Defender, automated investigation and response with self-healing capabilities works across your devices, email & content, and identities.</span></span>
 
> [!TIP]
> <span data-ttu-id="8773f-116">Cet article décrit le fonctionnement de l’examen et de la réponse automatisés.</span><span class="sxs-lookup"><span data-stu-id="8773f-116">This article describes how automated investigation and response works.</span></span> <span data-ttu-id="8773f-117">Pour configurer ces fonctionnalités, voir Configurer les fonctionnalités d’investigation et de réponse [automatisées dans Microsoft 365 Defender.](mtp-configure-auto-investigation-response.md)</span><span class="sxs-lookup"><span data-stu-id="8773f-117">To configure these capabilities, see [Configure automated investigation and response capabilities in Microsoft 365 Defender](mtp-configure-auto-investigation-response.md).</span></span>

## <a name="your-own-virtual-analyst"></a><span data-ttu-id="8773f-118">Votre propre analyste virtuel</span><span class="sxs-lookup"><span data-stu-id="8773f-118">Your own virtual analyst</span></span>

<span data-ttu-id="8773f-119">Imaginez un analyste virtuel au sein de votre équipe de sécurité de niveau 1/2.</span><span class="sxs-lookup"><span data-stu-id="8773f-119">Imagine having a virtual analyst in your Tier 1 / Tier 2 security operations team.</span></span> <span data-ttu-id="8773f-120">L’analyste virtuel est fidèle aux étapes recommandées par les opérations de sécurité pour examiner et corriger les menaces.</span><span class="sxs-lookup"><span data-stu-id="8773f-120">The virtual analyst mimics the ideal steps that security operations would take to investigate and remediate threats.</span></span> <span data-ttu-id="8773f-121">L’assistant virtuel peut fonctionner 24h/24, 7j/7, avec une capacité illimitée et une charge considérable d’examens et de correction des menaces.</span><span class="sxs-lookup"><span data-stu-id="8773f-121">The virtual assistant could work 24x7, with unlimited capacity, and take on a significant load of investigations and threat remediation.</span></span> <span data-ttu-id="8773f-122">Un assistant virtuel pourrait considérablement réduire le temps de réponse, libérant ainsi l’équipe en charge des opérations de sécurité pour d’autres projets stratégiques importants.</span><span class="sxs-lookup"><span data-stu-id="8773f-122">Such a virtual assistant could significantly reduce the time to respond, freeing up your security operations team for other important strategic projects.</span></span> <span data-ttu-id="8773f-123">Si ce scénario ressemble à une science fictive, ce n’est pas le cas !</span><span class="sxs-lookup"><span data-stu-id="8773f-123">If this scenario sounds like science fiction, it's not!</span></span> <span data-ttu-id="8773f-124">Cet analyste virtuel fait partie de votre suite Microsoft 365 Defender et son nom est examen et *réponse automatisés.*</span><span class="sxs-lookup"><span data-stu-id="8773f-124">Such a virtual analyst is part of your Microsoft 365 Defender suite, and its name is *automated investigation and response*.</span></span>

<span data-ttu-id="8773f-125">L’examen et la réponse automatisés permettent à votre équipe en charge des opérations de sécurité d’augmenter considérablement la capacité de votre organisation à gérer les alertes et les incidents de sécurité.</span><span class="sxs-lookup"><span data-stu-id="8773f-125">Automated investigation and response enables your security operations team to dramatically increase your organization's capacity to deal with security alerts and incidents.</span></span> <span data-ttu-id="8773f-126">Grâce à l’examen et à la réponse automatisés, vous pouvez réduire le coût de traitement des activités d’examen et de correction et utiliser au mieux votre suite de protection contre les menaces.</span><span class="sxs-lookup"><span data-stu-id="8773f-126">With automated investigation and response, you can reduce the cost of dealing with investigation and remediation activities and get the most out of your threat protection suite.</span></span> <span data-ttu-id="8773f-127">L’examen et la réponse automatisés aident votre équipe en matière d’opérations de sécurité en :</span><span class="sxs-lookup"><span data-stu-id="8773f-127">automated investigation and response helps your security operations team by:</span></span>

1. <span data-ttu-id="8773f-128">déterminer si une menace nécessite une action ;</span><span class="sxs-lookup"><span data-stu-id="8773f-128">Determining whether a threat requires action;</span></span>
2. <span data-ttu-id="8773f-129">effectuer (ou recommander) les actions de correction nécessaires ;</span><span class="sxs-lookup"><span data-stu-id="8773f-129">Performing (or recommending) any necessary remediation actions;</span></span>
3. <span data-ttu-id="8773f-130">déterminer des examens supplémentaires qui doivent avoir lieu ; et</span><span class="sxs-lookup"><span data-stu-id="8773f-130">Determining what additional investigations should occur; and</span></span>
4. <span data-ttu-id="8773f-131">répéter le processus autant de fois que nécessaire pour d’autres alertes.</span><span class="sxs-lookup"><span data-stu-id="8773f-131">Repeating the process as necessary for other alerts.</span></span>

## <a name="the-automated-investigation-process"></a><span data-ttu-id="8773f-132">Processus d’examen automatisé</span><span class="sxs-lookup"><span data-stu-id="8773f-132">The automated investigation process</span></span>

<span data-ttu-id="8773f-133">**Alerte** > **incident** > **examen automatisé** > **verdict** > **action de correction**</span><span class="sxs-lookup"><span data-stu-id="8773f-133">**Alert** > **incident** > **automated investigation** > **verdict** > **remediation action**</span></span>

<span data-ttu-id="8773f-134">Une alerte déclenchée crée un incident, qui peut démarrer une enquête automatisée.</span><span class="sxs-lookup"><span data-stu-id="8773f-134">A triggered alert creates an incident, which can start an automated investigation.</span></span> <span data-ttu-id="8773f-135">Cet examen peut donner lieu à une ou plusieurs actions de correction.</span><span class="sxs-lookup"><span data-stu-id="8773f-135">That investigation can result in one or more remediation actions.</span></span> <span data-ttu-id="8773f-136">Dans Microsoft 365 Defender, chaque enquête automatisée met en corrélation les signaux entre Microsoft Defender pour l’identité, Microsoft Defender pour le point de terminaison et Defender pour Office 365, comme résumé dans le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="8773f-136">In Microsoft 365 Defender, each automated investigation correlates signals across Microsoft Defender for Identity, Microsoft Defender for Endpoint, and Defender for Office 365, as summarized in the following table:</span></span> 

|<span data-ttu-id="8773f-137">Entités</span><span class="sxs-lookup"><span data-stu-id="8773f-137">Entities</span></span> |<span data-ttu-id="8773f-138">Services de protection contre les menaces</span><span class="sxs-lookup"><span data-stu-id="8773f-138">Threat protection services</span></span>  |
|---------|---------|
|<span data-ttu-id="8773f-139">Appareils (également appelés points de terminaison)</span><span class="sxs-lookup"><span data-stu-id="8773f-139">Devices (also referred to as endpoints)</span></span>     |[<span data-ttu-id="8773f-140">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="8773f-140">Microsoft Defender for Endpoint</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/automated-investigations)<br/>[<span data-ttu-id="8773f-141">Microsoft Defender pour Identity</span><span class="sxs-lookup"><span data-stu-id="8773f-141">Microsoft Defender for Identity</span></span>](https://docs.microsoft.com/azure-advanced-threat-protection/what-is-atp) |      
|<span data-ttu-id="8773f-142">Contenu de l’e-mail (fichiers et messages dans les boîtes aux lettres)</span><span class="sxs-lookup"><span data-stu-id="8773f-142">Email content (files and messages in mailboxes)</span></span>     |[<span data-ttu-id="8773f-143">Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="8773f-143">Microsoft Defender for Office 365</span></span>](https://docs.microsoft.com/microsoft-365/security/office-365-security/office-365-atp)         |

<span data-ttu-id="8773f-144">Chaque enquête génère des verdicts *(malveillants,* suspects ou aucune menace *trouvée)* pour chaque élément de preuve examiné.</span><span class="sxs-lookup"><span data-stu-id="8773f-144">Each investigation generates verdicts (*Malicious*, *Suspicious*, or *No threats found*) for each piece of evidence investigated.</span></span> <span data-ttu-id="8773f-145">Selon le type de menace et le verdict qui en résulte, les actions de correction se produisent automatiquement ou après approbation par l’équipe des opérations de sécurité de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="8773f-145">Depending on the type of threat and resulting verdict, remediation actions occur automatically or upon approval by your organization's security operations team.</span></span> <span data-ttu-id="8773f-146">Les actions en attente et achevées sont répertoriées dans le [Centre de notifications](mtp-action-center.md).</span><span class="sxs-lookup"><span data-stu-id="8773f-146">Pending and completed actions are listed in the [Action center](mtp-action-center.md).</span></span>

<span data-ttu-id="8773f-147">Pendant l’exécution d’un examen, les autres alertes associées qui apparaissent sont ajoutées à l’examen jusqu’à la fin de l’opération.</span><span class="sxs-lookup"><span data-stu-id="8773f-147">While an investigation is running, any other related alerts that arise are added to the investigation until it completes.</span></span> <span data-ttu-id="8773f-148">Si une entité suspecte est détectée ailleurs, l’examen automatisée s’étend pour inclure cette entité, et un manuel de sécurité général s’exécute.</span><span class="sxs-lookup"><span data-stu-id="8773f-148">If an incriminated entity is seen elsewhere, the automated investigation will expand its scope to include that entity, and a general security playbook will run.</span></span> 

> [!NOTE]
> <span data-ttu-id="8773f-149">Toutes les alertes ne déclenchent pas une enquête automatisée, et toutes les enquêtes n’entraînent pas des actions de correction automatisées ; Tout dépend de la façon dont l’examen et la réponse automatisés sont configurés pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="8773f-149">Not every alert triggers an automated investigation, and not every investigation results in automated remediation actions; this all depends on how automated investigation and response is configured for your organization.</span></span> <span data-ttu-id="8773f-150">Voir Configurer les fonctionnalités d’investigation et de réponse [automatisées dans Microsoft 365 Defender.](mtp-configure-auto-investigation-response.md)</span><span class="sxs-lookup"><span data-stu-id="8773f-150">See [Configure automated investigation and response capabilities in Microsoft 365 Defender](mtp-configure-auto-investigation-response.md).</span></span>


## <a name="next-steps"></a><span data-ttu-id="8773f-151">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="8773f-151">Next steps</span></span>

- [<span data-ttu-id="8773f-152">Consultez les conditions préalables à l’examen et à la réponse automatisés dans Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="8773f-152">See the prerequisites for automated investigation and response in Microsoft 365 Defender</span></span>](mtp-configure-auto-investigation-response.md#prerequisites-for-automated-investigation-and-response-in-microsoft-365-defender)
- [<span data-ttu-id="8773f-153">Configurer l’examen et la réponse automatisés pour votre organisation</span><span class="sxs-lookup"><span data-stu-id="8773f-153">Configure automated investigation and response for your organization</span></span>](mtp-configure-auto-investigation-response.md)
- <span data-ttu-id="8773f-154">[En savoir plus sur le centre de notifications](mtp-action-center.md).</span><span class="sxs-lookup"><span data-stu-id="8773f-154">[Learn more about the Action center](mtp-action-center.md)</span></span>
