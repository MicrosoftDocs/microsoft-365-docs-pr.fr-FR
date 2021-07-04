---
title: Suivre et répondre aux menaces émergentes avec l’analytique des menaces
ms.reviewer: ''
description: Découvrez les menaces émergentes et les techniques d’attaque et comment les arrêter. Évaluez leur impact sur votre organisation et évaluez la résilience de votre organisation.
keywords: analyse des menaces, évaluation des risques, Microsoft 365 Defender, M365D, état de l’atténuation, configuration sécurisée, Microsoft Defender pour Office 365, Microsoft Defender pour l’analyse des menaces Office 365, analyse des menaces MDO, données d’analyse des menaces MDE et MDO intégrées, intégration des données d’analyse des menaces, analyse des menaces Microsoft 365 Defender intégrée
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: microsoft-365-enterprise
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: maccruz
author: schmurky
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
- m365initiative-m365-defender
ms.topic: article
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: c03dfef28744e2ee565c25d921902b8d11ecb7a3
ms.sourcegitcommit: 4886457c0d4248407bddec56425dba50bb60d9c4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/03/2021
ms.locfileid: "53290242"
---
# <a name="track-and-respond-to-emerging-threats-with-threat-analytics"></a><span data-ttu-id="35c04-105">Suivre et répondre aux menaces émergentes avec l’analytique des menaces</span><span class="sxs-lookup"><span data-stu-id="35c04-105">Track and respond to emerging threats with threat analytics</span></span> 

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

<span data-ttu-id="35c04-106">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="35c04-106">**Applies to:**</span></span>
- <span data-ttu-id="35c04-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="35c04-107">Microsoft 365 Defender</span></span>

> <span data-ttu-id="35c04-108">Vous voulez essayer Microsoft 365 Defender ?</span><span class="sxs-lookup"><span data-stu-id="35c04-108">Want to experience Microsoft 365 Defender?</span></span> <span data-ttu-id="35c04-109">Vous pouvez [l’évaluer dans un environnement de laboratoire](m365d-evaluation.md?ocid=cx-docs-MTPtriallab) ou [exécuter votre projet pilote en production](m365d-pilot.md?ocid=cx-evalpilot).</span><span class="sxs-lookup"><span data-stu-id="35c04-109">You can [evaluate it in a lab environment](m365d-evaluation.md?ocid=cx-docs-MTPtriallab) or [run your pilot project in production](m365d-pilot.md?ocid=cx-evalpilot).</span></span>
>

[!INCLUDE [Prerelease](../includes/prerelease.md)]

<span data-ttu-id="35c04-110">L’analyse des menaces est notre solution d’intelligence contre les menaces dans le produit, conçue pour aider les équipes de sécurité à être aussi efficaces que possible face aux menaces émergentes, notamment :</span><span class="sxs-lookup"><span data-stu-id="35c04-110">Threat analytics is our in-product threat intelligence solution from expert Microsoft security researchers, designed to assist security teams to be as efficient as possible while facing emerging threats, including:</span></span>

- <span data-ttu-id="35c04-111">Acteurs actifs contre les menaces et leurs campagnes</span><span class="sxs-lookup"><span data-stu-id="35c04-111">Active threat actors and their campaigns</span></span>
- <span data-ttu-id="35c04-112">Techniques d’attaques nouvelles et populaires</span><span class="sxs-lookup"><span data-stu-id="35c04-112">Popular and new attack techniques</span></span>
- <span data-ttu-id="35c04-113">Vulnérabilités critiques</span><span class="sxs-lookup"><span data-stu-id="35c04-113">Critical vulnerabilities</span></span>
- <span data-ttu-id="35c04-114">Surface d'attaque courantes</span><span class="sxs-lookup"><span data-stu-id="35c04-114">Common attack surfaces</span></span>
- <span data-ttu-id="35c04-115">Programmes malveillants répandus</span><span class="sxs-lookup"><span data-stu-id="35c04-115">Prevalent malware</span></span>

<span data-ttu-id="35c04-116">Regardez cette courte vidéo pour en savoir plus sur la façon dont l’analyse des menaces peut vous aider à suivre les dernières menaces et à les arrêter.</span><span class="sxs-lookup"><span data-stu-id="35c04-116">Watch this short video to learn more about how threat analytics can help you track the latest threats and stop them.</span></span>

>[!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RWwJfU]

<span data-ttu-id="35c04-117">Vous pouvez accéder à l’analyse des menaces à partir du côté supérieur gauche de la barre de navigation du portail de sécurité Microsoft 365 ou à partir d’une carte de tableau de bord dédiée qui affiche les principales menaces dans votre organisation. Obtenir une visibilité sur les campagnes actives ou en cours et savoir quoi faire par le biais de l’analyse des menaces peut aider votre équipe en matière d’opérations de sécurité à prendre des décisions éclairées.</span><span class="sxs-lookup"><span data-stu-id="35c04-117">You can access threat analytics either from the upper left-hand side of Microsoft 365 security portal’s navigation bar, or from a dedicated dashboard card which shows the top threats in your org. Getting visibility on active or ongoing campaigns and knowing what to do through threat analytics can help equip your security operations team with informed decisions.</span></span> 

![Image du tableau de bord d’analyse des menaces](../../media/threat-analytics/ta_inlandingpage_mtp.png)

<span data-ttu-id="35c04-119">_Où accéder à l’analyse des menaces_</span><span class="sxs-lookup"><span data-stu-id="35c04-119">_Where to access threat analytics_</span></span>

<span data-ttu-id="35c04-120">Avec des adversaires plus sophistiqués et de nouvelles menaces émergentes fréquemment et répandues, il est essentiel de pouvoir rapidement :</span><span class="sxs-lookup"><span data-stu-id="35c04-120">With more sophisticated adversaries and new threats emerging frequently and prevalently, it's critical to be able to quickly:</span></span>

- <span data-ttu-id="35c04-121">Identifier et réagir aux menaces émergentes</span><span class="sxs-lookup"><span data-stu-id="35c04-121">Identify and react to emerging threats</span></span>
- <span data-ttu-id="35c04-122">Découvrez si vous êtes actuellement en cours d’attaque</span><span class="sxs-lookup"><span data-stu-id="35c04-122">Learn if you are currently under attack</span></span>
- <span data-ttu-id="35c04-123">Évaluer l’impact de la menace sur vos ressources</span><span class="sxs-lookup"><span data-stu-id="35c04-123">Assess the impact of the threat to your assets</span></span>
- <span data-ttu-id="35c04-124">Examiner votre résilience par rapport aux menaces ou leur exposition</span><span class="sxs-lookup"><span data-stu-id="35c04-124">Review your resilience against or exposure to the threats</span></span>
- <span data-ttu-id="35c04-125">Identifier les actions d’atténuation, de récupération ou de prévention que vous pouvez prendre pour arrêter ou contenir les menaces</span><span class="sxs-lookup"><span data-stu-id="35c04-125">Identify the mitigation, recovery, or prevention actions you can take to stop or contain the threats</span></span>

<span data-ttu-id="35c04-126">Chaque rapport fournit une analyse d’une menace de suivi et des instructions complètes sur la façon de se défendre contre cette menace.</span><span class="sxs-lookup"><span data-stu-id="35c04-126">Each report provides an analysis of a tracked threat and extensive guidance on how to defend against that threat.</span></span> <span data-ttu-id="35c04-127">Il intègre également des données de votre réseau, ce qui indique si la menace est active et si vous avez des protections applicables en place.</span><span class="sxs-lookup"><span data-stu-id="35c04-127">It also incorporates data from your network, indicating whether the threat is active and if you have applicable protections in place.</span></span>

## <a name="view-the-threat-analytics-dashboard"></a><span data-ttu-id="35c04-128">Afficher le tableau de bord d’analyse des menaces</span><span class="sxs-lookup"><span data-stu-id="35c04-128">View the threat analytics dashboard</span></span>

<span data-ttu-id="35c04-129">Le tableau de bord d’analyse[des menaces (security.microsoft.com/threatanalytics3](https://security.microsoft.com/threatanalytics3)) met en évidence les rapports les plus pertinents pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="35c04-129">The threat analytics dashboard ([security.microsoft.com/threatanalytics3](https://security.microsoft.com/threatanalytics3)) highlights the reports that are most relevant to your organization.</span></span> <span data-ttu-id="35c04-130">Il récapitule les menaces dans les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="35c04-130">It summarizes the threats in the following sections:</span></span>

- <span data-ttu-id="35c04-131">**Menaces les** plus récentes : répertorie les derniers rapports publiés ou mis à jour sur les menaces, ainsi que le nombre d’alertes actives et résolues.</span><span class="sxs-lookup"><span data-stu-id="35c04-131">**Latest threats**—lists the most recently published or updated threat reports, along with the number of active and resolved alerts.</span></span>
- <span data-ttu-id="35c04-132">**Menaces à fort impact**: répertorie les menaces qui ont le plus grand impact sur votre organisation.</span><span class="sxs-lookup"><span data-stu-id="35c04-132">**High-impact threats**—lists the threats that have the highest impact to your organization.</span></span> <span data-ttu-id="35c04-133">Cette section répertorie les menaces avec le plus grand nombre d’alertes actives et résolues en premier.</span><span class="sxs-lookup"><span data-stu-id="35c04-133">This section lists threats with the highest number of active and resolved alerts first.</span></span>
- <span data-ttu-id="35c04-134">**Résumé des menaces**: fournit l’impact global de toutes les menaces de suivi en affichant le nombre de menaces avec des alertes actives et résolues.</span><span class="sxs-lookup"><span data-stu-id="35c04-134">**Threat summary**—provides the overall impact of all tracked threats by showing the number of threats with active and resolved alerts.</span></span>

<span data-ttu-id="35c04-135">Sélectionnez une menace dans le tableau de bord pour afficher le rapport de cette menace.</span><span class="sxs-lookup"><span data-stu-id="35c04-135">Select a threat from the dashboard to view the report for that threat.</span></span>

![Capture d’écran du tableau de bord d’analyse des menaces](../../media/threat-analytics/ta_dashboard_mtp.png)

<span data-ttu-id="35c04-137">_Tableau de bord d’analyse des menaces. Vous pouvez également cliquer sur l’icône Rechercher pour trouver un mot clé lié au rapport d’analyse des menaces que vous souhaitez lire._</span><span class="sxs-lookup"><span data-stu-id="35c04-137">_Threat analytics dashboard. You can also click the Search icon to key in a keyword related to the threat analytics report that you'd like to read._</span></span> 

## <a name="view-a-threat-analytics-report"></a><span data-ttu-id="35c04-138">Afficher un rapport d’analyse des menaces</span><span class="sxs-lookup"><span data-stu-id="35c04-138">View a threat analytics report</span></span>

<span data-ttu-id="35c04-139">Chaque rapport d’analyse des menaces fournit des informations dans plusieurs sections :</span><span class="sxs-lookup"><span data-stu-id="35c04-139">Each threat analytics report provides information in several sections:</span></span>

- [<span data-ttu-id="35c04-140">**Présentation**</span><span class="sxs-lookup"><span data-stu-id="35c04-140">**Overview**</span></span>](#overview-quickly-understand-the-threat-assess-its-impact-and-review-defenses)
- [<span data-ttu-id="35c04-141">**Rapport d’analystes**</span><span class="sxs-lookup"><span data-stu-id="35c04-141">**Analyst report**</span></span>](#analyst-report-get-expert-insight-from-microsoft-security-researchers)
- [<span data-ttu-id="35c04-142">**Incidents connexes**</span><span class="sxs-lookup"><span data-stu-id="35c04-142">**Related incidents**</span></span>](#related-incidents-view-and-manage-related-incidents)
- [<span data-ttu-id="35c04-143">**Ressources impactées**</span><span class="sxs-lookup"><span data-stu-id="35c04-143">**Impacted assets**</span></span>](#impacted-assets-get-list-of-impacted-devices-and-mailboxes)
- [<span data-ttu-id="35c04-144">**Tentatives de courrier électronique empêchées**</span><span class="sxs-lookup"><span data-stu-id="35c04-144">**Prevented email attempts**</span></span>](#prevented-email-attempts-view-blocked-or-junked-threat-emails)
- [<span data-ttu-id="35c04-145">**Atténuations**</span><span class="sxs-lookup"><span data-stu-id="35c04-145">**Mitigations**</span></span>](#mitigations-review-list-of-mitigations-and-the-status-of-your-devices)

### <a name="overview-quickly-understand-the-threat-assess-its-impact-and-review-defenses"></a><span data-ttu-id="35c04-146">Vue d’ensemble : comprendre rapidement la menace, évaluer son impact et examiner les défenses</span><span class="sxs-lookup"><span data-stu-id="35c04-146">Overview: Quickly understand the threat, assess its impact, and review defenses</span></span>

<span data-ttu-id="35c04-147">La section **Vue d’ensemble** fournit un aperçu du rapport d’analyste détaillé.</span><span class="sxs-lookup"><span data-stu-id="35c04-147">The **Overview** section provides a preview of the detailed analyst report.</span></span> <span data-ttu-id="35c04-148">Il fournit également des graphiques qui mettent en évidence l’impact de la menace sur votre organisation et votre exposition par le biais d’appareils mal configurés et non configurés.</span><span class="sxs-lookup"><span data-stu-id="35c04-148">It also provides charts that highlight the impact of the threat to your organization and your exposure through misconfigured and unpatched devices.</span></span>

![Image de la section vue d’ensemble d’un rapport d’analyse des menaces](../../media/threat-analytics/ta_overview_mtp.png)

<span data-ttu-id="35c04-150">_Section Vue d’ensemble d’un rapport d’analyse des menaces_</span><span class="sxs-lookup"><span data-stu-id="35c04-150">_Overview section of a threat analytics report_</span></span>

#### <a name="assess-impact-on-your-organization"></a><span data-ttu-id="35c04-151">Évaluer l’impact sur votre organisation</span><span class="sxs-lookup"><span data-stu-id="35c04-151">Assess impact on your organization</span></span>

<span data-ttu-id="35c04-152">Chaque rapport inclut des graphiques conçus pour fournir des informations sur l’impact organisationnel d’une menace :</span><span class="sxs-lookup"><span data-stu-id="35c04-152">Each report includes charts designed to provide information about the organizational impact of a threat:</span></span>

- <span data-ttu-id="35c04-153">**Incidents connexes**: fournit une vue d’ensemble de l’impact de la menace sur votre organisation avec les données suivantes :</span><span class="sxs-lookup"><span data-stu-id="35c04-153">**Related incidents**—provides an overview of the impact of the tracked threat to your organization with the following data:</span></span>
  - <span data-ttu-id="35c04-154">Nombre d’alertes actives et nombre d’incidents actifs associés</span><span class="sxs-lookup"><span data-stu-id="35c04-154">Number of active alerts and the number of active incidents they are associated with</span></span>
  - <span data-ttu-id="35c04-155">Gravité des incidents actifs</span><span class="sxs-lookup"><span data-stu-id="35c04-155">Severity of active incidents</span></span>
- <span data-ttu-id="35c04-156">**Les alertes au fil du temps** indiquent le nombre d’alertes **actives** et résolues **associées** au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="35c04-156">**Alerts over time**—shows the number of related **Active** and **Resolved** alerts over time.</span></span> <span data-ttu-id="35c04-157">Le nombre d’alertes résolues indique la rapidité de réponse de votre organisation aux alertes associées à une menace.</span><span class="sxs-lookup"><span data-stu-id="35c04-157">The number of resolved alerts indicates how quickly your organization responds to alerts associated with a threat.</span></span> <span data-ttu-id="35c04-158">Dans l’idéal, le graphique doit afficher les alertes résolues dans un délai de quelques jours.</span><span class="sxs-lookup"><span data-stu-id="35c04-158">Ideally, the chart should be showing alerts resolved within a few days.</span></span>
- <span data-ttu-id="35c04-159">**Ressources impactées :** indique le nombre d’appareils et de comptes de messagerie distincts (boîtes aux lettres) qui ont actuellement au moins une alerte active associée à la menace de suivi.</span><span class="sxs-lookup"><span data-stu-id="35c04-159">**Impacted assets**—shows the number of distinct devices and email accounts (mailboxes) that currently have at least one active alert associated with the tracked threat.</span></span> <span data-ttu-id="35c04-160">Les alertes sont déclenchées pour les boîtes aux lettres qui ont reçu des e-mails de menace.</span><span class="sxs-lookup"><span data-stu-id="35c04-160">Alerts are triggered for mailboxes that received threat emails.</span></span> <span data-ttu-id="35c04-161">Examinez les stratégies au niveau de l’organisation et de l’utilisateur pour les remplacements qui entraînent la remise de messages électroniques de menace.</span><span class="sxs-lookup"><span data-stu-id="35c04-161">Review both org- and user-level policies for overrides that cause the delivery of threat emails.</span></span>
- <span data-ttu-id="35c04-162">**Tentatives de courrier électronique empêchées**: indique le nombre de messages électroniques des sept derniers jours qui ont été bloqués avant leur remise ou remis au dossier de courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="35c04-162">**Prevented email attempts**—shows the number of emails from the past seven days that were either blocked before delivery or delivered to the junk mail folder.</span></span>

#### <a name="review-security-resilience-and-posture"></a><span data-ttu-id="35c04-163">Passer en revue la résilience et la posture de sécurité</span><span class="sxs-lookup"><span data-stu-id="35c04-163">Review security resilience and posture</span></span>

<span data-ttu-id="35c04-164">Chaque rapport inclut des graphiques qui fournissent une vue d’ensemble de la résilience de votre organisation face à une menace donnée :</span><span class="sxs-lookup"><span data-stu-id="35c04-164">Each report includes charts that provide an overview of how resilient your organization is against a given threat:</span></span>

- <span data-ttu-id="35c04-165">**État de configuration** sécurisé : indique le nombre d’appareils avec des paramètres de sécurité mal configurés.</span><span class="sxs-lookup"><span data-stu-id="35c04-165">**Secure configuration status**—shows the number of devices with misconfigured security settings.</span></span> <span data-ttu-id="35c04-166">Appliquez les paramètres de sécurité recommandés pour atténuer la menace.</span><span class="sxs-lookup"><span data-stu-id="35c04-166">Apply the recommended security settings to help mitigate the threat.</span></span> <span data-ttu-id="35c04-167">Les appareils sont considérés **comme sécurisés** s’ils ont _appliqué tous_ les paramètres suivis.</span><span class="sxs-lookup"><span data-stu-id="35c04-167">Devices are considered **Secure** if they have applied _all_ the tracked settings.</span></span>
- <span data-ttu-id="35c04-168">**État de correction des vulnérabilités**: indique le nombre d’appareils vulnérables.</span><span class="sxs-lookup"><span data-stu-id="35c04-168">**Vulnerability patching status**—shows the number of vulnerable devices.</span></span> <span data-ttu-id="35c04-169">Appliquer des mises à jour de sécurité ou des correctifs pour résoudre les vulnérabilités exploitées par la menace.</span><span class="sxs-lookup"><span data-stu-id="35c04-169">Apply security updates or patches to address vulnerabilities exploited by the threat.</span></span>

#### <a name="view-reports-per-threat-tags"></a><span data-ttu-id="35c04-170">Afficher les rapports par balise de menace</span><span class="sxs-lookup"><span data-stu-id="35c04-170">View reports per threat tags</span></span>

<span data-ttu-id="35c04-171">Vous pouvez filtrer la liste des rapports sur les menaces et afficher les rapports les plus pertinents en fonction d’une balise de menace spécifique (catégorie) ou d’un type de rapport.</span><span class="sxs-lookup"><span data-stu-id="35c04-171">You can filter the threat report list and view the most relevant reports according to a specific threat tag (category) or a report type.</span></span>

- <span data-ttu-id="35c04-172">**Balises de menace**: vous aident à afficher les rapports les plus pertinents en fonction d’une catégorie de menace spécifique.</span><span class="sxs-lookup"><span data-stu-id="35c04-172">**Threat tags**—assist you in viewing the most relevant reports according to a specific threat category.</span></span> <span data-ttu-id="35c04-173">Par exemple, tous les rapports liés aux ransomware.</span><span class="sxs-lookup"><span data-stu-id="35c04-173">For example, all reports related to ransomware.</span></span>
- <span data-ttu-id="35c04-174">**Types de rapports**: vous aident à afficher les rapports les plus pertinents en fonction d’un type de rapport spécifique.</span><span class="sxs-lookup"><span data-stu-id="35c04-174">**Report types**—assist you in viewing the most relevant reports according to a specific report type.</span></span> <span data-ttu-id="35c04-175">Par exemple, tous les rapports qui couvrent les outils et les techniques.</span><span class="sxs-lookup"><span data-stu-id="35c04-175">For example, all reports that cover tools and techniques.</span></span> 
- <span data-ttu-id="35c04-176">**Filtres**: vous aident à passer en revue efficacement la liste des rapports sur les menaces et à filtrer l’affichage en fonction d’une balise de menace ou d’un type de rapport spécifique.</span><span class="sxs-lookup"><span data-stu-id="35c04-176">**Filters**—assist you in efficiently reviewing the threat report list and filtering the view based on a specific threat tag or report type.</span></span> <span data-ttu-id="35c04-177">Par exemple, examinez tous les rapports sur les menaces liés à la catégorie de ransomware ou les rapports sur les menaces qui couvrent les vulnérabilités.</span><span class="sxs-lookup"><span data-stu-id="35c04-177">For example, review all threat reports related to ransomware category, or threat reports that cover vulnerabilities.</span></span>

##### <a name="how-does-it-work"></a><span data-ttu-id="35c04-178">Comment cela fonctionne-t-il ?</span><span class="sxs-lookup"><span data-stu-id="35c04-178">How does it work?</span></span>

<span data-ttu-id="35c04-179">L’équipe Microsoft Threat Intelligence a ajouté des balises de menace à chaque rapport sur les menaces :</span><span class="sxs-lookup"><span data-stu-id="35c04-179">The Microsoft Threat Intelligence team has added threat tags to each threat report:</span></span>

- <span data-ttu-id="35c04-180">Quatre balises de menace sont désormais disponibles :</span><span class="sxs-lookup"><span data-stu-id="35c04-180">Four threat tags are now available:</span></span>
  - <span data-ttu-id="35c04-181">Ransomware</span><span class="sxs-lookup"><span data-stu-id="35c04-181">Ransomware</span></span>
  - <span data-ttu-id="35c04-182">Hameçonnage</span><span class="sxs-lookup"><span data-stu-id="35c04-182">Phishing</span></span>
  - <span data-ttu-id="35c04-183">Vulnérabilité</span><span class="sxs-lookup"><span data-stu-id="35c04-183">Vulnerability</span></span>
  - <span data-ttu-id="35c04-184">Groupe d’activités</span><span class="sxs-lookup"><span data-stu-id="35c04-184">Activity group</span></span>
- <span data-ttu-id="35c04-185">Les balises de menace sont présentées en haut de la page d’analyse des menaces, avec des compteurs pour le nombre de rapports disponibles sous chaque balise.</span><span class="sxs-lookup"><span data-stu-id="35c04-185">Threat tags are presented at the top of the threat analytics page, with counters for the number of available reports under each tag.</span></span>

  ![balises de menace](../../media/threat-analytics/ta-threattags-mtp.png)

- <span data-ttu-id="35c04-187">La liste peut également être triée par balises de menace :</span><span class="sxs-lookup"><span data-stu-id="35c04-187">The list can also be sorted by threat tags:</span></span>

  ![lists](../../media/threat-analytics//ta-taglist-mtp.png)

- <span data-ttu-id="35c04-189">Les filtres sont disponibles par balise de menace et type de rapport :</span><span class="sxs-lookup"><span data-stu-id="35c04-189">Filters are available per threat tag and report type:</span></span>

  ![filtres](../../media/threat-analytics/ta-threattag-filters-mtp.png)

### <a name="analyst-report-get-expert-insight-from-microsoft-security-researchers"></a><span data-ttu-id="35c04-191">Rapport d’analyste : obtenir des informations d’expert de la part de chercheurs en sécurité Microsoft</span><span class="sxs-lookup"><span data-stu-id="35c04-191">Analyst report: Get expert insight from Microsoft security researchers</span></span>

<span data-ttu-id="35c04-192">Dans la section **Rapport d’analyste,** lisez l’écriture détaillée de l’expert.</span><span class="sxs-lookup"><span data-stu-id="35c04-192">In the **Analyst report** section, read through the detailed expert write-up.</span></span> <span data-ttu-id="35c04-193">La plupart des rapports fournissent des descriptions détaillées des chaînes d’attaques, notamment des tactiques et des [](advanced-hunting-overview.md) techniques mappées à l’infrastructure CK MITRE ATT&, des listes exhaustives de recommandations et de puissants conseils de recherche de menaces.</span><span class="sxs-lookup"><span data-stu-id="35c04-193">Most reports provide detailed descriptions of attack chains, including tactics and techniques mapped to the MITRE ATT&CK framework, exhaustive lists of recommendations, and powerful [threat hunting](advanced-hunting-overview.md) guidance.</span></span>

[<span data-ttu-id="35c04-194">En savoir plus sur le rapport d’analyste</span><span class="sxs-lookup"><span data-stu-id="35c04-194">Learn more about the analyst report</span></span>](threat-analytics-analyst-reports.md)

### <a name="related-incidents-view-and-manage-related-incidents"></a><span data-ttu-id="35c04-195">Incidents connexes : afficher et gérer les incidents connexes</span><span class="sxs-lookup"><span data-stu-id="35c04-195">Related incidents: View and manage related incidents</span></span>

<span data-ttu-id="35c04-196">**L’onglet Incidents connexes** fournit la liste de tous les incidents liés à la menace de suivi.</span><span class="sxs-lookup"><span data-stu-id="35c04-196">The **Related incidents** tab provides the list of all incidents related to the tracked threat.</span></span> <span data-ttu-id="35c04-197">Vous pouvez affecter des incidents ou gérer des alertes liées à chaque incident.</span><span class="sxs-lookup"><span data-stu-id="35c04-197">You can assign incidents or manage alerts linked to each incident.</span></span> 


![Image de la section relative aux incidents connexes d’un rapport d’analyse des menaces](../../media/threat-analytics/ta_related_incidents_mtp.png)

<span data-ttu-id="35c04-199">_Section Incidents connexes d’un rapport d’analyse des menaces_</span><span class="sxs-lookup"><span data-stu-id="35c04-199">_Related incidents section of a threat analytics report_</span></span>

### <a name="impacted-assets-get-list-of-impacted-devices-and-mailboxes"></a><span data-ttu-id="35c04-200">Ressources impactées : obtenir la liste des appareils et boîtes aux lettres touchés</span><span class="sxs-lookup"><span data-stu-id="35c04-200">Impacted assets: Get list of impacted devices and mailboxes</span></span>

<span data-ttu-id="35c04-201">Un bien est considéré comme affecté s’il est affecté par une alerte active et non résolue.</span><span class="sxs-lookup"><span data-stu-id="35c04-201">An asset is considered impacted if it is affected by an active, unresolved alert.</span></span> <span data-ttu-id="35c04-202">**L’onglet Ressources impactées** répertorie les types suivants de biens touchés :</span><span class="sxs-lookup"><span data-stu-id="35c04-202">The **Impacted assets** tab lists the following types of impacted assets:</span></span>

- <span data-ttu-id="35c04-203">**Appareils touchés**: points de terminaison qui ont des alertes Microsoft Defender pour point de terminaison non résolues.</span><span class="sxs-lookup"><span data-stu-id="35c04-203">**Impacted devices**—endpoints that have unresolved Microsoft Defender for Endpoint alerts.</span></span> <span data-ttu-id="35c04-204">Ces alertes se firent généralement lors de la recherche d’indicateurs et d’activités de menace connus.</span><span class="sxs-lookup"><span data-stu-id="35c04-204">These alerts typically fire on sightings of known threat indicators and activities.</span></span>
- <span data-ttu-id="35c04-205">**Boîtes aux lettres impactées :** boîtes aux lettres qui ont reçu des messages électroniques qui ont déclenché Microsoft Defender Office 365 alertes.</span><span class="sxs-lookup"><span data-stu-id="35c04-205">**Impacted mailboxes**—mailboxes that have received email messages that have triggered Microsoft Defender for Office 365 alerts.</span></span> <span data-ttu-id="35c04-206">Alors que la plupart des messages qui déclenchent des alertes sont généralement bloqués, les stratégies au niveau de l’utilisateur ou de l’organisation peuvent remplacer les filtres.</span><span class="sxs-lookup"><span data-stu-id="35c04-206">While most messages that trigger alerts are typically blocked, user- or org-level policies can override filters.</span></span>

![Image de la section ressources impactées d’un rapport d’analyse des menaces](../../media/threat-analytics/ta_impacted_assets_mtp.png)

<span data-ttu-id="35c04-208">_Section Ressources impactées d’un rapport d’analyse des menaces_</span><span class="sxs-lookup"><span data-stu-id="35c04-208">_Impacted assets section of a threat analytics report_</span></span>

### <a name="prevented-email-attempts-view-blocked-or-junked-threat-emails"></a><span data-ttu-id="35c04-209">Tentatives de courrier électronique empêchées : afficher les e-mails de menace bloqués ou indésirables</span><span class="sxs-lookup"><span data-stu-id="35c04-209">Prevented email attempts: View blocked or junked threat emails</span></span>

<span data-ttu-id="35c04-210">Microsoft Defender pour Office 365 bloque généralement les e-mails avec des indicateurs de menace connus, y compris les pièces jointes ou les liens malveillants.</span><span class="sxs-lookup"><span data-stu-id="35c04-210">Microsoft Defender for Office 365 typically blocks emails with known threat indicators, including malicious links or attachments.</span></span> <span data-ttu-id="35c04-211">Dans certains cas, les mécanismes de filtrage proactifs qui vérifient la recherche de contenu suspect envoient plutôt des e-mails de menace au dossier de courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="35c04-211">In some cases, proactive filtering mechanisms that check for suspicious content will instead send threat emails to the junk mail folder.</span></span> <span data-ttu-id="35c04-212">Dans les deux cas, les risques de lancement du code anti-programme malveillant sur l’appareil sont réduits.</span><span class="sxs-lookup"><span data-stu-id="35c04-212">In either case, the chances of the threat launching malware code on the device is reduced.</span></span>

<span data-ttu-id="35c04-213">**L’onglet Tentatives** de courrier indésirable répertorie tous les e-mails qui ont été bloqués avant leur remise ou envoyés au dossier de courrier indésirable par Microsoft Defender pour Office 365.</span><span class="sxs-lookup"><span data-stu-id="35c04-213">The **Prevented email attempts** tab lists all the emails that have either been blocked before delivery or sent to the junk mail folder by Microsoft Defender for Office 365.</span></span> 

![Image de la section tentatives de courrier empêchée d’un rapport d’analyse des menaces](../../media/threat-analytics/ta_prevented_email_attempts_mtp.png)

<span data-ttu-id="35c04-215">_Section Tentatives de courriers électroniques empêchées d’un rapport d’analyse des menaces_</span><span class="sxs-lookup"><span data-stu-id="35c04-215">_Prevented email attempts section of a threat analytics report_</span></span>

### <a name="mitigations-review-list-of-mitigations-and-the-status-of-your-devices"></a><span data-ttu-id="35c04-216">Atténuations : examiner la liste des atténuations et l’état de vos appareils</span><span class="sxs-lookup"><span data-stu-id="35c04-216">Mitigations: Review list of mitigations and the status of your devices</span></span>

<span data-ttu-id="35c04-217">Dans la section **Atténuations,** examinez la liste des recommandations actionnables spécifiques qui peuvent vous aider à renforcer la résilience de votre organisation contre la menace.</span><span class="sxs-lookup"><span data-stu-id="35c04-217">In the **Mitigations** section, review the list of specific actionable recommendations that can help you increase your organizational resilience against the threat.</span></span> <span data-ttu-id="35c04-218">La liste des mesures de prévention de suivi inclut :</span><span class="sxs-lookup"><span data-stu-id="35c04-218">The list of tracked mitigations includes:</span></span>

- <span data-ttu-id="35c04-219">**Mises à jour de sécurité :** déploiement des mises à jour de sécurité logicielles prise en charge pour les vulnérabilités trouvées sur les appareils intégrés</span><span class="sxs-lookup"><span data-stu-id="35c04-219">**Security updates**—deployment of supported software security updates for vulnerabilities found on onboarded devices</span></span>
- <span data-ttu-id="35c04-220">**Configurations de sécurité prise en charge**</span><span class="sxs-lookup"><span data-stu-id="35c04-220">**Supported security configurations**</span></span>
  - <span data-ttu-id="35c04-221">Protection fournie par le cloud</span><span class="sxs-lookup"><span data-stu-id="35c04-221">Cloud-delivered protection</span></span>  
  - <span data-ttu-id="35c04-222">Protection des applications potentiellement indésirables (PUA)</span><span class="sxs-lookup"><span data-stu-id="35c04-222">Potentially unwanted application (PUA) protection</span></span>
  - <span data-ttu-id="35c04-223">Protection en temps réel</span><span class="sxs-lookup"><span data-stu-id="35c04-223">Real-time protection</span></span>

<span data-ttu-id="35c04-224">Les informations d’atténuation de cette section intègrent des données de [Gestion des menaces et des vulnérabilités](/windows/security/threat-protection/microsoft-defender-atp/next-gen-threat-and-vuln-mgt), qui fournit également des informations détaillées sur l’analyse à partir de différents liens du rapport.</span><span class="sxs-lookup"><span data-stu-id="35c04-224">Mitigation information in this section incorporates data from [threat and vulnerability management](/windows/security/threat-protection/microsoft-defender-atp/next-gen-threat-and-vuln-mgt), which also provides detailed drill-down information from various links in the report.</span></span>

![Image de la section préventions d’un rapport d’analyse des menaces affichant des détails de configuration sécurisés](../../media/threat-analytics/ta_mitigations_mtp.png)

![Image de la section préventions d’un rapport d’analyse des menaces affichant les détails de la vulnérabilité](../../media/threat-analytics/ta_mitigations_mtp2.png)

<span data-ttu-id="35c04-227">_Section Atténuations d’un rapport d’analyse des menaces_</span><span class="sxs-lookup"><span data-stu-id="35c04-227">_Mitigations section of a threat analytics report_</span></span>

## <a name="additional-report-details-and-limitations"></a><span data-ttu-id="35c04-228">Détails et limitations supplémentaires du rapport</span><span class="sxs-lookup"><span data-stu-id="35c04-228">Additional report details and limitations</span></span>

> [!NOTE]
> <span data-ttu-id="35c04-229">Dans le cadre de l’expérience de sécurité unifiée, l’analyse des menaces est désormais disponible non seulement pour Microsoft Defender pour le point de terminaison, mais également pour Microsoft Defender pour les titulaires de licence Office E5.</span><span class="sxs-lookup"><span data-stu-id="35c04-229">As part of the unified security experience, threat analytics is now available not just for Microsoft Defender for Endpoint, but also for Microsoft Defender for Office E5 license holders.</span></span>
>
> <span data-ttu-id="35c04-230">Si vous n’utilisez pas le portail de sécurité Microsoft 365 (Microsoft 365 Defender), vous pouvez également voir les détails du rapport (sans les données De Microsoft Defender pour Office) dans le portail Centre de sécurité Microsoft Defender (Microsoft Defender pour point de terminaison).</span><span class="sxs-lookup"><span data-stu-id="35c04-230">If you are not using the Microsoft 365 security portal (Microsoft 365 Defender), you can also see the report details (without the Microsoft Defender for Office data) in the Microsoft Defender Security Center portal (Microsoft Defender for Endpoint).</span></span>

<span data-ttu-id="35c04-231">Pour accéder au rapport d’analyse des menaces, vous avez besoin de certains rôles et autorisations.</span><span class="sxs-lookup"><span data-stu-id="35c04-231">To access threat analytics report you need certain roles and permissions.</span></span> <span data-ttu-id="35c04-232">Pour [plus d’informations, voir](custom-roles.md) Rôles personnalisés dans le contrôle d’accès basé sur Microsoft 365 Defender rôle.</span><span class="sxs-lookup"><span data-stu-id="35c04-232">See [Custom roles in role-based access control for Microsoft 365 Defender](custom-roles.md) for details.</span></span>

- <span data-ttu-id="35c04-233">Pour afficher les alertes, les incidents ou les données de ressources touchés, vous devez avoir des autorisations sur Microsoft Defender pour les Office ou microsoft Defender pour les données d’alertes de point de terminaison, ou les deux.</span><span class="sxs-lookup"><span data-stu-id="35c04-233">To view alerts, incidents, or impacted assets data, you need to have permissions to Microsoft Defender for Office or Microsoft Defender for Endpoint alerts data, or both.</span></span>
- <span data-ttu-id="35c04-234">Pour afficher les tentatives de courrier électronique empêchées, vous devez avoir des autorisations sur Microsoft Defender pour Office de recherche.</span><span class="sxs-lookup"><span data-stu-id="35c04-234">To view prevented email attempts, you need to have permissions to Microsoft Defender for Office hunting data.</span></span> 
- <span data-ttu-id="35c04-235">Pour afficher les atténuations, vous devez être autorisé à Gestion des menaces et des vulnérabilités données dans Microsoft Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="35c04-235">To view mitigations, you need to have permissions to threat and vulnerability management data in Microsoft Defender for Endpoint.</span></span>

<span data-ttu-id="35c04-236">Lorsque vous regardez les données d’analyse des menaces, n’oubliez pas les facteurs suivants :</span><span class="sxs-lookup"><span data-stu-id="35c04-236">When looking at the threat analytics data, remember the following factors:</span></span>

- <span data-ttu-id="35c04-237">Les graphiques reflètent uniquement les atténuations qui sont suivis.</span><span class="sxs-lookup"><span data-stu-id="35c04-237">Charts reflect only mitigations that are tracked.</span></span> <span data-ttu-id="35c04-238">Consultez la vue d’ensemble du rapport pour les atténuations supplémentaires qui ne sont pas affichées dans les graphiques.</span><span class="sxs-lookup"><span data-stu-id="35c04-238">Check the report overview for additional mitigations that are not shown in the charts.</span></span>
- <span data-ttu-id="35c04-239">Les atténuations ne garantissent pas une résilience complète.</span><span class="sxs-lookup"><span data-stu-id="35c04-239">Mitigations don't guarantee complete resilience.</span></span> <span data-ttu-id="35c04-240">Les atténuations fournies reflètent les meilleures actions possibles nécessaires pour améliorer la résilience.</span><span class="sxs-lookup"><span data-stu-id="35c04-240">The provided mitigations reflect the best possible actions needed to improve resiliency.</span></span>
- <span data-ttu-id="35c04-241">Les appareils sont comptés comme « indisponibles » s’ils n’ont pas transmis de données au service.</span><span class="sxs-lookup"><span data-stu-id="35c04-241">Devices are counted as "unavailable" if they have not transmitted data to the service.</span></span>
- <span data-ttu-id="35c04-242">Les statistiques antivirus sont basées sur Antivirus Microsoft Defender paramètres.</span><span class="sxs-lookup"><span data-stu-id="35c04-242">Antivirus-related statistics are based on Microsoft Defender Antivirus settings.</span></span> <span data-ttu-id="35c04-243">Les appareils avec des solutions antivirus tierces peuvent apparaître comme « exposés ».</span><span class="sxs-lookup"><span data-stu-id="35c04-243">Devices with third-party antivirus solutions can appear as "exposed".</span></span>

## <a name="related-topics"></a><span data-ttu-id="35c04-244">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="35c04-244">Related topics</span></span>

- [<span data-ttu-id="35c04-245">Rechercher de manière proactive les menaces avec le recherche avancée</span><span class="sxs-lookup"><span data-stu-id="35c04-245">Proactively find threats with advanced hunting</span></span>](advanced-hunting-overview.md) 
- [<span data-ttu-id="35c04-246">Comprendre la section rapport d’analyste</span><span class="sxs-lookup"><span data-stu-id="35c04-246">Understand the analyst report section</span></span>](threat-analytics-analyst-reports.md)
- [<span data-ttu-id="35c04-247">Évaluer et résoudre les faiblesses et les exposition de sécurité</span><span class="sxs-lookup"><span data-stu-id="35c04-247">Assess and resolve security weaknesses and exposures</span></span>](/windows/security/threat-protection/microsoft-defender-atp/next-gen-threat-and-vuln-mgt)
