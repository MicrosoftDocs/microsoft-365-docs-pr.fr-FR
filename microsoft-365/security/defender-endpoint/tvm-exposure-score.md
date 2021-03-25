---
title: Score d’exposition dans la gestion des menaces et des vulnérabilités
description: Le score d’exposition à la gestion des menaces et des vulnérabilités reflète la vulnérabilité de votre organisation aux menaces de cybersécurité.
keywords: score d’exposition, score d’exposition mdatp, score d’exposition tvm mdatp, score d’exposition de l’organisation, score d’exposition de l’organisation tvm, gestion des menaces et des vulnérabilités, Microsoft Defender pour le point de terminaison
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: ellevin
author: levinec
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- m365-security-compliance
- m365initiative-defender-endpoint
ms.topic: conceptual
ms.technology: mde
ms.openlocfilehash: cc7abd678d6f2d317d02c4ed2b8028e7e270b055
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51068449"
---
# <a name="exposure-score---threat-and-vulnerability-management"></a><span data-ttu-id="31893-104">Score d’exposition : gestion des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="31893-104">Exposure score - threat and vulnerability management</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="31893-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="31893-105">**Applies to:**</span></span>

- [<span data-ttu-id="31893-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="31893-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/?linkid=2154037)
- [<span data-ttu-id="31893-107">Gestion des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="31893-107">Threat and vulnerability management</span></span>](next-gen-threat-and-vuln-mgt.md)
- [<span data-ttu-id="31893-108">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="31893-108">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

><span data-ttu-id="31893-109">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="31893-109">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="31893-110">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="31893-110">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-portaloverview-abovefoldlink)

<span data-ttu-id="31893-111">Votre score d’exposition est visible dans le [tableau](tvm-dashboard-insights.md) de bord de gestion des menaces et des vulnérabilités du Centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="31893-111">Your exposure score is visible in the [Threat and vulnerability management dashboard](tvm-dashboard-insights.md) of the Microsoft Defender Security Center.</span></span> <span data-ttu-id="31893-112">Il reflète la vulnérabilité de votre organisation aux menaces de cybersécurité.</span><span class="sxs-lookup"><span data-stu-id="31893-112">It reflects how vulnerable your organization is to cybersecurity threats.</span></span> <span data-ttu-id="31893-113">Un faible score d’exposition signifie que vos appareils sont moins vulnérables à l’exploitation.</span><span class="sxs-lookup"><span data-stu-id="31893-113">Low exposure score means your devices are less vulnerable from exploitation.</span></span>

- <span data-ttu-id="31893-114">Comprenez et identifiez rapidement les informations de haut niveau concernant l’état de la sécurité dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="31893-114">Quickly understand and identify high-level takeaways about the state of security in your organization.</span></span>
- <span data-ttu-id="31893-115">Détecter et répondre aux domaines qui nécessitent une investigation ou une action pour améliorer l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="31893-115">Detect and respond to areas that require investigation or action to improve the current state.</span></span>
- <span data-ttu-id="31893-116">Communiquer avec les homologues et la direction sur l’impact des efforts de sécurité.</span><span class="sxs-lookup"><span data-stu-id="31893-116">Communicate with peers and management about the impact of security efforts.</span></span>

<span data-ttu-id="31893-117">La carte vous donne une vue générale de la tendance de votre score d’exposition au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="31893-117">The card gives you a high-level view of your exposure score trend over time.</span></span> <span data-ttu-id="31893-118">Les pics du graphique vous donnent une indication visuelle d’une exposition à une menace de cybersécurité élevée que vous pouvez examiner plus en détail.</span><span class="sxs-lookup"><span data-stu-id="31893-118">Any spikes in the chart give you a visual indication of a high cybersecurity threat exposure that you can investigate further.</span></span>

![Carte de score d’exposition](images/tvm_exp_score.png)

## <a name="how-it-works"></a><span data-ttu-id="31893-120">Mode de fonctionnement</span><span class="sxs-lookup"><span data-stu-id="31893-120">How it works</span></span>

<span data-ttu-id="31893-121">Le score d’exposition est décomposé selon les niveaux suivants :</span><span class="sxs-lookup"><span data-stu-id="31893-121">The exposure score is broken down into the following levels:</span></span>

- <span data-ttu-id="31893-122">0 à 29 : score d’exposition faible</span><span class="sxs-lookup"><span data-stu-id="31893-122">0–29: low exposure score</span></span>
- <span data-ttu-id="31893-123">30-69 : score d’exposition moyen</span><span class="sxs-lookup"><span data-stu-id="31893-123">30–69: medium exposure score</span></span>
- <span data-ttu-id="31893-124">70–100 : score d’exposition élevé</span><span class="sxs-lookup"><span data-stu-id="31893-124">70–100: high exposure score</span></span>

<span data-ttu-id="31893-125">Vous pouvez résoudre les problèmes en vous basant sur des [recommandations](tvm-security-recommendation.md) de sécurité prioritaires pour réduire le score d’exposition.</span><span class="sxs-lookup"><span data-stu-id="31893-125">You can remediate the issues based on prioritized [security recommendations](tvm-security-recommendation.md) to reduce the exposure score.</span></span> <span data-ttu-id="31893-126">Chaque logiciel présente des faiblesses qui sont transformées en recommandations et hiérarchisées en fonction des risques pour l’organisation.</span><span class="sxs-lookup"><span data-stu-id="31893-126">Each software has weaknesses that are transformed into recommendations and prioritized based on risk to the organization.</span></span>

## <a name="reduce-your-threat-and-vulnerability-exposure"></a><span data-ttu-id="31893-127">Réduire l’exposition aux menaces et vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="31893-127">Reduce your threat and vulnerability exposure</span></span>

<span data-ttu-id="31893-128">Réduire l’exposition aux menaces et vulnérabilités en remédiant aux [recommandations de sécurité.](tvm-security-recommendation.md)</span><span class="sxs-lookup"><span data-stu-id="31893-128">Lower your threat and vulnerability exposure by remediating [security recommendations](tvm-security-recommendation.md).</span></span> <span data-ttu-id="31893-129">Faites le plus d’impact sur votre score d’exposition en remédiant aux recommandations de sécurité les plus importantes, qui peuvent être vues dans le tableau de bord de gestion des menaces [et des vulnérabilités.](tvm-dashboard-insights.md)</span><span class="sxs-lookup"><span data-stu-id="31893-129">Make the most impact to your exposure score by remediating the top security recommendations, which can be viewed in the [threat and vulnerability management dashboard](tvm-dashboard-insights.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="31893-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="31893-130">Related topics</span></span>

- [<span data-ttu-id="31893-131">Vue d’ensemble de la gestion des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="31893-131">Threat and vulnerability management overview</span></span>](next-gen-threat-and-vuln-mgt.md)
- [<span data-ttu-id="31893-132">Score de sécurité Microsoft pour les appareils</span><span class="sxs-lookup"><span data-stu-id="31893-132">Microsoft Secure Score for Devices</span></span>](tvm-microsoft-secure-score-devices.md)
- [<span data-ttu-id="31893-133">Recommandations de sécurité</span><span class="sxs-lookup"><span data-stu-id="31893-133">Security recommendations</span></span>](tvm-security-recommendation.md)
- [<span data-ttu-id="31893-134">Chronologie des événements</span><span class="sxs-lookup"><span data-stu-id="31893-134">Event timeline</span></span>](threat-and-vuln-mgt-event-timeline.md)
