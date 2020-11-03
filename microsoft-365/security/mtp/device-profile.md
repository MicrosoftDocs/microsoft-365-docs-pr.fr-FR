---
title: Profil d’appareil dans le portail de sécurité Microsoft 365
description: Afficher les niveaux de risque et d’exposition d’un périphérique dans votre organisation. Analysez les menaces passées et actuelles, et protégez l’appareil avec les dernières mises à jour.
keywords: sécurité, programmes malveillants, Microsoft 365, M365, protection Microsoft contre les menaces, MTP, centre de sécurité, Microsoft Defender ATP, Office 365 ATP, Azure ATP, page appareil, profil d’appareil, page ordinateur, profil d’ordinateur
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
ms.openlocfilehash: 3840a6beae3b586fc90420f7813ff6e9d3cc6c60
ms.sourcegitcommit: 815229e39a0f905d9f06717f00dc82e2a028fa7c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2020
ms.locfileid: "48843851"
---
# <a name="device-profile-page"></a><span data-ttu-id="0dd7f-105">Page profil de périphérique</span><span class="sxs-lookup"><span data-stu-id="0dd7f-105">Device profile page</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="0dd7f-106">Le portail de sécurité Microsoft 365 vous fournit des pages de profil de périphérique, afin que vous puissiez rapidement évaluer l’intégrité et l’état des appareils sur votre réseau.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-106">The Microsoft 365 security portal provides you with device profile pages, so you can quickly assess the health and status of devices on your network.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0dd7f-107">La page de profil de périphérique peut sembler légèrement différente, selon que l’appareil est ou non s’inscrire dans Microsoft Defender pour le point de terminaison, Microsoft Defender pour l’identité ou les deux.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-107">The device profile page may appear slightly different, depending on whether the device is enrolled in Microsoft Defender for Endpoint, Microsoft Defender for Identity, or both.</span></span>

<span data-ttu-id="0dd7f-108">Si le périphérique est intégré à Microsoft Defender pour le point de terminaison, vous pouvez également utiliser la page profil de l’appareil pour effectuer certaines tâches de sécurité courantes.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-108">If the device is enrolled in Microsoft Defender for Endpoint, you can also use the device profile page to perform some common security tasks.</span></span>

## <a name="navigating-the-device-profile-page"></a><span data-ttu-id="0dd7f-109">Navigation dans la page de profil de l’appareil</span><span class="sxs-lookup"><span data-stu-id="0dd7f-109">Navigating the device profile page</span></span>

<span data-ttu-id="0dd7f-110">La page profil est divisée en plusieurs sections.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-110">The profile page is broken up into several broad sections.</span></span>

![Image de la page de profil de périphérique avec (1) barre d’onglets (2) et (3) actions mises en surbrillance en rouge](../../media/mtp-device-profile/hybrid-device-overall.png)

<span data-ttu-id="0dd7f-112">L’encadré (1) répertorie les détails de base sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-112">The sidebar (1) lists basic details about the device.</span></span>

<span data-ttu-id="0dd7f-113">La zone de contenu principale (2) contient des onglets que vous pouvez parcourir pour afficher différents types d’informations sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-113">The main content area (2) contains tabs that you can toggle through to view different kinds of information about the device.</span></span>

<span data-ttu-id="0dd7f-114">Si le périphérique est inscrit dans Microsoft Defender pour le point de terminaison, vous verrez également une liste d’actions de réponse (3).</span><span class="sxs-lookup"><span data-stu-id="0dd7f-114">If the device is enrolled in Microsoft Defender for Endpoint, you will also see a list of response actions (3).</span></span> <span data-ttu-id="0dd7f-115">Les actions de réponse vous permettent d’effectuer des tâches courantes liées à la sécurité.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-115">Response actions allow you to perform common security-related tasks.</span></span>

## <a name="sidebar"></a><span data-ttu-id="0dd7f-116">Gadgets</span><span class="sxs-lookup"><span data-stu-id="0dd7f-116">Sidebar</span></span>

<span data-ttu-id="0dd7f-117">En regard de la zone de contenu principale de la page de profil d’appareil est l’encadré.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-117">Beside the main content area of the device profile page is the sidebar.</span></span>

![Image de l’onglet du volet de navigation pour le profil d’appareil](../../media/mtp-device-profile/azure-atp-only-device-sidebar.png)

<span data-ttu-id="0dd7f-119">Le volet de navigation répertorie le nom complet et le niveau d’exposition de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-119">The sidebar lists the device's full name and exposure level.</span></span> <span data-ttu-id="0dd7f-120">Elle fournit également des informations de base importantes dans les sous-sections de petite taille qui peuvent être ouvertes ou fermées, telles que :</span><span class="sxs-lookup"><span data-stu-id="0dd7f-120">It also provides some important basic information in small subsections which can be toggled open or closed, such as:</span></span>

* <span data-ttu-id="0dd7f-121">**Tags** -tout Microsoft Defender pour point de terminaison, Microsoft Defender pour l’identité ou les balises personnalisées associées au périphérique.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-121">**Tags** - Any Microsoft Defender for Endpoint, Microsoft Defender for Identity, or custom tags associated with the device.</span></span> <span data-ttu-id="0dd7f-122">Les balises de Microsoft Defender for Identity ne sont pas modifiables.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-122">Tags from Microsoft Defender for Identity are not editable.</span></span>
* <span data-ttu-id="0dd7f-123">**Informations de sécurité** -incidents ouverts et alertes actives.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-123">**Security info** - Open incidents and active alerts.</span></span> <span data-ttu-id="0dd7f-124">Le niveau d’exposition et le niveau de risque sont également affichés dans Microsoft Defender pour le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-124">Devices enrolled in Microsoft Defender for Endpoint will also display exposure level and risk level.</span></span>

> [!TIP]
> <span data-ttu-id="0dd7f-125">Le niveau d’exposition indique le degré de conformité de l’appareil aux recommandations en matière de sécurité, tandis que le niveau de risque est calculé en fonction d’un certain nombre de facteurs, dont les types et la gravité des alertes actives.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-125">Exposure level relates to how much the device is complying with security recommendations, while risk level is calculated based on a number of factors, including the types and severity of active alerts.</span></span>

* <span data-ttu-id="0dd7f-126">**Détails** sur l’appareil-domaine, système d’exploitation, horodatage de la première vue de l’appareil, adresses IP, ressources.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-126">**Device details** - Domain, OS, timestamp for when the device was first seen, IP addresses, resources.</span></span> <span data-ttu-id="0dd7f-127">Les appareils qui sont intégrés à Microsoft Defender pour Endpoint affichent également l’état d’intégrité.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-127">Devices enrolled in Microsoft Defender for Endpoint also display health state.</span></span> <span data-ttu-id="0dd7f-128">Les appareils qui sont intégrés à Microsoft Defender pour Identity affichent le nom SAM et un horodatage pour la première création de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-128">Devices enrolled in Microsoft Defender for Identity will display SAM name and a timestamp for when the device was first created.</span></span>
* <span data-ttu-id="0dd7f-129">**Activité réseau** : pour la première fois et pour la dernière fois, le périphérique a été vu sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-129">**Network activity** - Timestamps for the first time and last time the device was seen on the network.</span></span>
* <span data-ttu-id="0dd7f-130">**Données d’annuaire** ( *uniquement pour les appareils qui sont intégrés à l’identité de Microsoft Defender* )-indicateurs [UAC](https://docs.microsoft.com/windows/security/identity-protection/user-account-control/user-account-control-overview) , [noms principaux](https://docs.microsoft.com/windows/win32/ad/service-principal-names)de propriété et appartenances aux groupes.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-130">**Directory data** ( *only for devices enrolled in Microsoft Defender for Identity* ) - [UAC](https://docs.microsoft.com/windows/security/identity-protection/user-account-control/user-account-control-overview) flags, [SPNs](https://docs.microsoft.com/windows/win32/ad/service-principal-names), and group memberships.</span></span>

## <a name="response-actions"></a><span data-ttu-id="0dd7f-131">Actions de réponse</span><span class="sxs-lookup"><span data-stu-id="0dd7f-131">Response actions</span></span>

<span data-ttu-id="0dd7f-132">Les actions de réponse offrent un moyen rapide de se défendre et d’analyser les menaces.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-132">Response actions offer a quick way to defend against and analyze threats.</span></span>

![Image de la barre d’action pour le profil d’appareil](../../media/mtp-device-profile/hybrid-device-long-action-bar.png)

> [!IMPORTANT]
> * <span data-ttu-id="0dd7f-134">Les [actions de réponse](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/respond-machine-alerts) ne sont disponibles que si le périphérique est intégré à Microsoft Defender pour le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-134">[Response actions](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/respond-machine-alerts) are only available if the device is enrolled in Microsoft Defender for Endpoint.</span></span>
> * <span data-ttu-id="0dd7f-135">Les appareils qui sont intégrés à Microsoft Defender pour le point de terminaison peuvent afficher plusieurs actions de réponse, en fonction du système d’exploitation et du numéro de version de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-135">Devices that are enrolled in Microsoft Defender for Endpoint may display different numbers of response actions, based on the device's OS and version number.</span></span>

<span data-ttu-id="0dd7f-136">Les actions disponibles sur la page profil d’appareil sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="0dd7f-136">Actions available on the device profile page include:</span></span>

* <span data-ttu-id="0dd7f-137">**Gérer les balises** : met à jour les balises personnalisées que vous avez appliquées à cet appareil.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-137">**Manage tags** - Updates custom tags you have applied to this device.</span></span>
* <span data-ttu-id="0dd7f-138">**Isoler l’appareil** : isole l’appareil du réseau de votre organisation tout en le gardant connecté à Microsoft Defender pour le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-138">**Isolate device** - Isolates the device from your organization's network while keeping it connected to Microsoft Defender for Endpoint.</span></span> <span data-ttu-id="0dd7f-139">Vous pouvez choisir d’autoriser l’exécution d’Outlook, de teams et de Skype entreprise lorsque l’appareil est isolé, à des fins de communication.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-139">You can choose to allow Outlook, Teams, and Skype for Business to run while the device is isolated, for communication purposes.</span></span>
* <span data-ttu-id="0dd7f-140">**Centre de notifications** : afficher l’état des actions soumises.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-140">**Action center** - View the status of submitted actions.</span></span> <span data-ttu-id="0dd7f-141">Disponible uniquement si une autre action a déjà été sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-141">Only available if another action has already been selected.</span></span>
* <span data-ttu-id="0dd7f-142">**Restreindre l’exécution de l’application** : empêche les applications qui ne sont pas signées par Microsoft de s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-142">**Restrict app execution** - Prevents applications that are not signed by Microsoft from running.</span></span>
* <span data-ttu-id="0dd7f-143">**Exécuter l’analyse antivirus** : met à jour les définitions de l’antivirus Windows Defender et exécute immédiatement une analyse antivirus.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-143">**Run antivirus scan** - Updates Windows Defender Antivirus definitions and immediately runs an antivirus scan.</span></span> <span data-ttu-id="0dd7f-144">Choisissez entre analyse rapide ou analyse complète.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-144">Choose between Quick scan or Full scan.</span></span>
* <span data-ttu-id="0dd7f-145">**Recueillir** des informations sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-145">**Collect investigation package** - Gathers information about the device.</span></span> <span data-ttu-id="0dd7f-146">Une fois l’enquête terminée, vous pouvez la télécharger.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-146">When the investigation is completed, you can download it.</span></span>
* <span data-ttu-id="0dd7f-147">**Lancer une session Live Response session** : charge un environnement distant sur le périphérique pour les [examens de sécurité approfondis](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/live-response).</span><span class="sxs-lookup"><span data-stu-id="0dd7f-147">**Initiate Live Response Session** - Loads a remote shell on the device for [in-depth security investigations](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/live-response).</span></span>
* <span data-ttu-id="0dd7f-148">**Lancer une enquête automatisée** : [enquête et corrige automatiquement les menaces](https://docs.microsoft.com/microsoft-365/security/office-365-security/office-365-air).</span><span class="sxs-lookup"><span data-stu-id="0dd7f-148">**Initiate automated investigation** - Automatically [investigates and remediates threats](https://docs.microsoft.com/microsoft-365/security/office-365-security/office-365-air).</span></span> <span data-ttu-id="0dd7f-149">Bien que vous puissiez déclencher manuellement des analyses automatisées à exécuter à partir de cette page, [certaines stratégies d’alerte](https://docs.microsoft.com/microsoft-365/compliance/alert-policies?view=o365-worldwide#default-alert-policies) déclenchent des enquêtes automatiques.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-149">Although you can manually trigger automated investigations to run from this page, [certain alert policies](https://docs.microsoft.com/microsoft-365/compliance/alert-policies?view=o365-worldwide#default-alert-policies) trigger automatic investigations on their own.</span></span>
* <span data-ttu-id="0dd7f-150">**Centre de notifications** : affiche des informations sur les actions de réponse en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-150">**Action center** - Displays information about any response actions that are currently running.</span></span>

## <a name="tabs-section"></a><span data-ttu-id="0dd7f-151">Section Onglets</span><span class="sxs-lookup"><span data-stu-id="0dd7f-151">Tabs section</span></span>

<span data-ttu-id="0dd7f-152">Les onglets de profil d’appareil vous permettent d’afficher une vue d’ensemble des détails de sécurité de l’appareil et des tableaux contenant une liste d’alertes.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-152">The device profile tabs allow you to toggle through an overview of security details about the device, and tables containing a list of alerts.</span></span>

<span data-ttu-id="0dd7f-153">Les appareils inscrits dans Microsoft Defender for Endpoint affichent également des onglets qui comportent une chronologie, une liste de recommandations de sécurité, un inventaire logiciel, une liste de vulnérabilités découvertes et des Kbits/s manquants (mises à jour de sécurité).</span><span class="sxs-lookup"><span data-stu-id="0dd7f-153">Devices enrolled in Microsoft Defender for Endpoint will also display tabs that feature a timeline, a list of security recommendations, a software inventory, a list of discovered vulnerabilities, and missing KBs (security updates).</span></span>

### <a name="overview-tab"></a><span data-ttu-id="0dd7f-154">Onglet vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="0dd7f-154">Overview tab</span></span>

<span data-ttu-id="0dd7f-155">L’onglet par défaut est **vue d’ensemble**.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-155">The default tab is **Overview**.</span></span> <span data-ttu-id="0dd7f-156">Elle fournit un aperçu rapide du plus important de la sécurité de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-156">It provides a quick look at the most important security fact about the device.</span></span>

![Image de l’onglet vue d’ensemble du profil de périphérique](../../media/mtp-device-profile/hybrid-device-tab-overview.png)

<span data-ttu-id="0dd7f-158">Ici, vous pouvez obtenir un aperçu rapide des alertes actives de l’appareil et des utilisateurs actuellement connectés.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-158">Here, you can get a quick look at the device's active alerts, and any currently logged on users.</span></span>

<span data-ttu-id="0dd7f-159">Si le périphérique est intégré à Microsoft Defender pour le point de terminaison, vous verrez également le niveau de risque de l’appareil et les données disponibles sur les évaluations de sécurité.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-159">If the device is enrolled in Microsoft Defender for Endpoint, you will also see the device's risk level and any available data on security assessments.</span></span> <span data-ttu-id="0dd7f-160">Les évaluations de sécurité décrivent le niveau d’exposition de l’appareil, fournissent des recommandations en matière de sécurité et répertorient les logiciels concernés et les vulnérabilités découvertes.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-160">The security assessments describe the device's exposure level, provide security recommendations, and list affected software and discovered vulnerabilities.</span></span>

### <a name="alerts-tab"></a><span data-ttu-id="0dd7f-161">Onglet Alertes</span><span class="sxs-lookup"><span data-stu-id="0dd7f-161">Alerts tab</span></span>

<span data-ttu-id="0dd7f-162">L’onglet **alertes** contient la liste des alertes qui ont été déclenchées sur l’appareil, de Microsoft Defender pour l’identité et de Microsoft Defender pour le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-162">The **Alerts** tab contains a list of alerts that have been raised on the device, from both Microsoft Defender for Identity and Microsoft Defender for Endpoint.</span></span>

![Image de l’onglet Alertes pour le profil d’appareil](../../media/mtp-device-profile/hybrid-device-tab-alerts.png)

<span data-ttu-id="0dd7f-164">Vous pouvez personnaliser le nombre d’éléments affichés, ainsi que les colonnes affichées pour chaque élément.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-164">You can customize the number of items displayed, as well as which columns are displayed for each item.</span></span> <span data-ttu-id="0dd7f-165">Le comportement par défaut consiste à répertorier trente éléments par page.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-165">The default behavior is to list thirty items per page.</span></span>

<span data-ttu-id="0dd7f-166">Les colonnes de cet onglet incluent des informations sur la gravité de la menace qui a déclenché l’alerte, ainsi que sur l’État, l’état de l’enquête et la personne à qui l’alerte a été affectée.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-166">The columns in this tab include information on the severity of the threat that triggered the alert, as well as status, investigation state, and who the alert has been assigned to.</span></span>

<span data-ttu-id="0dd7f-167">La colonne *entités concernées* fait référence au périphérique (entité) dont vous affichez actuellement le profil, ainsi qu’aux autres périphériques de votre réseau qui sont affectés.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-167">The *impacted entities* column refers to the device (entity) whose profile you are currently viewing, plus any other devices in your network that are affected.</span></span>

<span data-ttu-id="0dd7f-168">La sélection d’un élément dans cette liste ouvrira un lanceur contenant encore plus d’informations sur l’alerte sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-168">Selecting an item from this list will open a flyout containing even more information about the selected alert.</span></span>

<span data-ttu-id="0dd7f-169">Cette liste peut être filtrée en fonction de la gravité, de l’État ou de la personne à qui l’alerte a été affectée.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-169">This list can be filtered by severity, status, or who the alert has been assigned to.</span></span>

### <a name="timeline-tab"></a><span data-ttu-id="0dd7f-170">Onglet chronologie</span><span class="sxs-lookup"><span data-stu-id="0dd7f-170">Timeline tab</span></span>

<span data-ttu-id="0dd7f-171">L’onglet **chronologie** inclut un graphique interactif, chronologique, de tous les événements déclenchés sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-171">The **Timeline** tab includes an interactive, chronological chart of all events raised on the device.</span></span> <span data-ttu-id="0dd7f-172">En déplacant la zone mise en surbrillance du graphique vers la gauche ou la droite, vous pouvez afficher les événements sur différentes périodes de temps.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-172">By moving the highlighted area of the chart left or right, you can view events over different periods of time.</span></span> <span data-ttu-id="0dd7f-173">Vous pouvez également choisir une plage de dates personnalisée dans le menu déroulant entre le graphique interactif et la liste des événements.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-173">You can also choose a custom range of dates from the dropdown menu in between the interactive chart and the list of events.</span></span>

<span data-ttu-id="0dd7f-174">Sous le graphique se trouve une liste d’événements pour la plage de dates sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-174">Below the chart is a list of events for the selected range of dates.</span></span>

![Image de l’onglet chronologie pour le profil d’appareil](../../media/mtp-device-profile/hybrid-device-tab-timeline.png)

<span data-ttu-id="0dd7f-176">Le nombre d’éléments affichés et les colonnes de la liste peuvent être personnalisés.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-176">The number of items displayed and the columns on the list can both be customized.</span></span> <span data-ttu-id="0dd7f-177">Les colonnes par défaut répertorient l’heure de l’événement, l’utilisateur actif, le type d’action, les entités (processus) et des informations supplémentaires sur l’événement.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-177">The default columns list the event time, active user, action type, entities (processes), and additional information about the event.</span></span>

<span data-ttu-id="0dd7f-178">La sélection d’un élément dans cette liste ouvrira un menu volant affichant un graphique d’entités d’événements, affichant les processus parents et enfants impliqués dans l’événement.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-178">Selecting an item from this list will open a flyout displaying an Event entities graph, showing the parent and child processes involved in the event.</span></span>

<span data-ttu-id="0dd7f-179">La liste peut être filtrée par type d’événement spécifique ; par exemple, des événements de registre ou des événements Smart Screen.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-179">The list can be filtered by the specific kind of event; for example, Registry events or Smart Screen Events.</span></span>

<span data-ttu-id="0dd7f-180">La liste peut également être exportée dans un fichier CSV, par téléchargement.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-180">The list can also be exported to a CSV file, for download.</span></span> <span data-ttu-id="0dd7f-181">Bien que le fichier ne soit pas limité par le nombre d’événements, la plage de temps maximale que vous pouvez choisir pour l’exportation est de sept jours.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-181">Although the file is not limited by number of events, the maximum time range you can choose to export is seven days.</span></span>

### <a name="security-recommendations-tab"></a><span data-ttu-id="0dd7f-182">Onglet recommandations de sécurité</span><span class="sxs-lookup"><span data-stu-id="0dd7f-182">Security recommendations tab</span></span>

<span data-ttu-id="0dd7f-183">L’onglet **Security Recommendations** répertorie les actions que vous pouvez effectuer pour protéger l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-183">The **Security recommendations** tab lists actions you can take to protect the device.</span></span> <span data-ttu-id="0dd7f-184">La sélection d’un élément sur cette liste ouvre un menu volant dans lequel vous pouvez obtenir des instructions sur l’application de la recommandation.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-184">Selecting an item on this list will open a flyout where you can get instructions on how to apply the recommendation.</span></span>

![Image de l’onglet recommandations de sécurité pour le profil d’appareil](../../media/mtp-device-profile/hybrid-device-tab-security-recs.png)

<span data-ttu-id="0dd7f-186">Comme avec les onglets précédents, le nombre d’éléments affichés par page, ainsi que les colonnes visibles, peuvent être personnalisés.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-186">As with the previous tabs, the number of items displayed per page, as well as which columns are visible, can be customized.</span></span>

<span data-ttu-id="0dd7f-187">L’affichage par défaut inclut des colonnes qui détaillent les faiblesses de sécurité traitées, la menace associée, le composant ou le logiciel associé concerné par la menace, et bien plus encore.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-187">The default view includes columns that detail the security weaknesses addressed, the associated threat, the related component or software affected by the threat, and more.</span></span> <span data-ttu-id="0dd7f-188">Les éléments peuvent être filtrés selon l’état de la recommandation.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-188">Items can be filtered by the recommendation's status.</span></span>

### <a name="software-inventory"></a><span data-ttu-id="0dd7f-189">Inventaire des logiciels</span><span class="sxs-lookup"><span data-stu-id="0dd7f-189">Software inventory</span></span>

<span data-ttu-id="0dd7f-190">L’onglet **inventaire logiciel** répertorie les logiciels installés sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-190">The **Software inventory** tab lists software installed on the device.</span></span>

![Image de l’onglet inventaire logiciel pour le profil d’appareil](../../media/mtp-device-profile/hybrid-device-tab-software-inventory.png)

<span data-ttu-id="0dd7f-192">La vue par défaut affiche le fournisseur de logiciels, le numéro de version installé, le nombre de faiblesses logicielles connues, les informations de menace, le code de produit et les balises.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-192">The default view displays the software vendor, installed version number, number of known software weaknesses, threat insights, product code, and tags.</span></span> <span data-ttu-id="0dd7f-193">Le nombre d’éléments affichés et les colonnes affichées peuvent être personnalisés.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-193">The number of items displayed and which columns are displayed can both be customized.</span></span>

<span data-ttu-id="0dd7f-194">La sélection d’un élément dans cette liste ouvre un lanceur contenant des détails supplémentaires sur le logiciel sélectionné, ainsi que le chemin d’accès et l’horodatage de la dernière fois que le logiciel a été trouvé.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-194">Selecting an item from this list opens a flyout containing more details about the selected software, as well as the path and timestamp for the last time the software was found.</span></span>

<span data-ttu-id="0dd7f-195">Cette liste peut être filtrée par code de produit.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-195">This list can be filtered by product code.</span></span>

### <a name="discovered-vulnerabilities-tab"></a><span data-ttu-id="0dd7f-196">Onglet vulnérabilités découvertes</span><span class="sxs-lookup"><span data-stu-id="0dd7f-196">Discovered vulnerabilities tab</span></span>

<span data-ttu-id="0dd7f-197">L’onglet **vulnérabilités découvertes** répertorie les vulnérabilités et exploits courants (CVE) susceptibles d’affecter l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-197">The **Discovered vulnerabilities** tab lists any Common Vulnerabilities and Exploits (CVEs) that may affect the device.</span></span>

![Image de l’onglet vulnérabilités découvertes pour le profil d’appareil](../../media/mtp-device-profile/hybrid-device-tab-discovered-vulnerabilities.png)

<span data-ttu-id="0dd7f-199">L’affichage par défaut répertorie la gravité de CVE, le score commun de vulnérabilité (CVS), le logiciel associé à CVE, le moment où le CVE a été publié, la date de la dernière mise à jour et les menaces associées à CVE.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-199">The default view lists the severity of the CVE, the Common Vulnerability Score (CVS), the software related to the CVE, when the CVE was published, when the CVE was last updated, and threats associated with the CVE.</span></span>

<span data-ttu-id="0dd7f-200">Comme avec les onglets précédents, le nombre d’éléments affichés et les colonnes visibles peuvent être personnalisés.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-200">As with the previous tabs, the number of items displayed and which columns are visible can be customized.</span></span>

<span data-ttu-id="0dd7f-201">La sélection d’un élément dans cette liste ouvrira un menu volant qui décrit le CVE.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-201">Selecting an item from this list will open a flyout that describes the CVE.</span></span>

### <a name="missing-kbs"></a><span data-ttu-id="0dd7f-202">Ko manquants</span><span class="sxs-lookup"><span data-stu-id="0dd7f-202">Missing KBs</span></span>

<span data-ttu-id="0dd7f-203">L’onglet **Ko manquants** répertorie toutes les mises à jour Microsoft qui n’ont pas encore été appliquées au périphérique.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-203">The **Missing KBs** tab lists any Microsoft Updates that have yet to be applied to the device.</span></span> <span data-ttu-id="0dd7f-204">Le « Ko » en question sont des Articles de la [base de connaissances](https://support.microsoft.com/help/242450/how-to-query-the-microsoft-knowledge-base-by-using-keywords-and-query) qui décrivent ces mises à jour ; par exemple, [KB4551762](https://support.microsoft.com/help/4551762/windows-10-update-kb4551762).</span><span class="sxs-lookup"><span data-stu-id="0dd7f-204">The "KBs" in question are [Knowledge Base articles](https://support.microsoft.com/help/242450/how-to-query-the-microsoft-knowledge-base-by-using-keywords-and-query) which describe these updates; for example, [KB4551762](https://support.microsoft.com/help/4551762/windows-10-update-kb4551762).</span></span>

![Image de l’onglet Ko manquants pour le profil d’appareil](../../media/mtp-device-profile/hybrid-device-tab-missing-kbs.PNG)

<span data-ttu-id="0dd7f-206">L’affichage par défaut répertorie le Bulletin contenant les mises à jour, la version du système d’exploitation, les produits concernés, les CVE traités, le numéro de la base de connaissances et les balises.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-206">The default view lists the bulletin containing the updates, OS version, products affected, CVEs addressed, the KB number, and tags.</span></span>

<span data-ttu-id="0dd7f-207">Le nombre d’éléments affichés par page et les colonnes affichées peuvent être personnalisés.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-207">The number of items displayed per page and which columns are displayed can be customized.</span></span>

<span data-ttu-id="0dd7f-208">La sélection d’un élément ouvre un menu volant qui établit un lien vers la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="0dd7f-208">Selecting an item will open a flyout that links to the update.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0dd7f-209">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0dd7f-209">Related topics</span></span>

* [<span data-ttu-id="0dd7f-210">Vue d’ensemble de Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="0dd7f-210">Microsoft 365 Defender overview</span></span>](microsoft-threat-protection.md)
* [<span data-ttu-id="0dd7f-211">Activer Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="0dd7f-211">Turn on Microsoft 365 Defender</span></span>](mtp-enable.md)
* [<span data-ttu-id="0dd7f-212">Examiner les entités sur les appareils à l’aide de la réponse dynamique</span><span class="sxs-lookup"><span data-stu-id="0dd7f-212">Investigate entities on devices, using live response</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/live-response)
* [<span data-ttu-id="0dd7f-213">Recherche et réponse automatiques dans Office 365</span><span class="sxs-lookup"><span data-stu-id="0dd7f-213">Automated investigation and response (AIR) in Office 365</span></span>](https://docs.microsoft.com/microsoft-365/security/office-365-security/office-365-air)
