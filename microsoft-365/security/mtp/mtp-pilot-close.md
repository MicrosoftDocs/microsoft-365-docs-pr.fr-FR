---
title: Synthèse des résultats du projet pilote Microsoft 365 Defender
description: Concluez votre projet pilote de Microsoft 365 Defender en remplissant votre carte de performance, en analysant les résultats de vos rapports et en choisissant le mode de déplacement vers l’avant.
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
ms.openlocfilehash: 3fe5bfdec566b0988d9f565595624fc8dd597788
ms.sourcegitcommit: ce46d1bd67091d4ed0e2b776dfed55e2d88cdbf4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/18/2020
ms.locfileid: "49130922"
---
# <a name="closing-and-summarizing-your-microsoft-365-defender-pilot"></a><span data-ttu-id="1cb39-104">Fermeture et synthèse de votre pilote Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="1cb39-104">Closing and summarizing your Microsoft 365 Defender pilot</span></span>  

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="1cb39-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="1cb39-105">**Applies to:**</span></span>
- <span data-ttu-id="1cb39-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="1cb39-106">Microsoft 365 Defender</span></span>



|<span data-ttu-id="1cb39-107">[![Planification](../../media/phase-diagrams/1-planning.png)](mtp-pilot-plan.md)</span><span class="sxs-lookup"><span data-stu-id="1cb39-107">[![Planning](../../media/phase-diagrams/1-planning.png)](mtp-pilot-plan.md)</span></span><br/>[<span data-ttu-id="1cb39-108">Planification</span><span class="sxs-lookup"><span data-stu-id="1cb39-108">Planning</span></span>](mtp-pilot-plan.md) |<span data-ttu-id="1cb39-109">[![Préparation](../../media/phase-diagrams/2-prepare.png)](prepare-mtpeval.md)</span><span class="sxs-lookup"><span data-stu-id="1cb39-109">[![Prepare](../../media/phase-diagrams/2-prepare.png)](prepare-mtpeval.md)</span></span><br/>[<span data-ttu-id="1cb39-110">Préparation</span><span class="sxs-lookup"><span data-stu-id="1cb39-110">Preparation</span></span>](prepare-mtpeval.md) | <span data-ttu-id="1cb39-111">[![Simuler une attaque](../../media/phase-diagrams/3-simluate.png)](mtp-pilot-simulate.md)</span><span class="sxs-lookup"><span data-stu-id="1cb39-111">[![Simulate attack](../../media/phase-diagrams/3-simluate.png)](mtp-pilot-simulate.md)</span></span><br/>[<span data-ttu-id="1cb39-112">Simuler une attaque</span><span class="sxs-lookup"><span data-stu-id="1cb39-112">Simulate attack</span></span>](mtp-pilot-simulate.md) | ![Fermer et synthétiser](../../media/phase-diagrams/4-summary.png)<br/><span data-ttu-id="1cb39-114">Fermer et synthétiser</span><span class="sxs-lookup"><span data-stu-id="1cb39-114">Close and summarize</span></span>|
|--|--|--|--|
|| | |<span data-ttu-id="1cb39-115">*Vous êtes là !*</span><span class="sxs-lookup"><span data-stu-id="1cb39-115">*You are here!*</span></span>|


<span data-ttu-id="1cb39-116">Vous êtes actuellement à la fin de la phase de clôture et de synthèse.</span><span class="sxs-lookup"><span data-stu-id="1cb39-116">You're currently in the closing and summarizing phase.</span></span>

<span data-ttu-id="1cb39-117">Vous venez d’exécuter une simulation d’attaque de mémoire avancée uniquement qui a exécuté le code à distance sur un contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="1cb39-117">You’ve just ran an advanced memory-only attack simulation that executed code remotely on a domain controller.</span></span> <span data-ttu-id="1cb39-118">Vous avez vu comment Microsoft Defender for Endpoint and Microsoft Defender for Identity Detect et créer des alertes sur les activités malveillantes Stealthy.</span><span class="sxs-lookup"><span data-stu-id="1cb39-118">You’ve seen how Microsoft Defender for Endpoint and Microsoft Defender for Identity detect and create alerts on stealthy malicious activity.</span></span> <span data-ttu-id="1cb39-119">Vous avez également vu comment les alertes provenant de sources différentes sont fournies, ainsi que d’autres informations contextuelles en un seul incident dans le portail du centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="1cb39-119">You’ve also seen how alerts from different sources are delivered along with other contextual information into a single incident in the Microsoft 365 Security Center portal.</span></span> <span data-ttu-id="1cb39-120">Cette intégration permet à des analystes SOC d’examiner et de prendre les mesures nécessaires.</span><span class="sxs-lookup"><span data-stu-id="1cb39-120">Experiencing such integration enables SOC analysts to investigate and take necessary action.</span></span> <span data-ttu-id="1cb39-121">Vous avez également créé une requête de chasse avancée qui identifie les messages électroniques entrants à l’endroit où l’utilisateur a ouvert ou enregistré la pièce jointe et a créé une détection basée sur cette requête.</span><span class="sxs-lookup"><span data-stu-id="1cb39-121">You’ve also created an advanced hunting query that will identify inbound emails where the user opened or saved the attachment and created detection based on that query.</span></span>

<span data-ttu-id="1cb39-122">Vous avez atteint la fin du processus une fois tous les tests terminés.</span><span class="sxs-lookup"><span data-stu-id="1cb39-122">You’ve reached the end of the process after all tests have concluded.</span></span>

<span data-ttu-id="1cb39-123">La sortie finale doit être :</span><span class="sxs-lookup"><span data-stu-id="1cb39-123">The final output should be:</span></span>

- <span data-ttu-id="1cb39-124">Une carte de performance terminée</span><span class="sxs-lookup"><span data-stu-id="1cb39-124">A completed scorecard</span></span>
- <span data-ttu-id="1cb39-125">Un rapport détaillé sur les résultats du projet pilote</span><span class="sxs-lookup"><span data-stu-id="1cb39-125">A detailed report of the findings of the pilot</span></span>
- <span data-ttu-id="1cb39-126">Une décision concernant le déplacement vers l’avant</span><span class="sxs-lookup"><span data-stu-id="1cb39-126">A decision on how to move forward</span></span>

<span data-ttu-id="1cb39-127">Présenter les rapports de votre production finale aux parties prenantes internes (que vous avez identifiées pendant la phase de [préparation](https://docs.microsoft.com/microsoft-365/security/mtp/prepare-mtpeval) ) et les contacts Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1cb39-127">Present the reports from your final output to internal stakeholders (which you’ve identified during the [preparation](https://docs.microsoft.com/microsoft-365/security/mtp/prepare-mtpeval) phase) and Microsoft contacts.</span></span> <span data-ttu-id="1cb39-128">Un tel effort garantit que les commentaires peuvent être utilisés pour améliorer les produits et la documentation.</span><span class="sxs-lookup"><span data-stu-id="1cb39-128">Such an effort ensures that any feedback can be used to improve products and documentation.</span></span>

<span data-ttu-id="1cb39-129">Nous espérons que vous avez apprécié cette simulation.</span><span class="sxs-lookup"><span data-stu-id="1cb39-129">We hope you enjoyed this simulation.</span></span> <span data-ttu-id="1cb39-130">Commencez à implémenter ce que vous avez appris à une plus grande échelle dans votre organisation pour tirer le meilleur parti de la solution de sécurité intégrée.</span><span class="sxs-lookup"><span data-stu-id="1cb39-130">Start implementing what you've learned on a larger scale in your organization to get the most out of the integrated security solution.</span></span>

## <a name="next-step"></a><span data-ttu-id="1cb39-131">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="1cb39-131">Next step</span></span>
<span data-ttu-id="1cb39-132">Pour plus d’informations sur les piliers de Microsoft 365 Defender, consultez les guides interactifs suivants :</span><span class="sxs-lookup"><span data-stu-id="1cb39-132">Learn more about the Microsoft 365 Defender pillars through the following interactive guides:</span></span>
- [<span data-ttu-id="1cb39-133">Protéger votre organisation avec Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="1cb39-133">Safeguard your organization with Microsoft Defender for Office 365</span></span>](https://aka.ms/O365ATP-Interactive-Guide)
- [<span data-ttu-id="1cb39-134">Détecter les activités suspectes et les attaques potentielles avec Microsoft Defender pour l’identité</span><span class="sxs-lookup"><span data-stu-id="1cb39-134">Detect suspicious activities and potential attacks with Microsoft Defender for Identity</span></span>](https://aka.ms/AATP-Interactive-Guide)
- [<span data-ttu-id="1cb39-135">Détecter les menaces et gérer les alertes à l’aide de Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="1cb39-135">Detect threats and manage alerts with Microsoft Cloud App Security</span></span>](https://aka.ms/DetectThreatsAndAlertsMCAS-InteractiveGuide)
- [<span data-ttu-id="1cb39-136">Examiner et résoudre les menaces avec Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="1cb39-136">Investigate and remediate threats with Microsoft Defender for Endpoint</span></span>](https://aka.ms/MDATP-IR-Interactive-Guide)
