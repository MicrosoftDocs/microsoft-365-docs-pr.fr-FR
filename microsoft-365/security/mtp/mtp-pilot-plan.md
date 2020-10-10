---
title: Planification de votre projet pilote de protection des menaces Microsoft
description: Planifiez votre projet pilote de protection des menaces Microsoft avec les parties prenantes pour gérer les attentes et garantir le succès.
keywords: Microsoft Threat Protection Pilot, planifier le projet pilote de protection des menaces Microsoft, évaluer la protection de Microsoft contre les menaces en production, projet pilote Microsoft Threat Protection, protection contre la vulnérabilité, protection avancée contre les menaces, sécurité de l’entreprise, périphériques, appareil, identité, utilisateurs, données, applications, incidents, analyse automatisée et correction, recherche avancée
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
ms.collection:
- M365-security-compliance
- m365solution-scenario
- m365solution-pilotmtpproject
ms.topic: conceptual
ms.openlocfilehash: e62b4ec0ee6c9d05321accf269406e8127019f5b
ms.sourcegitcommit: a83acd5b9eeefd2e20e5bac916fe29d09fb53de9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/10/2020
ms.locfileid: "48418108"
---
# <a name="planning-your-pilot-microsoft-threat-protection-project"></a><span data-ttu-id="c6af1-104">Planification de votre projet pilote de protection des menaces Microsoft</span><span class="sxs-lookup"><span data-stu-id="c6af1-104">Planning your pilot Microsoft Threat Protection project</span></span> 

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="c6af1-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="c6af1-105">**Applies to:**</span></span>
- <span data-ttu-id="c6af1-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="c6af1-106">Microsoft Threat Protection</span></span>
<br>
<table border="0" width="100%" align="center">
  <tr style="text-align:center;">
    <td align="center" style="width:25%; border:0;" bgcolor="#d5f5e3">
      <a href= "https://docs.microsoft.com/microsoft-365/security/mtp/mtp-pilot-plan"> 
        <img src="../../media/mtp/plan.png" alt="Plan your pilot Microsoft Threat Protection project" title="Planification de votre projet pilote de protection contre les menaces Microsoft" />
      <br/><span data-ttu-id="c6af1-108">Prévision</a></span><span class="sxs-lookup"><span data-stu-id="c6af1-108">Plan</a></span></span><br>
    </td>
    <td align="center">
      <a href="https://docs.microsoft.com/microsoft-365/security/mtp/prepare-mtpeval">
        <img src="../../media/mtp/prep.png" alt="Prepare your Microsoft Threat Protection trial lab or pilot environment" title="Préparation de votre laboratoire d’évaluation ou de votre environnement pilote Microsoft Threat Protection" />
      <br/><span data-ttu-id="c6af1-110">Préparation</a></span><span class="sxs-lookup"><span data-stu-id="c6af1-110">Prepare</a></span></span><br>
    </td>
    <td align="center">
      <a href="https://docs.microsoft.com/microsoft-365/security/mtp/mtp-pilot-simulate">
        <img src="../../media/mtp/run-sim.png" alt="Run your Microsoft Threat Protection attack simulations" title="Exécuter vos simulations d’attaque de la protection contre les menaces Microsoft" />
     <br/><span data-ttu-id="c6af1-112">Simuler une attaque</a></span><span class="sxs-lookup"><span data-stu-id="c6af1-112">Simulate attack</a></span></span><br>
    </td>
    <td align="center">
      <a href="https://docs.microsoft.com/microsoft-365/security/mtp/mtp-pilot-close">
        <img src="../../media/mtp/close.png" alt="Close and summarize your Microsoft Threat Protection pilot" title="Fermer et résumer votre programme pilote de protection contre les menaces Microsoft" />
     <br/><span data-ttu-id="c6af1-114">Fermer et synthétiser</a></span><span class="sxs-lookup"><span data-stu-id="c6af1-114">Close and summarize</a></span></span><br>
    </td>
  </tr>
  <tr>
    <td style="width:25%; border:0;">
   
    </td>
    <td valign="top" style="width:25%; border:0;">
    
</td>
    <td valign="top" style="width:25%; border:0;">

</td>    
    <td valign="top" style="width:25%; border:0;">

</td>
  </tr>
</table>

<span data-ttu-id="c6af1-115">Vous êtes actuellement à la phase de planification.</span><span class="sxs-lookup"><span data-stu-id="c6af1-115">You're currently in the planning phase.</span></span>

<span data-ttu-id="c6af1-116">Pour vous assurer que votre projet pilote a réussi, il est essentiel de planifier soigneusement et d’obtenir des approbations de vos parties prenantes au début.</span><span class="sxs-lookup"><span data-stu-id="c6af1-116">To ensure that your pilot project is a success, it is essential to plan thoroughly with and get approvals from your stakeholders in the beginning.</span></span> <span data-ttu-id="c6af1-117">Les éléments de la planification incluent l’identification de l’étendue, des cas d’utilisation, des exigences et des critères de réussite.</span><span class="sxs-lookup"><span data-stu-id="c6af1-117">Elements of planning include identifying scope, use cases, requirements, and success criteria.</span></span>

<span data-ttu-id="c6af1-118">Ce guide vous guide tout au long de la planification de votre projet pilote.</span><span class="sxs-lookup"><span data-stu-id="c6af1-118">This guide walks you through how to plan your pilot project.</span></span> 

>[!IMPORTANT]
><span data-ttu-id="c6af1-119">Pour obtenir des résultats optimaux, suivez les instructions de pilote aussi étroitement que possible.</span><span class="sxs-lookup"><span data-stu-id="c6af1-119">For optimum results, follow the pilot instructions as closely as possible.</span></span>


## <a name="scope"></a><span data-ttu-id="c6af1-120">Portée</span><span class="sxs-lookup"><span data-stu-id="c6af1-120">Scope</span></span>

<span data-ttu-id="c6af1-121">L’étendue du projet pilote détermine la portée du test, en fonction de votre environnement et des méthodes de test acceptables.</span><span class="sxs-lookup"><span data-stu-id="c6af1-121">The scope of the pilot will determine how broad the test will be, based on your environment and acceptable testing methods.</span></span> <span data-ttu-id="c6af1-122">Voici quelques exemples d’étendues à prendre en compte :</span><span class="sxs-lookup"><span data-stu-id="c6af1-122">Here are some example scopes to consider:</span></span>
- <span data-ttu-id="c6af1-123">Environnement de développement ou de test qui inclut des points de terminaison, des serveurs, des contrôleurs de domaine.</span><span class="sxs-lookup"><span data-stu-id="c6af1-123">Development or test environment which includes endpoints, servers, domain controllers.</span></span>
- <span data-ttu-id="c6af1-124">Environnement de production avec Microsoft 365, Azure, services Active Directory, points de terminaison et serveurs</span><span class="sxs-lookup"><span data-stu-id="c6af1-124">Production environment with Microsoft 365, Azure, Active Directory services, endpoints, and servers</span></span>

>[!NOTE]
><span data-ttu-id="c6af1-125">Si vous ne disposez pas encore de toutes les licences, vous pouvez obtenir des licences d’évaluation pour [évaluer Microsoft Threat Protection](https://aka.ms/mtp-trial-lab) – plan, prepare, Setup, configure et Run the Pilot Project.</span><span class="sxs-lookup"><span data-stu-id="c6af1-125">If you don’t have the full licenses yet, you can get trial licenses to [evaluate Microsoft Threat Protection](https://aka.ms/mtp-trial-lab) – plan, prepare, setup, configure, and run your pilot project.</span></span> <span data-ttu-id="c6af1-126">Vos parties prenantes joueront un rôle important en facilitant le processus du début à la fin.</span><span class="sxs-lookup"><span data-stu-id="c6af1-126">Your stakeholders will play a big role in helping facilitate the process from start to finish.</span></span>

<span data-ttu-id="c6af1-127">Les types de systèmes d’exploitation à évaluer doivent également être définis en fonction de la composition de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="c6af1-127">The types of operating systems to be evaluated should also be defined based on the organizational makeup.</span></span> <span data-ttu-id="c6af1-128">Cela peut être le suivant : [points de terminaison Mac](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-atp-mac#system-requirements), [serveurs Linux](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-atp-linux#system-requirements), [points de terminaison windows 10](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/minimum-requirements#supported-windows-versions), [Windows Server 2016](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/minimum-requirements#supported-windows-versions).</span><span class="sxs-lookup"><span data-stu-id="c6af1-128">This may include the following: [Mac endpoints](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-atp-mac#system-requirements), [Linux Servers](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-atp-linux#system-requirements), [Windows 10 endpoints](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/minimum-requirements#supported-windows-versions), [Windows Server 2016](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/minimum-requirements#supported-windows-versions).</span></span>

## <a name="use-cases"></a><span data-ttu-id="c6af1-129">Cas d’utilisation</span><span class="sxs-lookup"><span data-stu-id="c6af1-129">Use cases</span></span>

<span data-ttu-id="c6af1-130">Les cas d’utilisation représentent des instructions expliquant comment l’outil testé est destiné à être consommé par les utilisateurs prévus.</span><span class="sxs-lookup"><span data-stu-id="c6af1-130">Use cases represent statements of how the tool being tested is meant to be consumed by its intended users.</span></span> <span data-ttu-id="c6af1-131">Celles-ci peuvent être formulées sous la forme de récits utilisateur du point de vue d’un personnage particulier, tel qu’un analyste SOC.</span><span class="sxs-lookup"><span data-stu-id="c6af1-131">These can be formulated as user stories from the point of view of a particular persona, such as a SOC analyst.</span></span> <span data-ttu-id="c6af1-132">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="c6af1-132">For example:</span></span>
- <span data-ttu-id="c6af1-133">En tant qu’analyste SOC, je dois afficher, corréler, évaluer et gérer les alertes et les événements sur les appareils, les utilisateurs et les boîtes aux lettres de mon réseau.</span><span class="sxs-lookup"><span data-stu-id="c6af1-133">As a SOC analyst, I need to view, correlate, assess and manage alerts and events across devices, users, and mailboxes in my network.</span></span> <span data-ttu-id="c6af1-134">[Gestion des incidents]</span><span class="sxs-lookup"><span data-stu-id="c6af1-134">[Incident management]</span></span>
- <span data-ttu-id="c6af1-135">En tant qu’analyste SOC, j’ai besoin de l’outil et du processus pour examiner et répondre automatiquement aux événements malveillants de mon réseau.</span><span class="sxs-lookup"><span data-stu-id="c6af1-135">As a SOC analyst, I must have the tool and process to automatically investigate and respond to malicious events in my network.</span></span> <span data-ttu-id="c6af1-136">[Auto IR]</span><span class="sxs-lookup"><span data-stu-id="c6af1-136">[Auto IR]</span></span>
- <span data-ttu-id="c6af1-137">En tant qu’analyste SOC, je dois Rechercher des données dans mon environnement pour trouver des menaces connues et potentielles, ainsi que des activités suspectes.</span><span class="sxs-lookup"><span data-stu-id="c6af1-137">As a SOC analyst, I must search data from my environment to find known and potential threats, and suspicious activities.</span></span> <span data-ttu-id="c6af1-138">[Chasse avancée]</span><span class="sxs-lookup"><span data-stu-id="c6af1-138">[Advanced Hunting]</span></span>

<span data-ttu-id="c6af1-139">N’oubliez pas que ces cas d’utilisation doivent être créés dans les paramètres de l’étendue définie.</span><span class="sxs-lookup"><span data-stu-id="c6af1-139">Keep in mind that these use cases should be created within the parameters of the defined scope.</span></span> <span data-ttu-id="c6af1-140">Si, par exemple, l’étendue du test n’inclut pas une évaluation des outils tels que Microsoft Cloud App Security, alors les cas d’utilisation qui s’en reposent en tant que source de données ne doivent pas être créés.</span><span class="sxs-lookup"><span data-stu-id="c6af1-140">If, for example, the scope of testing does not include an evaluation of tools such as Microsoft Cloud App Security, then use cases that rely on this as a data source should not be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6af1-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c6af1-141">Requirements</span></span>

<span data-ttu-id="c6af1-142">Dans la liste des cas d’utilisation, vous pouvez commencer à créer des exigences.</span><span class="sxs-lookup"><span data-stu-id="c6af1-142">From the list of use cases, you can start to create requirements.</span></span> <span data-ttu-id="c6af1-143">Les conditions requises incluent les fonctionnalités dont doit disposer un outil pour satisfaire les cas d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="c6af1-143">Requirements include features a tool must have to satisfy the use cases.</span></span> <span data-ttu-id="c6af1-144">Ces exigences peuvent être divisées en catégories telles que la configuration et la maintenance, la prise en charge des intégrations et les exigences spécifiques aux fonctionnalités telles que la possibilité de la chasse et la possibilité de créer des alertes personnalisées.</span><span class="sxs-lookup"><span data-stu-id="c6af1-144">These requirements can be broken down into categories such as configuration and maintenance, support for integrations, and feature-specific requirements like hunting ability and the ability to build custom alerts.</span></span>

## <a name="test-plan"></a><span data-ttu-id="c6af1-145">Plan de test</span><span class="sxs-lookup"><span data-stu-id="c6af1-145">Test plan</span></span>

<span data-ttu-id="c6af1-146">Selon les exigences, différentes méthodes de test peuvent être appropriées.</span><span class="sxs-lookup"><span data-stu-id="c6af1-146">Depending on the requirements, different methods of testing may be appropriate.</span></span> <span data-ttu-id="c6af1-147">Par exemple, si l’impératif est d’évaluer l’efficacité de la correction automatisée, le plan de test doit inclure des étapes pour générer le ou les comportements qui déclencheraient une action de correction automatisée dans Microsoft Threat Protection.</span><span class="sxs-lookup"><span data-stu-id="c6af1-147">For instance, if the requirement is to evaluate the efficacy of Automated Remediation, the test plan needs to include steps to generate the behavior(s) that would trigger an automated remediation action within Microsoft Threat Protection.</span></span> <span data-ttu-id="c6af1-148">Si la nécessité est de détecter un comportement ou une attaque particulière, le test peut impliquer davantage d’étapes.</span><span class="sxs-lookup"><span data-stu-id="c6af1-148">If the requirement is to detect a particular behavior or attack, then the test may involve more steps.</span></span> <span data-ttu-id="c6af1-149">Le point doit disposer d’un plan en place pour tester précisément votre configuration requise.</span><span class="sxs-lookup"><span data-stu-id="c6af1-149">The point is to have a plan in place to accurately test against your requirements.</span></span>

## <a name="success-criteria"></a><span data-ttu-id="c6af1-150">Critères de réussite</span><span class="sxs-lookup"><span data-stu-id="c6af1-150">Success criteria</span></span>

<span data-ttu-id="c6af1-151">Les critères de réussite correspondent finalement à la barre de mesure par rapport à ce que vous testez.</span><span class="sxs-lookup"><span data-stu-id="c6af1-151">Success criteria is ultimately the bar set to measure against what you are testing.</span></span> <span data-ttu-id="c6af1-152">Que vous testiez Microsoft Threat Protection (ou toute autre technologie) contre d’autres outils ou par lui-même, il doit exister des critères quantifiables pour déterminer la valeur fournie par l’outil.</span><span class="sxs-lookup"><span data-stu-id="c6af1-152">Whether you are testing Microsoft Threat Protection (or any other technology for that matter) against other tools or by itself, there must be some quantifiable criteria to determine the value the tool provides.</span></span> <span data-ttu-id="c6af1-153">En fonction de l’étendue, des exigences et du plan de test, les critères de réussite déterminent le score du test.</span><span class="sxs-lookup"><span data-stu-id="c6af1-153">Based on the scope, requirements, and testing plan, the success criteria will determine how to score the test.</span></span> <span data-ttu-id="c6af1-154">Cela doit être inférieur à la réussite ou à l’échec, ainsi qu’à un score pondéré en fonction de vos besoins.</span><span class="sxs-lookup"><span data-stu-id="c6af1-154">This should be less of a pass or fail and more of a weighted scoring based on your needs.</span></span> <span data-ttu-id="c6af1-155">Par exemple, pour réussir, un outil peut avoir besoin d’un score supérieur à 80% dans certaines zones critiques que vous identifiez.</span><span class="sxs-lookup"><span data-stu-id="c6af1-155">For example, to be successful, a tool may need to score above 80% in certain critical areas you identify.</span></span>

## <a name="scorecard"></a><span data-ttu-id="c6af1-156">Prospectif</span><span class="sxs-lookup"><span data-stu-id="c6af1-156">Scorecard</span></span>

<span data-ttu-id="c6af1-157">Une façon de rassembler tous les éléments de votre plan peut consister à créer une carte de performance.</span><span class="sxs-lookup"><span data-stu-id="c6af1-157">One way to bring all elements of your plan together can be to create a scorecard.</span></span> <span data-ttu-id="c6af1-158">Voir un exemple de carte de performance ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="c6af1-158">See a sample scorecard below:</span></span>

| <span data-ttu-id="c6af1-159">Cas d’utilisation</span><span class="sxs-lookup"><span data-stu-id="c6af1-159">Use case</span></span> | <span data-ttu-id="c6af1-160">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c6af1-160">Requirements</span></span> | <span data-ttu-id="c6af1-161">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c6af1-161">Configuration requirements</span></span> | <span data-ttu-id="c6af1-162">Plan de test</span><span class="sxs-lookup"><span data-stu-id="c6af1-162">Test plan</span></span> | <span data-ttu-id="c6af1-163">Résultat attendu</span><span class="sxs-lookup"><span data-stu-id="c6af1-163">Expected outcome</span></span> | <span data-ttu-id="c6af1-164">État du test</span><span class="sxs-lookup"><span data-stu-id="c6af1-164">Test status</span></span> | <span data-ttu-id="c6af1-165">Niveau</span><span class="sxs-lookup"><span data-stu-id="c6af1-165">Score</span></span> | <span data-ttu-id="c6af1-166">Notes</span><span class="sxs-lookup"><span data-stu-id="c6af1-166">Notes</span></span> |
|:-------|:-------|:-------|:-------|:-------|:-------|:-------|:-------|
|<span data-ttu-id="c6af1-167">Gestion des incidents</span><span class="sxs-lookup"><span data-stu-id="c6af1-167">Incident management</span></span>|<span data-ttu-id="c6af1-168">-Protection contre les menaces Microsoft</span><span class="sxs-lookup"><span data-stu-id="c6af1-168">-  Microsoft Threat Protection</span></span> </br></br><span data-ttu-id="c6af1-169">-Azure ATP</span><span class="sxs-lookup"><span data-stu-id="c6af1-169">- Azure ATP</span></span> </br></br><span data-ttu-id="c6af1-170">-Microsoft Defender ATP</span><span class="sxs-lookup"><span data-stu-id="c6af1-170">- Microsoft Defender ATP</span></span> </br></br><span data-ttu-id="c6af1-171">-Sécurité des applications Cloud Microsoft (facultatif)</span><span class="sxs-lookup"><span data-stu-id="c6af1-171">- Microsoft Cloud App Security (optional)</span></span>|<span data-ttu-id="c6af1-172">Voir les [conditions préalables](https://aka.ms/mtp-trial-lab) pour la préparation, l’installation et la configuration pour plus de détails</span><span class="sxs-lookup"><span data-stu-id="c6af1-172">See the [prerequisites](https://aka.ms/mtp-trial-lab) for preparation, set-up, and configuration for details</span></span> |[<span data-ttu-id="c6af1-173">Simuler une attaque</span><span class="sxs-lookup"><span data-stu-id="c6af1-173">Simulate attack</span></span>](mtp-pilot-simulate.md) <br></br>[<span data-ttu-id="c6af1-174">Examen de l’incident</span><span class="sxs-lookup"><span data-stu-id="c6af1-174">Investigate the incident</span></span>](https://docs.microsoft.com/microsoft-365/security/mtp/mtp-pilot-simulate#investigate-an-incident) |<span data-ttu-id="c6af1-175">Les investigateurs peuvent comprendre l’étendue et l’impact de l’incident et gérer l’incident.</span><span class="sxs-lookup"><span data-stu-id="c6af1-175">Investigators can understand the scope and impact of the incident and manage the incident</span></span>||||
|<span data-ttu-id="c6af1-176">AutoIR</span><span class="sxs-lookup"><span data-stu-id="c6af1-176">AutoIR</span></span>|<span data-ttu-id="c6af1-177">-Protection contre les menaces Microsoft</span><span class="sxs-lookup"><span data-stu-id="c6af1-177">-   Microsoft Threat Protection</span></span> </br></br><span data-ttu-id="c6af1-178">-Azure ATP</span><span class="sxs-lookup"><span data-stu-id="c6af1-178">- Azure ATP</span></span> </br></br><span data-ttu-id="c6af1-179">-Microsoft Defender ATP</span><span class="sxs-lookup"><span data-stu-id="c6af1-179">- Microsoft Defender ATP</span></span> |<span data-ttu-id="c6af1-180">Voir les [conditions préalables](https://aka.ms/mtp-trial-lab) pour la préparation, l’installation et la configuration pour plus de détails</span><span class="sxs-lookup"><span data-stu-id="c6af1-180">See the [prerequisites](https://aka.ms/mtp-trial-lab) for preparation, set-up, and configuration for details</span></span> <br><span data-ttu-id="c6af1-181">Activer AutoIR</span><span class="sxs-lookup"><span data-stu-id="c6af1-181">Enable AutoIR</span></span>  |[<span data-ttu-id="c6af1-182">Simuler une attaque</span><span class="sxs-lookup"><span data-stu-id="c6af1-182">Simulate attack</span></span>](mtp-pilot-simulate.md) <br></br>[<span data-ttu-id="c6af1-183">Enquête automatisée</span><span class="sxs-lookup"><span data-stu-id="c6af1-183">Automated investigation</span></span>](https://docs.microsoft.com/microsoft-365/security/mtp/mtp-pilot-simulate.md#automated-investigation-and-remediation) |<span data-ttu-id="c6af1-184">Les alertes et les incidents sont automatiquement résolus par la protection contre les menaces Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c6af1-184">Alerts and incidents are automatically remediated by Microsoft Threat Protection</span></span>||||
|<span data-ttu-id="c6af1-185">Repérage avancé</span><span class="sxs-lookup"><span data-stu-id="c6af1-185">Advanced hunting</span></span>|<span data-ttu-id="c6af1-186">-Protection contre les menaces Microsoft</span><span class="sxs-lookup"><span data-stu-id="c6af1-186">- Microsoft Threat Protection</span></span> </br></br><span data-ttu-id="c6af1-187">-Microsoft Defender ATP</span><span class="sxs-lookup"><span data-stu-id="c6af1-187">- Microsoft Defender ATP</span></span> </br></br><span data-ttu-id="c6af1-188">-Office 365 ATP</span><span class="sxs-lookup"><span data-stu-id="c6af1-188">- Office 365 ATP</span></span>   |<span data-ttu-id="c6af1-189">Voir les [conditions préalables](https://aka.ms/mtp-trial-lab) pour la préparation, l’installation et la configuration pour plus de détails</span><span class="sxs-lookup"><span data-stu-id="c6af1-189">See the [prerequisites](https://aka.ms/mtp-trial-lab) for preparation, set-up, and configuration for details</span></span>|[<span data-ttu-id="c6af1-190">Scénario de chasse avancé</span><span class="sxs-lookup"><span data-stu-id="c6af1-190">Advanced hunting scenario</span></span>](https://docs.microsoft.com/microsoft-365/security/mtp/mtp-pilot-simulate.md#advanced-hunting-scenario) |<span data-ttu-id="c6af1-191">Les investigateurs peuvent trouver des données par le biais d’une recherche avancée, d’un pivotement vers des entités affectées et en créant des détections personnalisées.</span><span class="sxs-lookup"><span data-stu-id="c6af1-191">Investigators can find data through advanced hunting, pivoting to impacted entities, and by creating custom detections</span></span>||||



## <a name="next-step"></a><span data-ttu-id="c6af1-192">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="c6af1-192">Next step</span></span>
|<span data-ttu-id="c6af1-193">![Phase de préparation](../../media/mtp/prep.png)</span><span class="sxs-lookup"><span data-stu-id="c6af1-193">![Preparation phase](../../media/mtp/prep.png)</span></span> <br>[<span data-ttu-id="c6af1-194">Phase de préparation</span><span class="sxs-lookup"><span data-stu-id="c6af1-194">Preparation phase</span></span>](prepare-mtpeval.md) | <span data-ttu-id="c6af1-195">Préparation de votre environnement pilote Microsoft Threat Protection</span><span class="sxs-lookup"><span data-stu-id="c6af1-195">Prepare your Microsoft Threat Protection pilot environment</span></span>
|:-------|:-----|
