---
title: Examiner les incidents dans Microsoft 365 Defender
description: Examiner les incidents liés aux appareils, aux utilisateurs et aux boîtes aux lettres.
keywords: incident, incidents, analyse, réponse, ordinateurs, appareils, utilisateurs, identités, courrier électronique, boîte aux lettres, enquête, graphique, preuve
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
- incidentresponse
- m365solution-incidentresponse
- m365solution-overview
ms.topic: conceptual
search.appverid:
- MOE150
- MET150
ms.technology: m365d
ms.openlocfilehash: fdfc065aea3549e99de72c968c0fa19412f9e246
ms.sourcegitcommit: ccbdf2638fc6646bfb89450169953f4c3ce4b9b0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/24/2021
ms.locfileid: "53105355"
---
# <a name="investigate-incidents-in-microsoft-365-defender"></a><span data-ttu-id="207f2-104">Examiner les incidents dans Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="207f2-104">Investigate incidents in Microsoft 365 Defender</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

<span data-ttu-id="207f2-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="207f2-105">**Applies to:**</span></span>

- <span data-ttu-id="207f2-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="207f2-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="207f2-107">Microsoft 365 Defender regroupe toutes les alertes, biens, enquêtes et preuves connexes de vos appareils, utilisateurs et boîtes aux lettres dans un incident pour vous donner une vue d’ensemble complète d’une attaque.</span><span class="sxs-lookup"><span data-stu-id="207f2-107">Microsoft 365 Defender aggregates all related alerts, assets, investigations, and evidence from across your devices, users, and mailboxes into an incident to give you a comprehensive look into the entire breadth of an attack.</span></span>

<span data-ttu-id="207f2-108">Au sein d’un incident, vous analysez les alertes qui affectent votre réseau, comprenez ce qu’elles signifient et rassemblez les preuves afin de pouvoir mettre au point un plan de correction efficace.</span><span class="sxs-lookup"><span data-stu-id="207f2-108">Within an incident, you analyze the alerts that affect your network, understand what they mean, and collate the evidence so that you can devise an effective remediation plan.</span></span>

## <a name="initial-investigation"></a><span data-ttu-id="207f2-109">Examen initial</span><span class="sxs-lookup"><span data-stu-id="207f2-109">Initial investigation</span></span>

<span data-ttu-id="207f2-110">Avant de vous plonger dans les détails, jetez un œil aux propriétés et à la synthèse de l’incident.</span><span class="sxs-lookup"><span data-stu-id="207f2-110">Before diving into the details, take a look at the properties and summary of the incident.</span></span>

<span data-ttu-id="207f2-111">Vous pouvez commencer par sélectionner l’incident dans la colonne de coche.</span><span class="sxs-lookup"><span data-stu-id="207f2-111">You can start by selecting the incident from the check mark column.</span></span> <span data-ttu-id="207f2-112">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="207f2-112">Here's an example.</span></span>

:::image type="content" source="../../media/investigate-incidents/incidents-ss-incident-select.png" alt-text="Exemple de sélection d’un incident dans la colonne de coche":::

<span data-ttu-id="207f2-114">Lorsque vous le faites, un volet de synthèse s’ouvre avec des informations clés sur l’incident, telles que la gravité, à qui il est affecté, et les catégories [MITRE ATT &trade;&CK](https://attack.mitre.org/) pour l’incident.</span><span class="sxs-lookup"><span data-stu-id="207f2-114">When you do, a summary pane opens with key information about the incident, such as severity, to whom it is assigned, and the [MITRE ATT&CK&trade;](https://attack.mitre.org/) categories for the incident.</span></span> <span data-ttu-id="207f2-115">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="207f2-115">Here's an example.</span></span>

:::image type="content" source="../../media/investigate-incidents/incidents-ss-incident-side-panel.png" alt-text="Exemple de volet récapitulatif pour un incident":::

<span data-ttu-id="207f2-117">À partir de là, vous pouvez sélectionner **Ouvrir la page Incident.**</span><span class="sxs-lookup"><span data-stu-id="207f2-117">From here, you can select **Open incident page**.</span></span> <span data-ttu-id="207f2-118">Cela ouvre la page principale de l’incident où vous trouverez des informations récapitulatifs et des onglets pour les alertes, les périphériques, les utilisateurs, les enquêtes et les preuves.</span><span class="sxs-lookup"><span data-stu-id="207f2-118">This opens the main page for the incident where you'll find more summary information and tabs for alerts, devices, users, investigations, and evidence.</span></span>

<span data-ttu-id="207f2-119">Vous pouvez également ouvrir la page principale d’un incident en sélectionnant le nom de l’incident dans la file d’attente des incidents.</span><span class="sxs-lookup"><span data-stu-id="207f2-119">You can also open the main page for an incident by selecting the incident name from the incident queue.</span></span>

## <a name="summary"></a><span data-ttu-id="207f2-120">Résumé</span><span class="sxs-lookup"><span data-stu-id="207f2-120">Summary</span></span>

<span data-ttu-id="207f2-121">La page **Résumé** vous donne un aperçu instantané des principaux éléments à noter concernant l’incident.</span><span class="sxs-lookup"><span data-stu-id="207f2-121">The **Summary** page gives you a snapshot glance at the top things to notice about the incident.</span></span>

:::image type="content" source="../../media/incidents-overview/incidents-ss-incident-summary.png" alt-text="Exemple de page Résumé d’un incident dans le centre de Microsoft 365 de sécurité":::

<span data-ttu-id="207f2-123">Les catégories d’attaques vous donnent une vue visuelle et numérique de l’avancement de l’attaque par rapport à la chaîne d’attaque.</span><span class="sxs-lookup"><span data-stu-id="207f2-123">The attack categories give you a visual and numeric view of how advanced the attack has progressed against the kill chain.</span></span> <span data-ttu-id="207f2-124">Comme avec d’autres produits de sécurité Microsoft, Microsoft 365 Defender est aligné sur l’infrastructure [MITRE ATT&&trade; CK.](https://attack.mitre.org/)</span><span class="sxs-lookup"><span data-stu-id="207f2-124">As with other Microsoft security products, Microsoft 365 Defender is aligned to the [MITRE ATT&CK&trade;](https://attack.mitre.org/) framework.</span></span>

<span data-ttu-id="207f2-125">La section l'étendue fournit la liste des principales ressources affectées à cet incident.</span><span class="sxs-lookup"><span data-stu-id="207f2-125">The scope section gives you a list of top impacted assets that are part of this incident.</span></span> <span data-ttu-id="207f2-126">S’il existe des informations spécifiques sur cet élément (par exemple, niveau de risque, priorité d’examen, et balisage sur les éléments) qui s’affichent également dans cette section.</span><span class="sxs-lookup"><span data-stu-id="207f2-126">If there is specific information regarding this asset, such as risk level, investigation priority as well as any tagging on the assets this will also surface in this section.</span></span>

<span data-ttu-id="207f2-127">La chronologie des alertes fournit un aperçu de l’ordre chronologique dans lequel les alertes se sont produites, ainsi que les raisons pour lesquelles ces alertes sont liées à cet incident.</span><span class="sxs-lookup"><span data-stu-id="207f2-127">The alerts timeline provides a sneak peek into the chronological order in which the alerts occurred, as well as the reasons that these alerts are linked to this incident.</span></span>

<span data-ttu-id="207f2-128">Enfin, la section preuve fournit un résumé du nombre d’artefacts différents inclus dans l’incident et de leur état de correction, afin que vous pouvez immédiatement identifier si vous avez besoin d’une action.</span><span class="sxs-lookup"><span data-stu-id="207f2-128">And last - the evidence section provides a summary of how many different artifacts were included in the incident and their remediation status, so you can immediately identify if any action is needed by you.</span></span>

<span data-ttu-id="207f2-129">Cette vue d’ensemble peut vous aider dans le tri initial de l’incident en fournissant des informations sur les principales caractéristiques de l’incident que vous devez connaître.</span><span class="sxs-lookup"><span data-stu-id="207f2-129">This overview can assist in the initial triage of the incident by providing insight into the top characteristics of the incident that you should be aware of.</span></span>

## <a name="alerts"></a><span data-ttu-id="207f2-130">Alertes</span><span class="sxs-lookup"><span data-stu-id="207f2-130">Alerts</span></span>

<span data-ttu-id="207f2-131">Sous **l’onglet** Alerte, vous pouvez afficher la file d’attente d’alertes pour les alertes liées à l’incident et d’autres informations les concernant, telles que :</span><span class="sxs-lookup"><span data-stu-id="207f2-131">On the **Alert** tab, you can view the alert queue for alerts related to the incident and other information about them such as:</span></span>

- <span data-ttu-id="207f2-132">Gravité.</span><span class="sxs-lookup"><span data-stu-id="207f2-132">Severity.</span></span>
- <span data-ttu-id="207f2-133">Entités impliquées dans l’alerte.</span><span class="sxs-lookup"><span data-stu-id="207f2-133">The entities that were involved in the alert.</span></span>
- <span data-ttu-id="207f2-134">Source des alertes (Microsoft Defender pour l’identité, Microsoft Defender pour le point de terminaison, Microsoft Defender pour Office 365).</span><span class="sxs-lookup"><span data-stu-id="207f2-134">The source of the alerts (Microsoft Defender for Identity, Microsoft Defender for Endpoint, Microsoft Defender for Office 365).</span></span>
- <span data-ttu-id="207f2-135">Raison pour laquelle ils ont été liés.</span><span class="sxs-lookup"><span data-stu-id="207f2-135">The reason they were linked together.</span></span>

<span data-ttu-id="207f2-136">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="207f2-136">Here's an example.</span></span>

:::image type="content" source="../../media/investigate-incidents/incident-alerts.png" alt-text="Exemple de page Alertes pour un incident":::

<span data-ttu-id="207f2-138">Par défaut, les alertes sont classés dans l’ordre chronologique pour vous permettre de voir comment l’incident s’est produit au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="207f2-138">By default, the alerts are ordered chronologically to allow you to see how the incident played out over time.</span></span> <span data-ttu-id="207f2-139">Lorsque vous sélectionnez une alerte dans un incident, Microsoft 365 Defender affiche les informations d’alerte spécifiques au contexte de l’incident global.</span><span class="sxs-lookup"><span data-stu-id="207f2-139">When you select an alert within an incident, Microsoft 365 Defender displays the alert information specific to the context of the overall incident.</span></span> 

<span data-ttu-id="207f2-140">Vous pouvez voir les événements de l’alerte, dont d’autres alertes déclenchées ont provoqué l’alerte actuelle, ainsi que toutes les entités et activités concernées impliquées dans l’attaque, y compris les fichiers, les utilisateurs et les boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="207f2-140">You can see the events of the alert, which other triggered alerts caused the current alert, and all the affected entities and activities involved in the attack, including files, users, and mailboxes.</span></span>

<span data-ttu-id="207f2-141">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="207f2-141">Here's an example.</span></span>

:::image type="content" source="../../media/investigate-incidents/incident-alert-example.png" alt-text="Exemple de page de détails d’alerte dans un incident":::

<span data-ttu-id="207f2-143">Cette page d’alerte d’incident se compose des sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="207f2-143">This incident alert page is composed of these sections:</span></span>

- <span data-ttu-id="207f2-144">Article sur l’alerte, qui inclut un résumé de ce qui s’est passé</span><span class="sxs-lookup"><span data-stu-id="207f2-144">Alert story, which includes a summary of what happened</span></span>
- <span data-ttu-id="207f2-145">Événements et alertes connexes</span><span class="sxs-lookup"><span data-stu-id="207f2-145">Related events and alerts</span></span>
- <span data-ttu-id="207f2-146">Détails récapitulatifs</span><span class="sxs-lookup"><span data-stu-id="207f2-146">Summary details</span></span>

<span data-ttu-id="207f2-147">Découvrez comment utiliser la file d’attente d’alertes et les pages d’alerte dans [examiner les alertes.](investigate-alerts.md)</span><span class="sxs-lookup"><span data-stu-id="207f2-147">Learn how to use the alert queue and alert pages in [investigate alerts](investigate-alerts.md).</span></span>

## <a name="devices"></a><span data-ttu-id="207f2-148">Appareils</span><span class="sxs-lookup"><span data-stu-id="207f2-148">Devices</span></span>

<span data-ttu-id="207f2-149">**L’onglet Appareils** répertorie tous les appareils liés à l’incident.</span><span class="sxs-lookup"><span data-stu-id="207f2-149">The **Devices** tab lists all the devices related to the incident.</span></span> <span data-ttu-id="207f2-150">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="207f2-150">Here's an example.</span></span>

:::image type="content" source="../../media/investigate-incidents/incident-devices.png" alt-text="Exemple de page Appareils pour un incident":::

<span data-ttu-id="207f2-152">Vous pouvez cocher la coche d’un appareil pour voir les détails de l’appareil, les données d’annuaire, les alertes actives et les utilisateurs connectés.</span><span class="sxs-lookup"><span data-stu-id="207f2-152">You can select the check mark for a device to see details of the device, directory data, active alerts, and logged on users.</span></span> <span data-ttu-id="207f2-153">Sélectionnez le nom de l’appareil pour voir les détails de l’appareil dans l’inventaire des appareils Microsoft Defender pour les points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="207f2-153">Select the name of the device to see device details in the Microsoft Defender for Endpoints device inventory.</span></span>

:::image type="content" source="../../media/investigate-incidents/incident-devices-details.png" alt-text="Exemple de page d’appareils pour Microsoft Defender pour les points de terminaison":::

<span data-ttu-id="207f2-155">Dans la page appareil, vous pouvez collecter des informations supplémentaires sur l’appareil, telles que toutes ses alertes, une chronologie et des recommandations de sécurité.</span><span class="sxs-lookup"><span data-stu-id="207f2-155">From the device page, you can gather additional information about the device, such as all of its alerts, a timeline, and security recommendations.</span></span> <span data-ttu-id="207f2-156">Par exemple,  à partir de l’onglet Chronologie, vous pouvez parcourir la chronologie de l’ordinateur et afficher tous les événements et comportements observés sur l’ordinateur dans l’ordre chronologique, entrecoupés des alertes.</span><span class="sxs-lookup"><span data-stu-id="207f2-156">For example, from the **Timeline** tab, you can scroll through the machine timeline and view all events and behaviors observed on the machine in chronological order, interspersed with the alerts raised.</span></span>

> [!TIP]
> <span data-ttu-id="207f2-157">Vous pouvez faire des analyses à la demande sur une page d’appareil.</span><span class="sxs-lookup"><span data-stu-id="207f2-157">You can do on-demand scans on a device page.</span></span> <span data-ttu-id="207f2-158">Dans le centre Microsoft 365 de sécurité, choisissez Points de **terminaison >'inventaire des appareils.**</span><span class="sxs-lookup"><span data-stu-id="207f2-158">In the Microsoft 365 security center, choose **Endpoints > Device inventory**.</span></span> <span data-ttu-id="207f2-159">Sélectionnez un appareil qui a des alertes, puis exécutez une analyse antivirus.</span><span class="sxs-lookup"><span data-stu-id="207f2-159">Select a device that has alerts, and then run an antivirus scan.</span></span> <span data-ttu-id="207f2-160">Les actions, telles que les analyses antivirus, sont suivis et sont visibles sur la page **d’inventaire des** appareils.</span><span class="sxs-lookup"><span data-stu-id="207f2-160">Actions, such as antivirus scans, are tracked and are visible on the **Device inventory** page.</span></span> <span data-ttu-id="207f2-161">Pour plus d’informations, voir [Exécuter Antivirus Microsoft Defender’analyse sur les appareils.](/microsoft-365/security/defender-endpoint/respond-machine-alerts#run-microsoft-defender-antivirus-scan-on-devices)</span><span class="sxs-lookup"><span data-stu-id="207f2-161">To learn more, see [Run Microsoft Defender Antivirus scan on devices](/microsoft-365/security/defender-endpoint/respond-machine-alerts#run-microsoft-defender-antivirus-scan-on-devices).</span></span>

## <a name="users"></a><span data-ttu-id="207f2-162">Utilisateurs</span><span class="sxs-lookup"><span data-stu-id="207f2-162">Users</span></span>

<span data-ttu-id="207f2-163">**L’onglet** Utilisateurs répertorie tous les utilisateurs qui ont été identifiés comme faisant partie ou associés à l’incident.</span><span class="sxs-lookup"><span data-stu-id="207f2-163">The **Users** tab lists all the users that have been identified to be part of or related to the incident.</span></span> <span data-ttu-id="207f2-164">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="207f2-164">Here's an example.</span></span>

:::image type="content" source="../../media/investigate-incidents/incident-users.png" alt-text="Exemple de page Utilisateurs pour un incident":::

<span data-ttu-id="207f2-166">Vous pouvez cocher la coche d’un utilisateur pour voir les détails de la menace, de l’exposition et des informations de contact du compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="207f2-166">You can select the check mark for a user to see details of the user account threat, exposure, and contact information.</span></span> <span data-ttu-id="207f2-167">Sélectionnez le nom d’utilisateur pour voir les détails supplémentaires du compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="207f2-167">Select the user name to see additional user account details.</span></span>

<span data-ttu-id="207f2-168">Découvrez comment afficher des informations utilisateur supplémentaires et gérer les utilisateurs d’un incident dans [l’examen des utilisateurs.](investigate-users.md)</span><span class="sxs-lookup"><span data-stu-id="207f2-168">Learn how to view additional user information and manage the users of an incident in [investigate users](investigate-users.md).</span></span>


## <a name="mailboxes"></a><span data-ttu-id="207f2-169">Boîtes aux lettres</span><span class="sxs-lookup"><span data-stu-id="207f2-169">Mailboxes</span></span>

<span data-ttu-id="207f2-170">**L’onglet Boîtes** aux lettres répertorie toutes les boîtes aux lettres qui ont été identifiées comme faisant partie ou associées à l’incident.</span><span class="sxs-lookup"><span data-stu-id="207f2-170">The **Mailboxes** tab lists all the mailboxes that have been identified to be part of or related to the incident.</span></span> <span data-ttu-id="207f2-171">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="207f2-171">Here's an example.</span></span>

:::image type="content" source="../../media/investigate-incidents/incident-mailboxes.png" alt-text="Exemple de page Boîtes aux lettres pour un incident":::

<span data-ttu-id="207f2-173">Vous pouvez cocher la coche d’une boîte aux lettres pour voir la liste des alertes actives.</span><span class="sxs-lookup"><span data-stu-id="207f2-173">You can select the check mark for a mailbox to see a list of active alerts.</span></span> <span data-ttu-id="207f2-174">Sélectionnez le nom de la boîte aux lettres pour voir des détails supplémentaires sur la page Explorateur de Microsoft Defender pour Office 365.</span><span class="sxs-lookup"><span data-stu-id="207f2-174">Select the mailbox name to see additional mailbox details on the Explorer page for Microsoft Defender for Office 365.</span></span>

## <a name="investigations"></a><span data-ttu-id="207f2-175">Examens</span><span class="sxs-lookup"><span data-stu-id="207f2-175">Investigations</span></span>

<span data-ttu-id="207f2-176">**L’onglet** Enquêtes répertorie toutes les [enquêtes](m365d-autoir.md) automatisées déclenchées par les alertes dans cet incident.</span><span class="sxs-lookup"><span data-stu-id="207f2-176">The **Investigations** tab lists all the [automated investigations](m365d-autoir.md) triggered by alerts in this incident.</span></span> <span data-ttu-id="207f2-177">Les enquêtes effectuent des actions de correction ou attendent l’approbation par un analyste des actions, selon la façon dont vous avez configuré vos enquêtes automatisées pour qu’ils s’exécutent dans Microsoft Defender pour Endpoint et Defender pour Office 365.</span><span class="sxs-lookup"><span data-stu-id="207f2-177">The investigations will perform remediation actions or wait for analyst approval of actions, depending on how you configured your automated investigations to run in Microsoft Defender for Endpoint and Defender for Office 365.</span></span>

:::image type="content" source="../../media/investigate-incidents/incident-investigations.png" alt-text="Exemple de page Investigations pour un incident":::

<span data-ttu-id="207f2-179">Sélectionnez un examen pour accéder à sa page de détails pour obtenir des informations complètes sur l’état de l’examen et de la correction.</span><span class="sxs-lookup"><span data-stu-id="207f2-179">Select an investigation to navigate to its details page for full information on the investigation and remediation status.</span></span> <span data-ttu-id="207f2-180">Si des actions sont en attente d’approbation dans le cadre de l’examen, elles apparaissent dans l’onglet Historique des **actions en** attente. Prendre des mesures dans le cadre de la correction des incidents.</span><span class="sxs-lookup"><span data-stu-id="207f2-180">If there are any actions pending for approval as part of the investigation, they will appear in the **Pending actions history** tab. Take action as part of incident remediation.</span></span>

<span data-ttu-id="207f2-181">Il existe également un onglet **Graphique d’enquête** qui indique :</span><span class="sxs-lookup"><span data-stu-id="207f2-181">There is also an **Investigation graph** tab that shows:</span></span>

- <span data-ttu-id="207f2-182">La connexion des alertes aux biens touchés dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="207f2-182">The connection of alerts to the impacted assets in your organization.</span></span>
- <span data-ttu-id="207f2-183">Les entités liées aux alertes et à la façon dont elles font partie de l’article de l’attaque.</span><span class="sxs-lookup"><span data-stu-id="207f2-183">Which entities are related to which alerts and how they are part of the story of the attack.</span></span>
- <span data-ttu-id="207f2-184">Alertes pour l’incident.</span><span class="sxs-lookup"><span data-stu-id="207f2-184">The alerts for the incident.</span></span>

<span data-ttu-id="207f2-185">Le graphique d’enquête vous permet de comprendre rapidement l’étendue complète de l’attaque en connectant les différentes entités suspectes faisant partie de l’attaque avec leurs biens connexes tels que les utilisateurs, les périphériques et les boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="207f2-185">The investigation graph helps you quickly understand the full scope of the attack by connecting the different suspicious entities that are part of the attack with their related assets such as users, devices, and mailboxes.</span></span> 

<span data-ttu-id="207f2-186">Pour plus d’informations, voir [Examen et réponse automatisés dans Microsoft 365 Defender](m365d-autoir.md).</span><span class="sxs-lookup"><span data-stu-id="207f2-186">For more information, see [Automated investigation and response in Microsoft 365 Defender](m365d-autoir.md).</span></span>

## <a name="evidence-and-response"></a><span data-ttu-id="207f2-187">Preuve et réponse</span><span class="sxs-lookup"><span data-stu-id="207f2-187">Evidence and Response</span></span>

<span data-ttu-id="207f2-188">**L’onglet Preuve et réponse** affiche tous les événements pris en charge et entités suspectes dans les alertes de l’incident.</span><span class="sxs-lookup"><span data-stu-id="207f2-188">The **Evidence and Response** tab shows all the supported events and suspicious entities in the alerts in the incident.</span></span> <span data-ttu-id="207f2-189">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="207f2-189">Here's an example.</span></span>

:::image type="content" source="../../media/investigate-incidents/incident-evidence.png" alt-text="Exemple de page Preuve et réponse pour un incident":::

<span data-ttu-id="207f2-191">Microsoft 365 Defender examine automatiquement tous les événements pris en charge par les incidents et les entités suspectes dans les alertes, en vous fournissant des informations sur les messages électroniques, fichiers, processus, services, adresses IP et bien plus encore.</span><span class="sxs-lookup"><span data-stu-id="207f2-191">Microsoft 365 Defender automatically investigates all the incidents' supported events and suspicious entities in the alerts, providing you with information about the important emails, files, processes, services, IP Addresses, and more.</span></span> <span data-ttu-id="207f2-192">Cela vous permet de détecter et de bloquer rapidement les menaces potentielles dans l’incident.</span><span class="sxs-lookup"><span data-stu-id="207f2-192">This helps you quickly detect and block potential threats in the incident.</span></span>

<span data-ttu-id="207f2-193">Chacune des entités analysées est marquée avec un verdict (malveillant, suspect, propre) et un état de correction.</span><span class="sxs-lookup"><span data-stu-id="207f2-193">Each of the analyzed entities is marked with a verdict (Malicious, Suspicious, Clean) and a remediation status.</span></span> <span data-ttu-id="207f2-194">Cela vous permet de comprendre l’état de correction de l’intégralité de l’incident et les étapes suivantes qui peuvent être prises.</span><span class="sxs-lookup"><span data-stu-id="207f2-194">This helps you understand the remediation status of the entire incident and what next steps can be taken.</span></span>

## <a name="next-steps"></a><span data-ttu-id="207f2-195">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="207f2-195">Next steps</span></span>

<span data-ttu-id="207f2-196">Selon les besoins :</span><span class="sxs-lookup"><span data-stu-id="207f2-196">As needed:</span></span>

- [<span data-ttu-id="207f2-197">Examiner les alertes d’un incident</span><span class="sxs-lookup"><span data-stu-id="207f2-197">Investigate the alerts of an incident</span></span>](investigate-alerts.md)
- [<span data-ttu-id="207f2-198">Examiner les utilisateurs d’un incident</span><span class="sxs-lookup"><span data-stu-id="207f2-198">Investigate the users of an incident</span></span>](investigate-users.md)

## <a name="see-also"></a><span data-ttu-id="207f2-199">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="207f2-199">See also</span></span>

- [<span data-ttu-id="207f2-200">Vue d’ensemble des incidents</span><span class="sxs-lookup"><span data-stu-id="207f2-200">Incidents overview</span></span>](incidents-overview.md)
- [<span data-ttu-id="207f2-201">Hiérarchiser les incidents</span><span class="sxs-lookup"><span data-stu-id="207f2-201">Prioritize incidents</span></span>](incident-queue.md)
- [<span data-ttu-id="207f2-202">Gérer les incidents</span><span class="sxs-lookup"><span data-stu-id="207f2-202">Manage incidents</span></span>](manage-incidents.md)

