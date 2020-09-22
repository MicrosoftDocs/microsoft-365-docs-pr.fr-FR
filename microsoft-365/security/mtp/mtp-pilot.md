---
title: Exécuter votre projet pilote de protection contre les menaces Microsoft
description: Exécutez votre projet pilote Microsoft Threat Protection dans production pour déterminer efficacement les avantages et l’adoption de Microsoft Threat Protection (MTP).
keywords: Microsoft Threat Protection Pilot, exécuter le projet pilote de protection contre les menaces Microsoft, évaluer la protection de Microsoft contre les menaces en production, projet pilote de protection contre les menaces Microsoft, protection contre la vulnérabilité, protection avancée contre les menaces, sécurité des entreprises, périphériques, appareil, identité, utilisateurs, données, applications, incidents, recherche et correction automatiques, chasse avancée
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: microsoft-365-enterprise
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: dolmont
author: DulceMontemayor
ms.localizationpriority: medium
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: conceptual
ms.openlocfilehash: 88d92558d86e0aa2e90ef04d88a3cd4676386f15
ms.sourcegitcommit: c083602dda3cdcb5b58cb8aa070d77019075f765
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/22/2020
ms.locfileid: "48195626"
---
# <a name="run-your-pilot-microsoft-threat-protection-project"></a><span data-ttu-id="7ff1b-104">Exécuter votre projet pilote de protection contre les menaces Microsoft</span><span class="sxs-lookup"><span data-stu-id="7ff1b-104">Run your pilot Microsoft Threat Protection project</span></span> 

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="7ff1b-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="7ff1b-105">**Applies to:**</span></span>
- <span data-ttu-id="7ff1b-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="7ff1b-106">Microsoft Threat Protection</span></span>

<span data-ttu-id="7ff1b-107">Pour déterminer efficacement l’avantage et l’adoption de Microsoft Threat Protection (MTP), vous pouvez exécuter un projet pilote.</span><span class="sxs-lookup"><span data-stu-id="7ff1b-107">To effectively determine the benefit and adoption of Microsoft Threat Protection (MTP), you can run a pilot project.</span></span> <span data-ttu-id="7ff1b-108">Avant d’activer la protection Microsoft contre les menaces dans votre environnement de production et de commencer avec des cas d’utilisation définis, il est préférable de passer en revue un processus de planification afin de déterminer les tâches à accomplir dans ce projet pilote, ainsi que les critères de réussite.</span><span class="sxs-lookup"><span data-stu-id="7ff1b-108">Before enabling Microsoft Threat Protection in your production environment and starting with defined use cases, it is best to go through a planning process to determine the tasks that must be accomplished in this pilot project, and the success criteria.</span></span> 


## <a name="how-to-use-this-pilot-playbook"></a><span data-ttu-id="7ff1b-109">Utilisation de ce manuel pilote</span><span class="sxs-lookup"><span data-stu-id="7ff1b-109">How to use this pilot playbook</span></span>

<span data-ttu-id="7ff1b-110">Ce guide fournit une vue d’ensemble de la protection contre les menaces Microsoft, ainsi que des conseils détaillés sur la façon de configurer votre projet pilote.</span><span class="sxs-lookup"><span data-stu-id="7ff1b-110">This guide provides an overview of Microsoft Threat Protection and step-by-step guidance on how to set up your pilot project.</span></span> 

![Phases de l’exécution d’un programme pilote Microsoft Threat Protection](../../media/pilotphases.png)

<span data-ttu-id="7ff1b-112">L’exemple de chronologie suivant varie en fonction de l’utilisation des ressources appropriées dans votre environnement.</span><span class="sxs-lookup"><span data-stu-id="7ff1b-112">The following sample timeline varies depending on having the right resources in your environment.</span></span> <span data-ttu-id="7ff1b-113">Certains éléments détectés et les flux de travail peuvent nécessiter plus de temps d’apprentissage que les autres.</span><span class="sxs-lookup"><span data-stu-id="7ff1b-113">Some detections and workflows might need more learning time than the others.</span></span>

![Exemple de chronologie dans l’exécution d’un programme pilote Microsoft Threat Protection](../../media/pilotimeline.png)

>[!IMPORTANT]
><span data-ttu-id="7ff1b-115">Pour obtenir des résultats optimaux, suivez les instructions de pilote aussi étroitement que possible.</span><span class="sxs-lookup"><span data-stu-id="7ff1b-115">For optimum results, follow the pilot instructions as closely as possible.</span></span>


### <a name="pilot-playbook-phases"></a><span data-ttu-id="7ff1b-116">Phases du projet pilote</span><span class="sxs-lookup"><span data-stu-id="7ff1b-116">Pilot playbook phases</span></span> 

<span data-ttu-id="7ff1b-117">L’exécution d’un programme pilote Microsoft Threat Protection a quatre phases :</span><span class="sxs-lookup"><span data-stu-id="7ff1b-117">There are four phases in running a Microsoft Threat Protection pilot:</span></span>

|<span data-ttu-id="7ff1b-118">Phase</span><span class="sxs-lookup"><span data-stu-id="7ff1b-118">Phase</span></span> | <span data-ttu-id="7ff1b-119">Description</span><span class="sxs-lookup"><span data-stu-id="7ff1b-119">Description</span></span> | 
|:-------|:-----|
| <span data-ttu-id="7ff1b-120">![Planification](../../media/mtp/plan.png)</span><span class="sxs-lookup"><span data-stu-id="7ff1b-120">![Planning](../../media/mtp/plan.png)</span></span><br>[<span data-ttu-id="7ff1b-121">Planification</span><span class="sxs-lookup"><span data-stu-id="7ff1b-121">Planning</span></span>](mtp-pilot-plan.md)| <span data-ttu-id="7ff1b-122">Découvrez ce que vous devez prendre en compte avant d’exécuter votre projet pilote Microsoft Threat Protection :</span><span class="sxs-lookup"><span data-stu-id="7ff1b-122">Learn what you need to consider before running your Microsoft Threat Protection pilot project:</span></span> <br><br><span data-ttu-id="7ff1b-123">-Étendue</span><span class="sxs-lookup"><span data-stu-id="7ff1b-123">- Scope</span></span> <br> <span data-ttu-id="7ff1b-124">Cas d’utilisation</span><span class="sxs-lookup"><span data-stu-id="7ff1b-124">- Use cases</span></span> <br><span data-ttu-id="7ff1b-125">- Conditions requises :</span><span class="sxs-lookup"><span data-stu-id="7ff1b-125">- Requirements</span></span> <br><span data-ttu-id="7ff1b-126">-Plan de test</span><span class="sxs-lookup"><span data-stu-id="7ff1b-126">- Test plan</span></span> <br> <span data-ttu-id="7ff1b-127">-Critères de réussite</span><span class="sxs-lookup"><span data-stu-id="7ff1b-127">- Success criteria</span></span> <br> <span data-ttu-id="7ff1b-128">-Scorecard</span><span class="sxs-lookup"><span data-stu-id="7ff1b-128">- Scorecard</span></span> 
| <span data-ttu-id="7ff1b-129">![Préparation](../../media/prepare.png)</span><span class="sxs-lookup"><span data-stu-id="7ff1b-129">![Preparation](../../media/prepare.png)</span></span> <br>[<span data-ttu-id="7ff1b-130">Préparation</span><span class="sxs-lookup"><span data-stu-id="7ff1b-130">Preparation</span></span>](mtp-evaluation.md)|  <span data-ttu-id="7ff1b-131">Accédez au centre de sécurité Microsoft 365 pour configurer votre environnement pilote de protection contre les menaces Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7ff1b-131">Access Microsoft 365 Security Center to setup your Microsoft Threat Protection pilot  environment.</span></span> <span data-ttu-id="7ff1b-132">Vous serez guidé pour :</span><span class="sxs-lookup"><span data-stu-id="7ff1b-132">You will be guided to:</span></span><br><br><span data-ttu-id="7ff1b-133">-Identifier les parties prenantes et se déconnecter pour votre projet pilote</span><span class="sxs-lookup"><span data-stu-id="7ff1b-133">- Identify stakeholders and seek sign-off for your pilot</span></span> <br> <span data-ttu-id="7ff1b-134">-Considérations sur l’environnement</span><span class="sxs-lookup"><span data-stu-id="7ff1b-134">- Environment considerations</span></span> <br><span data-ttu-id="7ff1b-135">-Accès</span><span class="sxs-lookup"><span data-stu-id="7ff1b-135">- Access</span></span> <br><span data-ttu-id="7ff1b-136">-Installation d’Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="7ff1b-136">- Azure Active Directory setup</span></span> <br> <span data-ttu-id="7ff1b-137">-Ordre de configuration</span><span class="sxs-lookup"><span data-stu-id="7ff1b-137">- Configuration order</span></span> <br> <span data-ttu-id="7ff1b-138">-Inscrivez-vous à la version d’évaluation de Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="7ff1b-138">- Sign up for Microsoft 365 E5 Trial</span></span> <br> <span data-ttu-id="7ff1b-139">-Configurer le domaine</span><span class="sxs-lookup"><span data-stu-id="7ff1b-139">- Configure domain</span></span> <br><span data-ttu-id="7ff1b-140">-Affecter les licences Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="7ff1b-140">- Assign Microsoft 365 E5 licenses</span></span> <br> <span data-ttu-id="7ff1b-141">-Exécutez l’Assistant Installation dans le portail.</span><span class="sxs-lookup"><span data-stu-id="7ff1b-141">- Complete the setup wizard in the portal</span></span>|
| <span data-ttu-id="7ff1b-142">![Simulation d’attaque](../../media/mtp/run-sim.png)</span><span class="sxs-lookup"><span data-stu-id="7ff1b-142">![Attack simulation](../../media/mtp/run-sim.png)</span></span> <br>[<span data-ttu-id="7ff1b-143">Simulation d’attaque</span><span class="sxs-lookup"><span data-stu-id="7ff1b-143">Attack simulation</span></span>](mtp-pilot-simulate.md) | <span data-ttu-id="7ff1b-144">Pour simuler une attaque, vous serez guidé pour :</span><span class="sxs-lookup"><span data-stu-id="7ff1b-144">To simulate an attack, you will be guided to:</span></span><br><br><span data-ttu-id="7ff1b-145">-Vérifier les conditions requises pour l’environnement de test</span><span class="sxs-lookup"><span data-stu-id="7ff1b-145">- Verify the test environment requirements</span></span> <br><span data-ttu-id="7ff1b-146">-Exécuter la simulation</span><span class="sxs-lookup"><span data-stu-id="7ff1b-146">-  Run the simulation</span></span> <br><span data-ttu-id="7ff1b-147">-Enquêter sur un incident</span><span class="sxs-lookup"><span data-stu-id="7ff1b-147">- Investigate an incident</span></span> <br><span data-ttu-id="7ff1b-148">-résoudre l’incident</span><span class="sxs-lookup"><span data-stu-id="7ff1b-148">- resolve the incident</span></span> 
| <span data-ttu-id="7ff1b-149">![Fermeture et résumé](../../media/mtp/close.png)</span><span class="sxs-lookup"><span data-stu-id="7ff1b-149">![Closing and summary](../../media/mtp/close.png)</span></span> <br>[<span data-ttu-id="7ff1b-150">Fermeture et résumé</span><span class="sxs-lookup"><span data-stu-id="7ff1b-150">Closing and summary</span></span>](mtp-pilot-close.md) | <span data-ttu-id="7ff1b-151">Une fois que vous avez atteint la fin de ce processus, vous serez guidé pour :</span><span class="sxs-lookup"><span data-stu-id="7ff1b-151">When you've reached the end of the process, you will be guided to:</span></span><br><br><span data-ttu-id="7ff1b-152">-Passer par le résultat final</span><span class="sxs-lookup"><span data-stu-id="7ff1b-152">- Go through your final output</span></span><br><span data-ttu-id="7ff1b-153">-Présenter votre sortie à vos parties prenantes</span><span class="sxs-lookup"><span data-stu-id="7ff1b-153">- Present your output to your stakeholders</span></span> <br><span data-ttu-id="7ff1b-154">-Fournir des commentaires</span><span class="sxs-lookup"><span data-stu-id="7ff1b-154">- Provide feedback</span></span> <br><span data-ttu-id="7ff1b-155">-Suivre les étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="7ff1b-155">- Take next steps</span></span> 

## <a name="next-step"></a><span data-ttu-id="7ff1b-156">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="7ff1b-156">Next step</span></span>
|<span data-ttu-id="7ff1b-157">![Phase de planification](../../media/mtp/plan.png)</span><span class="sxs-lookup"><span data-stu-id="7ff1b-157">![Planning phase](../../media/mtp/plan.png)</span></span> <br>[<span data-ttu-id="7ff1b-158">Phase de planification</span><span class="sxs-lookup"><span data-stu-id="7ff1b-158">Planning phase</span></span>](mtp-pilot-plan.md) | <span data-ttu-id="7ff1b-159">Planification de votre projet pilote Microsoft Threat Protection</span><span class="sxs-lookup"><span data-stu-id="7ff1b-159">Plan your Microsoft Threat Protection pilot project</span></span> 
|:-------|:-----|
