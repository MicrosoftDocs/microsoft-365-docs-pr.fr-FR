---
title: Étape 3. Effectuer un examen post-incident de votre premier incident
description: Comment passer en revue votre premier incident dans Microsoft 365 Defender.
keywords: incidents, alertes, enquêter, corrélation, attaque, machines, appareils, utilisateurs, identités, identité, boîte de réception, e-mail, 365, microsoft, m365
search.product: eADQiWindows 10XVcnh
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
search.appverid:
- MOE150
- MET150
ms.technology: m365d
ms.openlocfilehash: 1ceea1dbdb3f9d149f4e5a0bd892eda2bb9128aa
ms.sourcegitcommit: 05f40904f8278f53643efa76a907968b5c662d9a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/30/2021
ms.locfileid: "52114640"
---
# <a name="step-3-perform-a-post-incident-review-of-your-first-incident"></a><span data-ttu-id="0b07f-105">Étape 3.</span><span class="sxs-lookup"><span data-stu-id="0b07f-105">Step 3.</span></span> <span data-ttu-id="0b07f-106">Effectuer un examen post-incident de votre premier incident</span><span class="sxs-lookup"><span data-stu-id="0b07f-106">Perform a post-incident review of your first incident</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

<span data-ttu-id="0b07f-107">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="0b07f-107">**Applies to:**</span></span>
- <span data-ttu-id="0b07f-108">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="0b07f-108">Microsoft 365 Defender</span></span>

<span data-ttu-id="0b07f-109">Le National Institute of Standards and Technology (NIST) recommande qu'une fois que toutes les mesures ont été prises pour récupérer après l'attaque, les organisations doivent passer en revue l'incident pour en apprendre davantage et apprendre et améliorer la posture ou les processus de sécurité.</span><span class="sxs-lookup"><span data-stu-id="0b07f-109">National Institute of Standards and Technology (NIST) recommends that once all steps have been taken to recover from the attack, organizations must review the incident to learn from it and learn and improve security posture or processes.</span></span> <span data-ttu-id="0b07f-110">L'évaluation des différents aspects de la gestion des incidents devient importante lors de la préparation du prochain incident.</span><span class="sxs-lookup"><span data-stu-id="0b07f-110">Assessing the different aspects of incident-handling becomes important in preparing for the next incident.</span></span>

<span data-ttu-id="0b07f-111">Microsoft 365 Defender peut vous aider à effectuer des activités post-incident en fournissant à une organisation des alertes qui s'alignent sur [MITRE ATT&CK Framework](https://attack.mitre.org/).</span><span class="sxs-lookup"><span data-stu-id="0b07f-111">Microsoft 365 Defender can assist in performing post-incident activities by providing an organization with alerts that align with [MITRE ATT&CK Framework](https://attack.mitre.org/).</span></span> <span data-ttu-id="0b07f-112">Toutes les solutions Microsoft Defender étiquettent les attaques conformément à une technique ou une&CK att.</span><span class="sxs-lookup"><span data-stu-id="0b07f-112">All Microsoft Defender solutions label attacks in accordance with an ATT&CK tactic or technique.</span></span> 

<span data-ttu-id="0b07f-113">En m mappage d'alertes à cette infrastructure du secteur, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="0b07f-113">By mapping alerts to this industry framework, you can:</span></span>

- <span data-ttu-id="0b07f-114">Effectuer une analyse des lacunes dans la couverture de sécurité.</span><span class="sxs-lookup"><span data-stu-id="0b07f-114">Conduct an analysis of gaps in security coverage.</span></span>
- <span data-ttu-id="0b07f-115">Déterminer l'adversaire et l'attribution de la campagne.</span><span class="sxs-lookup"><span data-stu-id="0b07f-115">Determine adversary and campaign attribution.</span></span>
- <span data-ttu-id="0b07f-116">Effectuer une analyse de tendance.</span><span class="sxs-lookup"><span data-stu-id="0b07f-116">Perform trend analysis.</span></span>
- <span data-ttu-id="0b07f-117">Identifier les lacunes en matière de compétences dans la sensibilisation aux méthodes d'attaque.</span><span class="sxs-lookup"><span data-stu-id="0b07f-117">Identify skill gaps in attack method awareness.</span></span>
- <span data-ttu-id="0b07f-118">Créez un Power Automate playbook pour une correction plus rapide.</span><span class="sxs-lookup"><span data-stu-id="0b07f-118">Create a Power Automate Playbook for faster remediation.</span></span> 

<span data-ttu-id="0b07f-119">L'activité de révision post-incident peut également entraîner un ajustement de la configuration de la sécurité et des processus de votre équipe de sécurité, ce qui améliore les capacités de réponse de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="0b07f-119">Post-incident review activity can also result in fine-tuning your security configuration and security team's processes, enhancing your organization’s response capabilities.</span></span>

## <a name="next-step"></a><span data-ttu-id="0b07f-120">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="0b07f-120">Next step</span></span>

<span data-ttu-id="0b07f-121">Consultez les chemins d'accès d'investigation supplémentaires ci-après :</span><span class="sxs-lookup"><span data-stu-id="0b07f-121">See these additional investigation paths:</span></span>

- [<span data-ttu-id="0b07f-122">Courriers hameçons</span><span class="sxs-lookup"><span data-stu-id="0b07f-122">Phishing email</span></span>](first-incident-path-phishing.md)
- [<span data-ttu-id="0b07f-123">Attaque basée sur l'identité</span><span class="sxs-lookup"><span data-stu-id="0b07f-123">Identity-based attack</span></span>](first-incident-path-identity.md)


## <a name="see-also"></a><span data-ttu-id="0b07f-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0b07f-124">See also</span></span>

- [<span data-ttu-id="0b07f-125">Vue d’ensemble des incidents</span><span class="sxs-lookup"><span data-stu-id="0b07f-125">Incidents overview</span></span>](incidents-overview.md)
- [<span data-ttu-id="0b07f-126">Analyser des incidents</span><span class="sxs-lookup"><span data-stu-id="0b07f-126">Analyze incidents</span></span>](investigate-incidents.md)
- [<span data-ttu-id="0b07f-127">Gérer les incidents</span><span class="sxs-lookup"><span data-stu-id="0b07f-127">Manage incidents</span></span>](manage-incidents.md)