---
title: Exécuter votre projet Pilote Microsoft 365 Defender
description: Exécutez votre projet Pilote Microsoft 365 Defender en production pour déterminer efficacement les avantages et l’adoption de Microsoft 365 Defender.
keywords: Pilote Microsoft 365 Defender, exécutez le projet pilote Microsoft 365 Defender, évaluez Microsoft 365 Defender en production, projet pilote Microsoft 365 Defender, cybersécurité, menace avancée persistante, sécurité d’entreprise, appareils, appareil, identité, utilisateurs, données, applications, incidents, investigation et correction automatisées, recherche avancée
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: dolmont
author: DulceMontemayor
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
- m365solution-overview
- m365solution-pilotmtpproject
ms.topic: conceptual
ms.technology: m365d
ms.openlocfilehash: b1616b39597a90ff8e8f7b4c92f29f75c62fea18
ms.sourcegitcommit: a8d8cee7df535a150985d6165afdfddfdf21f622
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "51934428"
---
# <a name="run-your-pilot-microsoft-365-defender-project"></a><span data-ttu-id="61067-104">Exécuter votre projet Pilote Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="61067-104">Run your pilot Microsoft 365 Defender project</span></span> 

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="61067-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="61067-105">**Applies to:**</span></span>
- <span data-ttu-id="61067-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="61067-106">Microsoft 365 Defender</span></span>


<span data-ttu-id="61067-107">Ce guide vous aide à exécuter un projet pilote en fournissant des pointeurs pour vous assurer que vous disposez d’un plan bien structuré, en vous guidant tout au long de l’utilisation de la fonctionnalité de simulation d’attaque et en terminant le projet pilote avec des éléments clés pour que vous réfléchissiez et documentiez les résultats.</span><span class="sxs-lookup"><span data-stu-id="61067-107">This guide helps you run a pilot project by providing pointers to ensure you have a well-structured plan, guiding you through using the attack simulation feature, and finally concluding the pilot with key take-aways for you to reflect on and document results.</span></span>

![Phases d’exécution d’un pilote Microsoft 365 Defender](../../media/pilotphases.png)


<span data-ttu-id="61067-109">L’exécution d’un pilote vous permet de déterminer efficacement les avantages de l’adoption de Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="61067-109">Running a pilot helps you effectively determine the benefit of adoptiing Microsoft 365 Defender.</span></span> <span data-ttu-id="61067-110">Avant d’activer Microsoft 365 Defender dans votre environnement de production et de commencer vos cas d’utilisation, il est préférable de planifier les tâches à accomplir pour votre projet pilote et de définir les critères de réussite.</span><span class="sxs-lookup"><span data-stu-id="61067-110">Before enabling Microsoft 365 Defender in your production environment and starting your use cases, it's best to plan to determine the tasks to accomplish for your pilot project and set the success criteria.</span></span> 


## <a name="how-to-use-this-pilot-playbook"></a><span data-ttu-id="61067-111">Utilisation de ce manuel pilote</span><span class="sxs-lookup"><span data-stu-id="61067-111">How to use this pilot playbook</span></span>

<span data-ttu-id="61067-112">Ce guide fournit une vue d’ensemble de Microsoft 365 Defender et des instructions détaillées sur la façon de configurer votre projet pilote.</span><span class="sxs-lookup"><span data-stu-id="61067-112">This guide provides an overview of Microsoft 365 Defender and step-by-step instructions on how to set up your pilot project.</span></span> 

<span data-ttu-id="61067-113">Microsoft 365 Defender est une suite unifiée de défense d’entreprise avant et après la violation qui coordonne en natif la protection, la détection, la prévention, l’examen et la réponse entre les points de terminaison, les identités, le courrier électronique et les applications afin de fournir une protection intégrée contre les attaques sophistiquées.</span><span class="sxs-lookup"><span data-stu-id="61067-113">Microsoft 365 Defender is a unified pre- and post-breach enterprise defense suite that natively coordinates protection, detection, prevention, investigation, and response across endpoints, identities, email, and applications to provide integrated protection against sophisticated attacks.</span></span> <span data-ttu-id="61067-114">Pour ce faire, elle combine et orchestre les fonctionnalités suivantes dans une solution de sécurité unique :</span><span class="sxs-lookup"><span data-stu-id="61067-114">It does so by combining and orchestrating the following capabilities into a single security solution:</span></span>
  - <span data-ttu-id="61067-115">Microsoft Defender pour les points de terminaison (points de terminaison)</span><span class="sxs-lookup"><span data-stu-id="61067-115">Microsoft Defender for Endpoint (endpoints)</span></span>
  - <span data-ttu-id="61067-116">Microsoft Defender pour Office 365 (courrier électronique)</span><span class="sxs-lookup"><span data-stu-id="61067-116">Microsoft Defender for Office 365 (email)</span></span> 
  - <span data-ttu-id="61067-117">Microsoft Defender pour l’identité (identité)</span><span class="sxs-lookup"><span data-stu-id="61067-117">Microsoft Defender for Identity (identity)</span></span> 
  - <span data-ttu-id="61067-118">Microsoft Cloud App Security (applications)</span><span class="sxs-lookup"><span data-stu-id="61067-118">Microsoft Cloud App Security (apps)</span></span>

![Image of_Microsoft solution 365 Defender pour les utilisateurs, Microsoft Defender pour l'identité, pour les points de terminaison Microsoft Defender pour endpoint, pour les applications cloud, Microsoft Cloud App Security et pour les données, Microsoft Defender pour Office 365](../../media/mtp/m365pillars.png)

<span data-ttu-id="61067-120">Avec la solution Microsoft 365 Defender intégrée, les professionnels de la sécurité peuvent assembler les signaux de menace que Microsoft Defender pour endpoint, Microsoft Defender pour Office 365, Microsoft Defender pour identité et Microsoft Cloud App Security reçoivent, et déterminer l'étendue et l'impact complets de la menace, la façon dont il est entré dans l'environnement, ce qu'il est affecté et son impact actuel sur l'organisation.</span><span class="sxs-lookup"><span data-stu-id="61067-120">With the integrated Microsoft 365 Defender solution, security professionals can stitch together the threat signals that Microsoft Defender for Endpoint, Microsoft Defender for Office 365, Microsoft Defender for Identity, and Microsoft Cloud App Security receive, and determine the full scope and impact of the threat, how it entered the environment, what it's affected, and how it's currently impacting the organization.</span></span> <span data-ttu-id="61067-121">Microsoft 365 Defender prend des mesures automatiques pour empêcher ou arrêter l'attaque et auto-panser les boîtes aux lettres, les points de terminaison et les identités des utilisateurs affectés.</span><span class="sxs-lookup"><span data-stu-id="61067-121">Microsoft 365 Defender takes automatic action to prevent or stop the attack and self-heal affected mailboxes, endpoints, and user identities.</span></span> <span data-ttu-id="61067-122">Pour plus [d'informations, voir la vue d'ensemble de Microsoft 365 Defender.](microsoft-365-defender.md)</span><span class="sxs-lookup"><span data-stu-id="61067-122">See the [Microsoft 365 Defender overview](microsoft-365-defender.md) for details.</span></span>



<span data-ttu-id="61067-123">L'exemple de chronologie suivant varie selon que vous disposez des ressources appropriées dans votre environnement.</span><span class="sxs-lookup"><span data-stu-id="61067-123">The following sample timeline varies depending on having the right resources in your environment.</span></span> <span data-ttu-id="61067-124">Certaines détections et flux de travail peuvent avoir besoin de plus de temps d'apprentissage que les autres.</span><span class="sxs-lookup"><span data-stu-id="61067-124">Some detections and workflows might need more learning time than the others.</span></span>

![Exemple de chronologie lors de l'exécution d'un pilote Microsoft 365 Defender](../../media/phase-diagrams/pilot-phases.png)

>[!IMPORTANT]
><span data-ttu-id="61067-126">Pour obtenir des résultats optimaux, suivez les instructions pilotes aussi étroitement que possible.</span><span class="sxs-lookup"><span data-stu-id="61067-126">For optimum results, follow the pilot instructions as closely as possible.</span></span>


### <a name="pilot-playbook-phases"></a><span data-ttu-id="61067-127">Phases de lecture pilotes</span><span class="sxs-lookup"><span data-stu-id="61067-127">Pilot playbook phases</span></span> 

<span data-ttu-id="61067-128">L'exécution d'un pilote Microsoft 365 Defender se fait en quatre phases :</span><span class="sxs-lookup"><span data-stu-id="61067-128">There are four phases in running a Microsoft 365 Defender pilot:</span></span>

|<span data-ttu-id="61067-129">Phase</span><span class="sxs-lookup"><span data-stu-id="61067-129">Phase</span></span> | <span data-ttu-id="61067-130">Description</span><span class="sxs-lookup"><span data-stu-id="61067-130">Description</span></span> | 
|:-------|:-----|
| [<span data-ttu-id="61067-131">Planification</span><span class="sxs-lookup"><span data-stu-id="61067-131">Planning</span></span>](m365d-pilot-plan.md)<br> <span data-ttu-id="61067-132">~ 1 jour</span><span class="sxs-lookup"><span data-stu-id="61067-132">~ 1 day</span></span>| <span data-ttu-id="61067-133">Découvrez ce que vous devez prendre en compte avant d'exécutez votre projet pilote Microsoft 365 Defender :</span><span class="sxs-lookup"><span data-stu-id="61067-133">Learn what you need to consider before running your Microsoft 365 Defender pilot project:</span></span> <br><br><span data-ttu-id="61067-134">- Étendue</span><span class="sxs-lookup"><span data-stu-id="61067-134">- Scope</span></span> <br> <span data-ttu-id="61067-135">- Cas d'utilisation</span><span class="sxs-lookup"><span data-stu-id="61067-135">- Use cases</span></span> <br><span data-ttu-id="61067-136">- Conditions requises :</span><span class="sxs-lookup"><span data-stu-id="61067-136">- Requirements</span></span> <br><span data-ttu-id="61067-137">- Plan de test</span><span class="sxs-lookup"><span data-stu-id="61067-137">- Test plan</span></span> <br> <span data-ttu-id="61067-138">- Critères de réussite</span><span class="sxs-lookup"><span data-stu-id="61067-138">- Success criteria</span></span> <br> <span data-ttu-id="61067-139">- Carte de performance</span><span class="sxs-lookup"><span data-stu-id="61067-139">- Scorecard</span></span> 
| [<span data-ttu-id="61067-140">Préparation</span><span class="sxs-lookup"><span data-stu-id="61067-140">Preparation</span></span>](m365d-evaluation.md) <br><span data-ttu-id="61067-141">~2 jours</span><span class="sxs-lookup"><span data-stu-id="61067-141">~2 days</span></span>|  <span data-ttu-id="61067-142">Accédez au Centre de sécurité Microsoft 365 pour configurer votre environnement pilote Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="61067-142">Access Microsoft 365 Security Center to set up your Microsoft 365 Defender pilot  environment.</span></span> <span data-ttu-id="61067-143">Vous serez guidé vers :</span><span class="sxs-lookup"><span data-stu-id="61067-143">You'll be guided to:</span></span><br><br><span data-ttu-id="61067-144">- Identifier les parties prenantes et demander la signature de votre projet pilote</span><span class="sxs-lookup"><span data-stu-id="61067-144">- Identify stakeholders and seek sign-off for your pilot</span></span> <br> <span data-ttu-id="61067-145">- Considérations sur l'environnement</span><span class="sxs-lookup"><span data-stu-id="61067-145">- Environment considerations</span></span> <br><span data-ttu-id="61067-146">- Access</span><span class="sxs-lookup"><span data-stu-id="61067-146">- Access</span></span> <br><span data-ttu-id="61067-147">- Configuration d'Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="61067-147">- Azure Active Directory setup</span></span> <br> <span data-ttu-id="61067-148">- Ordre de configuration</span><span class="sxs-lookup"><span data-stu-id="61067-148">- Configuration order</span></span> <br> <span data-ttu-id="61067-149">- S'inscrire à la version d'essai de Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="61067-149">- Sign up for Microsoft 365 E5 Trial</span></span> <br> <span data-ttu-id="61067-150">- Configurer un domaine</span><span class="sxs-lookup"><span data-stu-id="61067-150">- Configure domain</span></span> <br><span data-ttu-id="61067-151">- Attribuer des licences Microsoft 365 E5</span><span class="sxs-lookup"><span data-stu-id="61067-151">- Assign Microsoft 365 E5 licenses</span></span> <br> <span data-ttu-id="61067-152">- Terminer l'Assistant Installation dans le portail</span><span class="sxs-lookup"><span data-stu-id="61067-152">- Complete the setup wizard in the portal</span></span>|
| [<span data-ttu-id="61067-153">Simulation d’attaque</span><span class="sxs-lookup"><span data-stu-id="61067-153">Attack simulation</span></span>](m365d-pilot-simulate.md) <br><span data-ttu-id="61067-154">~2 jours</span><span class="sxs-lookup"><span data-stu-id="61067-154">~2 days</span></span>| <span data-ttu-id="61067-155">Pour simuler une attaque, vous serez guidé vers :</span><span class="sxs-lookup"><span data-stu-id="61067-155">To simulate an attack, you'll be guided to:</span></span><br><br><span data-ttu-id="61067-156">- Vérifier les conditions requises pour l'environnement de test</span><span class="sxs-lookup"><span data-stu-id="61067-156">- Verify the test environment requirements</span></span> <br><span data-ttu-id="61067-157">- Exécuter la simulation</span><span class="sxs-lookup"><span data-stu-id="61067-157">-  Run the simulation</span></span> <br><span data-ttu-id="61067-158">- Examiner un incident</span><span class="sxs-lookup"><span data-stu-id="61067-158">- Investigate an incident</span></span> <br><span data-ttu-id="61067-159">- résoudre l'incident</span><span class="sxs-lookup"><span data-stu-id="61067-159">- resolve the incident</span></span> 
| [<span data-ttu-id="61067-160">Fermeture et résumé</span><span class="sxs-lookup"><span data-stu-id="61067-160">Closing and summary</span></span>](m365d-pilot-close.md) <br><span data-ttu-id="61067-161">~ 1 jour</span><span class="sxs-lookup"><span data-stu-id="61067-161">~ 1 day</span></span>| <span data-ttu-id="61067-162">Lorsque vous aurez atteint la fin du processus, vous serez guidé vers :</span><span class="sxs-lookup"><span data-stu-id="61067-162">When you've reached the end of the process, you'll be guided to:</span></span><br><br><span data-ttu-id="61067-163">- Passer par votre résultat final</span><span class="sxs-lookup"><span data-stu-id="61067-163">- Go through your final output</span></span><br><span data-ttu-id="61067-164">- Présenter votre résultat à vos parties prenantes</span><span class="sxs-lookup"><span data-stu-id="61067-164">- Present your output to your stakeholders</span></span> <br><span data-ttu-id="61067-165">- Fournir des commentaires</span><span class="sxs-lookup"><span data-stu-id="61067-165">- Provide feedback</span></span> <br><span data-ttu-id="61067-166">- Prendre les étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="61067-166">- Take next steps</span></span> 

## <a name="next-step"></a><span data-ttu-id="61067-167">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="61067-167">Next step</span></span>
|[<span data-ttu-id="61067-168">Phase de planification</span><span class="sxs-lookup"><span data-stu-id="61067-168">Planning phase</span></span>](m365d-pilot-plan.md) | <span data-ttu-id="61067-169">Planifier votre projet pilote Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="61067-169">Plan your Microsoft 365 Defender pilot project</span></span> 
|:-------|:-----|
