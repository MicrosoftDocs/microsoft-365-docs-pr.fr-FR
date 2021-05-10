---
title: Préparer votre posture de sécurité pour votre premier incident
description: Configurer la posture de Microsoft 365 de votre client pour votre premier incident dans Microsoft 365 Defender.
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
ms.openlocfilehash: 76bead8fd855e4119db6297d2ab1a3d08d64a48c
ms.sourcegitcommit: de5fce90de22ba588e75e1a1d2e87e03b9e25ec7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "52297163"
---
# <a name="prepare-your-security-posture-for-your-first-incident"></a><span data-ttu-id="0f1e9-104">Préparer votre posture de sécurité pour votre premier incident</span><span class="sxs-lookup"><span data-stu-id="0f1e9-104">Prepare your security posture for your first incident</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

<span data-ttu-id="0f1e9-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="0f1e9-105">**Applies to:**</span></span>
- <span data-ttu-id="0f1e9-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="0f1e9-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="0f1e9-107">La préparation de la gestion des incidents implique la configuration d’une protection suffisante du réseau d’une organisation contre différents types d’incidents de sécurité.</span><span class="sxs-lookup"><span data-stu-id="0f1e9-107">Preparing for incident handling involves setting up sufficient protection of an organization's network from different kinds of security incidents.</span></span> <span data-ttu-id="0f1e9-108">Pour réduire le risque d’incidents de sécurité, le National Institute of Standards and Technology (NIST) recommande plusieurs pratiques de sécurité, notamment les évaluations des risques, le renforcement de la sécurité de l’hôte, la configuration de réseaux en toute sécurité et la prévention des programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="0f1e9-108">To reduce the risk of security incidents, National Institute of Standards and Technology (NIST) recommends several security practices including risk assessments, hardening host security, configuring networks securely, and preventing malware.</span></span> 

<span data-ttu-id="0f1e9-109">Microsoft 365 Defender peut vous aider à résoudre plusieurs aspects de la prévention des incidents :</span><span class="sxs-lookup"><span data-stu-id="0f1e9-109">Microsoft 365 Defender can help address several aspects of incident prevention:</span></span> 

- <span data-ttu-id="0f1e9-110">Mise en œuvre [d’une infrastructure de confiance](https://docs.microsoft.com/security/zero-trust/) zéro</span><span class="sxs-lookup"><span data-stu-id="0f1e9-110">Implementing a [Zero Trust](https://docs.microsoft.com/security/zero-trust/) framework</span></span>
- <span data-ttu-id="0f1e9-111">Détermination de votre posture de sécurité en attribuant un score avec [le Niveau de sécurité Microsoft](microsoft-secure-score.md)</span><span class="sxs-lookup"><span data-stu-id="0f1e9-111">Determining your security posture by assigning a score with [Microsoft Secure Score](microsoft-secure-score.md)</span></span>
- <span data-ttu-id="0f1e9-112">Prévention des menaces par le biais d’évaluations des vulnérabilités dans [la gestion des menaces et des vulnérabilités](../defender-endpoint/next-gen-threat-and-vuln-mgt.md)</span><span class="sxs-lookup"><span data-stu-id="0f1e9-112">Preventing threats through vulnerability assessments in [Threat and Vulnerability Management](../defender-endpoint/next-gen-threat-and-vuln-mgt.md)</span></span>
- <span data-ttu-id="0f1e9-113">Comprendre les dernières menaces de sécurité afin de pouvoir les préparer</span><span class="sxs-lookup"><span data-stu-id="0f1e9-113">Understanding the latest security threats so you can prepare for them</span></span>

## <a name="step-1-implement-zero-trust"></a><span data-ttu-id="0f1e9-114">Étape 1.</span><span class="sxs-lookup"><span data-stu-id="0f1e9-114">Step 1.</span></span> <span data-ttu-id="0f1e9-115">Implémenter la confiance zéro</span><span class="sxs-lookup"><span data-stu-id="0f1e9-115">Implement Zero Trust</span></span>

<span data-ttu-id="0f1e9-116">[La](https://docs.microsoft.com/security/zero-trust/) confiance zéro est une philosophie de sécurité intégrée et une stratégie de bout en bout qui considère la nature complexe de tout environnement moderne, y compris le personnel mobile et les utilisateurs, appareils, applications et données, où qu’ils se trouvent.</span><span class="sxs-lookup"><span data-stu-id="0f1e9-116">[Zero Trust](https://docs.microsoft.com/security/zero-trust/) is an integrated security philosophy and end-to-end strategy that considers the complex nature of any modern environment, including the mobile workforce and the users, devices, applications and data, wherever they may be located.</span></span> <span data-ttu-id="0f1e9-117">En fournissant un volet unique pour gérer toutes les détections de point de terminaison de manière cohérente, Microsoft 365 Defender peut faciliter l’application des principes directeurs de la confiance zéro pour votre équipe en charge des [opérations](https://docs.microsoft.com/security/zero-trust/#guiding-principles-of-zero-trust) de sécurité.</span><span class="sxs-lookup"><span data-stu-id="0f1e9-117">By providing a single pane of glass to manage all endpoint detections in a consistent way, Microsoft 365 Defender can make it easier for your security operations team to implement the [guiding principles](https://docs.microsoft.com/security/zero-trust/#guiding-principles-of-zero-trust) of Zero Trust.</span></span> 

<span data-ttu-id="0f1e9-118">Les composants de Microsoft 365 Defender peuvent afficher des violations de règles qui ont été implémentées pour établir des stratégies d’accès conditionnel pour la confiance zéro en intégrant les données de Microsoft Defender pour point de terminaison (MDE) ou d’autres fournisseurs de sécurité mobile en tant que source d’informations pour les stratégies de conformité des appareils et l’implémentation de stratégies d’accès conditionnel basées sur les appareils.</span><span class="sxs-lookup"><span data-stu-id="0f1e9-118">Components of Microsoft 365 Defender can display violations of rules that have been implemented to establish Conditional Access policies for Zero Trust by integrating data from Microsoft Defender for Endpoint (MDE) or other mobile security vendors as an information source for device compliance policies and implementation of device-based Conditional Access policies.</span></span> 

<span data-ttu-id="0f1e9-119">Le risque de l’appareil influence directement les ressources qui seront accessibles par l’utilisateur de cet appareil.</span><span class="sxs-lookup"><span data-stu-id="0f1e9-119">Device risk directly influences what resources will be accessible by the user of that device.</span></span> <span data-ttu-id="0f1e9-120">Le refus d’accès aux ressources en fonction de certains critères est le thème principal de confiance zéro et Microsoft 365 Defender fournit les informations nécessaires pour déterminer les critères de niveau de confiance.</span><span class="sxs-lookup"><span data-stu-id="0f1e9-120">The denial of access to resources based on certain criteria is the main theme of Zero Trust and Microsoft 365 Defender provides information needed to determine the trust level criteria.</span></span> <span data-ttu-id="0f1e9-121">Par exemple, Microsoft 365 Defender peut fournir le niveau de version logicielle d’un appareil via la page Gestion des menaces et des vulnérabilités, tandis que les stratégies d’accès conditionnel limitent les appareils qui ont des versions obsolètes ou vulnérables.</span><span class="sxs-lookup"><span data-stu-id="0f1e9-121">For example, Microsoft 365 Defender can provide the software version level of a device through the Threat and Vulnerability Management page while Conditional Access policies restrict devices that have outdated or vulnerable versions.</span></span>

<span data-ttu-id="0f1e9-122">L’automatisation est un élément essentiel de l’implémentation et de la maintenance d’un environnement de confiance zéro, tout en réduisant le nombre d’alertes susceptibles de conduire à des événements de réponse aux incidents (IR).</span><span class="sxs-lookup"><span data-stu-id="0f1e9-122">Automation is a crucial part of implementing and maintaining a Zero Trust environment while also reducing the number of alerts that would potentially lead to incident response (IR) events.</span></span> <span data-ttu-id="0f1e9-123">Les composants de Microsoft 365 Defender peuvent être automatisés, tels que les [actions](m365d-autoir.md) de correction (appelées enquêtes pour un incident dans le centre de sécurité Microsoft 365), les actions de notification et même la création de tickets de support tels que [dans ServiceNow](https://microsoft.service-now.com/sp/).</span><span class="sxs-lookup"><span data-stu-id="0f1e9-123">Components of Microsoft 365 Defender can be automated such as [remediation actions](m365d-autoir.md) (known as investigations for an incident in the Microsoft 365 security center), notification actions, and even the creation of support tickets such as in [ServiceNow](https://microsoft.service-now.com/sp/).</span></span>

## <a name="step-2-determine-your-organizations-security-posture"></a><span data-ttu-id="0f1e9-124">Étape 2.</span><span class="sxs-lookup"><span data-stu-id="0f1e9-124">Step 2.</span></span> <span data-ttu-id="0f1e9-125">Déterminer la posture de sécurité de votre organisation</span><span class="sxs-lookup"><span data-stu-id="0f1e9-125">Determine your organization’s security posture</span></span>

<span data-ttu-id="0f1e9-126">Ensuite, les organisations peuvent utiliser le niveau de sécurité [Microsoft](microsoft-secure-score.md) dans Microsoft 365 Defender pour déterminer votre posture de sécurité actuelle et prendre en compte des recommandations sur la façon de l’améliorer.</span><span class="sxs-lookup"><span data-stu-id="0f1e9-126">Next, organizations can use the [Microsoft Secure Score](microsoft-secure-score.md) in Microsoft 365 Defender to determine your current security posture and consider recommendations on how to improve it.</span></span> <span data-ttu-id="0f1e9-127">Plus le score est élevé, plus l’organisation a mis en place de recommandations de sécurité et d’actions d’amélioration.</span><span class="sxs-lookup"><span data-stu-id="0f1e9-127">The higher the score is, the more security recommendations and improvement actions have been taken by the organization.</span></span> <span data-ttu-id="0f1e9-128">Les recommandations de niveau de sécurité peuvent être prises sur différents produits et permettre aux organisations d’augmenter leurs scores encore plus élevés.</span><span class="sxs-lookup"><span data-stu-id="0f1e9-128">Secure Score recommendations can be taken across different products and allow organizations to raise their scores even higher.</span></span> 

:::image type="content" source="../../media/first-incident-prepare/first-incident-secure-score.png" alt-text="Exemple de Niveau de sécurité Microsoft dans le Centre de sécurité Microsoft":::
 
## <a name="step-3-assess-your-organizations-vulnerability-exposure"></a><span data-ttu-id="0f1e9-130">Étape 3.</span><span class="sxs-lookup"><span data-stu-id="0f1e9-130">Step 3.</span></span> <span data-ttu-id="0f1e9-131">Évaluer l’exposition aux vulnérabilités de votre organisation</span><span class="sxs-lookup"><span data-stu-id="0f1e9-131">Assess your organization’s vulnerability exposure</span></span>

<span data-ttu-id="0f1e9-132">La prévention des incidents peut contribuer à rationaliser les opérations de sécurité afin de se concentrer sur les incidents de sécurité critiques et importants en cours.</span><span class="sxs-lookup"><span data-stu-id="0f1e9-132">Preventing incidents can help streamline security operations efforts to focus on on-going critical and important security incidents.</span></span> <span data-ttu-id="0f1e9-133">Les vulnérabilités logicielles sont souvent un point d’entrée empêchant les attaques qui peuvent entraîner un vol de données, une perte de données ou une perturbation des opérations de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="0f1e9-133">Software vulnerabilities are often a preventable entry point for attacks that can lead to data theft, data loss, or disruption of business operations.</span></span> <span data-ttu-id="0f1e9-134">Si aucune attaque n’est en cours, les opérations de sécurité doivent s’efforcer d’atteindre et de maintenir un niveau acceptable d’exposition aux vulnérabilités [dans](../defender-endpoint/tvm-exposure-score.md) leur organisation.</span><span class="sxs-lookup"><span data-stu-id="0f1e9-134">If no attacks are on-going, security operations must strive to achieve and maintain an acceptable level of [vulnerability exposure](../defender-endpoint/tvm-exposure-score.md) in their organization.</span></span>

<span data-ttu-id="0f1e9-135">Pour vérifier l’avancement des correctifs logiciels, consultez la [page](../defender-endpoint/next-gen-threat-and-vuln-mgt.md) Gestion des menaces et des vulnérabilités dans Defender pour le point de terminaison, à laquelle vous pouvez accéder à partir de Microsoft 365 Defender via l’onglet Ressources **supplémentaires.**</span><span class="sxs-lookup"><span data-stu-id="0f1e9-135">To check your software patching progress, visit the [Threat and Vulnerability Management](../defender-endpoint/next-gen-threat-and-vuln-mgt.md) page in Defender for Endpoint, which you can access from Microsoft 365 Defender through the **More resources** tab.</span></span>

:::image type="content" source="../../media/first-incident-prepare/first-incident-vulnerability.png" alt-text="Exemple de page Menace et vulnérabilité dans le Centre de sécurité Microsoft"::: 
 
## <a name="4-understand-emerging-threats"></a><span data-ttu-id="0f1e9-137">4. Comprendre les menaces émergentes</span><span class="sxs-lookup"><span data-stu-id="0f1e9-137">4. Understand emerging threats</span></span>

<span data-ttu-id="0f1e9-138">Utilisez [l’analyse des](threat-analytics.md) menaces Microsoft 365 centre de sécurité pour rester à jour avec le paysage actuel des menaces de sécurité.</span><span class="sxs-lookup"><span data-stu-id="0f1e9-138">Use [threat analytics](threat-analytics.md) in the Microsoft 365 security center to keep up-to-date with the current security threat landscape.</span></span> <span data-ttu-id="0f1e9-139">Des chercheurs spécialisés en matière de sécurité Microsoft créent des rapports qui décrivent en détail les dernières cybermenaces afin que vous compreniez en quoi elles peuvent affecter votre abonnement Microsoft 365, vos appareils et vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="0f1e9-139">Expert Microsoft security researchers create reports that describe the latest cyber-threats in detail so you can understand how they might affect your Microsoft 365 subscription, devices, and users.</span></span> <span data-ttu-id="0f1e9-140">Ces rapports peuvent inclure les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="0f1e9-140">These reports can include:</span></span>

- <span data-ttu-id="0f1e9-141">Acteurs actifs contre les menaces et leurs campagnes</span><span class="sxs-lookup"><span data-stu-id="0f1e9-141">Active threat actors and their campaigns</span></span>
- <span data-ttu-id="0f1e9-142">Techniques d’attaques nouvelles et populaires</span><span class="sxs-lookup"><span data-stu-id="0f1e9-142">Popular and new attack techniques</span></span>
- <span data-ttu-id="0f1e9-143">Vulnérabilités critiques</span><span class="sxs-lookup"><span data-stu-id="0f1e9-143">Critical vulnerabilities</span></span>
- <span data-ttu-id="0f1e9-144">Surfaces d’attaque courantes</span><span class="sxs-lookup"><span data-stu-id="0f1e9-144">Common attack surfaces</span></span>
- <span data-ttu-id="0f1e9-145">Programmes malveillants répandus</span><span class="sxs-lookup"><span data-stu-id="0f1e9-145">Prevalent malware</span></span>

<span data-ttu-id="0f1e9-146">Vous pouvez implémenter les recommandations d’une menace émergente pour renforcer votre posture de sécurité et réduire la surface d’attaque.</span><span class="sxs-lookup"><span data-stu-id="0f1e9-146">You can implement the recommendations of an emerging threat to strengthen your security posture and minimize your attack surface area.</span></span>

<span data-ttu-id="0f1e9-147">Veillez à consulter régulièrement la section [Analyse](threat-analytics.md) des menaces du centre de Microsoft 365 de sécurité.</span><span class="sxs-lookup"><span data-stu-id="0f1e9-147">Make time in your schedule to regularly check the [Threat Analytics](threat-analytics.md) section of the Microsoft 365 security center.</span></span>

## <a name="next-step"></a><span data-ttu-id="0f1e9-148">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="0f1e9-148">Next step</span></span>

<span data-ttu-id="0f1e9-149">[![Étape 1 : Découvrez comment trier et analyser les incidents](../../media/first-incident-overview/first-incident-path-step1.png)](first-incident-analyze.md)</span><span class="sxs-lookup"><span data-stu-id="0f1e9-149">[![Step 1: Learn how to triage and analyze incidents](../../media/first-incident-overview/first-incident-path-step1.png)](first-incident-analyze.md)</span></span>

<span data-ttu-id="0f1e9-150">Découvrez comment trier [et analyser les incidents.](first-incident-analyze.md)</span><span class="sxs-lookup"><span data-stu-id="0f1e9-150">Learn how to [triage and analyze incidents](first-incident-analyze.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="0f1e9-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0f1e9-151">See also</span></span>

- [<span data-ttu-id="0f1e9-152">Vue d’ensemble des incidents</span><span class="sxs-lookup"><span data-stu-id="0f1e9-152">Incidents overview</span></span>](incidents-overview.md)
- [<span data-ttu-id="0f1e9-153">Enquêter sur des incidents</span><span class="sxs-lookup"><span data-stu-id="0f1e9-153">Investigate incidents</span></span>](investigate-incidents.md)
- [<span data-ttu-id="0f1e9-154">Gérer les incidents</span><span class="sxs-lookup"><span data-stu-id="0f1e9-154">Manage incidents</span></span>](manage-incidents.md)
