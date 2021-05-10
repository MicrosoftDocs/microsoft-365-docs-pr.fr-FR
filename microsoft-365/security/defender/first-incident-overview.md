---
title: Présentation de la réponse à votre premier incident
description: Principes de base de la réponse à votre premier incident dans Microsoft 365 Defender.
keywords: incidents, alertes, examiner, corrélation, attaque, appareils, utilisateurs, identités, identité, boîte aux lettres, courrier électronique, 365, microsoft, m365, réponse aux incidents, cyber-attaque
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
ms.openlocfilehash: 5ea847e822e094049dd8f0b941f22f3bb4f7eff4
ms.sourcegitcommit: de5fce90de22ba588e75e1a1d2e87e03b9e25ec7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "52297175"
---
# <a name="introduction-to-responding-to-your-first-incident"></a><span data-ttu-id="c52bc-104">Présentation de la réponse à votre premier incident</span><span class="sxs-lookup"><span data-stu-id="c52bc-104">Introduction to responding to your first incident</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

<span data-ttu-id="c52bc-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="c52bc-105">**Applies to:**</span></span>
- <span data-ttu-id="c52bc-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="c52bc-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="c52bc-107">La stratégie de réponse aux incidents d’une organisation détermine sa capacité à gérer les incidents de sécurité et la cybercriminalité de plus en plus perturbants.</span><span class="sxs-lookup"><span data-stu-id="c52bc-107">An organization's incident response strategy determines its ability to deal with increasingly disruptive security incidents and cybercrime.</span></span> <span data-ttu-id="c52bc-108">Bien que la prise de mesures préventives soit importante, la possibilité d’agir rapidement pour contenir, atténuer et récupérer des incidents détectés peut réduire les dommages et les pertes de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="c52bc-108">While taking preventative measures is important, the ability to act quickly to contain, eradicate, and recover from detected incidents can minimize damage and business losses.</span></span>

<span data-ttu-id="c52bc-109">Cette procédure pas à pas de réponse aux incidents montre comment, dans le cadre d’une équipe des opérations de sécurité, vous pouvez effectuer la plupart des étapes clés de réponse aux incidents dans Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="c52bc-109">This incident response walkthrough shows how you, as part of a security operations team, can perform most of the key incident response steps within Microsoft 365 Defender.</span></span> <span data-ttu-id="c52bc-110">Voici les étapes à effectuer :</span><span class="sxs-lookup"><span data-stu-id="c52bc-110">Here are the steps:</span></span>

- <span data-ttu-id="c52bc-111">Préparation de votre posture de sécurité</span><span class="sxs-lookup"><span data-stu-id="c52bc-111">Preparation of your security posture</span></span>
- <span data-ttu-id="c52bc-112">Pour chaque incident :</span><span class="sxs-lookup"><span data-stu-id="c52bc-112">For each incident:</span></span>
  - <span data-ttu-id="c52bc-113">Étape 1 : Tri et analyse</span><span class="sxs-lookup"><span data-stu-id="c52bc-113">Step 1: Triage and analysis</span></span>
  - <span data-ttu-id="c52bc-114">Étape 2 : correction (élimination, éradication et récupération)</span><span class="sxs-lookup"><span data-stu-id="c52bc-114">Step 2: Remediation (containment, eradication, and recovery)</span></span>
  - <span data-ttu-id="c52bc-115">Étape 3 : révision post-incident</span><span class="sxs-lookup"><span data-stu-id="c52bc-115">Step 3: Post-incident review</span></span>

<span data-ttu-id="c52bc-116">Un incident de sécurité est défini par le National Institute of Standards and Technology (NIST) comme « une occurrence qui met réellement ou potentiellement en danger la confidentialité, l’intégrité ou la disponibilité d’un système d’information ; ou les informations que le système traite, stocke ou transmet ; ou qui constitue une violation ou une menace imminente de violation des stratégies de sécurité, des procédures de sécurité ou des stratégies d’utilisation acceptables. »</span><span class="sxs-lookup"><span data-stu-id="c52bc-116">A security incident is defined by National Institute of Standards and Technology (NIST) as "an occurrence that actually or potentially jeopardizes the confidentiality, integrity, or availability of an information system; or the information the system processes, stores, or transmits; or that constitutes a violation or imminent threat of violation of security policies, security procedures, or acceptable use policies."</span></span>

<span data-ttu-id="c52bc-117">Les incidents dans Microsoft 365 Defender sont les points de départ logiques pour l’analyse et la réponse aux incidents.</span><span class="sxs-lookup"><span data-stu-id="c52bc-117">Incidents in Microsoft 365 Defender are the logical starting points for analysis and incident response.</span></span> <span data-ttu-id="c52bc-118">L’analyse et la correction des incidents constitue généralement la plupart des tâches d’une équipe des opérations de sécurité.</span><span class="sxs-lookup"><span data-stu-id="c52bc-118">Analyzing and remediating incidents typically makes up most of a security operations team's tasks.</span></span>

## <a name="next-step"></a><span data-ttu-id="c52bc-119">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="c52bc-119">Next step</span></span>

<span data-ttu-id="c52bc-120">[![Préparer votre organisation et votre client Microsoft 365 client](../../media/first-incident-overview/first-incident-path.png)](first-incident-prepare.md)</span><span class="sxs-lookup"><span data-stu-id="c52bc-120">[![Prepare your organization and Microsoft 365 tenant](../../media/first-incident-overview/first-incident-path.png)](first-incident-prepare.md)</span></span>

<span data-ttu-id="c52bc-121">Assurez-vous que votre organisation et Microsoft 365 client sont [prêts pour la gestion des incidents.](first-incident-prepare.md)</span><span class="sxs-lookup"><span data-stu-id="c52bc-121">Make sure your organization and Microsoft 365 tenant is [prepared for incident handling](first-incident-prepare.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="c52bc-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c52bc-122">See also</span></span>

<span data-ttu-id="c52bc-123">Conseils de réponse aux incidents pour Microsoft 365 Defender :</span><span class="sxs-lookup"><span data-stu-id="c52bc-123">Incident response guidance for Microsoft 365 Defender:</span></span>

- [<span data-ttu-id="c52bc-124">Vue d’ensemble des incidents</span><span class="sxs-lookup"><span data-stu-id="c52bc-124">Incidents overview</span></span>](incidents-overview.md)
- [<span data-ttu-id="c52bc-125">Enquêter sur des incidents</span><span class="sxs-lookup"><span data-stu-id="c52bc-125">Investigate incidents</span></span>](investigate-incidents.md)
- [<span data-ttu-id="c52bc-126">Gérer les incidents</span><span class="sxs-lookup"><span data-stu-id="c52bc-126">Manage incidents</span></span>](manage-incidents.md)

<span data-ttu-id="c52bc-127">Exemples supplémentaires de réponses aux premiers incidents :</span><span class="sxs-lookup"><span data-stu-id="c52bc-127">Additional examples of first incident responses:</span></span>

- [<span data-ttu-id="c52bc-128">Courriers hameçons</span><span class="sxs-lookup"><span data-stu-id="c52bc-128">Phishing email</span></span>](first-incident-path-phishing.md)
- [<span data-ttu-id="c52bc-129">Attaque de base d’identité</span><span class="sxs-lookup"><span data-stu-id="c52bc-129">Identity-base attack</span></span>](first-incident-path-identity.md)

[<span data-ttu-id="c52bc-130">Manuels de réponse aux incidents détaillés</span><span class="sxs-lookup"><span data-stu-id="c52bc-130">Detailed incident response playbooks</span></span>](https://docs.microsoft.com/security/compass/incident-response-playbooks)


