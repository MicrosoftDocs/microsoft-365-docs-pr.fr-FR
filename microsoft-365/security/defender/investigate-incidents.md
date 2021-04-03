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
ms.openlocfilehash: f6b085f200d3b0c71bb3608f8e5ba9ed85632676
ms.sourcegitcommit: 582555d2b4ef5f2e2494ffdeab2c1d49e5d6b724
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51500327"
---
# <a name="investigate-incidents-in-microsoft-365-defender"></a><span data-ttu-id="6da27-104">Examiner les incidents dans Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="6da27-104">Investigate incidents in Microsoft 365 Defender</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="6da27-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="6da27-105">**Applies to:**</span></span>

- <span data-ttu-id="6da27-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="6da27-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="6da27-107">Microsoft 365 Defender regroupe toutes les alertes, biens, enquêtes et preuves connexes sur vos appareils, utilisateurs et boîtes aux lettres pour vous donner une vue d’ensemble complète d’une attaque.</span><span class="sxs-lookup"><span data-stu-id="6da27-107">Microsoft 365 Defender aggregates all related alerts, assets, investigations and evidence from across your devices, users, and mailboxes to give you a comprehensive look into the entire breadth of an attack.</span></span>

<span data-ttu-id="6da27-108">Examinez les alertes qui affectent votre réseau, déterminez leur signification et rassemblez des preuves associées aux incidents pour mettre en place une formule corrective efficace.</span><span class="sxs-lookup"><span data-stu-id="6da27-108">Investigate the alerts that affect your network, understand what they mean, and collate evidence associated with the incidents so that you can devise an effective remediation plan.</span></span>

## <a name="investigate-an-incident"></a><span data-ttu-id="6da27-109">Examiner un incident</span><span class="sxs-lookup"><span data-stu-id="6da27-109">Investigate an incident</span></span>

1. <span data-ttu-id="6da27-110">Sélectionnez un incident dans la file d’attente des incidents.</span><span class="sxs-lookup"><span data-stu-id="6da27-110">Select an incident from the incident queue.</span></span> <BR> <span data-ttu-id="6da27-111">Un panneau latéral s’ouvre et donne un aperçu des informations importantes telles que l’état, la gravité, les catégories et les entités impactées.</span><span class="sxs-lookup"><span data-stu-id="6da27-111">A side panel opens and gives a preview of important information such as status, severity, categories, and the impacted entities.</span></span>

    ![Image du volet latéral de l’incident](../../media/incident-side-panel.png)

2. <span data-ttu-id="6da27-113">Sélectionnez **Ouvrir la page incident**.</span><span class="sxs-lookup"><span data-stu-id="6da27-113">Select **Open incident page**.</span></span> <BR> <span data-ttu-id="6da27-114">Cette action ouvre la page d’incident dans laquelle vous trouverez plus d’informations sur les incidents, les commentaires et les actions, les onglets (vue d’ensemble, alertes, appareils, utilisateurs, enquêtes, preuves).</span><span class="sxs-lookup"><span data-stu-id="6da27-114">This opens the incident page where you'll find more information incident details, comments, and actions, tabs (overview, alerts, devices, users, investigations, evidence).</span></span>

3. <span data-ttu-id="6da27-115">Examinez les alertes, les appareils, les utilisateurs et les autres entités impliquées dans l’incident.</span><span class="sxs-lookup"><span data-stu-id="6da27-115">Review the alerts, devices, users, other entities involved in the incident.</span></span>

## <a name="incident-overview"></a><span data-ttu-id="6da27-116">Présentation de l’incident</span><span class="sxs-lookup"><span data-stu-id="6da27-116">Incident overview</span></span>

<span data-ttu-id="6da27-117">La page de présentation vous permet d’accéder à un instantané de l’événement.</span><span class="sxs-lookup"><span data-stu-id="6da27-117">The overview page gives you a snapshot glance into the top things to notice about the incident.</span></span>

![Image de la page de présentation des incidents](../../media/incidents-overview.png)

<span data-ttu-id="6da27-119">Les catégories d’attaque vous donnent une vue visuelle et numérique de l’avancement de l’attaque par rapport à la chaîne d’attaque.</span><span class="sxs-lookup"><span data-stu-id="6da27-119">The attack categories give you a visual and numeric view of how advanced the attack has progressed against the kill chain.</span></span> <span data-ttu-id="6da27-120">Comme avec d’autres produits de sécurité Microsoft, Microsoft 365 Defender est aligné sur l’infrastructure [MITRE ATT&&trade; CK.](https://attack.mitre.org/)</span><span class="sxs-lookup"><span data-stu-id="6da27-120">As with other Microsoft security products, Microsoft 365 Defender is aligned to the [MITRE ATT&CK&trade;](https://attack.mitre.org/) framework.</span></span>

<span data-ttu-id="6da27-121">La section l'étendue fournit la liste des principales ressources affectées à cet incident.</span><span class="sxs-lookup"><span data-stu-id="6da27-121">The scope section gives you a list of top impacted assets that are part of this incident.</span></span> <span data-ttu-id="6da27-122">S’il existe des informations spécifiques sur cet élément (par exemple, niveau de risque, priorité d’examen, et balisage sur les éléments) qui s’affichent également dans cette section.</span><span class="sxs-lookup"><span data-stu-id="6da27-122">If there is specific information regarding this asset, such as risk level, investigation priority as well as any tagging on the assets this will also surface in this section.</span></span>

<span data-ttu-id="6da27-123">La chronologie des alertes fournit un aperçu de l’ordre chronologique dans lequel les alertes se sont produites, ainsi que les raisons pour lesquelles ces alertes sont liées à cet incident.</span><span class="sxs-lookup"><span data-stu-id="6da27-123">The alerts timeline provides a sneak peek into the chronological order in which the alerts occurred, as well as the reasons that these alerts linked to this incident.</span></span>

<span data-ttu-id="6da27-124">Enfin, la section preuves fournit un résumé du nombre d’artefacts différents qui ont été inclus dans l’incident et de leur état de correction, pour que vous puissiez identifier immédiatement toute action nécessaire à la fin de l’opération.</span><span class="sxs-lookup"><span data-stu-id="6da27-124">And last - the evidence section provides a summary of how many different artifacts were included in the incident and their remediation status, so you can immediately identify if any action is needed on your end.</span></span>

<span data-ttu-id="6da27-125">Cette vue d’ensemble peut vous aider à procéder au triage initial de l’incident en fournissant un aperçu des principales caractéristiques de l’incident que vous devez connaître.</span><span class="sxs-lookup"><span data-stu-id="6da27-125">This overview can assist in the initial triage of the incident by providing insight to the top characteristics of the incident that you should be aware of.</span></span>

## <a name="alerts"></a><span data-ttu-id="6da27-126">Alertes</span><span class="sxs-lookup"><span data-stu-id="6da27-126">Alerts</span></span>

<span data-ttu-id="6da27-127">Vous pouvez afficher toutes les alertes liées à l’incident et d’autres informations les concernant, telles que la gravité, les entités impliquées dans l’alerte, la source des alertes (Microsoft Defender pour l’identité, Microsoft Defender pour endpoint, Microsoft Defender pour Office 365) et la raison pour laquelle elles ont été liées.</span><span class="sxs-lookup"><span data-stu-id="6da27-127">You can view all the alerts related to the incident and other information about them such as severity, entities that were involved in the alert, the source of the alerts (Microsoft Defender for Identity, Microsoft Defender for Endpoint, Microsoft Defender for Office 365) and the reason they were linked together.</span></span>

![Image de la page alertes d’incident](../../media/incident-alerts.png)

<span data-ttu-id="6da27-129">Par défaut, les alertes sont classées par ordre chronologique, pour vous permettre de consulter d’abord l’attaque au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="6da27-129">By default, the alerts are ordered chronologically, to allow you to first view how the attack played out over time.</span></span> <span data-ttu-id="6da27-130">Cliquez sur chaque alerte pour vous diriger vers la page d’alerte pertinente dans laquelle vous pouvez effectuer un examen approfondi de cette alerte.</span><span class="sxs-lookup"><span data-stu-id="6da27-130">Clicking on each alert will lead you to the relevant alert page where you can conduct an in-depth investigation of that alert.</span></span> <span data-ttu-id="6da27-131">Découvrez comment utiliser les pages d’alerte et la file d’attente d’alerte unifiée dans [Examiner les alertes](investigate-alerts.md)</span><span class="sxs-lookup"><span data-stu-id="6da27-131">Learn how to use alert pages and the unified alert queue in [Investigate alerts](investigate-alerts.md)</span></span>

## <a name="devices"></a><span data-ttu-id="6da27-132">Appareils</span><span class="sxs-lookup"><span data-stu-id="6da27-132">Devices</span></span>

<span data-ttu-id="6da27-133">L’onglet appareils répertorie tous les appareils pour lesquels des alertes liées à l’incident sont affichées.</span><span class="sxs-lookup"><span data-stu-id="6da27-133">The devices tab lists all the devices where alerts related to the incident are seen.</span></span>

<span data-ttu-id="6da27-134">En cliquant sur le nom de l’ordinateur sur lequel l’attaque a eu lieu, vous d’accéder à la page de l’ordinateur dans laquelle vous pouvez voir les alertes qui ont été déclenchées et les événements connexes fournis pour simplifier l’examen.</span><span class="sxs-lookup"><span data-stu-id="6da27-134">Clicking the name of the machine where the attack was conducted navigates you to its Machine page where you can see alerts that were triggered on it and related events provided to ease investigation.</span></span>

![Image de l’onglet ordinateurs d’un incident](../../media/incident-machines.png)

<span data-ttu-id="6da27-136">La sélection de l’onglet chronologie vous permet de faire défiler la chronologie de l’ordinateur et d’afficher tous les événements et comportements observés sur l’ordinateur dans l’ordre chronologique, accompagnés des alertes générées.</span><span class="sxs-lookup"><span data-stu-id="6da27-136">Selecting the Timeline tab enables you to scroll through the machine timeline and view all events and behaviors observed on the machine in chronological order, interspersed with the alerts raised.</span></span>

## <a name="users"></a><span data-ttu-id="6da27-137">Utilisateurs</span><span class="sxs-lookup"><span data-stu-id="6da27-137">Users</span></span>

<span data-ttu-id="6da27-138">Consultez la liste des utilisateurs qui ont été identifiés comme faisant partie d'un incident donné ou y étant liés.</span><span class="sxs-lookup"><span data-stu-id="6da27-138">See users that have been identified to be part of, or related to a given incident.</span></span>

<span data-ttu-id="6da27-139">En cliquant sur le nom d'utilisateur, vous accédez à la page Cloud App Security de l'utilisateur où un examen plus approfondie peut être effectuée.</span><span class="sxs-lookup"><span data-stu-id="6da27-139">Clicking the username navigates you to the user's Cloud App Security page where further investigation can be conducted.</span></span>

![Image de l’onglet utilisateurs d’un incident](../../media/incident-users.png)

## <a name="mailboxes"></a><span data-ttu-id="6da27-141">Boîtes aux lettres</span><span class="sxs-lookup"><span data-stu-id="6da27-141">Mailboxes</span></span>

<span data-ttu-id="6da27-142">Examinez les boîtes aux lettres qui ont été identifiés comme faisant partie d'un incident ou y étant liés.</span><span class="sxs-lookup"><span data-stu-id="6da27-142">Investigate mailboxes that's been identified to be part of, or related to an incident.</span></span> <span data-ttu-id="6da27-143">Pour poursuivre le travail d’investigation, la sélection de l’alerte liée à la messagerie ouvre Microsoft Defender pour Office 365 où vous pouvez prendre des mesures correctives.</span><span class="sxs-lookup"><span data-stu-id="6da27-143">To do further investigative work, selecting the mail-related alert will open Microsoft Defender for Office 365 where you can take remediation actions.</span></span>

![Image de l’onglet boîte aux lettres d’un incident](../../media/incident-mailboxes.png)

## <a name="investigations"></a><span data-ttu-id="6da27-145">Examens</span><span class="sxs-lookup"><span data-stu-id="6da27-145">Investigations</span></span>

<span data-ttu-id="6da27-146">Sélectionnez **Examens** pour voir toutes les enquêtes automatisées déclenchées par des alertes dans cet incident.</span><span class="sxs-lookup"><span data-stu-id="6da27-146">Select **Investigations** to see all the automated investigations triggered by alerts in this incident.</span></span> <span data-ttu-id="6da27-147">Les enquêtes effectuent des actions de correction ou attendent l’approbation par les analystes des actions, selon la façon dont vous avez configuré vos enquêtes automatisées pour qu’ils s’exécutent dans Microsoft Defender pour Endpoint et Defender pour Office 365.</span><span class="sxs-lookup"><span data-stu-id="6da27-147">The investigations will perform remediation actions or wait for analyst approval of actions, depending on how you configured your automated investigations to run in Microsoft Defender for Endpoint and Defender for Office 365.</span></span>

![Image de l’onglet examens d’un incident](../../media/incident-investigations.png)

<span data-ttu-id="6da27-149">Sélectionnez un examen pour accéder à la page Détails de l’examen pour obtenir des informations complètes sur l’état l’examen et de la correction.</span><span class="sxs-lookup"><span data-stu-id="6da27-149">Select an investigation to navigate to the Investigation details page to get full information on the investigation and remediation status.</span></span> <span data-ttu-id="6da27-150">Si des actions sont en attente d’approbation dans le cadre de l’examen, elles apparaissent dans l’onglet Actions en attente. Prendre des mesures dans le cadre de la correction des incidents.</span><span class="sxs-lookup"><span data-stu-id="6da27-150">If there are any actions pending for approval as part of the investigation, they will appear in the Pending actions tab. Take action as part of incident remediation.</span></span>

## <a name="evidence"></a><span data-ttu-id="6da27-151">Évidence</span><span class="sxs-lookup"><span data-stu-id="6da27-151">Evidence</span></span>

<span data-ttu-id="6da27-152">Microsoft 365 Defender examine automatiquement tous les événements pris en charge par les incidents et les entités suspectes dans les alertes, en vous fournissant des réponse automatiques et des informations sur les fichiers, processus, services, e-mails et bien plus encore.</span><span class="sxs-lookup"><span data-stu-id="6da27-152">Microsoft 365 Defender automatically investigates all the incidents' supported events and suspicious entities in the alerts, providing you with autoresponse and information about the important files, processes, services, emails, and more.</span></span> <span data-ttu-id="6da27-153">Cela permet de détecter et de bloquer rapidement les menaces potentielles dans l’incident.</span><span class="sxs-lookup"><span data-stu-id="6da27-153">This helps quickly detect and block potential threats in the incident.</span></span>

![Image de l’onglet preuve d’un incident](../../media/incident-evidence.png)

<span data-ttu-id="6da27-155">Chacune des entités analysées est signalée par un verdict (malveillant, Suspect, Sain) ainsi qu’un état de correction.</span><span class="sxs-lookup"><span data-stu-id="6da27-155">Each of the analyzed entities will be marked with a verdict (Malicious, Suspicious, Clean) as well as a remediation status.</span></span> <span data-ttu-id="6da27-156">Cela vous permet de comprendre l’état de la correction de l’ensemble de l’incident et les prochaines étapes à suivre pour la correction.</span><span class="sxs-lookup"><span data-stu-id="6da27-156">This assists you in understanding the remediation status of the entire incident and what are the next steps that can be taken to further remediate.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6da27-157">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="6da27-157">Related topics</span></span>

- [<span data-ttu-id="6da27-158">Vue d’ensemble des incidents</span><span class="sxs-lookup"><span data-stu-id="6da27-158">Incidents overview</span></span>](incidents-overview.md)
- [<span data-ttu-id="6da27-159">Hiérarchiser les incidents</span><span class="sxs-lookup"><span data-stu-id="6da27-159">Prioritize incidents</span></span>](incident-queue.md)
- [<span data-ttu-id="6da27-160">Gérer les incidents</span><span class="sxs-lookup"><span data-stu-id="6da27-160">Manage incidents</span></span>](manage-incidents.md)

