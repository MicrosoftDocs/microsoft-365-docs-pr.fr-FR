---
title: Présentation de la réponse à votre premier incident
description: Principes de base de la réponse à votre premier incident dans Microsoft 365 Defender.
keywords: incidents, alertes, examiner, corrélation, attaque, appareils, utilisateurs, identités, identité, boîte aux lettres, e-mail, 365, microsoft, m365, réponse aux incidents, cyber-attaque
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
ms.openlocfilehash: f66c9821e5db00cc3da5718f52b8aaaeff5a431e
ms.sourcegitcommit: 05f40904f8278f53643efa76a907968b5c662d9a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/30/2021
ms.locfileid: "52114628"
---
# <a name="introduction-to-responding-to-your-first-incident"></a><span data-ttu-id="87e86-104">Présentation de la réponse à votre premier incident</span><span class="sxs-lookup"><span data-stu-id="87e86-104">Introduction to responding to your first incident</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

<span data-ttu-id="87e86-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="87e86-105">**Applies to:**</span></span>
- <span data-ttu-id="87e86-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="87e86-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="87e86-107">La stratégie de réponse aux incidents d'une organisation détermine sa capacité à gérer les incidents de sécurité et la cybercriminalité de plus en plus perturbants.</span><span class="sxs-lookup"><span data-stu-id="87e86-107">An organization's incident response strategy determines its ability to deal with increasingly disruptive security incidents and cybercrime.</span></span> <span data-ttu-id="87e86-108">Bien que la prise de mesures préventives soit importante, la possibilité d'agir rapidement pour contenir, atténuer et récupérer des incidents détectés peut réduire les dommages et les pertes de l'entreprise.</span><span class="sxs-lookup"><span data-stu-id="87e86-108">While taking preventative measures is important, the ability to act quickly to contain, eradicate, and recover from detected incidents can minimize damage and business losses.</span></span>

<span data-ttu-id="87e86-109">Cette procédure pas à pas de réponse aux incidents montre comment, dans le cadre d'une équipe des opérations de sécurité, vous pouvez effectuer la plupart des étapes clés de réponse aux incidents dans Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="87e86-109">This incident response walkthrough shows how you, as part of a security operations team, can perform most of the key incident response steps within Microsoft 365 Defender.</span></span> <span data-ttu-id="87e86-110">Voici les étapes à effectuer :</span><span class="sxs-lookup"><span data-stu-id="87e86-110">Here are the steps:</span></span>

- <span data-ttu-id="87e86-111">Préparation de votre posture de sécurité</span><span class="sxs-lookup"><span data-stu-id="87e86-111">Preparation of your security posture</span></span>
- <span data-ttu-id="87e86-112">Pour chaque incident :</span><span class="sxs-lookup"><span data-stu-id="87e86-112">For each incident:</span></span>
  - <span data-ttu-id="87e86-113">Étape 1 : Tri et analyse</span><span class="sxs-lookup"><span data-stu-id="87e86-113">Step 1: Triage and analysis</span></span>
  - <span data-ttu-id="87e86-114">Étape 2 : correction (élimination, éradication et récupération)</span><span class="sxs-lookup"><span data-stu-id="87e86-114">Step 2: Remediation (containment, eradication, and recovery)</span></span>
  - <span data-ttu-id="87e86-115">Étape 3 : révision post-incident</span><span class="sxs-lookup"><span data-stu-id="87e86-115">Step 3: Post-incident review</span></span>

<span data-ttu-id="87e86-116">Un incident de sécurité est défini par le National Institute of Standards and Technology (NIST) comme « une occurrence qui met réellement ou potentiellement en danger la confidentialité, l'intégrité ou la disponibilité d'un système d'information ; ou les informations que le système traite, stocke ou transmet ; ou qui constitue une violation ou une menace imminente de violation des stratégies de sécurité, des procédures de sécurité ou des stratégies d'utilisation acceptables. »</span><span class="sxs-lookup"><span data-stu-id="87e86-116">A security incident is defined by National Institute of Standards and Technology (NIST) as "an occurrence that actually or potentially jeopardizes the confidentiality, integrity, or availability of an information system; or the information the system processes, stores, or transmits; or that constitutes a violation or imminent threat of violation of security policies, security procedures, or acceptable use policies."</span></span>

<span data-ttu-id="87e86-117">Les incidents dans Microsoft 365 Defender sont les points de départ logiques pour l'analyse et la réponse aux incidents.</span><span class="sxs-lookup"><span data-stu-id="87e86-117">Incidents in Microsoft 365 Defender are the logical starting points for analysis and incident response.</span></span> <span data-ttu-id="87e86-118">L'analyse et la correction des incidents constitue généralement la plupart des tâches d'une équipe des opérations de sécurité.</span><span class="sxs-lookup"><span data-stu-id="87e86-118">Analyzing and remediating incidents typically makes up most of a security operations team's tasks.</span></span>

## <a name="next-step"></a><span data-ttu-id="87e86-119">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="87e86-119">Next step</span></span>

<span data-ttu-id="87e86-120">[![Préparer votre organisation et votre client Microsoft 365 client](../../media/first-incident-overview/first-incident-path.png)](first-incident-prepare.md)</span><span class="sxs-lookup"><span data-stu-id="87e86-120">[![Prepare your organization and Microsoft 365 tenant](../../media/first-incident-overview/first-incident-path.png)](first-incident-prepare.md)</span></span>

<span data-ttu-id="87e86-121">Assurez-vous que votre organisation et Microsoft 365 client sont [prêts pour la gestion des incidents.](first-incident-prepare.md)</span><span class="sxs-lookup"><span data-stu-id="87e86-121">Make sure your organization and Microsoft 365 tenant is [prepared for incident handling](first-incident-prepare.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="87e86-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="87e86-122">See also</span></span>

- [<span data-ttu-id="87e86-123">Vue d’ensemble des incidents</span><span class="sxs-lookup"><span data-stu-id="87e86-123">Incidents overview</span></span>](incidents-overview.md)
- [<span data-ttu-id="87e86-124">Analyser des incidents</span><span class="sxs-lookup"><span data-stu-id="87e86-124">Analyze incidents</span></span>](investigate-incidents.md)
- [<span data-ttu-id="87e86-125">Gérer les incidents</span><span class="sxs-lookup"><span data-stu-id="87e86-125">Manage incidents</span></span>](manage-incidents.md)
