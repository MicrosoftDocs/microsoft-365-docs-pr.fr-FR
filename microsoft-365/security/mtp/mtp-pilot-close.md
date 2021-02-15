---
title: Synthèse des résultats de votre projet Microsoft 365 Defender pilote
description: Terminez votre projet Pilote Microsoft 365 Defender en complétant votre carte de performance, en analysant les résultats de votre rapport et en déterminant comment aller de l’avant.
keywords: Pilote de la Protection Microsoft contre les menaces, décidez de ce qu’il faut faire après le projet pilote de Protection Microsoft contre les menaces, ce qu’il faut faire après avoir évalué la Protection Microsoft contre les menaces en production, passer du pilote de la Protection Microsoft contre les menaces au déploiement, à la cybersécurité, aux menaces avancées persistantes, à la sécurité d’entreprise, aux appareils, aux appareils, à l’identité, aux utilisateurs, aux données, aux applications, aux incidents, à l’examen et à la correction automatisés, à la recherche avancée
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
ms.localizationpriority: medium
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
- m365solution-scenario
- m365solution-pilotmtpproject
ms.topic: conceptual
ms.technology: m365d
ms.openlocfilehash: c8608568301f11a20c940a5ff9f1c205ce6e48f1
ms.sourcegitcommit: 855719ee21017cf87dfa98cbe62806763bcb78ac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/22/2021
ms.locfileid: "49930161"
---
# <a name="closing-and-summarizing-your-microsoft-365-defender-pilot"></a><span data-ttu-id="5b36b-104">Fermeture et synthèse de votre pilote Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="5b36b-104">Closing and summarizing your Microsoft 365 Defender pilot</span></span>  

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="5b36b-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="5b36b-105">**Applies to:**</span></span>
- <span data-ttu-id="5b36b-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="5b36b-106">Microsoft 365 Defender</span></span>



|<span data-ttu-id="5b36b-107">[![Planification](../../media/phase-diagrams/1-planning.png)](mtp-pilot-plan.md)</span><span class="sxs-lookup"><span data-stu-id="5b36b-107">[![Planning](../../media/phase-diagrams/1-planning.png)](mtp-pilot-plan.md)</span></span><br/>[<span data-ttu-id="5b36b-108">Planification</span><span class="sxs-lookup"><span data-stu-id="5b36b-108">Planning</span></span>](mtp-pilot-plan.md) |<span data-ttu-id="5b36b-109">[![Préparation](../../media/phase-diagrams/2-prepare.png)](prepare-mtpeval.md)</span><span class="sxs-lookup"><span data-stu-id="5b36b-109">[![Prepare](../../media/phase-diagrams/2-prepare.png)](prepare-mtpeval.md)</span></span><br/>[<span data-ttu-id="5b36b-110">Préparation</span><span class="sxs-lookup"><span data-stu-id="5b36b-110">Preparation</span></span>](prepare-mtpeval.md) | <span data-ttu-id="5b36b-111">[![Simuler une attaque](../../media/phase-diagrams/3-simluate.png)](mtp-pilot-simulate.md)</span><span class="sxs-lookup"><span data-stu-id="5b36b-111">[![Simulate attack](../../media/phase-diagrams/3-simluate.png)](mtp-pilot-simulate.md)</span></span><br/>[<span data-ttu-id="5b36b-112">Simuler une attaque</span><span class="sxs-lookup"><span data-stu-id="5b36b-112">Simulate attack</span></span>](mtp-pilot-simulate.md) | ![Fermer et synthétiser](../../media/phase-diagrams/4-summary.png)<br/><span data-ttu-id="5b36b-114">Fermer et synthétiser</span><span class="sxs-lookup"><span data-stu-id="5b36b-114">Close and summarize</span></span>|
|--|--|--|--|
|| | |<span data-ttu-id="5b36b-115">*Vous êtes là !*</span><span class="sxs-lookup"><span data-stu-id="5b36b-115">*You are here!*</span></span>|


<span data-ttu-id="5b36b-116">Vous êtes actuellement en phase de fermeture et de synthèse.</span><span class="sxs-lookup"><span data-stu-id="5b36b-116">You're currently in the closing and summarizing phase.</span></span>

<span data-ttu-id="5b36b-117">Vous viennent d’exécuter une simulation d’attaque mémoire uniquement avancée qui exécutait le code à distance sur un contrôleur de domaine.</span><span class="sxs-lookup"><span data-stu-id="5b36b-117">You’ve just ran an advanced memory-only attack simulation that executed code remotely on a domain controller.</span></span> <span data-ttu-id="5b36b-118">Vous avez vu comment Microsoft Defender pour le point de terminaison et Microsoft Defender pour l’identité détectent et créent des alertes sur les activités malveillantes.</span><span class="sxs-lookup"><span data-stu-id="5b36b-118">You’ve seen how Microsoft Defender for Endpoint and Microsoft Defender for Identity detect and create alerts on stealthy malicious activity.</span></span> <span data-ttu-id="5b36b-119">Vous avez également vu comment les alertes provenant de différentes sources sont livrées avec d’autres informations contextuelles dans un incident unique dans le portail du Centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="5b36b-119">You’ve also seen how alerts from different sources are delivered along with other contextual information into a single incident in the Microsoft 365 Security Center portal.</span></span> <span data-ttu-id="5b36b-120">L’expérience d’une telle intégration permet aux analystes SOC d’examiner et de prendre les mesures nécessaires.</span><span class="sxs-lookup"><span data-stu-id="5b36b-120">Experiencing such integration enables SOC analysts to investigate and take necessary action.</span></span> <span data-ttu-id="5b36b-121">Vous avez également créé une requête de repérage avancé qui identifiera les e-mails entrants dans lequel l’utilisateur a ouvert ou enregistré la pièce jointe et créé la détection en fonction de cette requête.</span><span class="sxs-lookup"><span data-stu-id="5b36b-121">You’ve also created an advanced hunting query that will identify inbound emails where the user opened or saved the attachment and created detection based on that query.</span></span>

<span data-ttu-id="5b36b-122">Vous avez atteint la fin du processus une fois tous les tests terminés.</span><span class="sxs-lookup"><span data-stu-id="5b36b-122">You’ve reached the end of the process after all tests have concluded.</span></span>

<span data-ttu-id="5b36b-123">Le résultat final doit être :</span><span class="sxs-lookup"><span data-stu-id="5b36b-123">The final output should be:</span></span>

- <span data-ttu-id="5b36b-124">Une carte de performance terminée</span><span class="sxs-lookup"><span data-stu-id="5b36b-124">A completed scorecard</span></span>
- <span data-ttu-id="5b36b-125">Un rapport détaillé des résultats du projet pilote</span><span class="sxs-lookup"><span data-stu-id="5b36b-125">A detailed report of the findings of the pilot</span></span>
- <span data-ttu-id="5b36b-126">Décision sur la marche à suivre</span><span class="sxs-lookup"><span data-stu-id="5b36b-126">A decision on how to move forward</span></span>

<span data-ttu-id="5b36b-127">Présentez les rapports de votre sortie finale aux parties prenantes internes (que vous avez identifiées pendant la phase [de](https://docs.microsoft.com/microsoft-365/security/mtp/prepare-mtpeval) préparation) et aux contacts Microsoft.</span><span class="sxs-lookup"><span data-stu-id="5b36b-127">Present the reports from your final output to internal stakeholders (which you’ve identified during the [preparation](https://docs.microsoft.com/microsoft-365/security/mtp/prepare-mtpeval) phase) and Microsoft contacts.</span></span> <span data-ttu-id="5b36b-128">Un tel effort garantit que tous les commentaires peuvent être utilisés pour améliorer les produits et la documentation.</span><span class="sxs-lookup"><span data-stu-id="5b36b-128">Such an effort ensures that any feedback can be used to improve products and documentation.</span></span>

<span data-ttu-id="5b36b-129">Nous espérons que vous avez aimé cette simulation.</span><span class="sxs-lookup"><span data-stu-id="5b36b-129">We hope you enjoyed this simulation.</span></span> <span data-ttu-id="5b36b-130">Commencez à implémenter ce que vous avez appris à une plus grande échelle dans votre organisation pour tirer le meilleur partie de la solution de sécurité intégrée.</span><span class="sxs-lookup"><span data-stu-id="5b36b-130">Start implementing what you've learned on a larger scale in your organization to get the most out of the integrated security solution.</span></span>

## <a name="next-step"></a><span data-ttu-id="5b36b-131">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="5b36b-131">Next step</span></span>
<span data-ttu-id="5b36b-132">En savoir plus sur les piliers de Microsoft 365 Defender via les guides interactifs suivants :</span><span class="sxs-lookup"><span data-stu-id="5b36b-132">Learn more about the Microsoft 365 Defender pillars through the following interactive guides:</span></span>
- [<span data-ttu-id="5b36b-133">Protéger votre organisation avec Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="5b36b-133">Safeguard your organization with Microsoft Defender for Office 365</span></span>](https://aka.ms/O365ATP-Interactive-Guide)
- [<span data-ttu-id="5b36b-134">Détecter des activités suspectes et des attaques potentielles à l’aide de Microsoft Defender pour l’identité</span><span class="sxs-lookup"><span data-stu-id="5b36b-134">Detect suspicious activities and potential attacks with Microsoft Defender for Identity</span></span>](https://aka.ms/AATP-Interactive-Guide)
- [<span data-ttu-id="5b36b-135">Détecter les menaces et gérer les alertes avec Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="5b36b-135">Detect threats and manage alerts with Microsoft Cloud App Security</span></span>](https://aka.ms/DetectThreatsAndAlertsMCAS-InteractiveGuide)
- [<span data-ttu-id="5b36b-136">Examiner et corriger les menaces avec Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="5b36b-136">Investigate and remediate threats with Microsoft Defender for Endpoint</span></span>](https://aka.ms/MDATP-IR-Interactive-Guide)
