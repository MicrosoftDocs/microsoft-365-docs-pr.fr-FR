---
title: Enquêter sur les incidents dans la Protection Microsoft contre les menaces
description: Analyser les incidents liés aux appareils, aux utilisateurs et aux boîtes aux lettres.
keywords: incident, incidents, ordinateurs, appareils, utilisateurs, identités, courrier, courrier électronique, boîte aux lettres, investigation, graphique, preuves
search.product: eADQiWindows 10XVcnh
ms.prod: microsoft-365-enterprise
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: macapara
author: mjcaparas
ms.localizationpriority: medium
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: conceptual
search.appverid:
- MOE150
- MET150
ms.openlocfilehash: 7e0e98c94f66e2cac9300a65d0000b4447ec6d2b
ms.sourcegitcommit: 74bf600424d0cb7b9d16b4f391aeda7875058be1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/24/2020
ms.locfileid: "42235103"
---
# <a name="investigate-incidents-in-microsoft-threat-protection"></a><span data-ttu-id="2a2bb-104">Enquêter sur les incidents dans la Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="2a2bb-104">Investigate incidents in Microsoft Threat Protection</span></span>

<span data-ttu-id="2a2bb-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="2a2bb-105">**Applies to:**</span></span>
- <span data-ttu-id="2a2bb-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="2a2bb-106">Microsoft Threat Protection</span></span>




<span data-ttu-id="2a2bb-107">La Protection Microsoft contre les menaces regroupe toutes les alertes, ressources, examens et preuves connexes provenant de vos appareils, utilisateurs et boîtes aux lettres pour vous offrir une vue d’ensemble complète de la gamme d’attaques.</span><span class="sxs-lookup"><span data-stu-id="2a2bb-107">Microsoft Threat Protection aggregates all related alerts, assets, investigations and evidence from across your devices, users, and mailboxes to give you a comprehensive look into the entire breadth of an attack.</span></span> 

<span data-ttu-id="2a2bb-108">Examinez les alertes qui affectent votre réseau, déterminez leur signification et rassemblez des preuves associées aux incidents pour mettre en place une formule corrective efficace.</span><span class="sxs-lookup"><span data-stu-id="2a2bb-108">Investigate the alerts that affect your network, understand what they mean, and collate evidence associated with the incidents so that you can devise an effective remediation plan.</span></span> 

## <a name="investigate-an-incident"></a><span data-ttu-id="2a2bb-109">Examiner un incident</span><span class="sxs-lookup"><span data-stu-id="2a2bb-109">Investigate an incident</span></span>

1. <span data-ttu-id="2a2bb-110">Sélectionnez un incident dans la file d’attente des incidents.</span><span class="sxs-lookup"><span data-stu-id="2a2bb-110">Select an incident from the incident queue.</span></span> <BR> <span data-ttu-id="2a2bb-111">Cette opération ouvre un volet latéral et donne un aperçu des informations importantes telles que l’État, la gravité, les catégories et les entités affectées.</span><span class="sxs-lookup"><span data-stu-id="2a2bb-111">This opens a side panel and gives a preview of important information such as status, severity, categories, and the impacted entities.</span></span>

    ![Image du volet latéral de l’incident](../../media/incident-side-panel.png)

2. <span data-ttu-id="2a2bb-113">Sélectionnez **Ouvrir la page incident**.</span><span class="sxs-lookup"><span data-stu-id="2a2bb-113">Select **Open incident page**.</span></span> <BR> <span data-ttu-id="2a2bb-114">La page incident s’ouvre, dans laquelle vous trouverez des informations supplémentaires sur l’incident, des commentaires et des actions, des onglets (vue d’ensemble, alertes, appareils, utilisateurs, examens, preuves).</span><span class="sxs-lookup"><span data-stu-id="2a2bb-114">This opens the incident page where you'll find more information incident details, comments and actions, tabs (overview, alerts, devices, users, investigations, evidence).</span></span>

3. <span data-ttu-id="2a2bb-115">Examinez les alertes, les appareils, les utilisateurs et les autres entités impliquées dans l’incident.</span><span class="sxs-lookup"><span data-stu-id="2a2bb-115">Review the alerts, devices, users, other entities involved in the incident.</span></span>

## <a name="incident-overview"></a><span data-ttu-id="2a2bb-116">Présentation de l’incident</span><span class="sxs-lookup"><span data-stu-id="2a2bb-116">Incident overview</span></span> 
<span data-ttu-id="2a2bb-117">La page de présentation vous permet d’accéder à un instantané de l’événement.</span><span class="sxs-lookup"><span data-stu-id="2a2bb-117">The overview page gives you a snapshot glance into the top things to notice about the incident.</span></span>


![Image de la page de présentation des incidents](../../media/incidents-overview.png)


<span data-ttu-id="2a2bb-119">Les catégories d’attaques vous donnent une vue visuelle et numérique de l’avancement de l’attaque par rapport à la chaîne de terminaison.</span><span class="sxs-lookup"><span data-stu-id="2a2bb-119">The attack categories give you visual and numeric view of how advanced the attack has progressed against the kill chain.</span></span> <span data-ttu-id="2a2bb-120">Comme pour les autres produits de sécurité Microsoft, la Protection Microsoft contre les menaces est alignée à l’infrastructure [MITRE ATT&CK&trade;](https://attack.mitre.org/).</span><span class="sxs-lookup"><span data-stu-id="2a2bb-120">As with other Microsoft security products, Microsoft Threat Protection is aligned to the [MITRE ATT&CK&trade;](https://attack.mitre.org/) framework.</span></span> 

<span data-ttu-id="2a2bb-121">La section l'étendue fournit la liste des principales ressources affectées à cet incident.</span><span class="sxs-lookup"><span data-stu-id="2a2bb-121">The scope section gives you a list of top impacted assets that are part of this incident.</span></span> <span data-ttu-id="2a2bb-122">S’il existe des informations spécifiques sur cet élément (par exemple, niveau de risque, priorité d’examen, et balisage sur les éléments) qui s’affichent également dans cette section.</span><span class="sxs-lookup"><span data-stu-id="2a2bb-122">If there is specific information regarding this asset, such as risk level, investigation priority as well as any tagging on the assets this will also surface in this section.</span></span>

<span data-ttu-id="2a2bb-123">La chronologie des alertes fournit un aperçu de l’ordre chronologique dans lequel les alertes se sont produites, ainsi que les raisons pour lesquelles ces alertes sont liées à cet incident.</span><span class="sxs-lookup"><span data-stu-id="2a2bb-123">The alerts timeline provides a sneak peek into the chronological order in which the alerts occurred, as well as the reasons that these alerts linked to this incident.</span></span>

<span data-ttu-id="2a2bb-124">Enfin, la section preuves fournit un résumé du nombre d’artefacts différents qui ont été inclus dans l’incident et de leur état de correction, pour que vous puissiez identifier immédiatement toute action nécessaire à la fin de l’opération.</span><span class="sxs-lookup"><span data-stu-id="2a2bb-124">And last - the evidence section provides a summary of how many different artifacts were included in the incident and their remediation status, so you can immediately identify if any action is needed on your end.</span></span> 

<span data-ttu-id="2a2bb-125">Cette vue d’ensemble peut vous aider à procéder au triage initial de l’incident en fournissant un aperçu des principales caractéristiques de l’incident que vous devez connaître.</span><span class="sxs-lookup"><span data-stu-id="2a2bb-125">This overview can assist in the initial triage of the incident by providing insight to the top characteristics of the incident that you should be aware of.</span></span> 


## <a name="alerts"></a><span data-ttu-id="2a2bb-126">Alertes</span><span class="sxs-lookup"><span data-stu-id="2a2bb-126">Alerts</span></span> 
<span data-ttu-id="2a2bb-127">Vous pouvez afficher toutes les alertes relatives à l’incident et d’autres informations les concernant, telles que la gravité, les entités impliquées dans l’alerte, la source des alertes (Azure - Protection avancée contre les menaces, Microsoft Defender - Protection avancée contre les menaces, Office 365 - Protection avancée contre les menaces) et la raison pour laquelle ils ont été associés.</span><span class="sxs-lookup"><span data-stu-id="2a2bb-127">You can view all the alerts related to the incident and other information about them such as severity, entities that were involved in the alert, the source of the alerts (Azure ATP, Microsoft Defender ATP , Office  365 ATP) and the reason they were linked together.</span></span> 

![Image de la page alertes d’incident](../../media/incident-alerts.png)

<span data-ttu-id="2a2bb-129">Par défaut, les alertes sont classées par ordre chronologique, pour vous permettre de consulter d’abord l’attaque au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="2a2bb-129">By default, the alerts are ordered chronologically, to allow you to first view how the attack played out over time.</span></span> <span data-ttu-id="2a2bb-130">En cliquant sur chaque alerte, vous accédez à la page d'alerte correspondante sur laquelle vous pouvez effectuer un examen approfondi de cette alerte.</span><span class="sxs-lookup"><span data-stu-id="2a2bb-130">Clicking on each alert will lead you to the relevant alert page where you can conduct an in depth investigation of that alert.</span></span> 

## <a name="devices"></a><span data-ttu-id="2a2bb-131">Appareils</span><span class="sxs-lookup"><span data-stu-id="2a2bb-131">Devices</span></span> 
<span data-ttu-id="2a2bb-132">L’onglet appareils répertorie tous les appareils pour lesquels des alertes liées à l’incident sont affichées.</span><span class="sxs-lookup"><span data-stu-id="2a2bb-132">The devices tab lists all the devices where alerts related to the incident are seen.</span></span> 

<span data-ttu-id="2a2bb-133">En cliquant sur le nom de l’ordinateur sur lequel l’attaque a eu lieu, vous d’accéder à la page de l’ordinateur dans laquelle vous pouvez voir les alertes qui ont été déclenchées et les événements connexes fournis pour simplifier l’examen.</span><span class="sxs-lookup"><span data-stu-id="2a2bb-133">Clicking the name of the machine where the attack was conducted navigates you to its Machine page where you can see alerts that were triggered on it and related events provided to ease investigation.</span></span> 

![Image de l’onglet ordinateurs d’un incident](../../media/incident-machines.png)

<span data-ttu-id="2a2bb-135">La sélection de l’onglet chronologie vous permet de faire défiler la chronologie de l’ordinateur et d’afficher tous les événements et comportements observés sur l’ordinateur dans l’ordre chronologique, accompagnés des alertes générées.</span><span class="sxs-lookup"><span data-stu-id="2a2bb-135">Selecting the Timeline tab enables you to scroll through the machine timeline and view all events and behaviors observed on the machine in chronological order, interspersed with the alerts raised.</span></span> 


## <a name="users"></a><span data-ttu-id="2a2bb-136">Utilisateurs</span><span class="sxs-lookup"><span data-stu-id="2a2bb-136">Users</span></span> 
<span data-ttu-id="2a2bb-137">Consultez la liste des utilisateurs qui ont été identifiés comme faisant partie d'un incident donné ou y étant liés.</span><span class="sxs-lookup"><span data-stu-id="2a2bb-137">See users that have been identified to be part of, or related to a given incident.</span></span> 

<span data-ttu-id="2a2bb-138">En cliquant sur le nom d'utilisateur, vous accédez à la page Cloud App Security de l'utilisateur où un examen plus approfondie peut être effectuée.</span><span class="sxs-lookup"><span data-stu-id="2a2bb-138">Clicking the username navigates you to the user's Cloud App Security page where further investigation can be conducted.</span></span>


![Image de l’onglet utilisateurs d’un incident](../../media/incident-users.png)

## <a name="mailboxes"></a><span data-ttu-id="2a2bb-140">Boîtes aux lettres</span><span class="sxs-lookup"><span data-stu-id="2a2bb-140">Mailboxes</span></span>
<span data-ttu-id="2a2bb-141">Examinez les boîtes aux lettres qui ont été identifiés comme faisant partie d'un incident ou y étant liés.</span><span class="sxs-lookup"><span data-stu-id="2a2bb-141">Investigate mailboxes that's been identified to be part of, or related to an incident.</span></span> <span data-ttu-id="2a2bb-142">Pour approfondir l’examen, la sélection de l’alerte liée au courrier permet d’ouvrir Office 365 - Protection avancée contre les menaces dans laquelle vous pouvez prendre des actions de correction.</span><span class="sxs-lookup"><span data-stu-id="2a2bb-142">To do further investigative work, selecting the mail related alert will open Office 365 Advanced Threat Protection where you can take remediation actions.</span></span>


![Image de l’onglet boîte aux lettres d’un incident](../../media/incident-mailboxes.png)

## <a name="investigations"></a><span data-ttu-id="2a2bb-144">Examens</span><span class="sxs-lookup"><span data-stu-id="2a2bb-144">Investigations</span></span>
<span data-ttu-id="2a2bb-145">Sélectionnez **Examens** pour afficher toutes les examens automatisées annulées par alertes dans cet incident.</span><span class="sxs-lookup"><span data-stu-id="2a2bb-145">Select **Investigations** to see all the automated investigation striggered by alerts in this incident.</span></span> <span data-ttu-id="2a2bb-146">Les examens effectuent des actions de correction ou attendent l’approbation d’analystes d’actions, en fonction de la manière dont vous avez configuré vos examens automatisés pour qu’ils s’exécutent dans Microsoft Defender - Protection contre les menaces et Office 365 - Protection avancée contre les menaces.</span><span class="sxs-lookup"><span data-stu-id="2a2bb-146">The investigations will perform remediation actions or wait for analyst approval of actions, depending on how you configured your automated investigations to run in Microsoft Defender ATP and Office 365 Advanced Threat Protection.</span></span>

![Image de l’onglet examens d’un incident](../../media/incident-investigations.png)


<span data-ttu-id="2a2bb-148">Sélectionnez un examen pour accéder à la page Détails de l’examen pour obtenir des informations complètes sur l’état l’examen et de la correction.</span><span class="sxs-lookup"><span data-stu-id="2a2bb-148">Select an investigation to navigate to the Investigation details page to get full information on the investigation and remediation status.</span></span> <span data-ttu-id="2a2bb-149">S’il existe des actions en attente d’approbation dans le cadre de l’examen, celles-ci s’affichent dans l’onglet actions en attente. Effectuez des actions dans le cadre de la correction des incidents.</span><span class="sxs-lookup"><span data-stu-id="2a2bb-149">If there are any actions pending for approval as part of the investigation they will appear in the Pending actions tab. Take action as part of incident remediation.</span></span>


## <a name="evidence"></a><span data-ttu-id="2a2bb-150">Évidence</span><span class="sxs-lookup"><span data-stu-id="2a2bb-150">Evidence</span></span>
<span data-ttu-id="2a2bb-151">La Protection Microsoft contre les menaces examine automatiquement tous les événements et entités suspects pris en charge par les incidents dans les alertes, et vous fournit des réponses automatiques et des informations sur les fichiers, processus, services, courriers électroniques et bien plus encore.</span><span class="sxs-lookup"><span data-stu-id="2a2bb-151">Microsoft Threat Protection automatically investigates all the incidents' supported events and suspicious entities in the alerts, providing you with auto-response and information about the important files, processes, services, emails, and more.</span></span> <span data-ttu-id="2a2bb-152">Cela permet de détecter et de bloquer rapidement les menaces potentielles dans l’incident.</span><span class="sxs-lookup"><span data-stu-id="2a2bb-152">This helps quickly detect and block potential threats in the incident.</span></span> 

![Image de l’onglet preuve d’un incident](../../media/incident-evidence.png)

<span data-ttu-id="2a2bb-154">Chacune des entités analysées est signalée par un verdict (malveillant, Suspect, Sain) ainsi qu’un état de correction.</span><span class="sxs-lookup"><span data-stu-id="2a2bb-154">Each of the analyzed entities will be marked with a verdict (Malicious, Suspicious, Clean) as well as a remediation status.</span></span> <span data-ttu-id="2a2bb-155">Cela vous permet de comprendre l’état de la correction de l’ensemble de l’incident et les prochaines étapes à suivre pour la correction.</span><span class="sxs-lookup"><span data-stu-id="2a2bb-155">This assists you in understanding the remediation status of the entire incident and what are the next steps that can be taken to further remediate.</span></span>


## <a name="related-topics"></a><span data-ttu-id="2a2bb-156">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="2a2bb-156">Related topics</span></span>
- [<span data-ttu-id="2a2bb-157">Vue d’ensemble des incidents</span><span class="sxs-lookup"><span data-stu-id="2a2bb-157">Incidents overview</span></span>](incidents-overview.md)
- [<span data-ttu-id="2a2bb-158">Hiérarchiser les incidents</span><span class="sxs-lookup"><span data-stu-id="2a2bb-158">Prioritize incidents</span></span>](incident-queue.md)
- [<span data-ttu-id="2a2bb-159">Gérer les incidents</span><span class="sxs-lookup"><span data-stu-id="2a2bb-159">Manage incidents</span></span>](manage-incidents.md)
