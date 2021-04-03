---
title: Suivre les menaces émergentes et y répondre à l’aide de l’analyse des menaces Microsoft Defender ATP
ms.reviewer: ''
description: Découvrez les menaces émergentes et les techniques d’attaque et comment les arrêter. Évaluez leur impact sur votre organisation et évaluez la résilience de votre organisation.
keywords: analyse des menaces, évaluation des risques, atténuation du système d’exploitation, atténuation des microcodes, état de l’atténuation
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: maccruz
author: schmurky
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- m365-security-compliance
- m365initiative-defender-endpoint
ms.topic: article
ms.technology: mde
ms.openlocfilehash: 853a862556825e714bb06e51839f9c026e0cc0e0
ms.sourcegitcommit: 582555d2b4ef5f2e2494ffdeab2c1d49e5d6b724
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51501186"
---
# <a name="track-and-respond-to-emerging-threats-with-threat-analytics"></a><span data-ttu-id="57544-105">Suivre les menaces émergentes et y répondre avec l’analyse des menaces</span><span class="sxs-lookup"><span data-stu-id="57544-105">Track and respond to emerging threats with threat analytics</span></span> 

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="57544-106">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="57544-106">**Applies to:**</span></span>
- [<span data-ttu-id="57544-107">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="57544-107">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/?linkid=2154037)
- [<span data-ttu-id="57544-108">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="57544-108">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="57544-109">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="57544-109">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="57544-110">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="57544-110">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

<span data-ttu-id="57544-111">Avec des adversaires plus sophistiqués et de nouvelles menaces émergentes fréquemment et répandues, il est essentiel de pouvoir rapidement :</span><span class="sxs-lookup"><span data-stu-id="57544-111">With more sophisticated adversaries and new threats emerging frequently and prevalently, it's critical to be able to quickly:</span></span>

- <span data-ttu-id="57544-112">Évaluer l’impact des nouvelles menaces</span><span class="sxs-lookup"><span data-stu-id="57544-112">Assess the impact of new threats</span></span>
- <span data-ttu-id="57544-113">Examiner votre résilience par rapport aux menaces ou leur exposition</span><span class="sxs-lookup"><span data-stu-id="57544-113">Review your resilience against or exposure to the threats</span></span>
- <span data-ttu-id="57544-114">Identifier les actions que vous pouvez prendre pour arrêter ou contenir les menaces</span><span class="sxs-lookup"><span data-stu-id="57544-114">Identify the actions you can take to stop or contain the threats</span></span>

<span data-ttu-id="57544-115">L’analyse des menaces est un ensemble de rapports d’experts en matière de sécurité Microsoft couvrant les menaces les plus pertinentes, notamment :</span><span class="sxs-lookup"><span data-stu-id="57544-115">Threat analytics is a set of reports from expert Microsoft security researchers covering the most relevant threats, including:</span></span>

- <span data-ttu-id="57544-116">Acteurs actifs contre les menaces et leurs campagnes</span><span class="sxs-lookup"><span data-stu-id="57544-116">Active threat actors and their campaigns</span></span>
- <span data-ttu-id="57544-117">Techniques d’attaques nouvelles et populaires</span><span class="sxs-lookup"><span data-stu-id="57544-117">Popular and new attack techniques</span></span>
- <span data-ttu-id="57544-118">Vulnérabilités critiques</span><span class="sxs-lookup"><span data-stu-id="57544-118">Critical vulnerabilities</span></span>
- <span data-ttu-id="57544-119">Surfaces d’attaque courantes</span><span class="sxs-lookup"><span data-stu-id="57544-119">Common attack surfaces</span></span>
- <span data-ttu-id="57544-120">Programmes malveillants répandus</span><span class="sxs-lookup"><span data-stu-id="57544-120">Prevalent malware</span></span>

<span data-ttu-id="57544-121">Chaque rapport fournit une analyse détaillée d’une menace et des instructions complètes sur la façon de se défendre contre cette menace.</span><span class="sxs-lookup"><span data-stu-id="57544-121">Each report provides a detailed analysis of a threat and extensive guidance on how to defend against that threat.</span></span> <span data-ttu-id="57544-122">Il intègre également des données de votre réseau, ce qui indique si la menace est active et si vous avez des protections applicables en place.</span><span class="sxs-lookup"><span data-stu-id="57544-122">It also incorporates data from your network, indicating whether the threat is active and if you have applicable protections in place.</span></span>

<span data-ttu-id="57544-123">Regardez cette courte vidéo pour en savoir plus sur la façon dont l’analyse des menaces peut vous aider à suivre les dernières menaces et à les arrêter.</span><span class="sxs-lookup"><span data-stu-id="57544-123">Watch this short video to learn more about how threat analytics can help you track the latest threats and stop them.</span></span>
<p></p>

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4bw1f]

## <a name="view-the-threat-analytics-dashboard"></a><span data-ttu-id="57544-124">Afficher le tableau de bord d’analyse des menaces</span><span class="sxs-lookup"><span data-stu-id="57544-124">View the threat analytics dashboard</span></span>

<span data-ttu-id="57544-125">Le tableau de bord d’analyse des menaces constitue un excellent point de départ pour obtenir les rapports les plus pertinents pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="57544-125">The threat analytics dashboard is a great jump off point for getting to the reports that are most relevant to your organization.</span></span> <span data-ttu-id="57544-126">Il récapitule les menaces dans les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="57544-126">It summarizes the threats in the following sections:</span></span>

- <span data-ttu-id="57544-127">**Menaces les** plus récentes : répertorie les derniers rapports publiés sur les menaces, ainsi que le nombre d’appareils avec des alertes actives et résolues.</span><span class="sxs-lookup"><span data-stu-id="57544-127">**Latest threats**—lists the most recently published threat reports, along with the number of devices with active and resolved alerts.</span></span>
- <span data-ttu-id="57544-128">**Menaces à fort impact**: répertorie les menaces qui ont eu l’impact le plus élevé sur l’organisation.</span><span class="sxs-lookup"><span data-stu-id="57544-128">**High-impact threats**—lists the threats that have had the highest impact to the organization.</span></span> <span data-ttu-id="57544-129">Cette section classe les menaces par le nombre d’appareils qui ont des alertes actives.</span><span class="sxs-lookup"><span data-stu-id="57544-129">This section ranks threats by the number of devices that have active alerts.</span></span>
- <span data-ttu-id="57544-130">**Résumé des menaces**: affiche l’impact global du suivi des menaces en affichant le nombre de menaces avec des alertes actives et résolues.</span><span class="sxs-lookup"><span data-stu-id="57544-130">**Threat summary**—shows the overall impact of tracked threats by showing the number of threats with active and resolved alerts.</span></span>

<span data-ttu-id="57544-131">Sélectionnez une menace dans le tableau de bord pour afficher le rapport de cette menace.</span><span class="sxs-lookup"><span data-stu-id="57544-131">Select a threat from the dashboard to view the report for that threat.</span></span>

![Image d’un tableau de bord d’analyse des menaces](images/ta_dashboard.png)

## <a name="view-a-threat-analytics-report"></a><span data-ttu-id="57544-133">Afficher un rapport d’analyse des menaces</span><span class="sxs-lookup"><span data-stu-id="57544-133">View a threat analytics report</span></span>

<span data-ttu-id="57544-134">Chaque rapport d’analyse des menaces fournit des informations en trois sections : **Vue** d’ensemble, rapport **d’analyste** et **atténuations.**</span><span class="sxs-lookup"><span data-stu-id="57544-134">Each threat analytics report provides information in three sections: **Overview**, **Analyst report**, and **Mitigations**.</span></span>

### <a name="overview-quickly-understand-the-threat-assess-its-impact-and-review-defenses"></a><span data-ttu-id="57544-135">Vue d’ensemble : comprendre rapidement la menace, évaluer son impact et examiner les défenses</span><span class="sxs-lookup"><span data-stu-id="57544-135">Overview: Quickly understand the threat, assess its impact, and review defenses</span></span>

<span data-ttu-id="57544-136">La section **Vue d’ensemble** fournit un aperçu du rapport d’analyste détaillé.</span><span class="sxs-lookup"><span data-stu-id="57544-136">The **Overview** section provides a preview of the detailed analyst report.</span></span> <span data-ttu-id="57544-137">Il fournit également des graphiques qui mettent en évidence l’impact de la menace sur votre organisation et votre exposition par le biais d’appareils mal configurés et non configurés.</span><span class="sxs-lookup"><span data-stu-id="57544-137">It also provides charts that highlight the impact of the threat to your organization and your exposure through misconfigured and unpatched devices.</span></span>

<span data-ttu-id="57544-138">![Image de la section vue d’ensemble d’un rapport d’analyse des ](images/ta-overview.png)
 _menaces d’un rapport d’analyse des menaces_</span><span class="sxs-lookup"><span data-stu-id="57544-138">![Image of the overview section of a threat analytics report](images/ta-overview.png)
_Overview section of a threat analytics report_</span></span>

#### <a name="assess-the-impact-to-your-organization"></a><span data-ttu-id="57544-139">Évaluer l’impact sur votre organisation</span><span class="sxs-lookup"><span data-stu-id="57544-139">Assess the impact to your organization</span></span>
<span data-ttu-id="57544-140">Chaque rapport inclut des graphiques conçus pour fournir des informations sur l’impact organisationnel d’une menace :</span><span class="sxs-lookup"><span data-stu-id="57544-140">Each report includes charts designed to provide information about the organizational impact of a threat:</span></span>
- <span data-ttu-id="57544-141">**Appareils avec alertes**: indique le nombre actuel d’appareils distincts qui ont été touchés par la menace.</span><span class="sxs-lookup"><span data-stu-id="57544-141">**Devices with alerts**—shows the current number of distinct devices that have been impacted by the threat.</span></span> <span data-ttu-id="57544-142">Un appareil est classé comme **actif** s’il existe au  moins  une alerte associée à cette menace et résolu si toutes les alertes associées à la menace sur l’appareil ont été résolues.</span><span class="sxs-lookup"><span data-stu-id="57544-142">A device is categorized as **Active** if there is at least one alert associated with that threat and **Resolved** if *all* alerts associated with the threat on the device have been resolved.</span></span>
- <span data-ttu-id="57544-143">**Les appareils avec des alertes** au fil du temps indiquent le nombre d’appareils distincts avec des alertes **actives** **et** résolues au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="57544-143">**Devices with alerts over time**—shows the number of distinct devices with **Active** and **Resolved** alerts over time.</span></span> <span data-ttu-id="57544-144">Le nombre d’alertes résolues indique la rapidité de réponse de votre organisation aux alertes associées à une menace.</span><span class="sxs-lookup"><span data-stu-id="57544-144">The number of resolved alerts indicates how quickly your organization responds to alerts associated with a threat.</span></span> <span data-ttu-id="57544-145">Dans l’idéal, le graphique doit afficher les alertes résolues dans un délai de quelques jours.</span><span class="sxs-lookup"><span data-stu-id="57544-145">Ideally, the chart should be showing alerts resolved within a few days.</span></span>

#### <a name="review-security-resilience-and-posture"></a><span data-ttu-id="57544-146">Passer en revue la résilience et la posture de sécurité</span><span class="sxs-lookup"><span data-stu-id="57544-146">Review security resilience and posture</span></span>
<span data-ttu-id="57544-147">Chaque rapport inclut des graphiques qui fournissent une vue d’ensemble de la résilience de votre organisation face à une menace donnée :</span><span class="sxs-lookup"><span data-stu-id="57544-147">Each report includes charts that provide an overview of how resilient your organization is against a given threat:</span></span>
- <span data-ttu-id="57544-148">**État de la configuration** de la sécurité : indique le nombre d’appareils qui ont appliqué les paramètres de sécurité recommandés pour atténuer la menace.</span><span class="sxs-lookup"><span data-stu-id="57544-148">**Security configuration status**—shows the number of devices that have applied the recommended security settings that can help mitigate the threat.</span></span> <span data-ttu-id="57544-149">Les appareils sont considérés **comme sécurisés** s’ils ont _appliqué tous_ les paramètres suivis.</span><span class="sxs-lookup"><span data-stu-id="57544-149">Devices are considered **Secure** if they have applied _all_ the tracked settings.</span></span>
- <span data-ttu-id="57544-150">**État de correction des** vulnérabilités : indique le nombre d’appareils qui ont appliqué des mises à jour de sécurité ou des correctifs qui adressent les vulnérabilités exploitées par la menace.</span><span class="sxs-lookup"><span data-stu-id="57544-150">**Vulnerability patching status**—shows the number of devices that have applied security updates or patches that address vulnerabilities exploited by the threat.</span></span>

### <a name="analyst-report-get-expert-insight-from-microsoft-security-researchers"></a><span data-ttu-id="57544-151">Rapport d’analyste : obtenir des informations d’expert de la part de chercheurs en sécurité Microsoft</span><span class="sxs-lookup"><span data-stu-id="57544-151">Analyst report: Get expert insight from Microsoft security researchers</span></span>
<span data-ttu-id="57544-152">Go to the **Analyst report** section to read through the detailed expert write-up.</span><span class="sxs-lookup"><span data-stu-id="57544-152">Go to the **Analyst report** section to read through the detailed expert write-up.</span></span> <span data-ttu-id="57544-153">La plupart des rapports fournissent des descriptions détaillées des chaînes d’attaques, notamment des tactiques et des [](advanced-hunting-overview.md) techniques mappées à l’infrastructure CK MITRE ATT&, des listes exhaustives de recommandations et de puissants conseils de recherche de menaces.</span><span class="sxs-lookup"><span data-stu-id="57544-153">Most reports provide detailed descriptions of attack chains, including tactics and techniques mapped to the MITRE ATT&CK framework, exhaustive lists of recommendations, and powerful [threat hunting](advanced-hunting-overview.md) guidance.</span></span>

[<span data-ttu-id="57544-154">En savoir plus sur le rapport d’analyste</span><span class="sxs-lookup"><span data-stu-id="57544-154">Learn more about the analyst report</span></span>](threat-analytics-analyst-reports.md)

### <a name="mitigations-review-list-of-mitigations-and-the-status-of-your-devices"></a><span data-ttu-id="57544-155">Atténuations : examiner la liste des atténuations et l’état de vos appareils</span><span class="sxs-lookup"><span data-stu-id="57544-155">Mitigations: Review list of mitigations and the status of your devices</span></span>
<span data-ttu-id="57544-156">Dans la section **Atténuations,** examinez la liste des recommandations actionnables spécifiques qui peuvent vous aider à renforcer la résilience de votre organisation contre la menace.</span><span class="sxs-lookup"><span data-stu-id="57544-156">In the **Mitigations** section, review the list of specific actionable recommendations that can help you increase your organizational resilience against the threat.</span></span> <span data-ttu-id="57544-157">La liste des mesures de prévention de suivi inclut :</span><span class="sxs-lookup"><span data-stu-id="57544-157">The list of tracked mitigations includes:</span></span>

- <span data-ttu-id="57544-158">**Mises à jour de sécurité :** déploiement de mises à jour de sécurité ou de correctifs pour les vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="57544-158">**Security updates**—deployment of security updates or patches for vulnerabilities</span></span>
- <span data-ttu-id="57544-159">**Paramètres de l’Antivirus Microsoft Defender**</span><span class="sxs-lookup"><span data-stu-id="57544-159">**Microsoft Defender Antivirus settings**</span></span>
  - <span data-ttu-id="57544-160">Version de l’intelligence de la sécurité</span><span class="sxs-lookup"><span data-stu-id="57544-160">Security intelligence version</span></span>
  - <span data-ttu-id="57544-161">Protection cloud</span><span class="sxs-lookup"><span data-stu-id="57544-161">Cloud-delivered protection</span></span>  
  - <span data-ttu-id="57544-162">Protection des applications potentiellement indésirables (PUA)</span><span class="sxs-lookup"><span data-stu-id="57544-162">Potentially unwanted application (PUA) protection</span></span>
  - <span data-ttu-id="57544-163">Protection en temps réel</span><span class="sxs-lookup"><span data-stu-id="57544-163">Real-time protection</span></span>
 
<span data-ttu-id="57544-164">Les informations d’atténuation de [](next-gen-threat-and-vuln-mgt.md)cette section intègrent les données de la gestion des menaces et des vulnérabilités, qui fournissent également des informations détaillées sur l’analyse des différents liens du rapport.</span><span class="sxs-lookup"><span data-stu-id="57544-164">Mitigation information in this section incorporates data from [threat and vulnerability management](next-gen-threat-and-vuln-mgt.md), which also provides detailed drill-down information from various links in the report.</span></span>

<span data-ttu-id="57544-165">![Image de la section Préventions d’un rapport d’analyse des menaces Section ](images/ta-mitigations.png)
 _Atténuations d’un rapport d’analyse des menaces_</span><span class="sxs-lookup"><span data-stu-id="57544-165">![Image of the mitigations section of a threat analytics report](images/ta-mitigations.png)
_Mitigations section of a threat analytics report_</span></span>

## <a name="additional-report-details-and-limitations"></a><span data-ttu-id="57544-166">Détails et limitations supplémentaires du rapport</span><span class="sxs-lookup"><span data-stu-id="57544-166">Additional report details and limitations</span></span>
<span data-ttu-id="57544-167">Lorsque vous utilisez les rapports, gardez les informations suivantes à l’esprit :</span><span class="sxs-lookup"><span data-stu-id="57544-167">When using the reports, keep the following in mind:</span></span> 

- <span data-ttu-id="57544-168">Les données sont limitées en fonction de votre étendue de contrôle d’accès basé sur un rôle (RBAC).</span><span class="sxs-lookup"><span data-stu-id="57544-168">Data is scoped based on your role-based access control (RBAC) scope.</span></span> <span data-ttu-id="57544-169">Vous verrez l’état des appareils dans les [groupes accessibles.](machine-groups.md)</span><span class="sxs-lookup"><span data-stu-id="57544-169">You will see the status of devices in [groups that you can access](machine-groups.md).</span></span>
- <span data-ttu-id="57544-170">Les graphiques reflètent uniquement les atténuations qui sont suivis.</span><span class="sxs-lookup"><span data-stu-id="57544-170">Charts reflect only mitigations that are tracked.</span></span> <span data-ttu-id="57544-171">Consultez la vue d’ensemble du rapport pour les atténuations supplémentaires qui ne sont pas affichées dans les graphiques.</span><span class="sxs-lookup"><span data-stu-id="57544-171">Check the report overview for additional mitigations that are not shown in the charts.</span></span>
- <span data-ttu-id="57544-172">Les atténuations ne garantissent pas une résilience complète.</span><span class="sxs-lookup"><span data-stu-id="57544-172">Mitigations don't guarantee complete resilience.</span></span> <span data-ttu-id="57544-173">Les atténuations fournies reflètent les meilleures actions possibles nécessaires pour améliorer la résilience.</span><span class="sxs-lookup"><span data-stu-id="57544-173">The provided mitigations reflect the best possible actions needed to improve resiliency.</span></span>
- <span data-ttu-id="57544-174">Les appareils sont comptés comme « indisponibles » s’ils n’ont pas transmis de données au service.</span><span class="sxs-lookup"><span data-stu-id="57544-174">Devices are counted as "unavailable" if they have not transmitted data to the service.</span></span>
- <span data-ttu-id="57544-175">Les statistiques relatives aux antivirus sont basées sur les paramètres de l’Antivirus Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="57544-175">Antivirus-related statistics are based on Microsoft Defender Antivirus settings.</span></span> <span data-ttu-id="57544-176">Les appareils avec des solutions antivirus tierces peuvent apparaître comme « exposés ».</span><span class="sxs-lookup"><span data-stu-id="57544-176">Devices with third-party antivirus solutions can appear as "exposed".</span></span>

## <a name="related-topics"></a><span data-ttu-id="57544-177">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="57544-177">Related topics</span></span>
- [<span data-ttu-id="57544-178">Rechercher de manière proactive les menaces avec le recherche avancée</span><span class="sxs-lookup"><span data-stu-id="57544-178">Proactively find threats with advanced hunting</span></span>](advanced-hunting-overview.md) 
- [<span data-ttu-id="57544-179">Comprendre la section rapport d’analyste</span><span class="sxs-lookup"><span data-stu-id="57544-179">Understand the analyst report section</span></span>](threat-analytics-analyst-reports.md)
- [<span data-ttu-id="57544-180">Évaluer et résoudre les faiblesses et les exposition de sécurité</span><span class="sxs-lookup"><span data-stu-id="57544-180">Assess and resolve security weaknesses and exposures</span></span>](next-gen-threat-and-vuln-mgt.md)