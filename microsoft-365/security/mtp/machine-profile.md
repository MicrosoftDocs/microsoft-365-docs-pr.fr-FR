---
title: Profil de l’ordinateur dans le portail de sécurité Microsoft 365
description: Afficher les niveaux de risque et d’exposition d’un périphérique dans votre organisation. Analysez les menaces passées et actuelles, et protégez l’ordinateur avec les dernières mises à jour.
keywords: sécurité, programmes malveillants, Microsoft 365, M365, protection Microsoft contre les menaces, MTP, centre de sécurité, Microsoft Defender ATP, Office 365 ATP, Azure ATP, ordinateur, page, liste des ordinateurs, profil d’ordinateur
ms.prod: microsoft-365-enterprise
ms.mktglfcycl: deploy
ms.localizationpriority: medium
ms.author: v-maave
author: martyav
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
search.appverid: met150
ms.openlocfilehash: 1dfb567c8e6b8573397d503ae27c0aceb447c916
ms.sourcegitcommit: fce0d5cad32ea60a08ff001b228223284710e2ed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/21/2020
ms.locfileid: "42895462"
---
# <a name="machine-profile-page"></a><span data-ttu-id="2d006-105">Page de profil de l’appareil</span><span class="sxs-lookup"><span data-stu-id="2d006-105">Machine profile page</span></span>

<span data-ttu-id="2d006-106">Le portail de sécurité Microsoft 365 vous fournit des pages de profil d’ordinateur, afin que vous puissiez évaluer l’intégrité et l’état des appareils sur votre réseau.</span><span class="sxs-lookup"><span data-stu-id="2d006-106">The Microsoft 365 security portal provides you with Machine profile pages, so you can assess the health and status of devices on your network.</span></span> <span data-ttu-id="2d006-107">Chaque page de profil d’ordinateur contient une multitude d’informations sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2d006-107">Each Machine profile page contains a wealth of information about the device.</span></span>

<span data-ttu-id="2d006-108">Vous pouvez consulter des informations détaillées sur les logiciels exécutés, sur les alertes ou les événements de sécurité passés et présents, et trouver des liens vers les correctifs logiciels pertinents.</span><span class="sxs-lookup"><span data-stu-id="2d006-108">You can review in-depth information about what software it is running, any past and present security events or alerts, and find links to relevant software patches.</span></span>

<span data-ttu-id="2d006-109">Vous pouvez également utiliser le profil d’ordinateur pour effectuer des tâches courantes liées à la sécurité et examiner rapidement les détails de base sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2d006-109">You can also use the Machine profile to perform common security-related tasks, and quickly review basic details about the device.</span></span>

## <a name="navigating-the-machine-profile-page"></a><span data-ttu-id="2d006-110">Navigation dans la page de profil d’ordinateur</span><span class="sxs-lookup"><span data-stu-id="2d006-110">Navigating the Machine profile page</span></span>

<span data-ttu-id="2d006-111">La page profil de l’ordinateur est divisée en trois sections.</span><span class="sxs-lookup"><span data-stu-id="2d006-111">The machine profile page is broken up into three sections.</span></span>

![Image de la page de profil de l’ordinateur avec (1) barre d’onglets (2) et (3) actions mises en surbrillance en rouge](../../media/mtp-machine-profile/mtp-machine-profile-all.png)

<span data-ttu-id="2d006-113">La zone de contenu principale (1) contient sept onglets que vous pouvez parcourir pour afficher différents types d’informations sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="2d006-113">The main content area (1) contains seven tabs that you can toggle through to view different kinds of information about the machine.</span></span>

<span data-ttu-id="2d006-114">L’encadré (2) répertorie les détails de base sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="2d006-114">The sidebar (2) lists basic details about the machine.</span></span>

<span data-ttu-id="2d006-115">Des actions de réponse sont également disponibles dans un en-tête (3) avant les sections Sidebar et contenu principal.</span><span class="sxs-lookup"><span data-stu-id="2d006-115">There are also response actions available in a header (3) before the sidebar and main content sections.</span></span> <span data-ttu-id="2d006-116">Vous pouvez utiliser les actions de cet en-tête pour effectuer des tâches courantes liées à la sécurité.</span><span class="sxs-lookup"><span data-stu-id="2d006-116">You can use the actions in this header to perform common security-related tasks.</span></span>

## <a name="tabs-section"></a><span data-ttu-id="2d006-117">Section Onglets</span><span class="sxs-lookup"><span data-stu-id="2d006-117">Tabs section</span></span>

<span data-ttu-id="2d006-118">Les onglets de profil d’ordinateur vous permettent d’afficher une vue d’ensemble des détails de la sécurité sur l’ordinateur, ainsi que des tableaux contenant une liste d’alertes, une chronologie, une liste de recommandations de sécurité, un inventaire logiciel, une liste de vulnérabilités découvertes et des éléments manquants. Ko (mises à jour de sécurité).</span><span class="sxs-lookup"><span data-stu-id="2d006-118">The Machine profile tabs allow you to toggle through an overview of security details about the machine, and tables containing a list of alerts, a timeline, a list of security recommendations, a software inventory, a list of discovered vulnerabilities, and missing KBs (security updates).</span></span>

### <a name="overview-tab"></a><span data-ttu-id="2d006-119">Onglet vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="2d006-119">Overview tab</span></span>

<span data-ttu-id="2d006-120">L’onglet par défaut est **vue d’ensemble**.</span><span class="sxs-lookup"><span data-stu-id="2d006-120">The default tab is **Overview**.</span></span> <span data-ttu-id="2d006-121">Elle fournit un aperçu rapide du plus important de la sécurité de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2d006-121">It provides a quick look at the most important security fact about the device.</span></span>

![Image de l’onglet vue d’ensemble pour le profil d’ordinateur](../../media/mtp-machine-profile/overview.png)

<span data-ttu-id="2d006-123">Ici, vous pouvez trouver un graphique du niveau de risque de l’appareil et des alertes actives, des utilisateurs actuellement connectés, d’une liste succincte des utilisateurs les plus fréquents et les moins fréquents, ainsi que des évaluations de sécurité qui détaillent le niveau d’exposition de l’appareil, les recommandations en matière de sécurité, les logiciels concernés et vulnérabilités découvertes.</span><span class="sxs-lookup"><span data-stu-id="2d006-123">Here, you can find a chart of the device's risk level and active alerts, any currently logged on users, a brief list of most and least frequent users, and security assessments that detail the device's exposure level, security recommendations, affected software, and discovered vulnerabilities.</span></span>

### <a name="alerts-tab"></a><span data-ttu-id="2d006-124">Onglet Alertes</span><span class="sxs-lookup"><span data-stu-id="2d006-124">Alerts tab</span></span>

<span data-ttu-id="2d006-125">L’onglet **alertes** contient la liste des alertes signalées sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2d006-125">The **Alerts** tab contains a list of alerts that have been reported on the device.</span></span>

![Image de l’onglet Alertes pour le profil de l’ordinateur](../../media/mtp-machine-profile/alerts.png)

<span data-ttu-id="2d006-127">Vous pouvez personnaliser le nombre d’éléments affichés, ainsi que les colonnes affichées pour chaque élément.</span><span class="sxs-lookup"><span data-stu-id="2d006-127">You can customize the number of items displayed, as well as which columns are displayed for each item.</span></span> <span data-ttu-id="2d006-128">Le comportement par défaut consiste à répertorier 30 éléments par page et à afficher 11 colonnes sur Afficher.</span><span class="sxs-lookup"><span data-stu-id="2d006-128">The default behavior is to list 30 items per page, and have 11 columns toggled on to display.</span></span>

<span data-ttu-id="2d006-129">Les colonnes de cet onglet incluent des informations sur la gravité de la menace qui a déclenché l’alerte, ainsi que sur l’État, l’état de l’enquête et l’identité de l’utilisateur auquel l’alerte a été affectée.</span><span class="sxs-lookup"><span data-stu-id="2d006-129">The columns in this tab include information on the severity of the threat that triggered the alert, as well as status, investigation state, and who if anyone the alert has been assigned to.</span></span>

<span data-ttu-id="2d006-130">La colonne des *entités concernées* fait référence à l’ordinateur (entité) dont vous visualisez le profil que vous consultez actuellement, ainsi qu’aux autres machines de votre réseau qui sont affectées.</span><span class="sxs-lookup"><span data-stu-id="2d006-130">The *impacted entities* column refers to the machine (entity) whose profile you are currently viewing, plus any other machines in your network that are affected.</span></span>

<span data-ttu-id="2d006-131">La sélection d’un élément dans cette liste permet d’ouvrir un lien vers l’alerte sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="2d006-131">Selecting an item from this list will open a link to the selected alert.</span></span>

<span data-ttu-id="2d006-132">Cette liste peut être filtrée par gravité, État ou cessionnaire.</span><span class="sxs-lookup"><span data-stu-id="2d006-132">This list can be filtered by severity, status, or assignee.</span></span>

### <a name="timeline-tab"></a><span data-ttu-id="2d006-133">Onglet chronologie</span><span class="sxs-lookup"><span data-stu-id="2d006-133">Timeline tab</span></span>

<span data-ttu-id="2d006-134">L’onglet **chronologie** inclut un graphique interactif et chronologique des événements déclenchés sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2d006-134">The **Timeline** tab includes a interactive, chronological chart of events raised on the device.</span></span> <span data-ttu-id="2d006-135">En déplacant la zone mise en surbrillance du graphique, vous pouvez afficher les événements sur des plages de temps différentes.</span><span class="sxs-lookup"><span data-stu-id="2d006-135">By moving the highlighted area of the chart, you can view events over different ranges of time.</span></span> <span data-ttu-id="2d006-136">Vous pouvez également taper dans une plage de dates personnalisée.</span><span class="sxs-lookup"><span data-stu-id="2d006-136">You can also type in a custom range of dates.</span></span>

<span data-ttu-id="2d006-137">Sous le graphique se trouve une liste d’événements pour la plage de dates sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="2d006-137">Below the chart is a list of events for the selected range of dates.</span></span>

![Image de l’onglet chronologie pour le profil de l’ordinateur](../../media/mtp-machine-profile/timeline.png)

<span data-ttu-id="2d006-139">Le nombre d’éléments affichés et les colonnes de la liste peuvent être personnalisés.</span><span class="sxs-lookup"><span data-stu-id="2d006-139">The number of items displayed and the columns on the list can both be customized.</span></span> <span data-ttu-id="2d006-140">Les colonnes par défaut répertorient l’heure de l’événement, l’utilisateur actif, le type d’action, les entités (processus) et des informations supplémentaires sur l’événement.</span><span class="sxs-lookup"><span data-stu-id="2d006-140">The default columns list the event time, active user, action type, entities (processes), and additional information about the event.</span></span>

<span data-ttu-id="2d006-141">La sélection d’un élément dans la liste ouvre un menu volant affichant un graphique d’entités d’événements, affichant les processus parents et enfants qui ont déclenché l’événement.</span><span class="sxs-lookup"><span data-stu-id="2d006-141">Selecting an item from the list will open a flyout displaying an Event entities graph, showing the parent and child processes that triggered the event.</span></span>

<span data-ttu-id="2d006-142">Cette liste peut être filtrée par type d’événement spécifique ; par exemple, des événements de registre ou des événements Smart Screen.</span><span class="sxs-lookup"><span data-stu-id="2d006-142">This list can be filtered by the specific kind of event; for example, Registry events or Smart Screen Events.</span></span>

### <a name="security-recommendations-tab"></a><span data-ttu-id="2d006-143">Onglet recommandations de sécurité</span><span class="sxs-lookup"><span data-stu-id="2d006-143">Security recommendations tab</span></span>

<span data-ttu-id="2d006-144">L’onglet **Security Recommendations** répertorie les actions que vous pouvez effectuer pour protéger l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2d006-144">The **Security recommendations** tab lists actions you can take to protect the device.</span></span> <span data-ttu-id="2d006-145">La sélection d’un élément sur cette liste ouvre un menu volant dans lequel vous pouvez obtenir des instructions sur l’application de la recommandation.</span><span class="sxs-lookup"><span data-stu-id="2d006-145">Selecting an item on this list will open a flyout where you can get instructions on how to apply the recommendation.</span></span>

![Image de l’onglet recommandations de sécurité pour le profil de l’ordinateur](../../media/mtp-machine-profile/security-recs.png)

<span data-ttu-id="2d006-147">Comme avec les onglets précédents, le nombre d’éléments affichés par page et les colonnes visibles peuvent être personnalisés.</span><span class="sxs-lookup"><span data-stu-id="2d006-147">As with the previous tabs, the number of items displayed per page and which columns are visible can be customized.</span></span>

<span data-ttu-id="2d006-148">L’affichage par défaut inclut des colonnes qui détaillent les faiblesses de sécurité traitées, la menace associée, le composant ou le logiciel associé concerné par la menace, et bien plus encore.</span><span class="sxs-lookup"><span data-stu-id="2d006-148">The default view includes columns that detail the security weaknesses addressed, the associated threat, the related component or software affected by the threat, and more.</span></span> <span data-ttu-id="2d006-149">Les éléments peuvent être filtrés selon l’état de la recommandation.</span><span class="sxs-lookup"><span data-stu-id="2d006-149">Items can be filtered by the recommendation's status.</span></span>

### <a name="software-inventory"></a><span data-ttu-id="2d006-150">Inventaire des logiciels</span><span class="sxs-lookup"><span data-stu-id="2d006-150">Software inventory</span></span>

<span data-ttu-id="2d006-151">L’onglet **inventaire logiciel** répertorie les logiciels installés sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2d006-151">The **Software inventory** tab lists software installed on the device.</span></span>

![Image de l’onglet inventaire logiciel pour le profil de l’ordinateur](../../media/mtp-machine-profile/software-inventory.png)

<span data-ttu-id="2d006-153">La vue par défaut affiche le fournisseur de logiciels, le numéro de version installé, le nombre de faiblesses logicielles connues, les informations de menace, le code de produit et les balises.</span><span class="sxs-lookup"><span data-stu-id="2d006-153">The default view displays the software vendor, installed version number, number of known software weaknesses, threat insights, product code, and tags.</span></span> <span data-ttu-id="2d006-154">Le nombre d’éléments affichés et les colonnes affichées peuvent être personnalisés.</span><span class="sxs-lookup"><span data-stu-id="2d006-154">The number of items displayed and which columns are displayed can both be customized.</span></span>

<span data-ttu-id="2d006-155">La sélection d’un élément dans cette liste ouvre un lanceur contenant des détails supplémentaires sur le logiciel sélectionné, ainsi que le chemin d’accès et l’horodatage de la dernière fois que le logiciel a été trouvé.</span><span class="sxs-lookup"><span data-stu-id="2d006-155">Selecting an item from this list opens a flyout containing more details about the selected software, as well as the path and timestamp for the last time the software was found.</span></span>

<span data-ttu-id="2d006-156">Cette liste peut être filtrée par code de produit.</span><span class="sxs-lookup"><span data-stu-id="2d006-156">This list can be filtered by product code.</span></span>

### <a name="discovered-vulnerabilities-tab"></a><span data-ttu-id="2d006-157">Onglet vulnérabilités découvertes</span><span class="sxs-lookup"><span data-stu-id="2d006-157">Discovered vulnerabilities tab</span></span>

<span data-ttu-id="2d006-158">L’onglet **vulnérabilités découvertes** répertorie les vulnérabilités et exploits courants (CVE) susceptibles d’affecter l’appareil.</span><span class="sxs-lookup"><span data-stu-id="2d006-158">The **Discovered vulnerabilities** tab lists any Common Vulnerabilities and Exploits (CVEs) that may affect the device.</span></span>

![Image de l’onglet vulnérabilités découvertes pour le profil de l’ordinateur](../../media/mtp-machine-profile/discovered-vulnerabilities.png)

<span data-ttu-id="2d006-160">L’affichage par défaut répertorie la gravité de CVE, le score commun de vulnérabilité (CVS), le logiciel associé à CVE, le moment où le CVE a été publié, la date de la dernière mise à jour et les menaces associées à CVE.</span><span class="sxs-lookup"><span data-stu-id="2d006-160">The default view lists the severity of the CVE, the Common Vulnerability Score (CVS), the software related to the CVE, when the CVE was published, when the CVE was last updated, and threats associated with the CVE.</span></span>

<span data-ttu-id="2d006-161">Comme avec les onglets précédents, le nombre d’éléments affichés et les colonnes visibles peuvent être personnalisés.</span><span class="sxs-lookup"><span data-stu-id="2d006-161">As with the previous tabs, the number of items displayed and which columns are visible can be customized.</span></span>

<span data-ttu-id="2d006-162">La sélection d’un élément dans cette liste ouvrira un menu volant qui décrit le CVE.</span><span class="sxs-lookup"><span data-stu-id="2d006-162">Selecting an item from this list will open a flyout that describes the CVE.</span></span>

### <a name="missing-kbs"></a><span data-ttu-id="2d006-163">Ko manquants</span><span class="sxs-lookup"><span data-stu-id="2d006-163">Missing KBs</span></span>

<span data-ttu-id="2d006-164">L’onglet **Ko manquants** répertorie toutes les mises à jour Microsoft qui n’ont pas encore été appliquées à l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="2d006-164">The **Missing KBs** tab lists any Microsoft Updates that have yet to be applied to the machine.</span></span> <span data-ttu-id="2d006-165">Le « Ko » en question sont des Articles de la [base de connaissances](https://support.microsoft.com/help/242450/how-to-query-the-microsoft-knowledge-base-by-using-keywords-and-query) qui décrivent ces mises à jour ; par exemple, [KB4551762](https://support.microsoft.com/help/4551762/windows-10-update-kb4551762).</span><span class="sxs-lookup"><span data-stu-id="2d006-165">The "KBs" in question are [Knowledge Base articles](https://support.microsoft.com/help/242450/how-to-query-the-microsoft-knowledge-base-by-using-keywords-and-query) which describe these updates; for example, [KB4551762](https://support.microsoft.com/help/4551762/windows-10-update-kb4551762).</span></span>

![Image de l’onglet Ko manquants pour le profil de l’ordinateur](../../media/mtp-machine-profile/missing-kbs.PNG)

<span data-ttu-id="2d006-167">L’affichage par défaut répertorie le Bulletin contenant les mises à jour, la version du système d’exploitation, les produits concernés, les CVE traités, le numéro de la base de connaissances et les balises.</span><span class="sxs-lookup"><span data-stu-id="2d006-167">The default view lists the bulletin containing the updates, OS version, products affected, CVEs addressed, the KB number, and tags.</span></span>

<span data-ttu-id="2d006-168">Le nombre d’éléments affichés par page et les colonnes affichées peuvent être personnalisés.</span><span class="sxs-lookup"><span data-stu-id="2d006-168">The number of items displayed per page and which columns are displayed can be customized.</span></span>

<span data-ttu-id="2d006-169">La sélection d’un élément ouvre un menu volant qui établit un lien vers la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="2d006-169">Selecting an item will open a flyout that links to the update.</span></span>

## <a name="sidebar"></a><span data-ttu-id="2d006-170">Gadgets</span><span class="sxs-lookup"><span data-stu-id="2d006-170">Sidebar</span></span>

<span data-ttu-id="2d006-171">En regard de la zone de contenu principale de la page profil de l’ordinateur est l’encadré.</span><span class="sxs-lookup"><span data-stu-id="2d006-171">Beside the main content area of the Machine profile page is the sidebar.</span></span>

![Image de l’onglet du volet de navigation pour le profil d’ordinateur](../../media/mtp-machine-profile/sidebar.png)

<span data-ttu-id="2d006-173">Le volet de navigation fournit des informations de base importantes dans les sous-sections de petite taille, qui peuvent être ouvertes ou fermées.</span><span class="sxs-lookup"><span data-stu-id="2d006-173">The sidebar provides some important basic information in small subsections which can be toggled open or closed:</span></span>

* <span data-ttu-id="2d006-174">**Tags** -toutes les balises associées au périphérique</span><span class="sxs-lookup"><span data-stu-id="2d006-174">**Tags** - Any tags associated with the device</span></span>
* <span data-ttu-id="2d006-175">**Informations de sécurité** -incidents ouverts, alertes actives, niveau d’exposition et niveau de risque</span><span class="sxs-lookup"><span data-stu-id="2d006-175">**Security info** - Open incidents, active alerts, exposure level and risk level</span></span>
* <span data-ttu-id="2d006-176">**Détails des appareils** : domaine, système d’exploitation, groupe de biens, état d’intégrité, sensibilité des données et adresses IP</span><span class="sxs-lookup"><span data-stu-id="2d006-176">**Device details** - Domain, OS, Asset group, health state, data sensitivity, and IP addresses</span></span>
* <span data-ttu-id="2d006-177">**Activité réseau** : pour la première fois et pour la dernière fois, le périphérique a été vu sur le réseau</span><span class="sxs-lookup"><span data-stu-id="2d006-177">**Network activity** - Timestamps for the first time and last time the device was seen on the network</span></span>

<span data-ttu-id="2d006-178">Cette section inclut également le nom et le niveau d’exposition du périphérique, ainsi qu’une icône indiquant s’il est actif sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="2d006-178">This section also includes the name and exposure level of the device, and an icon to indicate if it is currently active on the network.</span></span>

## <a name="response-actions"></a><span data-ttu-id="2d006-179">Actions de réponse</span><span class="sxs-lookup"><span data-stu-id="2d006-179">Response actions</span></span>

<span data-ttu-id="2d006-180">Les actions de réponse offrent un moyen rapide de se défendre et d’analyser les menaces.</span><span class="sxs-lookup"><span data-stu-id="2d006-180">Response actions offer a quick way to defend against and analyze threats.</span></span>

![Image de l’onglet du volet de navigation pour le profil d’ordinateur](../../media/mtp-machine-profile/actions.PNG)

<span data-ttu-id="2d006-182">Les actions de réponse disponibles ici sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="2d006-182">The response actions available to you here include:</span></span>

* <span data-ttu-id="2d006-183">**Gérer les balises** : met à jour les balises personnalisées que vous avez appliquées à cet appareil.</span><span class="sxs-lookup"><span data-stu-id="2d006-183">**Manage tags** - Updates custom tags you have applied to this device.</span></span>
* <span data-ttu-id="2d006-184">**Isoler l’ordinateur** : isole l’ordinateur du réseau de votre organisation tout en le gardant connecté à la protection avancée contre les menaces de Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="2d006-184">**Isolate machine** - Isolates the machine from your organization's network while keeping it connected to Microsoft Defender Advanced Threat Protection.</span></span> <span data-ttu-id="2d006-185">Vous pouvez choisir d’autoriser l’exécution d’Outlook, de teams et de Skype entreprise pendant que l’ordinateur est isolé, à des fins de communication.</span><span class="sxs-lookup"><span data-stu-id="2d006-185">You can choose to allow Outlook, Teams, and Skype for Business to run while the machine is isolated, for communication purposes.</span></span>
* <span data-ttu-id="2d006-186">**Restreindre l’exécution de l’application** : empêche les applications qui ne sont pas signées par Microsoft de s’exécuter</span><span class="sxs-lookup"><span data-stu-id="2d006-186">**Restrict app execution** - Prevents applications that are not signed by Microsoft from running</span></span>
* <span data-ttu-id="2d006-187">**Exécuter l’analyse antivirus** : met à jour les définitions de l’antivirus Windows Defender et exécute immédiatement une analyse antivirus.</span><span class="sxs-lookup"><span data-stu-id="2d006-187">**Run antivirus scan** - Updates Windows Defender Antivirus definitions and immediately runs an antivirus scan.</span></span> <span data-ttu-id="2d006-188">Choisissez entre analyse rapide ou analyse complète.</span><span class="sxs-lookup"><span data-stu-id="2d006-188">Choose between Quick scan or Full scan.</span></span>
* <span data-ttu-id="2d006-189">**Recueillir** des informations sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="2d006-189">**Collect investigation package** - Gathers information about the machine.</span></span> <span data-ttu-id="2d006-190">Une fois l’enquête terminée, vous pouvez la télécharger.</span><span class="sxs-lookup"><span data-stu-id="2d006-190">When the investigation is completed, you can download it.</span></span>
* <span data-ttu-id="2d006-191">**Lancer une session Live Response session** : charge un environnement distant sur l’ordinateur pour les [examens de sécurité approfondis](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/live-response).</span><span class="sxs-lookup"><span data-stu-id="2d006-191">**Initiate Live Response session** - Loads a remote shell on the machine for [in-depth security investigations](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/live-response).</span></span>
* <span data-ttu-id="2d006-192">**Lancer une enquête automatisée** : [enquête et corrige automatiquement les menaces](https://docs.microsoft.com/microsoft-365/security/office-365-security/office-365-air).</span><span class="sxs-lookup"><span data-stu-id="2d006-192">**Initiate automated investigation** - Automatically [investigates and remediates threats](https://docs.microsoft.com/microsoft-365/security/office-365-security/office-365-air).</span></span> <span data-ttu-id="2d006-193">Bien que vous puissiez déclencher manuellement des analyses automatisées à exécuter à partir de cette page, [certaines stratégies d’alerte](https://docs.microsoft.com/microsoft-365/compliance/alert-policies?view=o365-worldwide#default-alert-policies) déclenchent des enquêtes automatiques.</span><span class="sxs-lookup"><span data-stu-id="2d006-193">Although you can manually trigger automated investigations to run from this page, [certain alert policies](https://docs.microsoft.com/microsoft-365/compliance/alert-policies?view=o365-worldwide#default-alert-policies) trigger automatic investigations on their own.</span></span>
* <span data-ttu-id="2d006-194">**Centre de notifications** : afficher l’état des actions soumises.</span><span class="sxs-lookup"><span data-stu-id="2d006-194">**Action center** - View the status of submitted actions.</span></span> <span data-ttu-id="2d006-195">Disponible uniquement si une autre action a déjà été sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="2d006-195">Only available if another action has already been selected.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2d006-196">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="2d006-196">Related topics</span></span>

* [<span data-ttu-id="2d006-197">Vue d’ensemble de la Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="2d006-197">Microsoft Threat Protection overview</span></span>](microsoft-threat-protection.md)
* [<span data-ttu-id="2d006-198">Activer la Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="2d006-198">Turn on Microsoft Threat Protection</span></span>](mtp-enable.md)
* [<span data-ttu-id="2d006-199">Examiner les entités sur les ordinateurs à l’aide de la réponse dynamique</span><span class="sxs-lookup"><span data-stu-id="2d006-199">Investigate entities on machines using live response</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/live-response)
* [<span data-ttu-id="2d006-200">Recherche et réponse automatiques dans Office 365</span><span class="sxs-lookup"><span data-stu-id="2d006-200">Automated investigation and response (AIR) in Office 365</span></span>](https://docs.microsoft.com/microsoft-365/security/office-365-security/office-365-air)
