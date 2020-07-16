---
title: Gérer les incidents dans la Protection Microsoft contre les menaces
description: Découvrez comment attribuer, mettre à jour l’état,
keywords: incident, incidents, alertes, alertes corrélées, attribuer, mettre à jour, état, gérer, classification, microsoft, 365, m365
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
ms.openlocfilehash: f711cc2ff38f15dfd22097e37a1dec42719eb5aa
ms.sourcegitcommit: 94f2f8e3e6bc3946d8b3cf798b3eb77a49ffd12a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/16/2020
ms.locfileid: "45148113"
---
# <a name="manage-incidents-in-microsoft-threat-protection"></a><span data-ttu-id="3a3e0-104">Gérer les incidents dans la Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="3a3e0-104">Manage incidents in Microsoft Threat Protection</span></span>

<span data-ttu-id="3a3e0-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="3a3e0-105">**Applies to:**</span></span>
- <span data-ttu-id="3a3e0-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="3a3e0-106">Microsoft Threat Protection</span></span>



<span data-ttu-id="3a3e0-107">La gestion des incidents est essentielle pour s’assurer que les menaces sont contenues et traitées.</span><span class="sxs-lookup"><span data-stu-id="3a3e0-107">Managing incidents is critical in ensuring that threats are contained and addressed.</span></span> <span data-ttu-id="3a3e0-108">La Protection Microsoft contre les menaces vous permet d’accéder à la gestion des incidents sur les appareils, chez les utilisateurs et dans les boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="3a3e0-108">In Microsoft Threat Protection, you have access to managing incidents on devices, users, and mailboxes.</span></span> 


<span data-ttu-id="3a3e0-109">Vous pouvez gérer les incidents en sélectionnant un incident dans la **file d’attente d’incidents**.</span><span class="sxs-lookup"><span data-stu-id="3a3e0-109">You can manage incidents by selecting an incident from the **Incidents queue**.</span></span> 

<span data-ttu-id="3a3e0-110">Vous pouvez modifier le nom d’un incident, le résoudre, déterminer sa classification et sa détermination.</span><span class="sxs-lookup"><span data-stu-id="3a3e0-110">You can edit the name of an incident, resolve it, set its classification and determination.</span></span> <span data-ttu-id="3a3e0-111">Vous pouvez également attribuer l’incident à vous-même, ajouter des balises d’incident et des commentaires.</span><span class="sxs-lookup"><span data-stu-id="3a3e0-111">You can also assign the incident to yourself, add incident tags and comments.</span></span>

<span data-ttu-id="3a3e0-112">Si, lors d’une investigation, vous devez déplacer des alertes d’un incident à un autre, vous pouvez également le faire à partir de l’onglet Alertes, ce qui permet de créer un incident plus important ou plus petit qui inclut toutes les alertes appropriées.</span><span class="sxs-lookup"><span data-stu-id="3a3e0-112">In cases where while investigating you would like to move alerts from one incident to another you can also do so from the Alerts tab, thus creating a larger or smaller incident that include all relevant alerts.</span></span>

## <a name="edit-incident-name"></a><span data-ttu-id="3a3e0-113">Modifier le nom de l’incident</span><span class="sxs-lookup"><span data-stu-id="3a3e0-113">Edit incident name</span></span>
<span data-ttu-id="3a3e0-114">Par défaut, un numéro est attribué à un incident.</span><span class="sxs-lookup"><span data-stu-id="3a3e0-114">By default, an incident is assigned a number.</span></span> <span data-ttu-id="3a3e0-115">Vous pouvez modifier le nom de l’incident afin de mieux l’aligner avec votre convention d’affectation de noms préférée.</span><span class="sxs-lookup"><span data-stu-id="3a3e0-115">You can modify the incident name to better align with your preferred naming convention.</span></span>

> [!TIP]
> <span data-ttu-id="3a3e0-116">Pour une visibilité plus complète en un clin d’œil, l’appellation automatique des incidents, actuellement en préversion publique, génère des noms d’incidents en fonction des attributs d’alerte, tels que le nombre de points de terminaison affectés, les utilisateurs affectés, les sources de détection ou les catégories.</span><span class="sxs-lookup"><span data-stu-id="3a3e0-116">For additional visibility at-a-glance, automatic incident naming, currently in public preview, generates incident names based on alert attributes such as the number of endpoints affected, users affected, detection sources or categories.</span></span> <span data-ttu-id="3a3e0-117">Cela vous permet de comprendre rapidement l’étendue de l’incident.</span><span class="sxs-lookup"><span data-stu-id="3a3e0-117">This allows you to quickly understand the scope of the incident.</span></span>
>
> <span data-ttu-id="3a3e0-118">Par exemple : plusieurs *étapes incident sur plusieurs points de terminaison signalés par plusieurs sources.*</span><span class="sxs-lookup"><span data-stu-id="3a3e0-118">For example: *Multi-stage incident on multiple endpoints reported by multiple sources.*</span></span>
>
> <span data-ttu-id="3a3e0-119">Les incidents qui existaient avant le déploiement de la dénomination automatique des incidents ne verront pas leur nom modifié.</span><span class="sxs-lookup"><span data-stu-id="3a3e0-119">Incidents that existed prior the rollout of automatic incident naming will not have their name changed.</span></span>
>
> <span data-ttu-id="3a3e0-120">En savoir plus sur l' [activation des fonctionnalités d’aperçu](preview.md#turn-on-preview-features).</span><span class="sxs-lookup"><span data-stu-id="3a3e0-120">Learn more about [turning on preview features](preview.md#turn-on-preview-features).</span></span>

## <a name="assign-incidents"></a><span data-ttu-id="3a3e0-121">Attribuer des incidents</span><span class="sxs-lookup"><span data-stu-id="3a3e0-121">Assign incidents</span></span>
<span data-ttu-id="3a3e0-122">Si aucun incident n’a encore été affecté, vous pouvez sélectionner **À moi-même** pour vous l’attribuer.</span><span class="sxs-lookup"><span data-stu-id="3a3e0-122">If an incident has not yet been assigned, you can select **Assign to me** to assign the incident to yourself.</span></span> <span data-ttu-id="3a3e0-123">Cette action suppose l’appropriation non seulement de l’incident, mais aussi de toutes les alertes associées.</span><span class="sxs-lookup"><span data-stu-id="3a3e0-123">Doing so assumes ownership of not just the incident, but also all the alerts associated with it.</span></span>

## <a name="set-status-and-classification"></a><span data-ttu-id="3a3e0-124">Définir l’état et la classification</span><span class="sxs-lookup"><span data-stu-id="3a3e0-124">Set status and classification</span></span>
### <a name="incident-status"></a><span data-ttu-id="3a3e0-125">État de l’incident</span><span class="sxs-lookup"><span data-stu-id="3a3e0-125">Incident status</span></span>
<span data-ttu-id="3a3e0-126">Vous pouvez classer les incidents (comme **actifs**ou **résolus**) en modifiant leur état au fur et à mesure de l’avancement de votre enquête.</span><span class="sxs-lookup"><span data-stu-id="3a3e0-126">You can categorize incidents (as **Active**, or **Resolved**) by changing their status as your investigation progresses.</span></span> <span data-ttu-id="3a3e0-127">Cela vous permet d’organiser et de gérer la manière dont votre équipe peut réagir aux incidents.</span><span class="sxs-lookup"><span data-stu-id="3a3e0-127">This helps you organize and manage how your team can respond to incidents.</span></span>

<span data-ttu-id="3a3e0-128">Par exemple, votre analyste SOC peut passer en revue les incidents **actifs** urgents pour la journée et décider de se les attribuer pour enquête.</span><span class="sxs-lookup"><span data-stu-id="3a3e0-128">For example, your SOC analyst can review the urgent **Active** incidents for the day, and decide to assign them to herself for investigation.</span></span>

<span data-ttu-id="3a3e0-129">Sinon, il est possible que votre analyste SOC configure l’incident comme **résolu** si l’incident a été corrigé.</span><span class="sxs-lookup"><span data-stu-id="3a3e0-129">Alternatively, your SOC analyst might set the incident as **Resolved** if the incident has been remediated.</span></span> <span data-ttu-id="3a3e0-130">La résolution d’un incident ferme automatiquement toutes les alertes toujours ouvertes faisant partie de l’incident.</span><span class="sxs-lookup"><span data-stu-id="3a3e0-130">Resolving an incident will automatically close all alerts that are part of the incident and still open.</span></span> 

### <a name="classification-and-determination"></a><span data-ttu-id="3a3e0-131">Classification et détermination</span><span class="sxs-lookup"><span data-stu-id="3a3e0-131">Classification and determination</span></span>
<span data-ttu-id="3a3e0-132">Vous pouvez choisir de ne pas définir de classification ou décider de spécifier si un incident est vrai ou faux.</span><span class="sxs-lookup"><span data-stu-id="3a3e0-132">You can choose not to set a classification, or decide to specify whether an incident is true or false.</span></span> <span data-ttu-id="3a3e0-133">Cette opération permet à l’équipe de voir les modèles et d’en apprendre davantage.</span><span class="sxs-lookup"><span data-stu-id="3a3e0-133">Doing so helps the team see patterns and learn from them.</span></span> 

## <a name="add-comments"></a><span data-ttu-id="3a3e0-134">Ajouter des commentaires</span><span class="sxs-lookup"><span data-stu-id="3a3e0-134">Add comments</span></span>
<span data-ttu-id="3a3e0-135">Vous pouvez ajouter des commentaires et afficher les événements historiques relatifs à un incident afin de voir les modifications précédentes apportées à ce dernier.</span><span class="sxs-lookup"><span data-stu-id="3a3e0-135">You can add comments and view historical events about an incident to see previous changes made to it.</span></span>

<span data-ttu-id="3a3e0-136">Chaque fois qu’une modification ou un commentaire est apporté à une alerte, cet élément est enregistré dans la section Commentaires et historique.</span><span class="sxs-lookup"><span data-stu-id="3a3e0-136">Whenever a change or comment is made to an alert, it is recorded in the Comments and history section.</span></span>

<span data-ttu-id="3a3e0-137">Les commentaires ajoutés apparaissent instantanément dans le volet.</span><span class="sxs-lookup"><span data-stu-id="3a3e0-137">Added comments instantly appear on the pane.</span></span>

## <a name="add-incident-tags"></a><span data-ttu-id="3a3e0-138">Ajouter des balises d’incident</span><span class="sxs-lookup"><span data-stu-id="3a3e0-138">Add incident tags</span></span>
<span data-ttu-id="3a3e0-139">Vous pouvez ajouter des balises personnalisées à un incident, par exemple, pour marquer un groupe d’incidents présentant des caractéristiques communes.</span><span class="sxs-lookup"><span data-stu-id="3a3e0-139">You can add custom tags to an incident, for example to flag a group of incidents with a common characteristics.</span></span> <span data-ttu-id="3a3e0-140">Vous pouvez filtrer ultérieurement la file d’attente des incidents pour afficher tous ceux qui contiennent une balise spécifique.</span><span class="sxs-lookup"><span data-stu-id="3a3e0-140">You can later filter the incidents queue for all incidents that contain a specific tag.</span></span>