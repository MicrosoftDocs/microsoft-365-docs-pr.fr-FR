---
title: Profil d’appareil dans Microsoft 365 de sécurité
description: Afficher les niveaux de risque et d’exposition d’un appareil de votre organisation. Analysez les menaces passées et présentes et protégez l’appareil avec les dernières mises à jour.
keywords: sécurité, programmes malveillants, Microsoft 365, M365, Microsoft 365 Defender, centre de sécurité, Microsoft Defender pour le point de terminaison, Microsoft Defender pour Office 365, Microsoft Defender pour identité, page appareil, profil d’appareil, page ordinateur, profil de l’ordinateur
ms.prod: m365-security
ms.mktglfcycl: deploy
localization_priority: Normal
ms.author: v-maave
author: martyav
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
search.appverid: met150
ms.technology: m365d
ms.openlocfilehash: 47b25ba541264d79216748753e9f41fb7435fc10
ms.sourcegitcommit: 48195345b21b409b175d68acdc25d9f2fc4fc5f1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "53229478"
---
# <a name="device-profile-page"></a><span data-ttu-id="f4cc7-105">Page de profil d’appareil</span><span class="sxs-lookup"><span data-stu-id="f4cc7-105">Device profile page</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="f4cc7-106">Le portail Microsoft 365 de sécurité vous fournit des pages de profil d’appareil, ce qui vous permet d’évaluer rapidement l’état et l’état des appareils sur votre réseau.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-106">The Microsoft 365 security portal provides you with device profile pages, so you can quickly assess the health and status of devices on your network.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f4cc7-107">La page de profil d’appareil peut apparaître légèrement différente, selon que l’appareil est inscrit dans Microsoft Defender pour le point de terminaison, Microsoft Defender pour l’identité ou les deux.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-107">The device profile page may appear slightly different, depending on whether the device is enrolled in Microsoft Defender for Endpoint, Microsoft Defender for Identity, or both.</span></span>

<span data-ttu-id="f4cc7-108">Si l’appareil est inscrit dans Microsoft Defender pour le point de terminaison, vous pouvez également utiliser la page de profil d’appareil pour effectuer certaines tâches de sécurité courantes.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-108">If the device is enrolled in Microsoft Defender for Endpoint, you can also use the device profile page to perform some common security tasks.</span></span>

## <a name="navigating-the-device-profile-page"></a><span data-ttu-id="f4cc7-109">Navigation dans la page de profil d’appareil</span><span class="sxs-lookup"><span data-stu-id="f4cc7-109">Navigating the device profile page</span></span>

<span data-ttu-id="f4cc7-110">La page de profil est décomposée en plusieurs sections larges.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-110">The profile page is broken up into several broad sections.</span></span>

![Image de la page de profil de l’appareil avec (1) zone d’onglet (2) barre latérale et (3) Actions mises en surbrillon en rouge](../../media/mtp-device-profile/hybrid-device-overall.png)

<span data-ttu-id="f4cc7-112">La barre latérale (1) répertorie les détails de base sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-112">The sidebar (1) lists basic details about the device.</span></span>

<span data-ttu-id="f4cc7-113">La zone de contenu principale (2) contient des onglets que vous pouvez faire passer pour afficher différents types d’informations sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-113">The main content area (2) contains tabs that you can toggle through to view different kinds of information about the device.</span></span>

<span data-ttu-id="f4cc7-114">Si l’appareil est inscrit dans Microsoft Defender pour le point de terminaison, vous verrez également une liste d’actions de réponse (3).</span><span class="sxs-lookup"><span data-stu-id="f4cc7-114">If the device is enrolled in Microsoft Defender for Endpoint, you will also see a list of response actions (3).</span></span> <span data-ttu-id="f4cc7-115">Les actions de réponse vous permettent d’effectuer des tâches courantes liées à la sécurité.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-115">Response actions allow you to perform common security-related tasks.</span></span>

## <a name="sidebar"></a><span data-ttu-id="f4cc7-116">Barre latérale</span><span class="sxs-lookup"><span data-stu-id="f4cc7-116">Sidebar</span></span>

<span data-ttu-id="f4cc7-117">À côté de la zone de contenu principale de la page de profil d’appareil se trouve la barre latérale.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-117">Beside the main content area of the device profile page is the sidebar.</span></span>

![Image de l’onglet de barre latérale pour le profil de l’appareil](../../media/mtp-device-profile/azure-atp-only-device-sidebar.png)

<span data-ttu-id="f4cc7-119">La barre latérale répertorie le nom complet et le niveau d’exposition de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-119">The sidebar lists the device's full name and exposure level.</span></span> <span data-ttu-id="f4cc7-120">Il fournit également des informations de base importantes dans les petites sous-sections qui peuvent être ouvertes ou fermées, telles que :</span><span class="sxs-lookup"><span data-stu-id="f4cc7-120">It also provides some important basic information in small subsections which can be toggled open or closed, such as:</span></span>

* <span data-ttu-id="f4cc7-121">**Balises** : tout Microsoft Defender pour point de terminaison, Microsoft Defender pour l’identité ou les balises personnalisées associées à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-121">**Tags** - Any Microsoft Defender for Endpoint, Microsoft Defender for Identity, or custom tags associated with the device.</span></span> <span data-ttu-id="f4cc7-122">Les balises de Microsoft Defender for Identity ne sont pas modifiables.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-122">Tags from Microsoft Defender for Identity are not editable.</span></span>
* <span data-ttu-id="f4cc7-123">**Informations de sécurité** : ouvrir les incidents et les alertes actives.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-123">**Security info** - Open incidents and active alerts.</span></span> <span data-ttu-id="f4cc7-124">Les appareils inscrits dans Microsoft Defender pour le point de terminaison affichent également le niveau d’exposition et le niveau de risque.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-124">Devices enrolled in Microsoft Defender for Endpoint will also display exposure level and risk level.</span></span>

> [!TIP]
> <span data-ttu-id="f4cc7-125">Le niveau d’exposition est lié au niveau de conformité de l’appareil aux recommandations de sécurité, tandis que le niveau de risque est calculé en fonction d’un certain nombre de facteurs, notamment les types et la gravité des alertes actives.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-125">Exposure level relates to how much the device is complying with security recommendations, while risk level is calculated based on a number of factors, including the types and severity of active alerts.</span></span>

* <span data-ttu-id="f4cc7-126">**Détails de l’appareil** : domaine, système d’exploitation, timestamp pour la première fois où l’appareil a été vu, adresses IP, ressources.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-126">**Device details** - Domain, OS, timestamp for when the device was first seen, IP addresses, resources.</span></span> <span data-ttu-id="f4cc7-127">Les appareils inscrits dans Microsoft Defender pour le point de terminaison affichent également l’état d’état d’état.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-127">Devices enrolled in Microsoft Defender for Endpoint also display health state.</span></span> <span data-ttu-id="f4cc7-128">Les appareils inscrits dans Microsoft Defender pour l’identité affichent le nom SAM et un timestamp pour la première création de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-128">Devices enrolled in Microsoft Defender for Identity will display SAM name and a timestamp for when the device was first created.</span></span>
* <span data-ttu-id="f4cc7-129">**Activité réseau** : timestamps pour la première et la dernière fois que l’appareil a été vu sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-129">**Network activity** - Timestamps for the first time and last time the device was seen on the network.</span></span>
* <span data-ttu-id="f4cc7-130">**Données d’annuaire** *(uniquement pour* les appareils inscrits dans Microsoft Defender pour l’identité) : indicateurs [UAC,](/windows/security/identity-protection/user-account-control/user-account-control-overview) [SNS](/windows/win32/ad/service-principal-names)et appartenances aux groupes.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-130">**Directory data** (*only for devices enrolled in Microsoft Defender for Identity*) - [UAC](/windows/security/identity-protection/user-account-control/user-account-control-overview) flags, [SPNs](/windows/win32/ad/service-principal-names), and group memberships.</span></span>

## <a name="response-actions"></a><span data-ttu-id="f4cc7-131">Actions de réponse</span><span class="sxs-lookup"><span data-stu-id="f4cc7-131">Response actions</span></span>

<span data-ttu-id="f4cc7-132">Les actions de réponse offrent un moyen rapide de se défendre contre les menaces et d’analyser ces menaces.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-132">Response actions offer a quick way to defend against and analyze threats.</span></span>

![Image de la barre d’action pour le profil de l’appareil](../../media/mtp-device-profile/hybrid-device-long-action-bar.png)

> [!IMPORTANT]
> * <span data-ttu-id="f4cc7-134">[Les actions de](/windows/security/threat-protection/microsoft-defender-atp/respond-machine-alerts) réponse sont disponibles uniquement si l’appareil est inscrit dans Microsoft Defender pour le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-134">[Response actions](/windows/security/threat-protection/microsoft-defender-atp/respond-machine-alerts) are only available if the device is enrolled in Microsoft Defender for Endpoint.</span></span>
> * <span data-ttu-id="f4cc7-135">Les appareils inscrits dans Microsoft Defender pour le point de terminaison peuvent afficher différents nombres d’actions de réponse, en fonction du système d’exploitation et du numéro de version de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-135">Devices that are enrolled in Microsoft Defender for Endpoint may display different numbers of response actions, based on the device's OS and version number.</span></span>

<span data-ttu-id="f4cc7-136">Les actions disponibles sur la page de profil d’appareil sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="f4cc7-136">Actions available on the device profile page include:</span></span>

* <span data-ttu-id="f4cc7-137">**Gérer les balises** : met à jour les balises personnalisées que vous avez appliquées à cet appareil.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-137">**Manage tags** - Updates custom tags you have applied to this device.</span></span>
* <span data-ttu-id="f4cc7-138">**Isoler l’appareil** : isole l’appareil du réseau de votre organisation tout en conservant sa connexion à Microsoft Defender pour endpoint.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-138">**Isolate device** - Isolates the device from your organization's network while keeping it connected to Microsoft Defender for Endpoint.</span></span> <span data-ttu-id="f4cc7-139">Vous pouvez choisir d’autoriser Outlook, Teams et Skype Entreprise’exécuter pendant que l’appareil est isolé, à des fins de communication.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-139">You can choose to allow Outlook, Teams, and Skype for Business to run while the device is isolated, for communication purposes.</span></span>
* <span data-ttu-id="f4cc7-140">**Centre de actions** : afficher l’état des actions envoyées.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-140">**Action center** - View the status of submitted actions.</span></span> <span data-ttu-id="f4cc7-141">Disponible uniquement si une autre action a déjà été sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-141">Only available if another action has already been selected.</span></span>
* <span data-ttu-id="f4cc7-142">**Restreindre l’exécution de** l’application : empêche l’exécution des applications qui ne sont pas signées par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-142">**Restrict app execution** - Prevents applications that are not signed by Microsoft from running.</span></span>
* <span data-ttu-id="f4cc7-143">**Exécuter une analyse antivirus** : met à jour Antivirus Windows Defender définitions et exécute immédiatement une analyse antivirus.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-143">**Run antivirus scan** - Updates Windows Defender Antivirus definitions and immediately runs an antivirus scan.</span></span> <span data-ttu-id="f4cc7-144">Choisissez entre l’analyse rapide ou l’analyse complète.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-144">Choose between Quick scan or Full scan.</span></span>
* <span data-ttu-id="f4cc7-145">**Collecter un package d’examen** : collecte des informations sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-145">**Collect investigation package** - Gathers information about the device.</span></span> <span data-ttu-id="f4cc7-146">Une fois l’examen terminé, vous pouvez le télécharger.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-146">When the investigation is completed, you can download it.</span></span>
* <span data-ttu-id="f4cc7-147">**Lancer une session De réponse en** direct : charge un shell distant sur l’appareil pour des [enquêtes de sécurité approfondies.](/microsoft-365/security/defender-endpoint/live-response)</span><span class="sxs-lookup"><span data-stu-id="f4cc7-147">**Initiate Live Response Session** - Loads a remote shell on the device for [in-depth security investigations](/microsoft-365/security/defender-endpoint/live-response).</span></span>
* <span data-ttu-id="f4cc7-148">**Lancer une enquête automatisée** : examine et [remédie automatiquement aux menaces.](../office-365-security/office-365-air.md)</span><span class="sxs-lookup"><span data-stu-id="f4cc7-148">**Initiate automated investigation** - Automatically [investigates and remediates threats](../office-365-security/office-365-air.md).</span></span> <span data-ttu-id="f4cc7-149">Bien que vous pouvez déclencher manuellement des enquêtes automatisées à partir de cette [page,](../../compliance/alert-policies.md#default-alert-policies) certaines stratégies d’alerte déclenchent elles-mêmes des enquêtes automatiques.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-149">Although you can manually trigger automated investigations to run from this page, [certain alert policies](../../compliance/alert-policies.md#default-alert-policies) trigger automatic investigations on their own.</span></span>
* <span data-ttu-id="f4cc7-150">**Centre de gestion** des actions : affiche des informations sur les actions de réponse en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-150">**Action center** - Displays information about any response actions that are currently running.</span></span>

## <a name="tabs-section"></a><span data-ttu-id="f4cc7-151">Section Onglets</span><span class="sxs-lookup"><span data-stu-id="f4cc7-151">Tabs section</span></span>

<span data-ttu-id="f4cc7-152">Les onglets de profil d’appareil vous permettent d’utiliser une vue d’ensemble des détails de sécurité sur l’appareil, ainsi que des tableaux contenant une liste d’alertes.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-152">The device profile tabs allow you to toggle through an overview of security details about the device, and tables containing a list of alerts.</span></span>

<span data-ttu-id="f4cc7-153">Les appareils inscrits dans Microsoft Defender pour le point de terminaison affichent également des onglets qui présentent une chronologie, une liste de recommandations de sécurité, un inventaire logiciel, une liste des vulnérabilités découvertes et des ko manquants (mises à jour de sécurité).</span><span class="sxs-lookup"><span data-stu-id="f4cc7-153">Devices enrolled in Microsoft Defender for Endpoint will also display tabs that feature a timeline, a list of security recommendations, a software inventory, a list of discovered vulnerabilities, and missing KBs (security updates).</span></span>

### <a name="overview-tab"></a><span data-ttu-id="f4cc7-154">Onglet Overview</span><span class="sxs-lookup"><span data-stu-id="f4cc7-154">Overview tab</span></span>

<span data-ttu-id="f4cc7-155">L’onglet par défaut est **Vue d’ensemble.**</span><span class="sxs-lookup"><span data-stu-id="f4cc7-155">The default tab is **Overview**.</span></span> <span data-ttu-id="f4cc7-156">Il fournit un aperçu rapide des faits de sécurité les plus importants concernant l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-156">It provides a quick look at the most important security fact about the device.</span></span>

![Image de l’onglet Vue d’ensemble pour le profil d’appareil](../../media/mtp-device-profile/hybrid-device-tab-overview.png)

<span data-ttu-id="f4cc7-158">Ici, vous pouvez obtenir un aperçu rapide des alertes actives de l’appareil et de tous les utilisateurs actuellement connectés.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-158">Here, you can get a quick look at the device's active alerts, and any currently logged on users.</span></span>

<span data-ttu-id="f4cc7-159">Si l’appareil est inscrit dans Microsoft Defender pour le point de terminaison, vous verrez également le niveau de risque de l’appareil et toutes les données disponibles sur les évaluations de sécurité.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-159">If the device is enrolled in Microsoft Defender for Endpoint, you will also see the device's risk level and any available data on security assessments.</span></span> <span data-ttu-id="f4cc7-160">Les évaluations de sécurité décrivent le niveau d’exposition de l’appareil, fournissent des recommandations de sécurité et indiquent les logiciels concernés et les vulnérabilités découvertes.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-160">The security assessments describe the device's exposure level, provide security recommendations, and list affected software and discovered vulnerabilities.</span></span>

### <a name="alerts-tab"></a><span data-ttu-id="f4cc7-161">Onglet Alertes</span><span class="sxs-lookup"><span data-stu-id="f4cc7-161">Alerts tab</span></span>

<span data-ttu-id="f4cc7-162">**L’onglet Alertes** contient une liste d’alertes qui ont été élevées sur l’appareil, à partir de Microsoft Defender pour l’identité et De Microsoft Defender pour le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-162">The **Alerts** tab contains a list of alerts that have been raised on the device, from both Microsoft Defender for Identity and Microsoft Defender for Endpoint.</span></span>

![Image de l’onglet Alertes pour le profil d’appareil](../../media/mtp-device-profile/hybrid-device-tab-alerts.png)

<span data-ttu-id="f4cc7-164">Vous pouvez personnaliser le nombre d’éléments affichés, ainsi que les colonnes affichées pour chaque élément.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-164">You can customize the number of items displayed, as well as which columns are displayed for each item.</span></span> <span data-ttu-id="f4cc7-165">Le comportement par défaut consiste à lister trente éléments par page.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-165">The default behavior is to list thirty items per page.</span></span>

<span data-ttu-id="f4cc7-166">Les colonnes de cet onglet incluent des informations sur la gravité de la menace ayant déclenché l’alerte, ainsi que sur l’état, l’état de l’enquête et la personne à qui l’alerte a été affectée.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-166">The columns in this tab include information on the severity of the threat that triggered the alert, as well as status, investigation state, and who the alert has been assigned to.</span></span>

<span data-ttu-id="f4cc7-167">La *colonne Entités* concernées fait référence à l’appareil (entité) dont vous affichez actuellement le profil, ainsi qu’à tous les autres appareils de votre réseau concernés.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-167">The *impacted entities* column refers to the device (entity) whose profile you are currently viewing, plus any other devices in your network that are affected.</span></span>

<span data-ttu-id="f4cc7-168">La sélection d’un élément dans cette liste ouvre un volant contenant encore plus d’informations sur l’alerte sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-168">Selecting an item from this list will open a flyout containing even more information about the selected alert.</span></span>

<span data-ttu-id="f4cc7-169">Cette liste peut être filtrée par gravité, état ou à qui l’alerte a été affectée.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-169">This list can be filtered by severity, status, or who the alert has been assigned to.</span></span>

### <a name="timeline-tab"></a><span data-ttu-id="f4cc7-170">Onglet Chronologie</span><span class="sxs-lookup"><span data-stu-id="f4cc7-170">Timeline tab</span></span>

<span data-ttu-id="f4cc7-171">**L’onglet** Chronologie inclut un graphique chronologique interactif de tous les événements qui se sont produit sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-171">The **Timeline** tab includes an interactive, chronological chart of all events raised on the device.</span></span> <span data-ttu-id="f4cc7-172">En déplaçant la zone en surbrillable du graphique à gauche ou à droite, vous pouvez afficher les événements sur différentes périodes de temps.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-172">By moving the highlighted area of the chart left or right, you can view events over different periods of time.</span></span> <span data-ttu-id="f4cc7-173">Vous pouvez également choisir une plage personnalisée de dates dans le menu déroulant entre le graphique interactif et la liste des événements.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-173">You can also choose a custom range of dates from the dropdown menu in between the interactive chart and the list of events.</span></span>

<span data-ttu-id="f4cc7-174">Sous le graphique se trouve une liste d’événements pour la plage de dates sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-174">Below the chart is a list of events for the selected range of dates.</span></span>

![Image de l’onglet Chronologie pour le profil d’appareil](../../media/mtp-device-profile/hybrid-device-tab-timeline.png)

<span data-ttu-id="f4cc7-176">Le nombre d’éléments affichés et les colonnes de la liste peuvent être personnalisés.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-176">The number of items displayed and the columns on the list can both be customized.</span></span> <span data-ttu-id="f4cc7-177">Les colonnes par défaut listent l’heure de l’événement, l’utilisateur actif, le type d’action, les entités (processus) et des informations supplémentaires sur l’événement.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-177">The default columns list the event time, active user, action type, entities (processes), and additional information about the event.</span></span>

<span data-ttu-id="f4cc7-178">La sélection d’un élément dans cette liste ouvre un écran volant affichant un graphique des entités Event, montrant les processus parent et enfant impliqués dans l’événement.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-178">Selecting an item from this list will open a flyout displaying an Event entities graph, showing the parent and child processes involved in the event.</span></span>

<span data-ttu-id="f4cc7-179">La liste peut être filtrée par type d’événement spécifique ; par exemple, les événements du Registre ou les événements d’écran intelligent.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-179">The list can be filtered by the specific kind of event; for example, Registry events or Smart Screen Events.</span></span>

<span data-ttu-id="f4cc7-180">La liste peut également être exportée vers un fichier CSV, en téléchargement.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-180">The list can also be exported to a CSV file, for download.</span></span> <span data-ttu-id="f4cc7-181">Bien que le fichier ne soit pas limité par le nombre d’événements, la période maximale que vous pouvez choisir d’exporter est de sept jours.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-181">Although the file is not limited by number of events, the maximum time range you can choose to export is seven days.</span></span>

### <a name="security-recommendations-tab"></a><span data-ttu-id="f4cc7-182">Onglet Recommandations de sécurité</span><span class="sxs-lookup"><span data-stu-id="f4cc7-182">Security recommendations tab</span></span>

<span data-ttu-id="f4cc7-183">**L’onglet Recommandations en matière** de sécurité répertorie les actions que vous pouvez prendre pour protéger l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-183">The **Security recommendations** tab lists actions you can take to protect the device.</span></span> <span data-ttu-id="f4cc7-184">La sélection d’un élément dans cette liste ouvre un volant dans lequel vous pouvez obtenir des instructions sur la façon d’appliquer la recommandation.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-184">Selecting an item on this list will open a flyout where you can get instructions on how to apply the recommendation.</span></span>

![Image de l’onglet Recommandations de sécurité pour le profil d’appareil](../../media/mtp-device-profile/hybrid-device-tab-security-recs.png)

<span data-ttu-id="f4cc7-186">Comme avec les onglets précédents, le nombre d’éléments affichés par page, ainsi que les colonnes visibles, peuvent être personnalisés.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-186">As with the previous tabs, the number of items displayed per page, as well as which columns are visible, can be customized.</span></span>

<span data-ttu-id="f4cc7-187">L’affichage par défaut inclut des colonnes qui détaillent les faiblesses de sécurité traitées, la menace associée, le composant ou le logiciel associé affecté par la menace, et bien plus encore.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-187">The default view includes columns that detail the security weaknesses addressed, the associated threat, the related component or software affected by the threat, and more.</span></span> <span data-ttu-id="f4cc7-188">Les éléments peuvent être filtrés selon l’état de la recommandation.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-188">Items can be filtered by the recommendation's status.</span></span>

### <a name="software-inventory"></a><span data-ttu-id="f4cc7-189">Inventaire des logiciels</span><span class="sxs-lookup"><span data-stu-id="f4cc7-189">Software inventory</span></span>

<span data-ttu-id="f4cc7-190">**L’onglet Inventaire** logiciel répertorie les logiciels installés sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-190">The **Software inventory** tab lists software installed on the device.</span></span>

![Image de l’onglet Inventaire logiciel pour le profil d’appareil](../../media/mtp-device-profile/hybrid-device-tab-software-inventory.png)

<span data-ttu-id="f4cc7-192">L’affichage par défaut affiche le fournisseur de logiciels, le numéro de version installé, le nombre de faiblesses logicielles connues, les informations sur les menaces, le code du produit et les balises.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-192">The default view displays the software vendor, installed version number, number of known software weaknesses, threat insights, product code, and tags.</span></span> <span data-ttu-id="f4cc7-193">Le nombre d’éléments affichés et les colonnes affichées peuvent être personnalisés.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-193">The number of items displayed and which columns are displayed can both be customized.</span></span>

<span data-ttu-id="f4cc7-194">La sélection d’un élément dans cette liste ouvre un volant contenant plus de détails sur le logiciel sélectionné, ainsi que le chemin d’accès et l’timestamp de la dernière fois que le logiciel a été trouvé.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-194">Selecting an item from this list opens a flyout containing more details about the selected software, as well as the path and timestamp for the last time the software was found.</span></span>

<span data-ttu-id="f4cc7-195">Cette liste peut être filtrée par code produit.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-195">This list can be filtered by product code.</span></span>

### <a name="discovered-vulnerabilities-tab"></a><span data-ttu-id="f4cc7-196">Onglet Vulnérabilités découvertes</span><span class="sxs-lookup"><span data-stu-id="f4cc7-196">Discovered vulnerabilities tab</span></span>

<span data-ttu-id="f4cc7-197">**L’onglet Vulnérabilités** découvertes répertorie les vulnérabilités courantes et les exploits (CVE) qui peuvent affecter l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-197">The **Discovered vulnerabilities** tab lists any Common Vulnerabilities and Exploits (CVEs) that may affect the device.</span></span>

![Image de l’onglet Vulnérabilités découvertes pour le profil d’appareil](../../media/mtp-device-profile/hybrid-device-tab-discovered-vulnerabilities.png)

<span data-ttu-id="f4cc7-199">L’affichage par défaut répertorie la gravité de la CVE, le score de vulnérabilité commun (CVS), le logiciel associé à la CVE, lors de la publication de la CVE, la dernière mise à jour de la CVE et les menaces associées à la CVE.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-199">The default view lists the severity of the CVE, the Common Vulnerability Score (CVS), the software related to the CVE, when the CVE was published, when the CVE was last updated, and threats associated with the CVE.</span></span>

<span data-ttu-id="f4cc7-200">Comme avec les onglets précédents, le nombre d’éléments affichés et les colonnes visibles peuvent être personnalisés.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-200">As with the previous tabs, the number of items displayed and which columns are visible can be customized.</span></span>

<span data-ttu-id="f4cc7-201">La sélection d’un élément dans cette liste ouvre un volant qui décrit la CVE.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-201">Selecting an item from this list will open a flyout that describes the CVE.</span></span>

### <a name="missing-kbs"></a><span data-ttu-id="f4cc7-202">Ko manquants</span><span class="sxs-lookup"><span data-stu-id="f4cc7-202">Missing KBs</span></span>

<span data-ttu-id="f4cc7-203">**L’onglet Ko manquant répertorie** toutes les mises à jour Microsoft qui n’ont pas encore été appliquées à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-203">The **Missing KBs** tab lists any Microsoft Updates that have yet to be applied to the device.</span></span> <span data-ttu-id="f4cc7-204">Les « bases de connaissances » en question sont des articles de [la Base](https://support.microsoft.com/help/242450/how-to-query-the-microsoft-knowledge-base-by-using-keywords-and-query) de connaissances qui décrivent ces mises à jour . par exemple, [KB4551762](https://support.microsoft.com/help/4551762/windows-10-update-kb4551762).</span><span class="sxs-lookup"><span data-stu-id="f4cc7-204">The "KBs" in question are [Knowledge Base articles](https://support.microsoft.com/help/242450/how-to-query-the-microsoft-knowledge-base-by-using-keywords-and-query) which describe these updates; for example, [KB4551762](https://support.microsoft.com/help/4551762/windows-10-update-kb4551762).</span></span>

![Image de l’onglet kbs manquant pour le profil d’appareil](../../media/mtp-device-profile/hybrid-device-tab-missing-kbs.PNG)

<span data-ttu-id="f4cc7-206">L’affichage par défaut répertorie le bulletin contenant les mises à jour, la version du système d’exploitation, les produits affectés, les CV traités, le numéro de la base de données et les balises.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-206">The default view lists the bulletin containing the updates, OS version, products affected, CVEs addressed, the KB number, and tags.</span></span>

<span data-ttu-id="f4cc7-207">Le nombre d’éléments affichés par page et les colonnes affichées peuvent être personnalisés.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-207">The number of items displayed per page and which columns are displayed can be customized.</span></span>

<span data-ttu-id="f4cc7-208">La sélection d’un élément ouvre un volant qui relie la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="f4cc7-208">Selecting an item will open a flyout that links to the update.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f4cc7-209">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f4cc7-209">Related topics</span></span>

* [<span data-ttu-id="f4cc7-210">Microsoft 365 Defender vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="f4cc7-210">Microsoft 365 Defender overview</span></span>](microsoft-365-defender.md)
* [<span data-ttu-id="f4cc7-211">Activer Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="f4cc7-211">Turn on Microsoft 365 Defender</span></span>](m365d-enable.md)
* [<span data-ttu-id="f4cc7-212">Examiner les entités sur les appareils, à l’aide d’une réponse en direct</span><span class="sxs-lookup"><span data-stu-id="f4cc7-212">Investigate entities on devices, using live response</span></span>](../defender-endpoint/live-response.md)
* [<span data-ttu-id="f4cc7-213">Examen et réponse automatisés (AIR) dans Office 365</span><span class="sxs-lookup"><span data-stu-id="f4cc7-213">Automated investigation and response (AIR) in Office 365</span></span>](../office-365-security/office-365-air.md)
