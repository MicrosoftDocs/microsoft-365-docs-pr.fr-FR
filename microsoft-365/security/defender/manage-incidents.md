---
title: Gérer les incidents dans Microsoft 365 Defender
description: Découvrez comment attribuer, mettre à jour l’état,
keywords: incident, incidents, alertes, alertes corrélées, attribuer, mettre à jour, état, gérer, classification, microsoft, 365, m365
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: macapara
author: mjcaparas
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
ms.openlocfilehash: 3edc7e52e93bc08d46536a520bf57735983f493b
ms.sourcegitcommit: 1244bbc4a3d150d37980cab153505ca462fa7ddc
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/26/2021
ms.locfileid: "51222622"
---
# <a name="manage-incidents-in-microsoft-365-defender"></a><span data-ttu-id="70299-104">Gérer les incidents dans Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="70299-104">Manage incidents in Microsoft 365 Defender</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="70299-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="70299-105">**Applies to:**</span></span>
- <span data-ttu-id="70299-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="70299-106">Microsoft 365 Defender</span></span>



<span data-ttu-id="70299-107">La gestion des incidents est essentielle pour s’assurer que les menaces sont contenues et traitées.</span><span class="sxs-lookup"><span data-stu-id="70299-107">Managing incidents is critical in ensuring that threats are contained and addressed.</span></span> <span data-ttu-id="70299-108">Dans Microsoft 365 Defender, vous avez accès à la gestion des incidents sur les appareils, les utilisateurs et les boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="70299-108">In Microsoft 365 Defender, you have access to managing incidents on devices, users, and mailboxes.</span></span> 


<span data-ttu-id="70299-109">Vous pouvez gérer les incidents en sélectionnant un incident dans la **file d’attente d’incidents**.</span><span class="sxs-lookup"><span data-stu-id="70299-109">You can manage incidents by selecting an incident from the **Incidents queue**.</span></span> 

<span data-ttu-id="70299-110">Vous pouvez modifier le nom d’un incident, le résoudre, déterminer sa classification et sa détermination.</span><span class="sxs-lookup"><span data-stu-id="70299-110">You can edit the name of an incident, resolve it, set its classification and determination.</span></span> <span data-ttu-id="70299-111">Vous pouvez également attribuer l’incident à vous-même, ajouter des balises d’incident et des commentaires.</span><span class="sxs-lookup"><span data-stu-id="70299-111">You can also assign the incident to yourself, add incident tags and comments.</span></span>

<span data-ttu-id="70299-112">Si, lors d’une investigation, vous devez déplacer des alertes d’un incident à un autre, vous pouvez également le faire à partir de l’onglet Alertes, ce qui permet de créer un incident plus important ou plus petit qui inclut toutes les alertes appropriées.</span><span class="sxs-lookup"><span data-stu-id="70299-112">In cases where while investigating you would like to move alerts from one incident to another you can also do so from the Alerts tab, thus creating a larger or smaller incident that include all relevant alerts.</span></span>

## <a name="edit-incident-name"></a><span data-ttu-id="70299-113">Modifier le nom de l’incident</span><span class="sxs-lookup"><span data-stu-id="70299-113">Edit incident name</span></span>
<span data-ttu-id="70299-114">Un nom est automatiquement attribué aux incidents en fonction des attributs d’alerte tels que le nombre de points de terminaison affectés, les utilisateurs affectés, les sources de détection ou les catégories.</span><span class="sxs-lookup"><span data-stu-id="70299-114">Incidents are automatically assigned a name based on alert attributes such as the number of endpoints affected, users affected, detection sources or categories.</span></span> <span data-ttu-id="70299-115">Cela vous permet de comprendre rapidement l’étendue de l’incident.</span><span class="sxs-lookup"><span data-stu-id="70299-115">This allows you to quickly understand the scope of the incident.</span></span>

<span data-ttu-id="70299-116">Par exemple : incident en plusieurs étapes sur plusieurs points de *terminaison signalés par plusieurs sources.*</span><span class="sxs-lookup"><span data-stu-id="70299-116">For example: *Multi-stage incident on multiple endpoints reported by multiple sources.*</span></span>

<span data-ttu-id="70299-117">Vous pouvez modifier le nom de l’incident afin de mieux l’aligner avec votre convention d’affectation de noms préférée.</span><span class="sxs-lookup"><span data-stu-id="70299-117">You can modify the incident name to better align with your preferred naming convention.</span></span>

> [!NOTE]
> <span data-ttu-id="70299-118">Les incidents qui existaient avant le déploiement de la fonctionnalité de nommage automatique des incidents conserveront leur nom.</span><span class="sxs-lookup"><span data-stu-id="70299-118">Incidents that existed prior the rollout of the automatic incident naming feature will retain their name.</span></span>



## <a name="assign-incidents"></a><span data-ttu-id="70299-119">Attribuer des incidents</span><span class="sxs-lookup"><span data-stu-id="70299-119">Assign incidents</span></span>
<span data-ttu-id="70299-120">Si aucun incident n’a encore été affecté, vous pouvez sélectionner **À moi-même** pour vous l’attribuer.</span><span class="sxs-lookup"><span data-stu-id="70299-120">If an incident has not yet been assigned, you can select **Assign to me** to assign the incident to yourself.</span></span> <span data-ttu-id="70299-121">Cette action suppose l’appropriation non seulement de l’incident, mais aussi de toutes les alertes associées.</span><span class="sxs-lookup"><span data-stu-id="70299-121">Doing so assumes ownership of not just the incident, but also all the alerts associated with it.</span></span>

## <a name="set-status-and-classification"></a><span data-ttu-id="70299-122">Définir l’état et la classification</span><span class="sxs-lookup"><span data-stu-id="70299-122">Set status and classification</span></span>
### <a name="incident-status"></a><span data-ttu-id="70299-123">État de l’incident</span><span class="sxs-lookup"><span data-stu-id="70299-123">Incident status</span></span>
<span data-ttu-id="70299-124">Vous pouvez classer les incidents (comme **actifs** ou **résolus**) en modifiant leur état au fur et à mesure de l’avancement de votre enquête.</span><span class="sxs-lookup"><span data-stu-id="70299-124">You can categorize incidents (as **Active**, or **Resolved**) by changing their status as your investigation progresses.</span></span> <span data-ttu-id="70299-125">Cela vous permet d’organiser et de gérer la manière dont votre équipe peut réagir aux incidents.</span><span class="sxs-lookup"><span data-stu-id="70299-125">This helps you organize and manage how your team can respond to incidents.</span></span>

<span data-ttu-id="70299-126">Par exemple, votre analyste SOC peut passer en revue les incidents **actifs** urgents pour la journée et décider de se les attribuer pour enquête.</span><span class="sxs-lookup"><span data-stu-id="70299-126">For example, your SOC analyst can review the urgent **Active** incidents for the day, and decide to assign them to herself for investigation.</span></span>

<span data-ttu-id="70299-127">Sinon, il est possible que votre analyste SOC configure l’incident comme **résolu** si l’incident a été corrigé.</span><span class="sxs-lookup"><span data-stu-id="70299-127">Alternatively, your SOC analyst might set the incident as **Resolved** if the incident has been remediated.</span></span> <span data-ttu-id="70299-128">La résolution d’un incident ferme automatiquement toutes les alertes toujours ouvertes faisant partie de l’incident.</span><span class="sxs-lookup"><span data-stu-id="70299-128">Resolving an incident will automatically close all alerts that are part of the incident and still open.</span></span> 

### <a name="classification-and-determination"></a><span data-ttu-id="70299-129">Classification et détermination</span><span class="sxs-lookup"><span data-stu-id="70299-129">Classification and determination</span></span>
<span data-ttu-id="70299-130">Vous pouvez choisir de ne pas définir de classification ou décider de spécifier si un incident est vrai ou faux.</span><span class="sxs-lookup"><span data-stu-id="70299-130">You can choose not to set a classification, or decide to specify whether an incident is true or false.</span></span> <span data-ttu-id="70299-131">Cette opération permet à l’équipe de voir les modèles et d’en apprendre davantage.</span><span class="sxs-lookup"><span data-stu-id="70299-131">Doing so helps the team see patterns and learn from them.</span></span> 

## <a name="add-comments"></a><span data-ttu-id="70299-132">Ajouter des commentaires</span><span class="sxs-lookup"><span data-stu-id="70299-132">Add comments</span></span>
<span data-ttu-id="70299-133">Vous pouvez ajouter des commentaires et afficher les événements historiques relatifs à un incident afin de voir les modifications précédentes apportées à ce dernier.</span><span class="sxs-lookup"><span data-stu-id="70299-133">You can add comments and view historical events about an incident to see previous changes made to it.</span></span>

<span data-ttu-id="70299-134">Chaque fois qu’une modification ou un commentaire est apporté à une alerte, cet élément est enregistré dans la section Commentaires et historique.</span><span class="sxs-lookup"><span data-stu-id="70299-134">Whenever a change or comment is made to an alert, it is recorded in the Comments and history section.</span></span>

<span data-ttu-id="70299-135">Les commentaires ajoutés apparaissent instantanément dans le volet.</span><span class="sxs-lookup"><span data-stu-id="70299-135">Added comments instantly appear on the pane.</span></span>

## <a name="add-incident-tags"></a><span data-ttu-id="70299-136">Ajouter des balises d’incident</span><span class="sxs-lookup"><span data-stu-id="70299-136">Add incident tags</span></span>
<span data-ttu-id="70299-137">Vous pouvez ajouter des balises personnalisées à un incident, par exemple pour baliser un groupe d’incidents avec une caractéristique commune.</span><span class="sxs-lookup"><span data-stu-id="70299-137">You can add custom tags to an incident, for example to flag a group of incidents with a common characteristic.</span></span> <span data-ttu-id="70299-138">Vous pouvez filtrer ultérieurement la file d’attente des incidents pour afficher tous ceux qui contiennent une balise spécifique.</span><span class="sxs-lookup"><span data-stu-id="70299-138">You can later filter the incidents queue for all incidents that contain a specific tag.</span></span>
