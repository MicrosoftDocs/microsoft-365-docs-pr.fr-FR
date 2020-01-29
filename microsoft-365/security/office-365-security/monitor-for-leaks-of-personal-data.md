---
title: Surveillance des fuites de données personnelles
ms.author: bcarter
author: brendacarter
manager: laurawi
ms.date: 02/07/2018
audience: ITPro
ms.topic: overview
ms.collection:
- Strat_O365_Enterprise
- Ent_O365
- GDPR
- M365-security-compliance
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MET150
description: Découvrez trois outils qui permettent de surveiller les fuites de données personnelles.
ms.openlocfilehash: 43133ed638f91957307b832826c21ae81aa269b0
ms.sourcegitcommit: 3f8957ddd04b8710bb5f314a0902fdee50c7c9b7
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/28/2020
ms.locfileid: "41572971"
---
# <a name="monitor-for-leaks-of-personal-data"></a><span data-ttu-id="e6b67-103">Surveillance des fuites de données personnelles</span><span class="sxs-lookup"><span data-stu-id="e6b67-103">Monitor for leaks of personal data</span></span>

<span data-ttu-id="e6b67-p101">Il existe de nombreux outils qui peuvent être utilisés pour surveiller l’utilisation et le transport des données personnelles. Cette rubrique décrit trois outils qui fonctionnent correctement.</span><span class="sxs-lookup"><span data-stu-id="e6b67-p101">There are many tools that can be used to monitor the use and transport of personal data. This topic describes three tools that work well.</span></span>

![Outils permettant de surveiller l’utilisation et le transport des données personnelles](../media/Monitor-for-leaks-of-personal-data-image1.png)

<span data-ttu-id="e6b67-107">Dans cette illustration :</span><span class="sxs-lookup"><span data-stu-id="e6b67-107">In the illustration:</span></span>

- <span data-ttu-id="e6b67-p102">Commencez par les rapports sur la protection contre la perte de données Office 365 pour surveiller les données personnelles dans SharePoint Online, OneDrive Entreprise et le courrier électronique en transit. Ils offrent le meilleur niveau de détail pour surveiller les données personnelles. Toutefois, ces rapports n’incluent pas tous les services dans Office 365.</span><span class="sxs-lookup"><span data-stu-id="e6b67-p102">Start with Office 365 data loss prevention reports for monitoring personal data in SharePoint Online, OneDrive for Business, and email in transit. These provide the greatest level of detail for monitoring personal data. However, these reports don’t include all services in Office 365.</span></span>

- <span data-ttu-id="e6b67-p103">Utilisez ensuite les stratégies d’alerte et le journal d’audit Office 365 pour surveiller l’activité des services Office 365. Configurez la surveillance continue ou faites des recherches dans le journal d’audit pour identifier un incident. Le journal d’audit Office 365 fonctionne sur tous les services Office 365 (Sway, PowerBI, eDiscovery, Dynamics 365, Microsoft Flow, Microsoft Teams, l’activité d’administration, OneDrive Entreprise, SharePoint Online, le courrier électronique en transit et les boîtes aux lettres au repos). Les conversations Skype sont incluses dans les boîtes aux lettres au repos.</span><span class="sxs-lookup"><span data-stu-id="e6b67-p103">Next, use alert policies and the Office 365 audit log to monitor activity across Office 365 services. Setup ongoing monitoring or search the audit log to investigate an incident. The Office 365 audit log works across Office 365 services — Sway, PowerBI, eDiscovery, Dynamics 365, Microsoft Flow, Microsoft Teams, Admin activity, OneDrive for Business, SharePoint Online, mail in transit, and mailboxes at rest. Skype conversations are included in mailboxes at rest.</span></span>

- <span data-ttu-id="e6b67-p104">Enfin, utilisez Microsoft Cloud App Security pour surveiller les fichiers contenant des données sensibles chez d’autres fournisseurs SaaS. Il sera bientôt possible d’utiliser des types d’informations sensibles Office 365 et des étiquettes unifiées dans Azure Information Protection et Office avec Cloud App Security. Vous pouvez configurer des stratégies qui s’appliquent à toutes vos applications SaaS ou des applications spécifiques (Box, par exemple). Cloud App Security ne découvre pas les fichiers dans Exchange Online, y compris les fichiers joints à un courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="e6b67-p104">Finally, Use Microsoft Cloud App Security to monitor files with sensitive data in other SaaS providers. Coming soon is the ability to use Office 365 sensitive information types and unified labels across Azure Information Protection and Office with Cloud App Security. You can setup policies that apply to all of your SaaS apps or specific apps (like Box). Cloud App Security doesn’t discover files in Exchange Online, including files attached to email.</span></span>

## <a name="office-365-data-loss-prevention-reports"></a><span data-ttu-id="e6b67-119">Rapports de protection contre la perte de données d’Office 365</span><span class="sxs-lookup"><span data-stu-id="e6b67-119">Office 365 data loss prevention reports</span></span>

<span data-ttu-id="e6b67-p105">Après avoir créé des stratégies de protection contre la perte de données, vous voulez vérifier qu’elles fonctionnent comme prévu et vous aident à maintenir la conformité. Avec les rapports DLP d’Office 365, vous pouvez rapidement visualiser le nombre de correspondances de stratégie DLP, de remplacements et de faux positifs, savoir si ce nombre augmente ou diminue dans le temps, filtrer le rapport de différentes manières et afficher des détails supplémentaires en sélectionnant un point sur une ligne du graphique.</span><span class="sxs-lookup"><span data-stu-id="e6b67-p105">After you create your data loss prevention (DLP) policies, you’ll want to verify that they’re working as you intended and helping you to stay compliant. With the DLP reports in Office 365, you can quickly view the number of DLP policy matches, overrides, or false positives; see whether they’re trending up or down over time; filter the report in different ways; and view additional details by selecting a point on a line on the graph.</span></span>

<span data-ttu-id="e6b67-122">Vous pouvez utiliser les rapports DLP pour :</span><span class="sxs-lookup"><span data-stu-id="e6b67-122">You can use the DLP reports to:</span></span>

- <span data-ttu-id="e6b67-123">Vous concentrer sur des périodes de temps spécifiques et comprendre les raisons des pics et des tendances.</span><span class="sxs-lookup"><span data-stu-id="e6b67-123">Focus on specific time periods and understand the reasons for spikes and trends.</span></span>

- <span data-ttu-id="e6b67-124">Découvrir les processus d’entreprise qui enfreignent les stratégies DLP de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="e6b67-124">Discover business processes that violate your organization’s DLP policies.</span></span>

- <span data-ttu-id="e6b67-125">Comprendre l’incidence des stratégies DLP sur l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="e6b67-125">Understand any business impact of the DLP policies.</span></span>

- <span data-ttu-id="e6b67-126">Afficher les motifs présentés par les utilisateurs lorsqu'ils passent outre une stratégie ou signalent un faux positif.</span><span class="sxs-lookup"><span data-stu-id="e6b67-126">View the justifications submitted by users when they resolve a policy tip by overriding the policy or reporting a false positive.</span></span>

- <span data-ttu-id="e6b67-127">Vérifier la conformité avec une stratégie DLP spécifique en affichant les correspondances pour cette stratégie.</span><span class="sxs-lookup"><span data-stu-id="e6b67-127">Verify compliance with a specific DLP policy by showing any matches for that policy.</span></span>

- <span data-ttu-id="e6b67-128">Afficher la liste des fichiers avec des données sensibles qui correspondent à vos stratégies DLP dans le volet de détails.</span><span class="sxs-lookup"><span data-stu-id="e6b67-128">View a list of files with sensitive data that matches your DLP policies in the details pane.</span></span>

<span data-ttu-id="e6b67-129">En outre, vous pouvez utiliser les rapports DLP pour affiner vos stratégies DLP lorsque vous les exécutez en mode test.</span><span class="sxs-lookup"><span data-stu-id="e6b67-129">In addition, you can use the DLP reports to fine tune your DLP policies as you run them in test mode.</span></span>

<span data-ttu-id="e6b67-130">Les rapports DLP sont dans le centre de sécurité et le centre de conformité.</span><span class="sxs-lookup"><span data-stu-id="e6b67-130">DLP reports are in the security center and the compliance center.</span></span> <span data-ttu-id="e6b67-131">Accéder aux rapports \>Afficher des rapports.</span><span class="sxs-lookup"><span data-stu-id="e6b67-131">Navigate to Reports \> View reports.</span></span> <span data-ttu-id="e6b67-132">Sous Protection contre la perte de données (DLP), choisissez soit Correspondances avec les règles et les stratégies DLP ou Remplacements et faux positifs DLP.</span><span class="sxs-lookup"><span data-stu-id="e6b67-132">Under Data loss prevention (DLP), go to either DLP policy and rule matches or DLP false positives and overrides.</span></span>

<span data-ttu-id="e6b67-133">Pour plus d’informations, consultez la rubrique [Affichage des rapports de protection contre la perte de données](https://docs.microsoft.com/microsoft-365/compliance/view-the-dlp-reports).</span><span class="sxs-lookup"><span data-stu-id="e6b67-133">For more information, see [View the reports for data loss prevention](https://docs.microsoft.com/microsoft-365/compliance/view-the-dlp-reports).</span></span>

![Rapport affichant les correspondances de stratégie DLP](../media/Monitor-for-leaks-of-personal-data-image2.png)

## <a name="office-365-audit-log-and-alert-policies"></a><span data-ttu-id="e6b67-135">Journal d’audit Office 365 et stratégies d’alerte</span><span class="sxs-lookup"><span data-stu-id="e6b67-135">Office 365 audit log and alert policies</span></span>

<span data-ttu-id="e6b67-136">Le journal d’audit Office 365 contient les événements Exchange Online, SharePoint Online, OneDrive Entreprise, Azure Active Directory, Microsoft Teams, Power BI, Sway et d’autres services Office 365.</span><span class="sxs-lookup"><span data-stu-id="e6b67-136">The Office 365 audit log contains events from Exchange Online, SharePoint Online, OneDrive for Business, Azure Active Directory, Microsoft Teams, Power BI, Sway, and other Office 365 services.</span></span>

<span data-ttu-id="e6b67-137">Le Centre de sécurité et de conformité propose deux méthodes pour surveiller et générer des rapports sur la base du journal d’audit Office 365 :</span><span class="sxs-lookup"><span data-stu-id="e6b67-137">The security center and compliance center provide two ways to monitor and report against the Office 365 audit log:</span></span>

- <span data-ttu-id="e6b67-138">Configurer des stratégies d’alerte, afficher des alertes et surveiller les tendances : utilisez les nouveaux outils de tableau de bord d’alertes et de stratégie d’alerte dans le Centre de sécurité et de conformité.</span><span class="sxs-lookup"><span data-stu-id="e6b67-138">Setup alert policies, view alerts, and monitor trends — Use the alert policy and alert dashboard tools in either the security center or compliance center.</span></span>

- <span data-ttu-id="e6b67-p107">Effectuer des recherches directement dans le journal d’audit : vous pouvez rechercher tous les événements dans une plage de dates spécifiée ou filtrer les résultats en fonction de critères spécifiques, tels que l’utilisateur ayant effectué l’action, l’action ou l’objet cible.</span><span class="sxs-lookup"><span data-stu-id="e6b67-p107">Search the audit log directly — Search for all events in a specified date rage. Or you can filter the results based on specific criteria, such as the user who performed the action, the action, or the target object.</span></span>

<span data-ttu-id="e6b67-p108">Les équipes de conformité et de sécurité des informations peuvent utiliser ces outils pour revoir de façon proactive les activités effectuées par les utilisateurs finaux et les administrateurs dans les services Office 365. Des alertes automatiques peuvent être configurées pour envoyer des notifications par courrier électronique lorsque certaines activités se produisent sur des collections de sites spécifiques (par exemple, lorsque le contenu est partagé à partir de sites connus pour contenir des informations relatives au RGPD). Ainsi, ces équipes peuvent suivre les utilisateurs afin de vérifier que les stratégies de sécurité d’entreprise sont suivies, ou de fournir des formations supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="e6b67-p108">Information security and compliance teams can use these tools to proactively review activities performed by both end users and administrators across Office 365 services. Automatic alerts can be configured to send email notifications when certain activities occur on specific site collections - for example when content is shared from sites known to contain GDPR related information. This allows those teams to follow up with users to ensure that corporate security policies are followed, or to provide additional training.</span></span>

<span data-ttu-id="e6b67-p109">Les équipes de sécurité des informations peuvent aussi effectuer des recherches dans le journal pour enquêter sur des violations de données présumées, déterminer la cause initiale et l’étendue de la violation. Cette fonctionnalité intégrée facilite la conformité à l’article 33 et 34 du RGPD, qui exige que des notifications soient fournies à l’autorité de surveillance du RGPD et aux personnes victimes d’une violation de données sur une période donnée. Les entrées du journal d’audit sont conservées pendant 90 jours seulement au sein du service (il est souvent recommandé que ces journaux soient conservés pour des périodes de temps plus longues et de nombreuses organisations en ont fait la demande).</span><span class="sxs-lookup"><span data-stu-id="e6b67-p109">Information security teams can also search the audit log to investigate suspected data breaches and determine both root cause and the extent of the breach. This built in capability facilitates compliance with article 33 and 34 of the GDPR, which require notifications be provided to the GDPR supervisory authority and to the data subjects themselves of a data breach within a specific time period. Audit log entries are only retained for 90 days within the service - it is often recommended and many organizations required that these logs be retained for longer periods of time.</span></span>

<span data-ttu-id="e6b67-p110">Il existe des solutions qui s’abonnent aux journaux d’audit unifiés via l’API Activité de gestion Microsoft et qui peuvent à la fois stocker des entrées du journal et fournir des alertes et des tableaux de bord avancés. [Microsoft Operations Management Suite (OMS)](https://docs.microsoft.com/azure/operations-management-suite/oms-solution-office-365) en est un exemple.</span><span class="sxs-lookup"><span data-stu-id="e6b67-p110">Solutions are available which subscribe to the Unified Audit Logs through the Microsoft Management Activity API and can both store log entries as needed, and provide advanced dashboards and alerts. One example is [Microsoft Operations Management Suite (OMS)](https://docs.microsoft.com/azure/operations-management-suite/oms-solution-office-365).</span></span>

<span data-ttu-id="e6b67-149">Plus d’informations sur les stratégies d’alerte et l’exécution d’une recherche dans le journal d’audit :</span><span class="sxs-lookup"><span data-stu-id="e6b67-149">More information about alert policies and searching the audit log:</span></span>

- [<span data-ttu-id="e6b67-150">Stratégies d’alerte dans le Centre de sécurité et de conformité Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="e6b67-150">Alert policies in the Microsoft 365 security and compliance centers</span></span>](https://docs.microsoft.com/microsoft-365/compliance/alert-policies)

- <span data-ttu-id="e6b67-151">[Effectuer des recherches dans le journal d’audit dans le Centre de sécurité et de conformité Office 365](https://docs.microsoft.com/microsoft-365/compliance/search-the-audit-log) (introduction)</span><span class="sxs-lookup"><span data-stu-id="e6b67-151">[Search the audit log for user and admin activity in Office 365](https://docs.microsoft.com/microsoft-365/compliance/search-the-audit-log) (introduction)</span></span>

- [<span data-ttu-id="e6b67-152">Activer ou désactiver la recherche dans un journal d’audit Office 365</span><span class="sxs-lookup"><span data-stu-id="e6b67-152">Turn Office 365 audit log search on or off</span></span>](https://docs.microsoft.com/microsoft-365/compliance/turn-audit-log-search-on-or-off)

- [<span data-ttu-id="e6b67-153">Rechercher le journal d’audit</span><span class="sxs-lookup"><span data-stu-id="e6b67-153">Search the audit log</span></span>](https://docs.microsoft.com/microsoft-365/compliance/search-the-audit-log-in-security-and-compliance)

- <span data-ttu-id="e6b67-154">[Search-UnifiedAuditLog](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-audit/search-unifiedauditlog) (cmdlet)</span><span class="sxs-lookup"><span data-stu-id="e6b67-154">[Search-UnifiedAuditLog](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-audit/search-unifiedauditlog) (cmdlet)</span></span>

- [<span data-ttu-id="e6b67-155">Propriétés détaillées dans le journal d’audit Office 365</span><span class="sxs-lookup"><span data-stu-id="e6b67-155">Detailed properties in the Office 365 audit log</span></span>](https://docs.microsoft.com/microsoft-365/compliance/detailed-properties-in-the-office-365-audit-log)

## <a name="microsoft-cloud-app-security"></a><span data-ttu-id="e6b67-156">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="e6b67-156">Microsoft Cloud App Security</span></span>

<span data-ttu-id="e6b67-157">Microsoft Cloud App Security vous permet de découvrir d’autres applications SaaS utilisées dans vos réseaux et les données sensibles qui sont envoyées vers et depuis ces applications.</span><span class="sxs-lookup"><span data-stu-id="e6b67-157">Microsoft Cloud App Security helps you discover other SaaS apps in use across your networks and sensitive data that is sent to and from these apps.</span></span>

<span data-ttu-id="e6b67-p111">Microsoft Cloud App Security est un service complet fournissant une grande visibilité, des contrôles précis et une meilleure protection contre les menaces pour vos applications cloud. Il identifie plus de 15 000 applications cloud dans votre réseau (de tous les appareils) et fournit une notation des risques et une analyse et évaluation continues des risques. Aucun agent n’est obligatoire : les informations sont collectées à partir de vos pare-feu et proxys afin d’offrir une visibilité et un contexte complets pour l’utilisation du cloud et du Shadow IT.</span><span class="sxs-lookup"><span data-stu-id="e6b67-p111">Microsoft Cloud App Security is a comprehensive service providing deep visibility, granular controls and enhanced threat protection for your cloud apps. It identifies more than 15,000 cloud applications in your network-from all devices-and provides risk scoring and ongoing risk assessment and analytics. No agents required: information is collected from your firewalls and proxies to give you complete visibility and context for cloud usage and shadow IT.</span></span>

<span data-ttu-id="e6b67-p112">Pour mieux comprendre votre environnement cloud, la fonctionnalité d’examen de Cloud App Security fournit une grande visibilité sur l’ensemble des activités, fichiers et comptes pour les applications approuvées et gérées. Vous pouvez obtenir des informations détaillées sur un niveau de fichier et découvrir où se déplacent les données dans les applications cloud.</span><span class="sxs-lookup"><span data-stu-id="e6b67-p112">To better understand your cloud environment, Cloud App Security investigate feature provides deep visibility into all activities, files and accounts for sanctioned and managed apps. You can gain detailed information on a file level and discover where data travels in the cloud apps.</span></span>

<span data-ttu-id="e6b67-163">Pour consulter des exemples, l’illustration suivante décrit deux stratégies Cloud App Security qui peuvent vous aider avec le RGPD.</span><span class="sxs-lookup"><span data-stu-id="e6b67-163">For examples, the following illustration demonstrates two Cloud App Security policies that can help with GDPR.</span></span>

![Exemple de stratégies Cloud App Security](../media/Monitor-for-leaks-of-personal-data-image3.png)

<span data-ttu-id="e6b67-165">La première stratégie signale lorsque des fichiers avec un attribut PII prédéfini ou une expression personnalisée que vous choisissez sont partagés en dehors de l’organisation à partir des applications SaaS que vous choisissez.</span><span class="sxs-lookup"><span data-stu-id="e6b67-165">The first policy alerts when files with a predefined PII attribute or custom expression that you choose is shared outside the organization from the SaaS apps that you choose.</span></span>

<span data-ttu-id="e6b67-p113">La seconde stratégie bloque les téléchargements de fichiers sur des appareils non gérés. Vous choisissez les attributs dans les fichiers à rechercher et les applications SaaS auxquelles vous souhaitez appliquer la stratégie.</span><span class="sxs-lookup"><span data-stu-id="e6b67-p113">The second policy blocks downloads of files to any unmanaged device. You choose the attributes within the files to look for and the SaaS apps you want the policy to apply to.</span></span>

<span data-ttu-id="e6b67-168">Les types d’attribut suivants seront bientôt disponibles dans Cloud App Security :</span><span class="sxs-lookup"><span data-stu-id="e6b67-168">These attribute types are coming soon to Cloud App Security:</span></span>

- <span data-ttu-id="e6b67-169">Types d'informations sensibles Office 365</span><span class="sxs-lookup"><span data-stu-id="e6b67-169">Office 365 sensitive information types</span></span>

- <span data-ttu-id="e6b67-170">Étiquettes unifiées dans Office 365 et Azure Information Protection</span><span class="sxs-lookup"><span data-stu-id="e6b67-170">Unified labels across Office 365 and Azure Information Protection</span></span>

### <a name="cloud-app-security-dashboard"></a><span data-ttu-id="e6b67-171">Tableau de bord Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="e6b67-171">Cloud App Security dashboard</span></span>

<span data-ttu-id="e6b67-p114">Si vous n’avez pas encore commencé à utiliser Cloud App Security, commencez par l’activer. Pour accéder à Cloud App Security : <https://portal.cloudappsecurity.com>.</span><span class="sxs-lookup"><span data-stu-id="e6b67-p114">If you haven’t yet started to use Cloud App Security, begin by starting it up. To access Cloud App Security: <https://portal.cloudappsecurity.com>.</span></span>

<span data-ttu-id="e6b67-p115">Remarque : veillez à activer l’option 'Analyser automatiquement les fichiers pour les étiquettes de classification Azure Information Protection' (dans les paramètres généraux) lors de la prise en main de Cloud App Security ou avant d’attribuer des étiquettes. Après la configuration, Cloud App Security n’analyse pas de nouveau les fichiers existants tant qu’ils ne sont pas modifiés.</span><span class="sxs-lookup"><span data-stu-id="e6b67-p115">Note: Be sure to enable ‘Automatically scan files for Azure Information Protection classification labels’ (in General settings) when getting started with Cloud App Security or before you assign labels. After setup, Cloud App Security does not scan existing files again until they are modified.</span></span>

![Tableau de bord affichant des informations sur les alertes](../media/Monitor-for-leaks-of-personal-data-image4.png)

<span data-ttu-id="e6b67-177">Plus d’informations :</span><span class="sxs-lookup"><span data-stu-id="e6b67-177">More information:</span></span>

- <span data-ttu-id="e6b67-178">Rubrique relative au [déploiement de Cloud App Security](https://docs.microsoft.com/cloud-app-security/getting-started-with-cloud-app-security)</span><span class="sxs-lookup"><span data-stu-id="e6b67-178">[Deploy Cloud App Security](https://docs.microsoft.com/cloud-app-security/getting-started-with-cloud-app-security)</span></span>

- <span data-ttu-id="e6b67-179">Rubrique relative aux [informations supplémentaires concernant Microsoft Cloud App Security](https://www.microsoft.com/cloud-platform/cloud-app-security)</span><span class="sxs-lookup"><span data-stu-id="e6b67-179">[More information about Microsoft Cloud App Security](https://www.microsoft.com/cloud-platform/cloud-app-security)</span></span>

- <span data-ttu-id="e6b67-180">Rubrique relative au [blocage des téléchargements d’informations sensibles à l’aide du proxy Microsoft Cloud App Security](https://docs.microsoft.com/cloud-app-security/use-case-proxy-block-session-aad)</span><span class="sxs-lookup"><span data-stu-id="e6b67-180">[Block downloads of sensitive information using the Microsoft Cloud App Security proxy](https://docs.microsoft.com/cloud-app-security/use-case-proxy-block-session-aad)</span></span>

## <a name="example-file-and-activity-policies-to-detect-sharing-of-personal-data"></a><span data-ttu-id="e6b67-181">Exemple de stratégies d’activité et de fichier pour détecter le partage de données personnelles</span><span class="sxs-lookup"><span data-stu-id="e6b67-181">Example file and activity policies to detect sharing of personal data</span></span>

### <a name="detect-sharing-of-files-containing-pii--credit-card-number"></a><span data-ttu-id="e6b67-182">Détection du partage de fichiers contenant des informations PII : numéro de carte de crédit</span><span class="sxs-lookup"><span data-stu-id="e6b67-182">Detect sharing of files containing PII — Credit card number</span></span>

<span data-ttu-id="e6b67-183">Alerte lorsqu’un fichier contenant un numéro de carte de crédit est partagé à partir d’une application cloud approuvée.</span><span class="sxs-lookup"><span data-stu-id="e6b67-183">Alert when a file containing a credit card number is shared from an approved cloud app.</span></span>

<table>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e6b67-184"><strong>Contrôle</strong></span><span class="sxs-lookup"><span data-stu-id="e6b67-184"><strong>Control</strong></span></span></th>
<th align="left"><span data-ttu-id="e6b67-185"><strong>Paramètres</strong></span><span class="sxs-lookup"><span data-stu-id="e6b67-185"><strong>Settings</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><span data-ttu-id="e6b67-186">Type de stratégie</span><span class="sxs-lookup"><span data-stu-id="e6b67-186">Policy type</span></span></td>
<td align="left"><span data-ttu-id="e6b67-187">Stratégie de fichier</span><span class="sxs-lookup"><span data-stu-id="e6b67-187">File policy</span></span></td>
</tr>
<tr class="even">
<td align="left"><span data-ttu-id="e6b67-188">Modèle de stratégie</span><span class="sxs-lookup"><span data-stu-id="e6b67-188">Policy template</span></span></td>
<td align="left"><span data-ttu-id="e6b67-189">Aucun modèle</span><span class="sxs-lookup"><span data-stu-id="e6b67-189">No template</span></span></td>
</tr>
<tr class="odd">
<td align="left"><span data-ttu-id="e6b67-190">Gravité de la stratégie</span><span class="sxs-lookup"><span data-stu-id="e6b67-190">Policy severity</span></span></td>
<td align="left"><span data-ttu-id="e6b67-191">Importante</span><span class="sxs-lookup"><span data-stu-id="e6b67-191">High</span></span></td>
</tr>
<tr class="even">
<td align="left"><span data-ttu-id="e6b67-192">Catégorie</span><span class="sxs-lookup"><span data-stu-id="e6b67-192">Category</span></span></td>
<td align="left"><span data-ttu-id="e6b67-193">DLP</span><span class="sxs-lookup"><span data-stu-id="e6b67-193">DLP</span></span></td>
</tr>
<tr class="odd">
<td align="left"><span data-ttu-id="e6b67-194">Paramètres de filtre</span><span class="sxs-lookup"><span data-stu-id="e6b67-194">Filter settings</span></span></td>
<td align="left"><p><span data-ttu-id="e6b67-195">Niveau d’accès = Public (Internet), Public, Externe</span><span class="sxs-lookup"><span data-stu-id="e6b67-195">Access level = Public (Internet), Public, External</span></span></p>
<p><span data-ttu-id="e6b67-196">Application = &lt;sélectionner les applications&gt; (utiliser ce paramètre pour limiter la surveillance à des applications SaaS spécifiques)</span><span class="sxs-lookup"><span data-stu-id="e6b67-196">App = &lt;select apps&gt; (use this setting if you want to limit monitoring to specific SaaS apps)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><span data-ttu-id="e6b67-197">Appliquer à</span><span class="sxs-lookup"><span data-stu-id="e6b67-197">Apply to</span></span></td>
<td align="left"><span data-ttu-id="e6b67-198">Tous les fichiers, tous les propriétaires</span><span class="sxs-lookup"><span data-stu-id="e6b67-198">All files, all owners</span></span></td>
</tr>
<tr class="odd">
<td align="left"><span data-ttu-id="e6b67-199">Inspection du contenu</span><span class="sxs-lookup"><span data-stu-id="e6b67-199">Content inspection</span></span></td>
<td align="left"><p><span data-ttu-id="e6b67-200">Inclut les fichiers qui correspondent à une expression présente : Tous les pays: Finance: Numéro de carte de crédit</span><span class="sxs-lookup"><span data-stu-id="e6b67-200">Includes files that match a present expression: All countries: Finance: Credit card number</span></span></p>
<p><span data-ttu-id="e6b67-201">N’exige pas de contexte approprié : désactivé (ceci correspondra aux mots-clés et aux expressions régulières)</span><span class="sxs-lookup"><span data-stu-id="e6b67-201">Don’t require relevant context: unchecked (this will match keywords as well as regex)</span></span></p>
<p><span data-ttu-id="e6b67-202">Inclut les fichiers avec au moins 1 correspondance</span><span class="sxs-lookup"><span data-stu-id="e6b67-202">Includes files with at least 1 match</span></span></p>
<p><span data-ttu-id="e6b67-203">Annuler le masquage des 4 derniers caractères de la violation : activé</span><span class="sxs-lookup"><span data-stu-id="e6b67-203">Unmask the last 4 characters of the violation: checked</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><span data-ttu-id="e6b67-204">Alertes</span><span class="sxs-lookup"><span data-stu-id="e6b67-204">Alerts</span></span></td>
<td align="left"><p><span data-ttu-id="e6b67-205">Crée une alerte pour chaque fichier correspondant : activé</span><span class="sxs-lookup"><span data-stu-id="e6b67-205">Create an alert for each matching file: checked</span></span></p>
<p><span data-ttu-id="e6b67-206">Limite quotidienne d’alertes : 1 000</span><span class="sxs-lookup"><span data-stu-id="e6b67-206">Daily alert limit: 1000</span></span></p>
<p><span data-ttu-id="e6b67-207">Sélectionner une alerte en tant qu’e-mail : activé</span><span class="sxs-lookup"><span data-stu-id="e6b67-207">Select an alert as email: checked</span></span></p>
<p><span data-ttu-id="e6b67-208">À : infosec@contoso.com</span><span class="sxs-lookup"><span data-stu-id="e6b67-208">To: infosec@contoso.com</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><span data-ttu-id="e6b67-209">Gouvernance</span><span class="sxs-lookup"><span data-stu-id="e6b67-209">Governance</span></span></td>
<td align="left"><p><span data-ttu-id="e6b67-210">Microsoft OneDrive Entreprise</span><span class="sxs-lookup"><span data-stu-id="e6b67-210">Microsoft OneDrive for Business</span></span></p>
<p><span data-ttu-id="e6b67-211">Donner un caractère privé : sélectionner Supprimer les utilisateurs externes</span><span class="sxs-lookup"><span data-stu-id="e6b67-211">Make private: check Remove External Users</span></span></p>
<p><span data-ttu-id="e6b67-212">Tous les autres paramètres : désactivé</span><span class="sxs-lookup"><span data-stu-id="e6b67-212">All other settings: unchecked</span></span></p>
<p><span data-ttu-id="e6b67-213">Microsoft SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="e6b67-213">Microsoft SharePoint Online</span></span></p>
<p><span data-ttu-id="e6b67-214">Donner un caractère privé : sélectionner Supprimer les utilisateurs externes</span><span class="sxs-lookup"><span data-stu-id="e6b67-214">Make private: check Remove External Users</span></span></p>
<p><span data-ttu-id="e6b67-215">Tous les autres paramètres : désactivé</span><span class="sxs-lookup"><span data-stu-id="e6b67-215">All other settings: unchecked</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e6b67-216">Stratégies similaires :</span><span class="sxs-lookup"><span data-stu-id="e6b67-216">Similar policies:</span></span>

- <span data-ttu-id="e6b67-217">Détection du partage de fichiers contenant des informations PII : adresse e-mail</span><span class="sxs-lookup"><span data-stu-id="e6b67-217">Detect sharing of Files containing PII - Email Address</span></span>

- <span data-ttu-id="e6b67-218">Détection du partage de fichiers contenant des informations PII : numéro de passeport</span><span class="sxs-lookup"><span data-stu-id="e6b67-218">Detect sharing of Files containing PII - Passport Number</span></span>

### <a name="detect-customer-or-hr-data-in-box-or-onedrive-for-business"></a><span data-ttu-id="e6b67-219">Détection des données client ou RH dans Box ou OneDrive Entreprise</span><span class="sxs-lookup"><span data-stu-id="e6b67-219">Detect Customer or HR Data in Box or OneDrive for Business</span></span>

<span data-ttu-id="e6b67-220">Alerte lorsqu’un fichier étiqueté en tant que Données client ou Données RH est chargé dans OneDrive Entreprise ou Box.</span><span class="sxs-lookup"><span data-stu-id="e6b67-220">Alert when a file labeled as Customer Data or HR Data is uploaded to OneDrive for Business or Box.</span></span>

<span data-ttu-id="e6b67-221">Remarques :</span><span class="sxs-lookup"><span data-stu-id="e6b67-221">Notes:</span></span>

- <span data-ttu-id="e6b67-222">La surveillance de Box requiert un connecteur configuré à l’aide du kit de développement logiciel (SDK) du connecteur de l’API.</span><span class="sxs-lookup"><span data-stu-id="e6b67-222">Box monitoring requires a connector be configured using the API Connector SDK.</span></span>

- <span data-ttu-id="e6b67-223">Cette stratégie exige des fonctionnalités qui sont actuellement en Private Preview.</span><span class="sxs-lookup"><span data-stu-id="e6b67-223">This policy requires capabilities that are currently in private preview.</span></span>

<table>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="e6b67-224"><strong>Contrôle</strong></span><span class="sxs-lookup"><span data-stu-id="e6b67-224"><strong>Control</strong></span></span></th>
<th align="left"><span data-ttu-id="e6b67-225"><strong>Paramètres</strong></span><span class="sxs-lookup"><span data-stu-id="e6b67-225"><strong>Settings</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><span data-ttu-id="e6b67-226">Type de stratégie</span><span class="sxs-lookup"><span data-stu-id="e6b67-226">Policy type</span></span></td>
<td align="left"><span data-ttu-id="e6b67-227">Stratégie d’activité</span><span class="sxs-lookup"><span data-stu-id="e6b67-227">Activity policy</span></span></td>
</tr>
<tr class="even">
<td align="left"><span data-ttu-id="e6b67-228">Modèle de stratégie</span><span class="sxs-lookup"><span data-stu-id="e6b67-228">Policy template</span></span></td>
<td align="left"><span data-ttu-id="e6b67-229">Aucun modèle</span><span class="sxs-lookup"><span data-stu-id="e6b67-229">No template</span></span></td>
</tr>
<tr class="odd">
<td align="left"><span data-ttu-id="e6b67-230">Gravité de la stratégie</span><span class="sxs-lookup"><span data-stu-id="e6b67-230">Policy severity</span></span></td>
<td align="left"><span data-ttu-id="e6b67-231">Importante</span><span class="sxs-lookup"><span data-stu-id="e6b67-231">High</span></span></td>
</tr>
<tr class="even">
<td align="left"><span data-ttu-id="e6b67-232">Catégorie</span><span class="sxs-lookup"><span data-stu-id="e6b67-232">Category</span></span></td>
<td align="left"><span data-ttu-id="e6b67-233">Contrôle partagé</span><span class="sxs-lookup"><span data-stu-id="e6b67-233">Sharing Control</span></span></td>
</tr>
<tr class="odd">
<td align="left"><span data-ttu-id="e6b67-234">Agir sur</span><span class="sxs-lookup"><span data-stu-id="e6b67-234">Act on</span></span></td>
<td align="left"><span data-ttu-id="e6b67-235">Activité unique</span><span class="sxs-lookup"><span data-stu-id="e6b67-235">Single activity</span></span></td>
</tr>
<tr class="even">
<td align="left"><span data-ttu-id="e6b67-236">Paramètres de filtre</span><span class="sxs-lookup"><span data-stu-id="e6b67-236">Filter settings</span></span></td>
<td align="left"><p><span data-ttu-id="e6b67-237">Type d’activité = Charger un fichier</span><span class="sxs-lookup"><span data-stu-id="e6b67-237">Activity type = Upload File</span></span></p>
<p><span data-ttu-id="e6b67-238">Application = Microsoft OneDrive Entreprise et Box</span><span class="sxs-lookup"><span data-stu-id="e6b67-238">App = Microsoft OneDrive for Business and Box</span></span></p>
<p><span data-ttu-id="e6b67-239">Étiquette de classification (actuellement en Private Preview) : Azure Information Protection = données sur les clients, ressources humaines - données sur le salaire, ressources humaines - données sur les employés</span><span class="sxs-lookup"><span data-stu-id="e6b67-239">Classification Label (currently in private preview): Azure Information Protection = Customer Data, Human Resources—Salary Data, Human Resources—Employee Data</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><span data-ttu-id="e6b67-240">Alertes</span><span class="sxs-lookup"><span data-stu-id="e6b67-240">Alerts</span></span></td>
<td align="left"><p><span data-ttu-id="e6b67-241">Créer une alerte : activé</span><span class="sxs-lookup"><span data-stu-id="e6b67-241">Create an alert: checked</span></span></p>
<p><span data-ttu-id="e6b67-242">Limite quotidienne d’alertes : 1 000</span><span class="sxs-lookup"><span data-stu-id="e6b67-242">Daily alert limit: 1000</span></span></p>
<p><span data-ttu-id="e6b67-243">Sélectionner une alerte en tant qu’e-mail : activé</span><span class="sxs-lookup"><span data-stu-id="e6b67-243">Select an alert as email: checked</span></span></p>
<p><span data-ttu-id="e6b67-244">À : infosec@contoso.com</span><span class="sxs-lookup"><span data-stu-id="e6b67-244">To: infosec@contoso.com</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><span data-ttu-id="e6b67-245">Gouvernance</span><span class="sxs-lookup"><span data-stu-id="e6b67-245">Governance</span></span></td>
<td align="left"><p><span data-ttu-id="e6b67-246">Toutes les applications</span><span class="sxs-lookup"><span data-stu-id="e6b67-246">All apps</span></span></p>
<p><span data-ttu-id="e6b67-247">Mettre l’utilisateur en quarantaine : activé</span><span class="sxs-lookup"><span data-stu-id="e6b67-247">Put user in quarantine: check</span></span></p>
<p><span data-ttu-id="e6b67-248">Tous les autres paramètres : désactivé</span><span class="sxs-lookup"><span data-stu-id="e6b67-248">All other settings: unchecked</span></span></p>
<p><span data-ttu-id="e6b67-249">Office 365</span><span class="sxs-lookup"><span data-stu-id="e6b67-249">Office 365</span></span></p>
<p><span data-ttu-id="e6b67-250">Mettre l’utilisateur en quarantaine : activé</span><span class="sxs-lookup"><span data-stu-id="e6b67-250">Put user in quarantine: check</span></span></p>
<p><span data-ttu-id="e6b67-251">Tous les autres paramètres : désactivé</span><span class="sxs-lookup"><span data-stu-id="e6b67-251">All other settings: unchecked</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e6b67-252">Stratégies similaires :</span><span class="sxs-lookup"><span data-stu-id="e6b67-252">Similar policies:</span></span>

- <span data-ttu-id="e6b67-253">Détection de téléchargements volumineux de données client ou de données RH : alerte lorsqu’un grand nombre de fichiers contenant des données client ou des données RH ont été téléchargés par un utilisateur unique dans un court délai.</span><span class="sxs-lookup"><span data-stu-id="e6b67-253">Detect large downloads of Customer data or HR Data — Alert when a large number of files containing customer data or HR data have been detected being downloaded by a single user within a short period of time.</span></span>

- <span data-ttu-id="e6b67-254">Détection du partage de données clients et de données RH : alerte lorsque des fichiers contenant des données clients ou des données RH sont partagés.</span><span class="sxs-lookup"><span data-stu-id="e6b67-254">Detect Sharing of Customer and HR Data — Alert when files containing Customer or HR Data are shared.</span></span>
