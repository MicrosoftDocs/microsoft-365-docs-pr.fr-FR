---
title: Examiner les incidents dans Microsoft 365 Defender
description: Analyser les incidents liés aux appareils, aux utilisateurs et aux boîtes aux lettres.
keywords: incident, incidents, ordinateurs, appareils, utilisateurs, identités, courrier, courrier électronique, boîte aux lettres, investigation, graphique, preuves
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
ms.openlocfilehash: 5fe594dca935b7377a385b487f1464c3f0a91151
ms.sourcegitcommit: 223a36a86753fe9cebee96f05ab4c9a144133677
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2021
ms.locfileid: "51760296"
---
# <a name="investigate-incidents-in-microsoft-365-defender"></a><span data-ttu-id="9d3f3-104">Examiner les incidents dans Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="9d3f3-104">Investigate incidents in Microsoft 365 Defender</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="9d3f3-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="9d3f3-105">**Applies to:**</span></span>

- <span data-ttu-id="9d3f3-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="9d3f3-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="9d3f3-107">Microsoft 365 Defender regroupe toutes les alertes, biens, enquêtes et preuves connexes sur vos appareils, utilisateurs et boîtes aux lettres dans un incident pour vous donner une vue d'ensemble complète d'une attaque.</span><span class="sxs-lookup"><span data-stu-id="9d3f3-107">Microsoft 365 Defender aggregates all related alerts, assets, investigations and evidence from across your devices, users, and mailboxes into an incident to give you a comprehensive look into the entire breadth of an attack.</span></span>

<span data-ttu-id="9d3f3-108">Au sein d'un incident, vous examinez les alertes qui affectent votre réseau, comprenez ce qu'elles signifient et rassemblez les preuves afin de pouvoir mettre au point un plan de correction efficace.</span><span class="sxs-lookup"><span data-stu-id="9d3f3-108">Within an incident, you investigate the alerts that affect your network, understand what they mean, and collate the evidence so that you can devise an effective remediation plan.</span></span>

## <a name="initial-investigation"></a><span data-ttu-id="9d3f3-109">Examen initial</span><span class="sxs-lookup"><span data-stu-id="9d3f3-109">Initial investigation</span></span>

<span data-ttu-id="9d3f3-110">Avant de vous plonger dans les détails, jetez un œil aux propriétés et à la synthèse de l'incident.</span><span class="sxs-lookup"><span data-stu-id="9d3f3-110">Before diving into the details, take a look at the properties and summary of the incident.</span></span>

<span data-ttu-id="9d3f3-111">Vous pouvez commencer par sélectionner l'incident dans la colonne de coche.</span><span class="sxs-lookup"><span data-stu-id="9d3f3-111">You can start by selecting the incident from the check mark column.</span></span> <span data-ttu-id="9d3f3-112">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="9d3f3-112">Here's an example.</span></span>

:::image type="content" source="../../media/investigate-incidents/incidents-ss-incident-select.png" alt-text="Exemple de sélection d'un incident dans la colonne de coche":::

<span data-ttu-id="9d3f3-114">Lorsque vous le faites, un volet récapitulatif s'ouvre avec des informations clés sur l'incident, telles que la gravité, à qui il est affecté et les catégories [MITRE ATT &trade;&CK](https://attack.mitre.org/) pour l'incident.</span><span class="sxs-lookup"><span data-stu-id="9d3f3-114">When you do, a summary pane opens with key information about the incident, such as severity, who it is assigned to, and the [MITRE ATT&CK&trade;](https://attack.mitre.org/) categories for the incident.</span></span> <span data-ttu-id="9d3f3-115">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="9d3f3-115">Here's an example.</span></span>

:::image type="content" source="../../media/investigate-incidents/incidents-ss-incident-side-panel.png" alt-text="Exemple de volet récapitulatif pour un incident":::

<span data-ttu-id="9d3f3-117">À partir de là, vous pouvez sélectionner **Ouvrir la page Incident.**</span><span class="sxs-lookup"><span data-stu-id="9d3f3-117">From here, you can select **Open incident page**.</span></span> <span data-ttu-id="9d3f3-118">Cela ouvre la page principale de l'incident où vous trouverez des informations récapitulatifs et des onglets pour les alertes, les périphériques, les utilisateurs, les enquêtes et les preuves.</span><span class="sxs-lookup"><span data-stu-id="9d3f3-118">This opens the main page for the incident where you'll find more summary information and tabs for alerts, devices, users, investigations, and evidence.</span></span>

<span data-ttu-id="9d3f3-119">Vous pouvez également ouvrir la page principale d'un incident en sélectionnant le nom de l'incident dans la file d'attente des incidents.</span><span class="sxs-lookup"><span data-stu-id="9d3f3-119">You can also open the main page for an incident by selecting the incident name from the incident queue.</span></span>

## <a name="summary"></a><span data-ttu-id="9d3f3-120">Résumé</span><span class="sxs-lookup"><span data-stu-id="9d3f3-120">Summary</span></span>

<span data-ttu-id="9d3f3-121">La page **Résumé** vous donne un aperçu instantané des principaux éléments à noter concernant l'incident.</span><span class="sxs-lookup"><span data-stu-id="9d3f3-121">The **Summary** page gives you a snapshot glance at the top things to notice about the incident.</span></span>

:::image type="content" source="../../media/incidents-overview/incidents-ss-incident-summary.png" alt-text="Exemple de page Résumé d'un incident dans le Centre de sécurité Microsoft 365":::

<span data-ttu-id="9d3f3-123">Les catégories d'attaque vous donnent une vue visuelle et numérique de l'avancement de l'attaque par rapport à la chaîne d'attaque.</span><span class="sxs-lookup"><span data-stu-id="9d3f3-123">The attack categories give you a visual and numeric view of how advanced the attack has progressed against the kill chain.</span></span> <span data-ttu-id="9d3f3-124">Comme avec d'autres produits de sécurité Microsoft, Microsoft 365 Defender est aligné sur l'infrastructure [MITRE ATT&&trade; CK.](https://attack.mitre.org/)</span><span class="sxs-lookup"><span data-stu-id="9d3f3-124">As with other Microsoft security products, Microsoft 365 Defender is aligned to the [MITRE ATT&CK&trade;](https://attack.mitre.org/) framework.</span></span>

<span data-ttu-id="9d3f3-125">La section l'étendue fournit la liste des principales ressources affectées à cet incident.</span><span class="sxs-lookup"><span data-stu-id="9d3f3-125">The scope section gives you a list of top impacted assets that are part of this incident.</span></span> <span data-ttu-id="9d3f3-126">S’il existe des informations spécifiques sur cet élément (par exemple, niveau de risque, priorité d’examen, et balisage sur les éléments) qui s’affichent également dans cette section.</span><span class="sxs-lookup"><span data-stu-id="9d3f3-126">If there is specific information regarding this asset, such as risk level, investigation priority as well as any tagging on the assets this will also surface in this section.</span></span>

<span data-ttu-id="9d3f3-127">La chronologie des alertes fournit un aperçu de l'ordre chronologique dans lequel les alertes se sont produites, ainsi que les raisons pour lesquelles ces alertes sont liées à cet incident.</span><span class="sxs-lookup"><span data-stu-id="9d3f3-127">The alerts timeline provides a sneak peek into the chronological order in which the alerts occurred, as well as the reasons that these alerts are linked to this incident.</span></span>

<span data-ttu-id="9d3f3-128">Enfin, la section preuves fournit un résumé du nombre d’artefacts différents qui ont été inclus dans l’incident et de leur état de correction, pour que vous puissiez identifier immédiatement toute action nécessaire à la fin de l’opération.</span><span class="sxs-lookup"><span data-stu-id="9d3f3-128">And last - the evidence section provides a summary of how many different artifacts were included in the incident and their remediation status, so you can immediately identify if any action is needed on your end.</span></span>

<span data-ttu-id="9d3f3-129">Cette vue d'ensemble peut vous aider dans le tri initial de l'incident en fournissant des informations sur les principales caractéristiques de l'incident que vous devez connaître.</span><span class="sxs-lookup"><span data-stu-id="9d3f3-129">This overview can assist in the initial triage of the incident by providing insight into the top characteristics of the incident that you should be aware of.</span></span>

## <a name="alerts"></a><span data-ttu-id="9d3f3-130">Alertes</span><span class="sxs-lookup"><span data-stu-id="9d3f3-130">Alerts</span></span>

<span data-ttu-id="9d3f3-131">Sous **l'onglet** Alerte, vous pouvez afficher la file d'attente d'alertes pour les alertes liées à l'incident et d'autres informations les concernant, telles que :</span><span class="sxs-lookup"><span data-stu-id="9d3f3-131">On the **Alert** tab, you can view the alert queue for alerts related to the incident and other information about them such as:</span></span>

- <span data-ttu-id="9d3f3-132">Gravité.</span><span class="sxs-lookup"><span data-stu-id="9d3f3-132">Severity.</span></span>
- <span data-ttu-id="9d3f3-133">Entités impliquées dans l'alerte.</span><span class="sxs-lookup"><span data-stu-id="9d3f3-133">The entities that were involved in the alert.</span></span>
- <span data-ttu-id="9d3f3-134">Source des alertes (Microsoft Defender pour l'identité, Microsoft Defender pour le point de terminaison, Microsoft Defender pour Office 365).</span><span class="sxs-lookup"><span data-stu-id="9d3f3-134">The source of the alerts (Microsoft Defender for Identity, Microsoft Defender for Endpoint, Microsoft Defender for Office 365).</span></span>
- <span data-ttu-id="9d3f3-135">Raison pour laquelle ils ont été liés.</span><span class="sxs-lookup"><span data-stu-id="9d3f3-135">The reason they were linked together.</span></span>

<span data-ttu-id="9d3f3-136">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="9d3f3-136">Here's an example.</span></span>

:::image type="content" source="../../media/investigate-incidents/incident-alerts.png" alt-text="Exemple de page Alertes pour un incident":::

<span data-ttu-id="9d3f3-138">Par défaut, les alertes sont classés dans l'ordre chronologique pour vous permettre de voir comment l'incident s'est produit au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="9d3f3-138">By default, the alerts are ordered chronologically to allow you to see how the incident played out over time.</span></span> <span data-ttu-id="9d3f3-139">La sélection de chaque alerte vous conduit à la page principale de l'alerte, où vous pouvez effectuer un examen approfondi de cette alerte.</span><span class="sxs-lookup"><span data-stu-id="9d3f3-139">Selecting each alert takes you to the alert's main page where you can conduct an in-depth investigation of that alert.</span></span> 

<span data-ttu-id="9d3f3-140">Découvrez comment utiliser la file d'attente d'alertes et les pages d'alerte dans [Examiner les alertes](investigate-alerts.md)</span><span class="sxs-lookup"><span data-stu-id="9d3f3-140">Learn how to use the alert queue and alert pages in [Investigate alerts](investigate-alerts.md)</span></span>

## <a name="devices"></a><span data-ttu-id="9d3f3-141">Appareils</span><span class="sxs-lookup"><span data-stu-id="9d3f3-141">Devices</span></span>

<span data-ttu-id="9d3f3-142">**L'onglet Appareils** répertorie tous les appareils liés à l'incident.</span><span class="sxs-lookup"><span data-stu-id="9d3f3-142">The **Devices** tab lists all the devices related to the incident.</span></span> <span data-ttu-id="9d3f3-143">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="9d3f3-143">Here's an example.</span></span>

:::image type="content" source="../../media/investigate-incidents/incident-devices.png" alt-text="Exemple de page Appareils pour un incident":::

<span data-ttu-id="9d3f3-145">Vous pouvez cocher la coche d'un appareil pour voir les détails de l'appareil, les données d'annuaire, les alertes actives et les utilisateurs connectés.</span><span class="sxs-lookup"><span data-stu-id="9d3f3-145">You can select the check mark for a device to see details of the device, directory data, active alerts, and logged on users.</span></span> <span data-ttu-id="9d3f3-146">Sélectionnez le nom de l'appareil pour voir les détails de l'appareil dans l'inventaire des appareils Microsoft Defender pour les points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="9d3f3-146">Select the name of the device to see device details in the Microsoft Defender for Endpoints device inventory.</span></span>

:::image type="content" source="../../media/investigate-incidents/incident-devices-details.png" alt-text="Exemple de page d'appareils pour Microsoft Defender pour les points de terminaison":::

<span data-ttu-id="9d3f3-148">Dans la page appareil, vous pouvez collecter des informations supplémentaires sur l'appareil, telles que toutes ses alertes, une chronologie et des recommandations de sécurité.</span><span class="sxs-lookup"><span data-stu-id="9d3f3-148">From the device page, you can gather additional information about the device, such as all of its alerts, a timeline, and security recommendations.</span></span> <span data-ttu-id="9d3f3-149">Par exemple,  à partir de l'onglet Chronologie, vous pouvez parcourir la chronologie de l'ordinateur et afficher tous les événements et comportements observés sur l'ordinateur dans l'ordre chronologique, entrecoupés des alertes.</span><span class="sxs-lookup"><span data-stu-id="9d3f3-149">For example, from the **Timeline** tab, you can scroll through the machine timeline and view all events and behaviors observed on the machine in chronological order, interspersed with the alerts raised.</span></span>

> [!TIP]
> <span data-ttu-id="9d3f3-150">Vous pouvez faire des analyses à la demande sur une page d'appareil.</span><span class="sxs-lookup"><span data-stu-id="9d3f3-150">You can do on-demand scans on a device page.</span></span> <span data-ttu-id="9d3f3-151">Dans le Centre de sécurité Microsoft 365, sélectionnez Points de terminaison **>'inventaire des appareils.**</span><span class="sxs-lookup"><span data-stu-id="9d3f3-151">In the Microsoft 365 security center, choose **Endpoints > Device inventory**.</span></span> <span data-ttu-id="9d3f3-152">Sélectionnez un appareil qui a des alertes, puis exécutez une analyse antivirus.</span><span class="sxs-lookup"><span data-stu-id="9d3f3-152">Select a device that has alerts, and then run an antivirus scan.</span></span> <span data-ttu-id="9d3f3-153">Les actions, telles que les analyses antivirus, sont suivis et sont visibles sur la page **d'inventaire des** appareils.</span><span class="sxs-lookup"><span data-stu-id="9d3f3-153">Actions, such as antivirus scans, are tracked and are visible on the **Device inventory** page.</span></span> <span data-ttu-id="9d3f3-154">Pour en savoir plus, [consultez l'analyse de l'Antivirus Microsoft Defender sur les appareils.](/microsoft-365/security/defender-endpoint/respond-machine-alerts#run-microsoft-defender-antivirus-scan-on-devices)</span><span class="sxs-lookup"><span data-stu-id="9d3f3-154">To learn more, see [Run Microsoft Defender Antivirus scan on devices](/microsoft-365/security/defender-endpoint/respond-machine-alerts#run-microsoft-defender-antivirus-scan-on-devices).</span></span>

## <a name="users"></a><span data-ttu-id="9d3f3-155">Utilisateurs</span><span class="sxs-lookup"><span data-stu-id="9d3f3-155">Users</span></span>

<span data-ttu-id="9d3f3-156">**L'onglet** Utilisateurs répertorie tous les utilisateurs qui ont été identifiés comme faisant partie ou associés à l'incident.</span><span class="sxs-lookup"><span data-stu-id="9d3f3-156">The **Users** tab lists all the users that have been identified to be part of or related to the incident.</span></span> <span data-ttu-id="9d3f3-157">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="9d3f3-157">Here's an example.</span></span>

:::image type="content" source="../../media/investigate-incidents/incident-users.png" alt-text="Exemple de page Utilisateurs pour un incident":::

<span data-ttu-id="9d3f3-159">Vous pouvez cocher la coche d'un utilisateur pour voir les détails de la menace, de l'exposition et des informations de contact du compte d'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9d3f3-159">You can select the check mark for a user to see details of the user account threat, exposure, and contact information.</span></span> <span data-ttu-id="9d3f3-160">Sélectionnez le nom d'utilisateur pour voir les détails supplémentaires du compte d'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9d3f3-160">Select the user name to see additional user account details.</span></span>

## <a name="mailboxes"></a><span data-ttu-id="9d3f3-161">Boîtes aux lettres</span><span class="sxs-lookup"><span data-stu-id="9d3f3-161">Mailboxes</span></span>

<span data-ttu-id="9d3f3-162">**L'onglet Boîtes** aux lettres répertorie toutes les boîtes aux lettres qui ont été identifiées comme faisant partie ou associées à l'incident.</span><span class="sxs-lookup"><span data-stu-id="9d3f3-162">The **Mailboxes** tab lists all the mailboxes that have been identified to be part of or related to the incident.</span></span> <span data-ttu-id="9d3f3-163">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="9d3f3-163">Here's an example.</span></span>

:::image type="content" source="../../media/investigate-incidents/incident-mailboxes.png" alt-text="Exemple de page Boîtes aux lettres pour un incident":::

<span data-ttu-id="9d3f3-165">Vous pouvez cocher la coche d'une boîte aux lettres pour voir la liste des alertes actives.</span><span class="sxs-lookup"><span data-stu-id="9d3f3-165">You can select the check mark for a mailbox to see a list of active alerts.</span></span> <span data-ttu-id="9d3f3-166">Sélectionnez le nom de la boîte aux lettres pour voir des détails supplémentaires sur la page Explorateur de Microsoft Defender pour Office 365.</span><span class="sxs-lookup"><span data-stu-id="9d3f3-166">Select the mailbox name to see additional mailbox details on the Explorer page for Microsoft Defender for Office 365.</span></span>

## <a name="investigations"></a><span data-ttu-id="9d3f3-167">Examens</span><span class="sxs-lookup"><span data-stu-id="9d3f3-167">Investigations</span></span>

<span data-ttu-id="9d3f3-168">**L'onglet** Enquêtes répertorie toutes les enquêtes automatisées déclenchées par les alertes dans cet incident.</span><span class="sxs-lookup"><span data-stu-id="9d3f3-168">The **Investigations** tab lists all the automated investigations triggered by alerts in this incident.</span></span> <span data-ttu-id="9d3f3-169">Les enquêtes effectuent des actions de correction ou attendent l'approbation par les analystes des actions, selon la façon dont vous avez configuré vos enquêtes automatisées pour qu'ils s'exécutent dans Microsoft Defender pour Endpoint et Defender pour Office 365.</span><span class="sxs-lookup"><span data-stu-id="9d3f3-169">The investigations will perform remediation actions or wait for analyst approval of actions, depending on how you configured your automated investigations to run in Microsoft Defender for Endpoint and Defender for Office 365.</span></span>

:::image type="content" source="../../media/investigate-incidents/incident-investigations.png" alt-text="Exemple de page Investigations pour un incident":::

<span data-ttu-id="9d3f3-171">Sélectionnez un examen pour accéder à la page Détails de l’examen pour obtenir des informations complètes sur l’état l’examen et de la correction.</span><span class="sxs-lookup"><span data-stu-id="9d3f3-171">Select an investigation to navigate to the Investigation details page to get full information on the investigation and remediation status.</span></span> <span data-ttu-id="9d3f3-172">Si des actions sont en attente d'approbation dans le cadre de l'examen, elles apparaissent dans l'onglet Actions en attente. Prendre des mesures dans le cadre de la correction des incidents.</span><span class="sxs-lookup"><span data-stu-id="9d3f3-172">If there are any actions pending for approval as part of the investigation, they will appear in the Pending actions tab. Take action as part of incident remediation.</span></span>

## <a name="evidence-and-response"></a><span data-ttu-id="9d3f3-173">Preuve et réponse</span><span class="sxs-lookup"><span data-stu-id="9d3f3-173">Evidence and Response</span></span>

<span data-ttu-id="9d3f3-174">**L'onglet Preuve et réponse** affiche tous les événements pris en charge et entités suspectes dans les alertes de l'incident.</span><span class="sxs-lookup"><span data-stu-id="9d3f3-174">The **Evidence and Response** tab shows all the supported events and suspicious entities in the alerts in the incident.</span></span> <span data-ttu-id="9d3f3-175">Voici un exemple.</span><span class="sxs-lookup"><span data-stu-id="9d3f3-175">Here's an example.</span></span>

:::image type="content" source="../../media/investigate-incidents/incident-evidence.png" alt-text="Exemple de page Preuve et réponse pour un incident":::

<span data-ttu-id="9d3f3-177">Microsoft 365 Defender examine automatiquement tous les événements pris en charge par les incidents et les entités suspectes dans les alertes, en vous fournissant des informations sur les messages électroniques, fichiers, processus, services, adresses IP et bien plus encore.</span><span class="sxs-lookup"><span data-stu-id="9d3f3-177">Microsoft 365 Defender automatically investigates all the incidents' supported events and suspicious entities in the alerts, providing you with information about the important emails, files, processes, services, IP Addresses, and more.</span></span> <span data-ttu-id="9d3f3-178">Cela vous permet de détecter et de bloquer rapidement les menaces potentielles dans l'incident.</span><span class="sxs-lookup"><span data-stu-id="9d3f3-178">This helps you quickly detect and block potential threats in the incident.</span></span>

<span data-ttu-id="9d3f3-179">Chacune des entités analysées est marquée avec un verdict (malveillant, suspect, propre) et un état de correction.</span><span class="sxs-lookup"><span data-stu-id="9d3f3-179">Each of the analyzed entities is marked with a verdict (Malicious, Suspicious, Clean) and a remediation status.</span></span> <span data-ttu-id="9d3f3-180">Cela vous permet de comprendre l’état de correction de l’intégralité de l’incident et les étapes suivantes qui peuvent être prises.</span><span class="sxs-lookup"><span data-stu-id="9d3f3-180">This helps you understand the remediation status of the entire incident and what next steps can be taken.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9d3f3-181">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="9d3f3-181">Related topics</span></span>

- [<span data-ttu-id="9d3f3-182">Vue d’ensemble des incidents</span><span class="sxs-lookup"><span data-stu-id="9d3f3-182">Incidents overview</span></span>](incidents-overview.md)
- [<span data-ttu-id="9d3f3-183">Hiérarchiser les incidents</span><span class="sxs-lookup"><span data-stu-id="9d3f3-183">Prioritize incidents</span></span>](incident-queue.md)
- [<span data-ttu-id="9d3f3-184">Gérer les incidents</span><span class="sxs-lookup"><span data-stu-id="9d3f3-184">Manage incidents</span></span>](manage-incidents.md)

