---
title: Examiner les appareils dans la liste Defender pour les appareils de point de terminaison
description: Examinez les appareils concernés en consultant les alertes, les informations de connexion réseau, l'ajout de balises et de groupes d'appareils et la vérification de l'état du service.
keywords: devices, tags, groups, endpoint, alerts queue, alerts, device name, domain, last seen, internal IP, active alerts, threat category, filter, sort, review alerts, network, connection, type, password stealer, ransomware, exploit, threat, low severity, service health
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: macapara
author: mjcaparas
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- m365-security-compliance
- m365initiative-defender-endpoint
ms.topic: article
ms.technology: mde
ms.openlocfilehash: c1e572910ad311daba18a8b0f5eeb546ffe36956
ms.sourcegitcommit: a8d8cee7df535a150985d6165afdfddfdf21f622
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2021
ms.locfileid: "51929108"
---
# <a name="investigate-devices-in-the-microsoft-defender-for-endpoint-devices-list"></a><span data-ttu-id="37078-104">Examiner les appareils de la liste Microsoft Defender pour les appareils de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="37078-104">Investigate devices in the Microsoft Defender for Endpoint Devices list</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="37078-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="37078-105">**Applies to:**</span></span>
- [<span data-ttu-id="37078-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="37078-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="37078-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="37078-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

><span data-ttu-id="37078-108">Vous souhaitez faire l'expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="37078-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="37078-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="37078-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-investigatemachines-abovefoldlink)

<span data-ttu-id="37078-110">Examinez les détails d'une alerte sur un appareil spécifique pour identifier d'autres comportements ou événements qui peuvent être liés à l'alerte ou à l'étendue potentielle de la violation.</span><span class="sxs-lookup"><span data-stu-id="37078-110">Investigate the details of an alert raised on a specific device to identify other behaviors or events that might be related to the alert or the potential scope of the breach.</span></span>

> [!NOTE]
> <span data-ttu-id="37078-111">Dans le cadre du processus d'examen ou de réponse, vous pouvez collecter un package d'enquête à partir d'un appareil.</span><span class="sxs-lookup"><span data-stu-id="37078-111">As part of the investigation or response process, you can collect an investigation package from a device.</span></span> <span data-ttu-id="37078-112">Voici comment : Collecter un [package d'enquête à partir d'appareils.](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/respond-machine-alerts#collect-investigation-package-from-devices)</span><span class="sxs-lookup"><span data-stu-id="37078-112">Here's how: [Collect investigation package from devices](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/respond-machine-alerts#collect-investigation-package-from-devices).</span></span>

<span data-ttu-id="37078-113">Vous pouvez cliquer sur les appareils concernés chaque fois que vous les voyez dans le portail pour ouvrir un rapport détaillé sur cet appareil.</span><span class="sxs-lookup"><span data-stu-id="37078-113">You can click on affected devices whenever you see them in the portal to open a detailed report about that device.</span></span> <span data-ttu-id="37078-114">Les appareils concernés sont identifiés dans les zones suivantes :</span><span class="sxs-lookup"><span data-stu-id="37078-114">Affected devices are identified in the following areas:</span></span>

- [<span data-ttu-id="37078-115">Liste des appareils</span><span class="sxs-lookup"><span data-stu-id="37078-115">Devices list</span></span>](investigate-machines.md)
- [<span data-ttu-id="37078-116">File d’attente des alertes</span><span class="sxs-lookup"><span data-stu-id="37078-116">Alerts queue</span></span>](alerts-queue.md)
- [<span data-ttu-id="37078-117">Tableau de bord des opérations de sécurité</span><span class="sxs-lookup"><span data-stu-id="37078-117">Security operations dashboard</span></span>](security-operations-dashboard.md)
- <span data-ttu-id="37078-118">Toute alerte individuelle</span><span class="sxs-lookup"><span data-stu-id="37078-118">Any individual alert</span></span>
- <span data-ttu-id="37078-119">Affichage des détails d'un fichier individuel</span><span class="sxs-lookup"><span data-stu-id="37078-119">Any individual file details view</span></span>
- <span data-ttu-id="37078-120">N'importe quelle adresse IP ou vue des détails de domaine</span><span class="sxs-lookup"><span data-stu-id="37078-120">Any IP address or domain details view</span></span>

<span data-ttu-id="37078-121">Lorsque vous examinez un appareil spécifique, vous voyez :</span><span class="sxs-lookup"><span data-stu-id="37078-121">When you investigate a specific device, you'll see:</span></span>

- <span data-ttu-id="37078-122">Détails de l'appareil</span><span class="sxs-lookup"><span data-stu-id="37078-122">Device details</span></span>
- <span data-ttu-id="37078-123">Actions de réponse</span><span class="sxs-lookup"><span data-stu-id="37078-123">Response actions</span></span>
- <span data-ttu-id="37078-124">Onglets (vue d'ensemble, alertes, chronologie, recommandations en matière de sécurité, inventaire logiciel, vulnérabilités découvertes, ko manquants)</span><span class="sxs-lookup"><span data-stu-id="37078-124">Tabs (overview, alerts, timeline, security recommendations, software inventory, discovered vulnerabilities, missing KBs)</span></span>
- <span data-ttu-id="37078-125">Cartes (alertes actives, utilisateurs connectés, évaluation de la sécurité)</span><span class="sxs-lookup"><span data-stu-id="37078-125">Cards (active alerts, logged on users, security assessment)</span></span>

![Image de l'affichage de l'appareil](images/specific-device.png)

## <a name="device-details"></a><span data-ttu-id="37078-127">Détails de l'appareil</span><span class="sxs-lookup"><span data-stu-id="37078-127">Device details</span></span>

<span data-ttu-id="37078-128">La section Détails de l'appareil fournit des informations telles que le domaine, le système d'exploitation et l'état d'état de l'appareil.</span><span class="sxs-lookup"><span data-stu-id="37078-128">The device details section provides information such as the domain, OS, and health state of the device.</span></span> <span data-ttu-id="37078-129">Si un package d'enquête est disponible sur l'appareil, vous verrez un lien qui vous permet de télécharger le package.</span><span class="sxs-lookup"><span data-stu-id="37078-129">If there's an investigation package available on the device, you'll see a link that allows you to download the package.</span></span>

## <a name="response-actions"></a><span data-ttu-id="37078-130">Actions de réponse</span><span class="sxs-lookup"><span data-stu-id="37078-130">Response actions</span></span>

<span data-ttu-id="37078-131">Les actions de réponse s'exécutent le long de la partie supérieure d'une page d'appareil spécifique et incluent :</span><span class="sxs-lookup"><span data-stu-id="37078-131">Response actions run along the top of a specific device page and include:</span></span>

- <span data-ttu-id="37078-132">Gérer des balises</span><span class="sxs-lookup"><span data-stu-id="37078-132">Manage tags</span></span>
- <span data-ttu-id="37078-133">Isoler l'appareil</span><span class="sxs-lookup"><span data-stu-id="37078-133">Isolate device</span></span>
- <span data-ttu-id="37078-134">Restreindre l’exécution des applications</span><span class="sxs-lookup"><span data-stu-id="37078-134">Restrict app execution</span></span>
- <span data-ttu-id="37078-135">Exécuter une analyse antivirus</span><span class="sxs-lookup"><span data-stu-id="37078-135">Run antivirus scan</span></span>
- <span data-ttu-id="37078-136">Collecter un package d’examen</span><span class="sxs-lookup"><span data-stu-id="37078-136">Collect investigation package</span></span>
- <span data-ttu-id="37078-137">Lancer une session de réponse en direct</span><span class="sxs-lookup"><span data-stu-id="37078-137">Initiate Live Response Session</span></span>
- <span data-ttu-id="37078-138">Lancer une enquête automatisée</span><span class="sxs-lookup"><span data-stu-id="37078-138">Initiate automated investigation</span></span>
- <span data-ttu-id="37078-139">Consulter un spécialiste des menaces</span><span class="sxs-lookup"><span data-stu-id="37078-139">Consult a threat expert</span></span>
- <span data-ttu-id="37078-140">Centre de notifications</span><span class="sxs-lookup"><span data-stu-id="37078-140">Action center</span></span>

<span data-ttu-id="37078-141">Vous pouvez prendre des mesures de réponse dans le centre de réponse, dans une page d'appareil spécifique ou dans une page de fichier spécifique.</span><span class="sxs-lookup"><span data-stu-id="37078-141">You can take response actions in the Action center, in a specific device page, or in a specific file page.</span></span>

<span data-ttu-id="37078-142">Pour plus d'informations sur la façon d'agir sur un appareil, voir [Prendre une action de réponse sur un appareil.](respond-machine-alerts.md)</span><span class="sxs-lookup"><span data-stu-id="37078-142">For more information on how to take action on a device, see [Take response action on a device](respond-machine-alerts.md).</span></span>

<span data-ttu-id="37078-143">Pour plus d'informations, voir [Examiner les entités utilisateur.](investigate-user.md)</span><span class="sxs-lookup"><span data-stu-id="37078-143">For more information, see [Investigate user entities](investigate-user.md).</span></span>

## <a name="tabs"></a><span data-ttu-id="37078-144">Onglets</span><span class="sxs-lookup"><span data-stu-id="37078-144">Tabs</span></span>

<span data-ttu-id="37078-145">Les onglets fournissent des informations pertinentes sur la sécurité et la prévention des menaces relatives à l'appareil.</span><span class="sxs-lookup"><span data-stu-id="37078-145">The tabs provide relevant security and threat prevention information related to the device.</span></span> <span data-ttu-id="37078-146">Dans chaque onglet, vous pouvez personnaliser les  colonnes affichées en sélectionnant Personnaliser les colonnes dans la barre au-dessus des en-têtes de colonne.</span><span class="sxs-lookup"><span data-stu-id="37078-146">In each tab, you can customize the columns that are shown by selecting **Customize columns** from the bar above the column headers.</span></span>

### <a name="overview"></a><span data-ttu-id="37078-147">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="37078-147">Overview</span></span>
<span data-ttu-id="37078-148">**L'onglet** Vue d'ensemble affiche les [cartes](#cards) pour les alertes actives, les utilisateurs connectés et l'évaluation de la sécurité.</span><span class="sxs-lookup"><span data-stu-id="37078-148">The **Overview** tab displays the [cards](#cards) for active alerts, logged on users, and security assessment.</span></span>

![Image de l'onglet Vue d'ensemble sur la page de l'appareil](images/overview-device.png)

### <a name="alerts"></a><span data-ttu-id="37078-150">Alertes</span><span class="sxs-lookup"><span data-stu-id="37078-150">Alerts</span></span>

<span data-ttu-id="37078-151">**L'onglet Alertes** fournit une liste des alertes associées à l'appareil.</span><span class="sxs-lookup"><span data-stu-id="37078-151">The **Alerts** tab provides a list of alerts that are associated with the device.</span></span> <span data-ttu-id="37078-152">Cette liste est une version filtrée de la file d'attente des [alertes](alerts-queue.md)et affiche une brève description de l'alerte, de la gravité (élevée, moyenne, faible, informationnelle), de l'état dans la file d'attente (nouveau, en cours, résolu), de la classification (non définie, false alerte, alerte vraie), de l'état d'investigation, de la catégorie d'alerte, de la personne qui résout l'alerte et de la dernière activité.</span><span class="sxs-lookup"><span data-stu-id="37078-152">This list is a filtered version of the [Alerts queue](alerts-queue.md), and shows a short description of the alert, severity (high, medium, low, informational), status in the queue (new, in progress, resolved), classification (not set, false alert, true alert), investigation state, category of alert, who is addressing the alert, and last activity.</span></span> <span data-ttu-id="37078-153">Vous pouvez également filtrer les alertes.</span><span class="sxs-lookup"><span data-stu-id="37078-153">You can also filter the alerts.</span></span>

![Image des alertes liées à l'appareil](images/alerts-device.png)

<span data-ttu-id="37078-155">Lorsque l'icône de cercle à gauche d'une alerte est sélectionnée, un volant s'affiche.</span><span class="sxs-lookup"><span data-stu-id="37078-155">When the circle icon to the left of an alert is selected, a fly-out appears.</span></span> <span data-ttu-id="37078-156">À partir de ce panneau, vous pouvez gérer l'alerte et afficher plus de détails, tels que le numéro d'incident et les appareils associés.</span><span class="sxs-lookup"><span data-stu-id="37078-156">From this panel you can manage the alert and view more details such as incident number and related devices.</span></span> <span data-ttu-id="37078-157">Plusieurs alertes peuvent être sélectionnées à la fois.</span><span class="sxs-lookup"><span data-stu-id="37078-157">Multiple alerts can be selected at a time.</span></span>

<span data-ttu-id="37078-158">Pour afficher une vue de page complète d'une alerte, y compris le graphique d'incident et l'arborescence de processus, sélectionnez le titre de l'alerte.</span><span class="sxs-lookup"><span data-stu-id="37078-158">To see a full page view of an alert including incident graph and process tree, select the title of the alert.</span></span>

### <a name="timeline"></a><span data-ttu-id="37078-159">Chronologie</span><span class="sxs-lookup"><span data-stu-id="37078-159">Timeline</span></span>

<span data-ttu-id="37078-160">**L'onglet** Chronologie fournit une vue chronologique des événements et des alertes associées qui ont été observés sur l'appareil.</span><span class="sxs-lookup"><span data-stu-id="37078-160">The **Timeline** tab provides a chronological view of the events and associated alerts that have been observed on the device.</span></span> <span data-ttu-id="37078-161">Cela peut vous aider à corréler tous les événements, fichiers et adresses IP par rapport à l'appareil.</span><span class="sxs-lookup"><span data-stu-id="37078-161">This can help you correlate any events, files, and IP addresses in relation to the device.</span></span>

<span data-ttu-id="37078-162">La chronologie vous permet également d'aller de manière sélective dans les événements qui se sont produits au cours d'une période donnée.</span><span class="sxs-lookup"><span data-stu-id="37078-162">The timeline also enables you to selectively drill down into events that occurred within a given time period.</span></span> <span data-ttu-id="37078-163">Vous pouvez afficher la séquence temporelle des événements qui se sont produits sur un appareil pendant une période sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="37078-163">You can view the temporal sequence of events that occurred on a device over a selected time period.</span></span> <span data-ttu-id="37078-164">Pour mieux contrôler votre affichage, vous pouvez filtrer par groupes d'événements ou personnaliser les colonnes.</span><span class="sxs-lookup"><span data-stu-id="37078-164">To further control your view, you can filter by event groups or customize the columns.</span></span>

>[!NOTE]
> <span data-ttu-id="37078-165">Pour afficher les événements de pare-feu, vous devez activer la stratégie d'audit, voir Connexion à la plateforme de filtrage [d'audit.](https://docs.microsoft.com/windows/security/threat-protection/auditing/audit-filtering-platform-connection)</span><span class="sxs-lookup"><span data-stu-id="37078-165">For firewall events to be displayed, you'll need to enable the audit policy, see [Audit Filtering Platform connection](https://docs.microsoft.com/windows/security/threat-protection/auditing/audit-filtering-platform-connection).</span></span>
><span data-ttu-id="37078-166">Le pare-feu couvre les événements suivants</span><span class="sxs-lookup"><span data-stu-id="37078-166">Firewall covers the following events</span></span>
>
>- <span data-ttu-id="37078-167">[5025](https://docs.microsoft.com/windows/security/threat-protection/auditing/event-5025) - Service de pare-feu arrêté</span><span class="sxs-lookup"><span data-stu-id="37078-167">[5025](https://docs.microsoft.com/windows/security/threat-protection/auditing/event-5025) - firewall service stopped</span></span>
>- <span data-ttu-id="37078-168">[5031](https://docs.microsoft.com/windows/security/threat-protection/auditing/event-5031) : application bloquée pour accepter les connexions entrantes sur le réseau</span><span class="sxs-lookup"><span data-stu-id="37078-168">[5031](https://docs.microsoft.com/windows/security/threat-protection/auditing/event-5031) - application blocked from accepting incoming connections on the network</span></span>
>- <span data-ttu-id="37078-169">[5157](https://docs.microsoft.com/windows/security/threat-protection/auditing/event-5157) : connexion bloquée</span><span class="sxs-lookup"><span data-stu-id="37078-169">[5157](https://docs.microsoft.com/windows/security/threat-protection/auditing/event-5157) - blocked connection</span></span>

![Image de la chronologie de l'appareil avec des événements](images/timeline-device.png)

<span data-ttu-id="37078-171">Voici quelques-unes des fonctionnalités :</span><span class="sxs-lookup"><span data-stu-id="37078-171">Some of the functionality includes:</span></span>

- <span data-ttu-id="37078-172">Rechercher des événements spécifiques</span><span class="sxs-lookup"><span data-stu-id="37078-172">Search for specific events</span></span>
  - <span data-ttu-id="37078-173">Utilisez la barre de recherche pour rechercher des événements de chronologie spécifiques.</span><span class="sxs-lookup"><span data-stu-id="37078-173">Use the search bar to look for specific timeline events.</span></span>
- <span data-ttu-id="37078-174">Filtrer les événements à partir d'une date spécifique</span><span class="sxs-lookup"><span data-stu-id="37078-174">Filter events from a specific date</span></span>
  - <span data-ttu-id="37078-175">Sélectionnez l'icône de calendrier dans le coin supérieur gauche du tableau pour afficher les événements du dernier jour, semaine, 30 jours ou plage personnalisée.</span><span class="sxs-lookup"><span data-stu-id="37078-175">Select the calendar icon in the upper left of the table to display events in the past day, week, 30 days, or custom range.</span></span> <span data-ttu-id="37078-176">Par défaut, la chronologie de l'appareil est définie pour afficher les événements des 30 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="37078-176">By default, the device timeline is set to display the events from the past 30 days.</span></span>
  - <span data-ttu-id="37078-177">Utilisez la chronologie pour passer à un moment spécifique dans le temps en mettant en surbrillance la section.</span><span class="sxs-lookup"><span data-stu-id="37078-177">Use the timeline to jump to a specific moment in time by highlighting the section.</span></span> <span data-ttu-id="37078-178">Les flèches de la chronologie recherchent des investigations automatisées</span><span class="sxs-lookup"><span data-stu-id="37078-178">The arrows on the timeline pinpoint automated investigations</span></span>
- <span data-ttu-id="37078-179">Exporter des événements de chronologie détaillés de l'appareil</span><span class="sxs-lookup"><span data-stu-id="37078-179">Export detailed device timeline events</span></span>
  - <span data-ttu-id="37078-180">Exportez la chronologie de l'appareil pour la date actuelle ou une plage de dates spécifiée jusqu'à sept jours.</span><span class="sxs-lookup"><span data-stu-id="37078-180">Export the device timeline for the current date or a specified date range up to seven days.</span></span>

<span data-ttu-id="37078-181">Des informations supplémentaires sur certains événements sont fournies dans la section **Informations supplémentaires.**</span><span class="sxs-lookup"><span data-stu-id="37078-181">More details about certain events are provided in the **Additional information** section.</span></span> <span data-ttu-id="37078-182">Ces détails varient en fonction du type d'événement, par exemple :</span><span class="sxs-lookup"><span data-stu-id="37078-182">These details vary depending on the type of event, for example:</span></span> 

- <span data-ttu-id="37078-183">Contenu par Application Guard : l'événement de navigateur web a été limité par un conteneur isolé</span><span class="sxs-lookup"><span data-stu-id="37078-183">Contained by Application Guard - the web browser event was restricted by an isolated container</span></span>
- <span data-ttu-id="37078-184">Menace active détectée : la détection des menaces s'est produite pendant l'exécution de la menace</span><span class="sxs-lookup"><span data-stu-id="37078-184">Active threat detected - the threat detection occurred while the threat was running</span></span>
- <span data-ttu-id="37078-185">Correction infructueuse : une tentative de correction de la menace détectée a été invoquée mais a échoué</span><span class="sxs-lookup"><span data-stu-id="37078-185">Remediation unsuccessful - an attempt to remediate the detected threat was invoked but failed</span></span>
- <span data-ttu-id="37078-186">Correction réussie : la menace détectée a été arrêtée et nettoyée</span><span class="sxs-lookup"><span data-stu-id="37078-186">Remediation successful - the detected threat was stopped and cleaned</span></span>
- <span data-ttu-id="37078-187">Avertissement contourné par l'utilisateur : l'avertissement Windows Defender SmartScreen a été rejeté et a été contourné par un utilisateur</span><span class="sxs-lookup"><span data-stu-id="37078-187">Warning bypassed by user - the Windows Defender SmartScreen warning was dismissed and overridden by a user</span></span>
- <span data-ttu-id="37078-188">Script suspect détecté : un script potentiellement malveillant a été détecté en cours d'exécution</span><span class="sxs-lookup"><span data-stu-id="37078-188">Suspicious script detected - a potentially malicious script was found running</span></span>
- <span data-ttu-id="37078-189">Catégorie d'alerte : si l'événement a conduit à la génération d'une alerte, la catégorie d'alerte ( « Mouvement latéral », par exemple) est fournie.</span><span class="sxs-lookup"><span data-stu-id="37078-189">The alert category - if the event led to the generation of an alert, the alert category  ("Lateral Movement", for example) is provided</span></span>

#### <a name="event-details"></a><span data-ttu-id="37078-190">Détails de l'événement</span><span class="sxs-lookup"><span data-stu-id="37078-190">Event details</span></span>
<span data-ttu-id="37078-191">Sélectionnez un événement pour afficher les détails pertinents sur cet événement.</span><span class="sxs-lookup"><span data-stu-id="37078-191">Select an event to view relevant details about that event.</span></span> <span data-ttu-id="37078-192">Un panneau s'affiche pour afficher des informations générales sur les événements.</span><span class="sxs-lookup"><span data-stu-id="37078-192">A panel displays to show general event information.</span></span> <span data-ttu-id="37078-193">Le cas échéant et lorsque des données sont disponibles, un graphique montrant les entités associées et leurs relations est également affiché.</span><span class="sxs-lookup"><span data-stu-id="37078-193">When applicable and data is available, a graph showing related entities and their relationships are also shown.</span></span>

<span data-ttu-id="37078-194">Pour inspecter plus en détail l'événement [](advanced-hunting-overview.md) et les événements connexes, vous pouvez rapidement exécuter une requête de recherche avancée en sélectionnant **Hunt pour les événements connexes.**</span><span class="sxs-lookup"><span data-stu-id="37078-194">To further inspect the event and related events, you can quickly run an [advanced hunting](advanced-hunting-overview.md) query by selecting **Hunt for related events**.</span></span> <span data-ttu-id="37078-195">La requête retourne l'événement sélectionné et la liste des autres événements qui se sont produits au même moment sur le même point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="37078-195">The query will return the selected event and the list of other events that occurred around the same time on the same endpoint.</span></span>

![Image du panneau Détails de l'événement](images/event-details.png)

### <a name="security-recommendations"></a><span data-ttu-id="37078-197">Recommandations de sécurité</span><span class="sxs-lookup"><span data-stu-id="37078-197">Security recommendations</span></span>

<span data-ttu-id="37078-198">**Des recommandations en matière** de sécurité sont générées à partir de Microsoft Defender pour la fonctionnalité de gestion des menaces [& vulnérabilités du](tvm-dashboard-insights.md) point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="37078-198">**Security recommendations** are generated from Microsoft Defender for Endpoint's [Threat & Vulnerability Management](tvm-dashboard-insights.md) capability.</span></span> <span data-ttu-id="37078-199">La sélection d'une recommandation affiche un panneau dans lequel vous pouvez afficher des détails pertinents, tels que la description de la recommandation et les risques potentiels associés à sa non-utilisation.</span><span class="sxs-lookup"><span data-stu-id="37078-199">Selecting a recommendation will show a panel where you can view relevant details such as description of the recommendation and the potential risks associated with not enacting it.</span></span> <span data-ttu-id="37078-200">Pour plus [d'informations, voir](tvm-security-recommendation.md) recommandations en matière de sécurité.</span><span class="sxs-lookup"><span data-stu-id="37078-200">See [Security recommendation](tvm-security-recommendation.md) for details.</span></span>

![Image de l'onglet Recommandations de sécurité](images/security-recommendations-device.png)

### <a name="software-inventory"></a><span data-ttu-id="37078-202">Inventaire des logiciels</span><span class="sxs-lookup"><span data-stu-id="37078-202">Software inventory</span></span>

<span data-ttu-id="37078-203">**L'onglet Inventaire** logiciel vous permet d'afficher le logiciel sur l'appareil, ainsi que les faiblesses ou menaces.</span><span class="sxs-lookup"><span data-stu-id="37078-203">The **Software inventory** tab lets you view software on the device, along with any weaknesses or threats.</span></span> <span data-ttu-id="37078-204">La sélection du nom du logiciel vous permet d'afficher les recommandations de sécurité, les vulnérabilités découvertes, les appareils installés et la distribution des versions sur la page de détails du logiciel.</span><span class="sxs-lookup"><span data-stu-id="37078-204">Selecting the name of the software will take you to the software details page where you can view security recommendations, discovered vulnerabilities, installed devices, and version distribution.</span></span> <span data-ttu-id="37078-205">Voir [l'inventaire logiciel](tvm-software-inventory.md) pour plus d'informations</span><span class="sxs-lookup"><span data-stu-id="37078-205">See [Software inventory](tvm-software-inventory.md) for details</span></span>

![Image de l'onglet Inventaire logiciel](images/software-inventory-device.png)

### <a name="discovered-vulnerabilities"></a><span data-ttu-id="37078-207">Vulnérabilités découvertes</span><span class="sxs-lookup"><span data-stu-id="37078-207">Discovered vulnerabilities</span></span>

<span data-ttu-id="37078-208">**L'onglet Vulnérabilités** découvertes affiche le nom, la gravité et les informations sur les menaces des vulnérabilités découvertes sur l'appareil.</span><span class="sxs-lookup"><span data-stu-id="37078-208">The **Discovered vulnerabilities** tab shows the name, severity, and threat insights of discovered vulnerabilities on the device.</span></span> <span data-ttu-id="37078-209">La sélection de vulnérabilités spécifiques affiche une description et des détails.</span><span class="sxs-lookup"><span data-stu-id="37078-209">Selecting specific vulnerabilities will show a description and details.</span></span>

![Image de l'onglet Vulnérabilités découvertes](images/discovered-vulnerabilities-device.png)

### <a name="missing-kbs"></a><span data-ttu-id="37078-211">Ko manquants</span><span class="sxs-lookup"><span data-stu-id="37078-211">Missing KBs</span></span>
<span data-ttu-id="37078-212">**L'onglet Ko manquant répertorie** les mises à jour de sécurité manquantes pour l'appareil.</span><span class="sxs-lookup"><span data-stu-id="37078-212">The **Missing KBs** tab lists the missing security updates for the device.</span></span>

![Image de l'onglet kbs manquant](images/missing-kbs-device.png)

## <a name="cards"></a><span data-ttu-id="37078-214">Cartes</span><span class="sxs-lookup"><span data-stu-id="37078-214">Cards</span></span>

### <a name="active-alerts"></a><span data-ttu-id="37078-215">Alertes actives</span><span class="sxs-lookup"><span data-stu-id="37078-215">Active alerts</span></span>

<span data-ttu-id="37078-216">La carte **Azure Advanced Threat Protection** affiche une vue d'ensemble des alertes relatives à l'appareil et à son niveau de risque, si vous avez activé la fonctionnalité Microsoft Defender pour l'identité et qu'il existe des alertes actives.</span><span class="sxs-lookup"><span data-stu-id="37078-216">The **Azure Advanced Threat Protection** card will display a high-level overview of alerts related to the device and their risk level, if you have enabled the Microsoft Defender for Identity feature, and there are any active alerts.</span></span> <span data-ttu-id="37078-217">Plus d'informations sont disponibles dans l'exercice « Alertes ».</span><span class="sxs-lookup"><span data-stu-id="37078-217">More information is available in the "Alerts" drill down.</span></span>

![Image de la carte d'alertes active](images/risk-level-small.png)

>[!NOTE]
><span data-ttu-id="37078-219">Vous devez activer l'intégration sur Microsoft Defender pour l'identité et Defender pour le point de terminaison pour utiliser cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="37078-219">You'll need to enable the integration on both Microsoft Defender for Identity and Defender for Endpoint to use this feature.</span></span> <span data-ttu-id="37078-220">Dans Defender pour point de terminaison, vous pouvez activer cette fonctionnalité dans les fonctionnalités avancées.</span><span class="sxs-lookup"><span data-stu-id="37078-220">In Defender for Endpoint, you can enable this feature in advanced features.</span></span> <span data-ttu-id="37078-221">Pour plus d'informations sur l'activer, voir [Activer les fonctionnalités avancées.](advanced-features.md)</span><span class="sxs-lookup"><span data-stu-id="37078-221">For more information on how to enable advanced features, see [Turn on advanced features](advanced-features.md).</span></span>

### <a name="logged-on-users"></a><span data-ttu-id="37078-222">Utilisateurs connectés</span><span class="sxs-lookup"><span data-stu-id="37078-222">Logged on users</span></span>

<span data-ttu-id="37078-223">La **carte Utilisateurs** connectés indique le nombre d'utilisateurs connectés au cours des 30 derniers jours, ainsi que les utilisateurs les plus fréquents et les moins fréquents.</span><span class="sxs-lookup"><span data-stu-id="37078-223">The **Logged on users** card shows how many users have logged on in the past 30 days, along with the most and least frequent users.</span></span> <span data-ttu-id="37078-224">La sélection du lien « Afficher tous les utilisateurs » ouvre le volet d'informations, qui affiche des informations telles que le type d'utilisateur, le type de connexion et le moment où l'utilisateur a été vu pour la première fois et pour la dernière fois.</span><span class="sxs-lookup"><span data-stu-id="37078-224">Selecting the "See all users" link opens the details pane, which displays information such as user type, log on type, and when the user was first and last seen.</span></span> <span data-ttu-id="37078-225">Pour plus d'informations, voir [Examiner les entités utilisateur.](investigate-user.md)</span><span class="sxs-lookup"><span data-stu-id="37078-225">For more information, see [Investigate user entities](investigate-user.md).</span></span>

![Image du volet d'informations de l'utilisateur](images/logged-on-users.png)

### <a name="security-assessments"></a><span data-ttu-id="37078-227">Tests d’évaluation de la sécurité</span><span class="sxs-lookup"><span data-stu-id="37078-227">Security assessments</span></span>

<span data-ttu-id="37078-228">La **carte d'évaluation de** la sécurité indique le niveau d'exposition global, les recommandations en matière de sécurité, les logiciels installés et les vulnérabilités découvertes.</span><span class="sxs-lookup"><span data-stu-id="37078-228">The **Security assessments** card shows the overall exposure level, security recommendations, installed software, and discovered vulnerabilities.</span></span> <span data-ttu-id="37078-229">Le niveau d'exposition d'un appareil est déterminé par l'impact cumulé de ses recommandations de sécurité en attente.</span><span class="sxs-lookup"><span data-stu-id="37078-229">A device's exposure level is determined by the cumulative impact of its pending security recommendations.</span></span>

![Image de la carte d'évaluation de la sécurité](images/security-assessments.png)

## <a name="related-topics"></a><span data-ttu-id="37078-231">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="37078-231">Related topics</span></span>

- [<span data-ttu-id="37078-232">Afficher et organiser la file d'attente des alertes microsoft Defender pour les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="37078-232">View and organize the Microsoft Defender for Endpoint Alerts queue</span></span>](alerts-queue.md)
- [<span data-ttu-id="37078-233">Gérer les alertes microsoft Defender pour les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="37078-233">Manage Microsoft Defender for Endpoint alerts</span></span>](manage-alerts.md)
- [<span data-ttu-id="37078-234">Examiner microsoft Defender pour les alertes de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="37078-234">Investigate Microsoft Defender for Endpoint alerts</span></span>](investigate-alerts.md)
- [<span data-ttu-id="37078-235">Examiner un fichier associé à une alerte Defender for Endpoint</span><span class="sxs-lookup"><span data-stu-id="37078-235">Investigate a file associated with a Defender for Endpoint alert</span></span>](investigate-files.md)
- [<span data-ttu-id="37078-236">Examiner une adresse IP associée à une alerte Defender for Endpoint</span><span class="sxs-lookup"><span data-stu-id="37078-236">Investigate an IP address associated with a Defender for Endpoint alert</span></span>](investigate-ip.md)
- [<span data-ttu-id="37078-237">Examiner un domaine associé à une alerte Defender for Endpoint</span><span class="sxs-lookup"><span data-stu-id="37078-237">Investigate a domain associated with a Defender for Endpoint alert</span></span>](investigate-domain.md)
- [<span data-ttu-id="37078-238">Examiner un compte d'utilisateur dans Defender for Endpoint</span><span class="sxs-lookup"><span data-stu-id="37078-238">Investigate a user account in Defender for Endpoint</span></span>](investigate-user.md)
- [<span data-ttu-id="37078-239">Recommandations en matière de sécurité</span><span class="sxs-lookup"><span data-stu-id="37078-239">Security recommendation</span></span>](tvm-security-recommendation.md)
- [<span data-ttu-id="37078-240">Inventaire des logiciels</span><span class="sxs-lookup"><span data-stu-id="37078-240">Software inventory</span></span>](tvm-software-inventory.md)
