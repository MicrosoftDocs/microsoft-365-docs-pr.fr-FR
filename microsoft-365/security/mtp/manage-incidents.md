---
title: Gérer les incidents dans la Protection Microsoft contre les menaces
description: Découvrez comment attribuer, mettre à jour l’état,
keywords: incident, incidents, alertes, alertes corrélées, attribuer, mettre à jour, état, gérer, classification, microsoft, 365, m365
search.product: eADQiWindows 10XVcnh
ms.prod: microsoft-365-enterprise
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
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
ms.openlocfilehash: d6b7c754db3b43e909871a5a60fa1ab155f2d01d
ms.sourcegitcommit: 0ad0092d9c5cb2d69fc70c990a9b7cc03140611b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2019
ms.locfileid: "40806953"
---
# <a name="manage-incidents-in-microsoft-threat-protection"></a><span data-ttu-id="10bb2-104">Gérer les incidents dans la Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="10bb2-104">Manage incidents in Microsoft Threat Protection</span></span>

<span data-ttu-id="10bb2-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="10bb2-105">**Applies to:**</span></span>
- <span data-ttu-id="10bb2-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="10bb2-106">Microsoft Threat Protection</span></span>

[!INCLUDE [Prerelease information](../includes/prerelease.md)]

<span data-ttu-id="10bb2-107">La gestion des incidents est essentielle pour s’assurer que les menaces sont contenues et traitées.</span><span class="sxs-lookup"><span data-stu-id="10bb2-107">Managing incidents is critical in ensuring that threats are contained and addressed.</span></span> <span data-ttu-id="10bb2-108">La Protection Microsoft contre les menaces vous permet d’accéder à la gestion des incidents sur les appareils, chez les utilisateurs et dans les boîtes aux lettres.</span><span class="sxs-lookup"><span data-stu-id="10bb2-108">In Microsoft Threat Protection, you have access to managing incidents on devices, users, and mailboxes.</span></span> 


<span data-ttu-id="10bb2-109">Vous pouvez gérer les incidents en sélectionnant un incident dans la **file d’attente d’incidents**.</span><span class="sxs-lookup"><span data-stu-id="10bb2-109">You can manage incidents by selecting an incident from the **Incidents queue**.</span></span> 

<span data-ttu-id="10bb2-110">Vous pouvez modifier le nom d’un incident, le résoudre, déterminer sa classification et sa détermination.</span><span class="sxs-lookup"><span data-stu-id="10bb2-110">You can edit the name of an incident, resolve it, set its classification and determination.</span></span> <span data-ttu-id="10bb2-111">Vous pouvez également attribuer l’incident à vous-même, ajouter des balises d’incident et des commentaires.</span><span class="sxs-lookup"><span data-stu-id="10bb2-111">You can also assign the incident to yourself, add incident tags and comments.</span></span>

<span data-ttu-id="10bb2-112">Si, lors d’une investigation, vous devez déplacer des alertes d’un incident à un autre, vous pouvez également le faire à partir de l’onglet Alertes, ce qui permet de créer un incident plus important ou plus petit qui inclut toutes les alertes appropriées.</span><span class="sxs-lookup"><span data-stu-id="10bb2-112">In cases where while investigating you would like to move alerts from one incident to another you can also do so from the Alerts tab, thus creating a larger or smaller incident that include all relevant alerts.</span></span>

## <a name="edit-incident-name"></a><span data-ttu-id="10bb2-113">Modifier le nom de l’incident</span><span class="sxs-lookup"><span data-stu-id="10bb2-113">Edit incident name</span></span>
<span data-ttu-id="10bb2-114">Par défaut, un numéro est attribué à un incident.</span><span class="sxs-lookup"><span data-stu-id="10bb2-114">By default, an incident is assigned a number.</span></span> <span data-ttu-id="10bb2-115">Vous pouvez modifier le nom de l’incident afin de mieux l’aligner avec votre convention d’affectation de noms préférée.</span><span class="sxs-lookup"><span data-stu-id="10bb2-115">You can modify the incident name to better align with your preferred naming convention.</span></span>
 
## <a name="assign-incidents"></a><span data-ttu-id="10bb2-116">Attribuer des incidents</span><span class="sxs-lookup"><span data-stu-id="10bb2-116">Assign incidents</span></span>
<span data-ttu-id="10bb2-117">Si aucun incident n’a encore été affecté, vous pouvez sélectionner **À moi-même** pour vous l’attribuer.</span><span class="sxs-lookup"><span data-stu-id="10bb2-117">If an incident has not yet been assigned, you can select **Assign to me** to assign the incident to yourself.</span></span> <span data-ttu-id="10bb2-118">Cette action suppose l’appropriation non seulement de l’incident, mais aussi de toutes les alertes associées.</span><span class="sxs-lookup"><span data-stu-id="10bb2-118">Doing so assumes ownership of not just the incident, but also all the alerts associated with it.</span></span>

## <a name="set-status-and-classification"></a><span data-ttu-id="10bb2-119">Définir l’état et la classification</span><span class="sxs-lookup"><span data-stu-id="10bb2-119">Set status and classification</span></span>
### <a name="incident-status"></a><span data-ttu-id="10bb2-120">État de l’incident</span><span class="sxs-lookup"><span data-stu-id="10bb2-120">Incident status</span></span>
<span data-ttu-id="10bb2-121">Vous pouvez classer les incidents (comme **actifs**ou **résolus**) en modifiant leur état au fur et à mesure de l’avancement de votre enquête.</span><span class="sxs-lookup"><span data-stu-id="10bb2-121">You can categorize incidents (as **Active**, or **Resolved**) by changing their status as your investigation progresses.</span></span> <span data-ttu-id="10bb2-122">Cela vous permet d’organiser et de gérer la manière dont votre équipe peut réagir aux incidents.</span><span class="sxs-lookup"><span data-stu-id="10bb2-122">This helps you organize and manage how your team can respond to incidents.</span></span>

<span data-ttu-id="10bb2-123">Par exemple, votre analyste SOC peut passer en revue les incidents **actifs** urgents pour la journée et décider de se les attribuer pour enquête.</span><span class="sxs-lookup"><span data-stu-id="10bb2-123">For example, your SOC analyst can review the urgent **Active** incidents for the day, and decide to assign them to herself for investigation.</span></span>

<span data-ttu-id="10bb2-124">Sinon, il est possible que votre analyste SOC configure l’incident comme **résolu** si l’incident a été corrigé.</span><span class="sxs-lookup"><span data-stu-id="10bb2-124">Alternatively, your SOC analyst might set the incident as **Resolved** if the incident has been remediated.</span></span> <span data-ttu-id="10bb2-125">La résolution d’un incident ferme automatiquement toutes les alertes toujours ouvertes faisant partie de l’incident.</span><span class="sxs-lookup"><span data-stu-id="10bb2-125">Resolving an incident will automatically close all alerts that are part of the incident and still open.</span></span> 

### <a name="classification-and-determination"></a><span data-ttu-id="10bb2-126">Classification et détermination</span><span class="sxs-lookup"><span data-stu-id="10bb2-126">Classification and determination</span></span>
<span data-ttu-id="10bb2-127">Vous pouvez choisir de ne pas définir de classification ou décider de spécifier si un incident est vrai ou faux.</span><span class="sxs-lookup"><span data-stu-id="10bb2-127">You can choose not to set a classification, or decide to specify whether an incident is true or false.</span></span> <span data-ttu-id="10bb2-128">Cette opération permet à l’équipe de voir les modèles et d’en apprendre davantage.</span><span class="sxs-lookup"><span data-stu-id="10bb2-128">Doing so helps the team see patterns and learn from them.</span></span> 

## <a name="add-comments"></a><span data-ttu-id="10bb2-129">Ajouter des commentaires</span><span class="sxs-lookup"><span data-stu-id="10bb2-129">Add comments</span></span>
<span data-ttu-id="10bb2-130">Vous pouvez ajouter des commentaires et afficher les événements historiques relatifs à un incident afin de voir les modifications précédentes apportées à ce dernier.</span><span class="sxs-lookup"><span data-stu-id="10bb2-130">You can add comments and view historical events about an incident to see previous changes made to it.</span></span>

<span data-ttu-id="10bb2-131">Chaque fois qu’une modification ou un commentaire est apporté à une alerte, cet élément est enregistré dans la section Commentaires et historique.</span><span class="sxs-lookup"><span data-stu-id="10bb2-131">Whenever a change or comment is made to an alert, it is recorded in the Comments and history section.</span></span>

<span data-ttu-id="10bb2-132">Les commentaires ajoutés apparaissent instantanément dans le volet.</span><span class="sxs-lookup"><span data-stu-id="10bb2-132">Added comments instantly appear on the pane.</span></span>

## <a name="add-incident-tags"></a><span data-ttu-id="10bb2-133">Ajouter des balises d’incident</span><span class="sxs-lookup"><span data-stu-id="10bb2-133">Add incident tags</span></span>
<span data-ttu-id="10bb2-134">Vous pouvez ajouter des balises personnalisées à un incident, par exemple, pour marquer un groupe d’incidents présentant des caractéristiques communes.</span><span class="sxs-lookup"><span data-stu-id="10bb2-134">You can add custom tags to an incident, for example to flag a group of incidents with a common characteristics.</span></span> <span data-ttu-id="10bb2-135">Vous pouvez filtrer ultérieurement la file d’attente des incidents pour afficher tous ceux qui contiennent une balise spécifique.</span><span class="sxs-lookup"><span data-stu-id="10bb2-135">You can later filter the incidents queue for all incidents that contain a specific tag.</span></span>

