---
title: Synthèse des résultats du projet pilote Microsoft Threat Protection
description: Concluez votre projet pilote de protection Microsoft contre les menaces en complétant votre carte de performance, en analysant les résultats de vos rapports et en choisissant le mode de déplacement vers l’avant.
keywords: Microsoft Threat Protection Pilot, déterminer ce qu’il faut faire immédiatement après le projet pilote de protection contre les menaces Microsoft, ce qu’il faut faire après avoir évalué Microsoft Threat Protection en production, passer de Microsoft Threat Protection Pilot au déploiement, Cyber Security, Advanced persistent, Enterprise Security, périphériques, Device, Identity, Users, Data, applications, incidents, analyse et correction automatisées
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
ms.openlocfilehash: 1a7b87432ce1eb16c29f462fb4865bfa5c5e2201
ms.sourcegitcommit: a83acd5b9eeefd2e20e5bac916fe29d09fb53de9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/10/2020
ms.locfileid: "48418096"
---
# <a name="closing-and-summarizing-your-microsoft-threat-protection-pilot"></a><span data-ttu-id="e829f-104">Fermeture et synthèse de votre programme pilote de protection contre les menaces Microsoft</span><span class="sxs-lookup"><span data-stu-id="e829f-104">Closing and summarizing your Microsoft Threat Protection pilot</span></span>  

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="e829f-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="e829f-105">**Applies to:**</span></span>
- <span data-ttu-id="e829f-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="e829f-106">Microsoft Threat Protection</span></span>

<br>
<table border="0" width="100%" align="center">
  <tr style="text-align:center;">
    <td align="center" style="width:25%; border:0;" >
      <a href= "https://docs.microsoft.com/microsoft-365/security/mtp/mtp-pilot-plan"> 
        <img src="../../media/mtp/plan.png" alt="Plan your pilot Microsoft Threat Protection project" title="Planification de votre projet pilote de protection contre les menaces Microsoft" />
      <br/><span data-ttu-id="e829f-108">Coplanaires </a></span><span class="sxs-lookup"><span data-stu-id="e829f-108">Plan </a></span></span><br>
    </td>
    <td align="center">
      <a href="https://docs.microsoft.com/microsoft-365/security/mtp/prepare-mtpeval">
        <img src="../../media/mtp/prep.png" alt="Prepare your Microsoft Threat Protection trial lab or pilot environment" title="Préparation de votre laboratoire d’évaluation ou de votre environnement pilote Microsoft Threat Protection" />
      <br/><span data-ttu-id="e829f-110">Instructions </a></span><span class="sxs-lookup"><span data-stu-id="e829f-110">Prepare </a></span></span><br>
    </td>
    <td align="center">
      <a href="https://docs.microsoft.com/microsoft-365/security/mtp/mtp-pilot-simulate">
        <img src="../../media/mtp/run-sim.png" alt="Run your Microsoft Threat Protection attack simulations" title="Exécuter vos simulations d’attaque de la protection contre les menaces Microsoft" />
      <br/><span data-ttu-id="e829f-112">Simuler une attaque </a></span><span class="sxs-lookup"><span data-stu-id="e829f-112">Simulate attack </a></span></span><br>
    </td>
    <td align="center"bgcolor="#d5f5e3">
      <a href="https://docs.microsoft.com/microsoft-365/security/mtp/mtp-pilot-close">
        <img src="../../media/mtp/close.png" alt="Close and summarize your Microsoft Threat Protection pilot" title="Fermer et résumer votre programme pilote de protection contre les menaces Microsoft" />
      <br/><span data-ttu-id="e829f-114">Fermer et résumer </a></span><span class="sxs-lookup"><span data-stu-id="e829f-114">Close and summarize </a></span></span><br>
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

<span data-ttu-id="e829f-115">Vous êtes actuellement à la fin de la phase de clôture et de synthèse.</span><span class="sxs-lookup"><span data-stu-id="e829f-115">You're currently in the closing and summarizing phase.</span></span>

<span data-ttu-id="e829f-116">Vous venez d’exécuter une simulation d’attaque de mémoire avancée uniquement qui a exécuté le code à distance sur un contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="e829f-116">You’ve just ran an advanced memory-only attack simulation that executed code remotely on a domain controller.</span></span> <span data-ttu-id="e829f-117">Vous avez vu comment Microsoft Defender ATP et Azure ATP détectent et créent des alertes sur les activités malveillantes de Stealthy.</span><span class="sxs-lookup"><span data-stu-id="e829f-117">You’ve seen how Microsoft Defender ATP and Azure ATP detect and create alerts on stealthy malicious activity.</span></span> <span data-ttu-id="e829f-118">Vous avez également vu comment les alertes provenant de sources différentes sont fournies, ainsi que d’autres informations contextuelles en un seul incident dans le portail du centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="e829f-118">You’ve also seen how alerts from different sources are delivered along with other contextual information into a single incident in the Microsoft 365 Security Center portal.</span></span> <span data-ttu-id="e829f-119">Cette intégration permet à des analystes SOC d’examiner et de prendre les mesures nécessaires.</span><span class="sxs-lookup"><span data-stu-id="e829f-119">Experiencing such integration enables SOC analysts to investigate and take necessary action.</span></span> <span data-ttu-id="e829f-120">Vous avez également créé une requête de chasse avancée qui identifie les messages électroniques entrants à l’endroit où l’utilisateur a ouvert ou enregistré la pièce jointe et a créé une détection basée sur cette requête.</span><span class="sxs-lookup"><span data-stu-id="e829f-120">You’ve also created an advanced hunting query that will identify inbound emails where the user opened or saved the attachment and created detection based on that query.</span></span>

<span data-ttu-id="e829f-121">Vous avez atteint la fin du processus une fois tous les tests terminés.</span><span class="sxs-lookup"><span data-stu-id="e829f-121">You’ve reached the end of the process after all tests have concluded.</span></span>

<span data-ttu-id="e829f-122">La sortie finale doit être :</span><span class="sxs-lookup"><span data-stu-id="e829f-122">The final output should be:</span></span>

- <span data-ttu-id="e829f-123">Une carte de performance terminée</span><span class="sxs-lookup"><span data-stu-id="e829f-123">A completed scorecard</span></span>
- <span data-ttu-id="e829f-124">Un rapport détaillé sur les résultats du projet pilote</span><span class="sxs-lookup"><span data-stu-id="e829f-124">A detailed report of the findings of the pilot</span></span>
- <span data-ttu-id="e829f-125">Une décision concernant le déplacement vers l’avant</span><span class="sxs-lookup"><span data-stu-id="e829f-125">A decision on how to move forward</span></span>

<span data-ttu-id="e829f-126">Présenter les rapports de la sortie finale des parties prenantes internes (que vous avez identifiées pendant la phase de [préparation](https://docs.microsoft.com/microsoft-365/security/mtp/prepare-mtpeval) ) et des contacts Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e829f-126">Present the reports from your final output both internal stakeholders (which you’ve identified during the [preparation](https://docs.microsoft.com/microsoft-365/security/mtp/prepare-mtpeval) phase) and Microsoft contacts.</span></span> <span data-ttu-id="e829f-127">Un tel effort garantit que les commentaires peuvent être utilisés pour améliorer les produits et la documentation.</span><span class="sxs-lookup"><span data-stu-id="e829f-127">Such an effort ensures that any feedback can be used to improve products and documentation.</span></span>

<span data-ttu-id="e829f-128">Nous espérons que vous avez apprécié cette simulation.</span><span class="sxs-lookup"><span data-stu-id="e829f-128">We hope you enjoyed this simulation.</span></span> <span data-ttu-id="e829f-129">Commencez à implémenter ce que vous avez appris à une plus grande échelle dans votre organisation pour tirer le meilleur parti de la solution de sécurité intégrée.</span><span class="sxs-lookup"><span data-stu-id="e829f-129">Start implementing what you've learned on a larger scale in your organization to get the most out of the integrated security solution.</span></span>

## <a name="next-step"></a><span data-ttu-id="e829f-130">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="e829f-130">Next step</span></span>
<span data-ttu-id="e829f-131">Pour plus d’informations sur les piliers de la protection contre les menaces Microsoft, consultez les guides interactifs suivants :</span><span class="sxs-lookup"><span data-stu-id="e829f-131">Learn more about the Microsoft Threat Protection pillars through the following interactive guides:</span></span>
- [<span data-ttu-id="e829f-132">Protéger votre organisation avec Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="e829f-132">Safeguard your organization with Microsoft Defender for Office 365</span></span>](https://aka.ms/O365ATP-Interactive-Guide)
- [<span data-ttu-id="e829f-133">Détecter les activités suspectes et les attaques potentielles avec Microsoft Defender pour l’identité</span><span class="sxs-lookup"><span data-stu-id="e829f-133">Detect suspicious activities and potential attacks with Microsoft Defender for Identity</span></span>](https://aka.ms/AATP-Interactive-Guide)
- [<span data-ttu-id="e829f-134">Détecter les menaces et gérer les alertes à l’aide de Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="e829f-134">Detect threats and manage alerts with Microsoft Cloud App Security</span></span>](https://aka.ms/DetectThreatsAndAlertsMCAS-InteractiveGuide)
- [<span data-ttu-id="e829f-135">Examiner et résoudre les menaces avec Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="e829f-135">Investigate and remediate threats with Microsoft Defender for Endpoint</span></span>](https://aka.ms/MDATP-IR-Interactive-Guide)
