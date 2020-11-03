---
title: Planification de votre projet pilote Microsoft 365 Defender
description: Planifiez votre projet pilote Microsoft 365 Defender avec les parties prenantes pour gérer les attentes et garantir le bon déroulement de l’opération.
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
ms.openlocfilehash: ec2bfe52308231577e4f2749e1f4cdf24a36f604
ms.sourcegitcommit: 815229e39a0f905d9f06717f00dc82e2a028fa7c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2020
ms.locfileid: "48846019"
---
# <a name="planning-your-pilot-microsoft-365-defender-project"></a><span data-ttu-id="167c9-104">Planification de votre projet pilote Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="167c9-104">Planning your pilot Microsoft 365 Defender project</span></span> 

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="167c9-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="167c9-105">**Applies to:**</span></span>
- <span data-ttu-id="167c9-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="167c9-106">Microsoft 365 Defender</span></span>
<br>
<table border="0" width="100%" align="center">
  <tr style="text-align:center;">
    <td align="center" style="width:25%; border:0;" bgcolor="#d5f5e3">
      <a href= "https://docs.microsoft.com/microsoft-365/security/mtp/mtp-pilot-plan"> 
        <img src="../../media/mtp/plan.png" alt="Plan your pilot Microsoft 365 Defender project" title="Planification de votre projet pilote Microsoft 365 Defender" />
      <br/><span data-ttu-id="167c9-108">Prévision</a></span><span class="sxs-lookup"><span data-stu-id="167c9-108">Plan</a></span></span><br>
    </td>
    <td align="center">
      <a href="https://docs.microsoft.com/microsoft-365/security/mtp/prepare-mtpeval">
        <img src="../../media/mtp/prep.png" alt="Prepare your Microsoft 365 Defender trial lab or pilot environment" title="Préparation de votre laboratoire d’évaluation ou de votre environnement pilote Microsoft 365 Defender" />
      <br/><span data-ttu-id="167c9-110">Préparation</a></span><span class="sxs-lookup"><span data-stu-id="167c9-110">Prepare</a></span></span><br>
    </td>
    <td align="center">
      <a href="https://docs.microsoft.com/microsoft-365/security/mtp/mtp-pilot-simulate">
        <img src="../../media/mtp/run-sim.png" alt="Run your Microsoft 365 Defender attack simulations" title="Exécuter vos simulations d’attaque de Microsoft 365 Defender" />
     <br/><span data-ttu-id="167c9-112">Simuler une attaque</a></span><span class="sxs-lookup"><span data-stu-id="167c9-112">Simulate attack</a></span></span><br>
    </td>
    <td align="center">
      <a href="https://docs.microsoft.com/microsoft-365/security/mtp/mtp-pilot-close">
        <img src="../../media/mtp/close.png" alt="Close and summarize your Microsoft 365 Defender pilot" title="Fermeture et synthèse de votre pilote Microsoft 365 Defender" />
     <br/><span data-ttu-id="167c9-114">Fermer et synthétiser</a></span><span class="sxs-lookup"><span data-stu-id="167c9-114">Close and summarize</a></span></span><br>
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

<span data-ttu-id="167c9-115">Vous êtes actuellement à la phase de planification.</span><span class="sxs-lookup"><span data-stu-id="167c9-115">You're currently in the planning phase.</span></span>

<span data-ttu-id="167c9-116">Pour vous assurer que votre projet pilote a réussi, il est essentiel de planifier soigneusement et d’obtenir des approbations de vos parties prenantes au début.</span><span class="sxs-lookup"><span data-stu-id="167c9-116">To ensure that your pilot project is a success, it is essential to plan thoroughly with and get approvals from your stakeholders in the beginning.</span></span> <span data-ttu-id="167c9-117">Les éléments de la planification incluent l’identification de l’étendue, des cas d’utilisation, des exigences et des critères de réussite.</span><span class="sxs-lookup"><span data-stu-id="167c9-117">Elements of planning include identifying scope, use cases, requirements, and success criteria.</span></span>

<span data-ttu-id="167c9-118">Ce guide vous guide tout au long de la planification de votre projet pilote.</span><span class="sxs-lookup"><span data-stu-id="167c9-118">This guide walks you through how to plan your pilot project.</span></span> 

>[!IMPORTANT]
><span data-ttu-id="167c9-119">Pour obtenir des résultats optimaux, suivez les instructions de pilote aussi étroitement que possible.</span><span class="sxs-lookup"><span data-stu-id="167c9-119">For optimum results, follow the pilot instructions as closely as possible.</span></span>


## <a name="scope"></a><span data-ttu-id="167c9-120">Portée</span><span class="sxs-lookup"><span data-stu-id="167c9-120">Scope</span></span>

<span data-ttu-id="167c9-121">L’étendue du projet pilote détermine la portée du test, en fonction de votre environnement et des méthodes de test acceptables.</span><span class="sxs-lookup"><span data-stu-id="167c9-121">The scope of the pilot will determine how broad the test will be, based on your environment and acceptable testing methods.</span></span> <span data-ttu-id="167c9-122">Voici quelques exemples d’étendues à prendre en compte :</span><span class="sxs-lookup"><span data-stu-id="167c9-122">Here are some example scopes to consider:</span></span>
- <span data-ttu-id="167c9-123">Environnement de développement ou de test qui inclut des points de terminaison, des serveurs, des contrôleurs de domaine.</span><span class="sxs-lookup"><span data-stu-id="167c9-123">Development or test environment which includes endpoints, servers, domain controllers.</span></span>
- <span data-ttu-id="167c9-124">Environnement de production avec Microsoft 365, Azure, services Active Directory, points de terminaison et serveurs</span><span class="sxs-lookup"><span data-stu-id="167c9-124">Production environment with Microsoft 365, Azure, Active Directory services, endpoints, and servers</span></span>

>[!NOTE]
><span data-ttu-id="167c9-125">Si vous ne disposez pas encore de toutes les licences, vous pouvez obtenir des licences d’évaluation pour [évaluer Microsoft 365 Defender](https://aka.ms/mtp-trial-lab) – planification, préparation, configuration, configuration et exécution de votre projet pilote.</span><span class="sxs-lookup"><span data-stu-id="167c9-125">If you don’t have the full licenses yet, you can get trial licenses to [evaluate Microsoft 365 Defender](https://aka.ms/mtp-trial-lab) – plan, prepare, setup, configure, and run your pilot project.</span></span> <span data-ttu-id="167c9-126">Vos parties prenantes joueront un rôle important en facilitant le processus du début à la fin.</span><span class="sxs-lookup"><span data-stu-id="167c9-126">Your stakeholders will play a big role in helping facilitate the process from start to finish.</span></span>

<span data-ttu-id="167c9-127">Les types de systèmes d’exploitation à évaluer doivent également être définis en fonction de la composition de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="167c9-127">The types of operating systems to be evaluated should also be defined based on the organizational makeup.</span></span> <span data-ttu-id="167c9-128">Cela peut être le suivant : [points de terminaison Mac](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-atp-mac#system-requirements), [serveurs Linux](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-atp-linux#system-requirements), [points de terminaison windows 10](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/minimum-requirements#supported-windows-versions), [Windows Server 2016](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/minimum-requirements#supported-windows-versions).</span><span class="sxs-lookup"><span data-stu-id="167c9-128">This may include the following: [Mac endpoints](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-atp-mac#system-requirements), [Linux Servers](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-atp-linux#system-requirements), [Windows 10 endpoints](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/minimum-requirements#supported-windows-versions), [Windows Server 2016](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/minimum-requirements#supported-windows-versions).</span></span>

## <a name="use-cases"></a><span data-ttu-id="167c9-129">Cas d'utilisation</span><span class="sxs-lookup"><span data-stu-id="167c9-129">Use cases</span></span>

<span data-ttu-id="167c9-130">Les cas d’utilisation représentent des instructions expliquant comment l’outil testé est destiné à être consommé par les utilisateurs prévus.</span><span class="sxs-lookup"><span data-stu-id="167c9-130">Use cases represent statements of how the tool being tested is meant to be consumed by its intended users.</span></span> <span data-ttu-id="167c9-131">Celles-ci peuvent être formulées sous la forme de récits utilisateur du point de vue d’un personnage particulier, tel qu’un analyste SOC.</span><span class="sxs-lookup"><span data-stu-id="167c9-131">These can be formulated as user stories from the point of view of a particular persona, such as a SOC analyst.</span></span> <span data-ttu-id="167c9-132">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="167c9-132">For example:</span></span>
- <span data-ttu-id="167c9-133">En tant qu’analyste SOC, je dois afficher, corréler, évaluer et gérer les alertes et les événements sur les appareils, les utilisateurs et les boîtes aux lettres de mon réseau.</span><span class="sxs-lookup"><span data-stu-id="167c9-133">As a SOC analyst, I need to view, correlate, assess and manage alerts and events across devices, users, and mailboxes in my network.</span></span> <span data-ttu-id="167c9-134">[Gestion des incidents]</span><span class="sxs-lookup"><span data-stu-id="167c9-134">[Incident management]</span></span>
- <span data-ttu-id="167c9-135">En tant qu’analyste SOC, j’ai besoin de l’outil et du processus pour examiner et répondre automatiquement aux événements malveillants de mon réseau.</span><span class="sxs-lookup"><span data-stu-id="167c9-135">As a SOC analyst, I must have the tool and process to automatically investigate and respond to malicious events in my network.</span></span> <span data-ttu-id="167c9-136">[Auto IR]</span><span class="sxs-lookup"><span data-stu-id="167c9-136">[Auto IR]</span></span>
- <span data-ttu-id="167c9-137">En tant qu’analyste SOC, je dois Rechercher des données dans mon environnement pour trouver des menaces connues et potentielles, ainsi que des activités suspectes.</span><span class="sxs-lookup"><span data-stu-id="167c9-137">As a SOC analyst, I must search data from my environment to find known and potential threats, and suspicious activities.</span></span> <span data-ttu-id="167c9-138">[Chasse avancée]</span><span class="sxs-lookup"><span data-stu-id="167c9-138">[Advanced Hunting]</span></span>

<span data-ttu-id="167c9-139">N’oubliez pas que ces cas d’utilisation doivent être créés dans les paramètres de l’étendue définie.</span><span class="sxs-lookup"><span data-stu-id="167c9-139">Keep in mind that these use cases should be created within the parameters of the defined scope.</span></span> <span data-ttu-id="167c9-140">Si, par exemple, l’étendue du test n’inclut pas une évaluation des outils tels que Microsoft Cloud App Security, alors les cas d’utilisation qui s’en reposent en tant que source de données ne doivent pas être créés.</span><span class="sxs-lookup"><span data-stu-id="167c9-140">If, for example, the scope of testing does not include an evaluation of tools such as Microsoft Cloud App Security, then use cases that rely on this as a data source should not be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="167c9-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="167c9-141">Requirements</span></span>

<span data-ttu-id="167c9-142">Dans la liste des cas d’utilisation, vous pouvez commencer à créer des exigences.</span><span class="sxs-lookup"><span data-stu-id="167c9-142">From the list of use cases, you can start to create requirements.</span></span> <span data-ttu-id="167c9-143">Les conditions requises incluent les fonctionnalités dont doit disposer un outil pour satisfaire les cas d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="167c9-143">Requirements include features a tool must have to satisfy the use cases.</span></span> <span data-ttu-id="167c9-144">Ces exigences peuvent être divisées en catégories telles que la configuration et la maintenance, la prise en charge des intégrations et les exigences spécifiques aux fonctionnalités telles que la possibilité de la chasse et la possibilité de créer des alertes personnalisées.</span><span class="sxs-lookup"><span data-stu-id="167c9-144">These requirements can be broken down into categories such as configuration and maintenance, support for integrations, and feature-specific requirements like hunting ability and the ability to build custom alerts.</span></span>

## <a name="test-plan"></a><span data-ttu-id="167c9-145">Plan de test</span><span class="sxs-lookup"><span data-stu-id="167c9-145">Test plan</span></span>

<span data-ttu-id="167c9-146">Selon les exigences, différentes méthodes de test peuvent être appropriées.</span><span class="sxs-lookup"><span data-stu-id="167c9-146">Depending on the requirements, different methods of testing may be appropriate.</span></span> <span data-ttu-id="167c9-147">Par exemple, si l’impératif est d’évaluer l’efficacité de la correction automatisée, le plan de test doit inclure des étapes pour générer le ou les comportements qui déclencheraient une action de correction automatisée dans Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="167c9-147">For instance, if the requirement is to evaluate the efficacy of Automated Remediation, the test plan needs to include steps to generate the behavior(s) that would trigger an automated remediation action within Microsoft 365 Defender.</span></span> <span data-ttu-id="167c9-148">Si la nécessité est de détecter un comportement ou une attaque particulière, le test peut impliquer davantage d’étapes.</span><span class="sxs-lookup"><span data-stu-id="167c9-148">If the requirement is to detect a particular behavior or attack, then the test may involve more steps.</span></span> <span data-ttu-id="167c9-149">Le point doit disposer d’un plan en place pour tester précisément votre configuration requise.</span><span class="sxs-lookup"><span data-stu-id="167c9-149">The point is to have a plan in place to accurately test against your requirements.</span></span>

## <a name="success-criteria"></a><span data-ttu-id="167c9-150">Critères de réussite</span><span class="sxs-lookup"><span data-stu-id="167c9-150">Success criteria</span></span>

<span data-ttu-id="167c9-151">Les critères de réussite correspondent finalement à la barre de mesure par rapport à ce que vous testez.</span><span class="sxs-lookup"><span data-stu-id="167c9-151">Success criteria is ultimately the bar set to measure against what you are testing.</span></span> <span data-ttu-id="167c9-152">Que vous testiez Microsoft 365 Defender (ou toute autre technologie) contre d’autres outils ou par lui-même, il doit exister des critères quantifiables pour déterminer la valeur fournie par l’outil.</span><span class="sxs-lookup"><span data-stu-id="167c9-152">Whether you are testing Microsoft 365 Defender (or any other technology for that matter) against other tools or by itself, there must be some quantifiable criteria to determine the value the tool provides.</span></span> <span data-ttu-id="167c9-153">En fonction de l’étendue, des exigences et du plan de test, les critères de réussite déterminent le score du test.</span><span class="sxs-lookup"><span data-stu-id="167c9-153">Based on the scope, requirements, and testing plan, the success criteria will determine how to score the test.</span></span> <span data-ttu-id="167c9-154">Cela doit être inférieur à la réussite ou à l’échec, ainsi qu’à un score pondéré en fonction de vos besoins.</span><span class="sxs-lookup"><span data-stu-id="167c9-154">This should be less of a pass or fail and more of a weighted scoring based on your needs.</span></span> <span data-ttu-id="167c9-155">Par exemple, pour réussir, un outil peut avoir besoin d’un score supérieur à 80% dans certaines zones critiques que vous identifiez.</span><span class="sxs-lookup"><span data-stu-id="167c9-155">For example, to be successful, a tool may need to score above 80% in certain critical areas you identify.</span></span>

## <a name="scorecard"></a><span data-ttu-id="167c9-156">Prospectif</span><span class="sxs-lookup"><span data-stu-id="167c9-156">Scorecard</span></span>

<span data-ttu-id="167c9-157">Une façon de rassembler tous les éléments de votre plan peut consister à créer une carte de performance.</span><span class="sxs-lookup"><span data-stu-id="167c9-157">One way to bring all elements of your plan together can be to create a scorecard.</span></span> <span data-ttu-id="167c9-158">Voir un exemple de carte de performance ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="167c9-158">See a sample scorecard below:</span></span>

| <span data-ttu-id="167c9-159">Cas d’utilisation</span><span class="sxs-lookup"><span data-stu-id="167c9-159">Use case</span></span> | <span data-ttu-id="167c9-160">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="167c9-160">Requirements</span></span> | <span data-ttu-id="167c9-161">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="167c9-161">Configuration requirements</span></span> | <span data-ttu-id="167c9-162">Plan de test</span><span class="sxs-lookup"><span data-stu-id="167c9-162">Test plan</span></span> | <span data-ttu-id="167c9-163">Résultat attendu</span><span class="sxs-lookup"><span data-stu-id="167c9-163">Expected outcome</span></span> | <span data-ttu-id="167c9-164">État du test</span><span class="sxs-lookup"><span data-stu-id="167c9-164">Test status</span></span> | <span data-ttu-id="167c9-165">Niveau</span><span class="sxs-lookup"><span data-stu-id="167c9-165">Score</span></span> | <span data-ttu-id="167c9-166">Notes</span><span class="sxs-lookup"><span data-stu-id="167c9-166">Notes</span></span> |
|:-------|:-------|:-------|:-------|:-------|:-------|:-------|:-------|
|<span data-ttu-id="167c9-167">Gestion des incidents</span><span class="sxs-lookup"><span data-stu-id="167c9-167">Incident management</span></span>|<span data-ttu-id="167c9-168">-Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="167c9-168">-  Microsoft 365 Defender</span></span>  </br></br><span data-ttu-id="167c9-169">-Microsoft Defender pour l’identité</span><span class="sxs-lookup"><span data-stu-id="167c9-169">- Microsoft Defender for Identity</span></span> </br></br><span data-ttu-id="167c9-170">-Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="167c9-170">- Microsoft Defender for Endpoint</span></span> </br></br><span data-ttu-id="167c9-171">-Sécurité des applications Cloud Microsoft (facultatif)</span><span class="sxs-lookup"><span data-stu-id="167c9-171">- Microsoft Cloud App Security (optional)</span></span>|<span data-ttu-id="167c9-172">Voir les [conditions préalables](https://aka.ms/mtp-trial-lab) pour la préparation, l’installation et la configuration pour plus de détails</span><span class="sxs-lookup"><span data-stu-id="167c9-172">See the [prerequisites](https://aka.ms/mtp-trial-lab) for preparation, set-up, and configuration for details</span></span> |[<span data-ttu-id="167c9-173">Simuler une attaque</span><span class="sxs-lookup"><span data-stu-id="167c9-173">Simulate attack</span></span>](mtp-pilot-simulate.md) <br></br>[<span data-ttu-id="167c9-174">Examen de l’incident</span><span class="sxs-lookup"><span data-stu-id="167c9-174">Investigate the incident</span></span>](https://docs.microsoft.com/microsoft-365/security/mtp/mtp-pilot-simulate#investigate-an-incident) |<span data-ttu-id="167c9-175">Les investigateurs peuvent comprendre l’étendue et l’impact de l’incident et gérer l’incident.</span><span class="sxs-lookup"><span data-stu-id="167c9-175">Investigators can understand the scope and impact of the incident and manage the incident</span></span>||||
|<span data-ttu-id="167c9-176">AutoIR</span><span class="sxs-lookup"><span data-stu-id="167c9-176">AutoIR</span></span>|<span data-ttu-id="167c9-177">-Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="167c9-177">-   Microsoft 365 Defender</span></span> </br></br><span data-ttu-id="167c9-178">-Microsoft Defender pour l’identité</span><span class="sxs-lookup"><span data-stu-id="167c9-178">- Microsoft Defender for Identity</span></span> </br></br><span data-ttu-id="167c9-179">-Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="167c9-179">- Microsoft Defender for Endpoint</span></span> |<span data-ttu-id="167c9-180">Voir les [conditions préalables](https://aka.ms/mtp-trial-lab) pour la préparation, l’installation et la configuration pour plus de détails</span><span class="sxs-lookup"><span data-stu-id="167c9-180">See the [prerequisites](https://aka.ms/mtp-trial-lab) for preparation, set-up, and configuration for details</span></span> <br><span data-ttu-id="167c9-181">Activer AutoIR</span><span class="sxs-lookup"><span data-stu-id="167c9-181">Enable AutoIR</span></span>  |[<span data-ttu-id="167c9-182">Simuler une attaque</span><span class="sxs-lookup"><span data-stu-id="167c9-182">Simulate attack</span></span>](mtp-pilot-simulate.md) <br></br>[<span data-ttu-id="167c9-183">Enquête automatisée</span><span class="sxs-lookup"><span data-stu-id="167c9-183">Automated investigation</span></span>](https://docs.microsoft.com/microsoft-365/security/mtp/mtp-pilot-simulate.md#automated-investigation-and-remediation) |<span data-ttu-id="167c9-184">Les alertes et les incidents sont automatiquement résolus par Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="167c9-184">Alerts and incidents are automatically remediated by Microsoft 365 Defender</span></span>||||
|<span data-ttu-id="167c9-185">Repérage avancé</span><span class="sxs-lookup"><span data-stu-id="167c9-185">Advanced hunting</span></span>|<span data-ttu-id="167c9-186">-Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="167c9-186">- Microsoft 365 Defender</span></span> </br></br><span data-ttu-id="167c9-187">-Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="167c9-187">- Microsoft Defender for Endpoint</span></span> </br></br><span data-ttu-id="167c9-188">-Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="167c9-188">-Microsoft Defender for Office 365</span></span> |<span data-ttu-id="167c9-189">Voir les [conditions préalables](https://aka.ms/mtp-trial-lab) pour la préparation, l’installation et la configuration pour plus de détails</span><span class="sxs-lookup"><span data-stu-id="167c9-189">See the [prerequisites](https://aka.ms/mtp-trial-lab) for preparation, set-up, and configuration for details</span></span>|[<span data-ttu-id="167c9-190">Scénario de chasse avancé</span><span class="sxs-lookup"><span data-stu-id="167c9-190">Advanced hunting scenario</span></span>](https://docs.microsoft.com/microsoft-365/security/mtp/mtp-pilot-simulate.md#advanced-hunting-scenario) |<span data-ttu-id="167c9-191">Les investigateurs peuvent trouver des données par le biais d’une recherche avancée, d’un pivotement vers des entités affectées et en créant des détections personnalisées.</span><span class="sxs-lookup"><span data-stu-id="167c9-191">Investigators can find data through advanced hunting, pivoting to impacted entities, and by creating custom detections</span></span>||||



## <a name="next-step"></a><span data-ttu-id="167c9-192">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="167c9-192">Next step</span></span>
|<span data-ttu-id="167c9-193">![Phase de préparation](../../media/mtp/prep.png)</span><span class="sxs-lookup"><span data-stu-id="167c9-193">![Preparation phase](../../media/mtp/prep.png)</span></span> <br>[<span data-ttu-id="167c9-194">Phase de préparation</span><span class="sxs-lookup"><span data-stu-id="167c9-194">Preparation phase</span></span>](prepare-mtpeval.md) | <span data-ttu-id="167c9-195">Préparation de votre environnement pilote Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="167c9-195">Prepare your Microsoft 365 Defender pilot environment</span></span>
|:-------|:-----|
