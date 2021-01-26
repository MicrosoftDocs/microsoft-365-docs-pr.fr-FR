---
title: 'Gérer les rubriques dans le centre de rubriques dans Expériences des rubriques (aperçu) '
description: Comment gérer des rubriques dans le Centre de rubriques.
author: efrene
ms.author: efrene
manager: pamgreen
audience: admin
ms.topic: article
ms.prod: microsoft-365-enterprise
search.appverid: ''
ms.collection:
- enabler-strategic
- m365initiative-topics
ROBOTS: NOINDEX, NOFOLLOW
localization_priority: None
ms.openlocfilehash: 371ccc16e787b331f42026dec48e5e3113b2b172
ms.sourcegitcommit: 162c01dfaa2fdb3225ce4c24964c1065ce22ed5d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/25/2021
ms.locfileid: "49976190"
---
# <a name="manage-topics-in-the-topic-center-preview"></a><span data-ttu-id="b4e82-103">Gérer les rubriques dans le centre de rubriques (aperçu)</span><span class="sxs-lookup"><span data-stu-id="b4e82-103">Manage topics in the Topic center (Preview)</span></span>

> [!Note] 
> <span data-ttu-id="b4e82-104">Le contenu de cet article est pour Project Private Preview.</span><span class="sxs-lookup"><span data-stu-id="b4e82-104">The content in this article is for Project Cortex Private Preview.</span></span> <span data-ttu-id="b4e82-105">[En savoir plus sur le Projet cortex](https://aka.ms/projectcortex).</span><span class="sxs-lookup"><span data-stu-id="b4e82-105">[Find out more about Project Cortex](https://aka.ms/projectcortex).</span></span>

</br>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4LxDx]  

</br>


<span data-ttu-id="b4e82-106">Dans le centre de rubriques, un gestionnaire de connaissances peut afficher la page Gérer les **rubriques** pour passer en revue les rubriques qui ont été identifiées dans les emplacements sources SharePoint comme spécifié par votre administrateur de connaissances.</span><span class="sxs-lookup"><span data-stu-id="b4e82-106">In the Topic center, a knowledge manager can view the **Manage topics** page to review topics that have been identified in SharePoint source locations as specified by your knowledge admin.</span></span>  

   ![Centre de rubriques](../media/knowledge-management/topic-center.png) </br> 



<span data-ttu-id="b4e82-108">Les gestionnaires de connaissances vous aident à guider les rubriques découvertes tout au long du cycle de vie des rubriques dans lesquelles les rubriques sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="b4e82-108">Knowledge managers help to guide discovered topics through the topic lifecycle in which topics are:</span></span>

- <span data-ttu-id="b4e82-109">Suggestion : une rubrique a été identifiée par l’IA et dispose de suffisamment de ressources de prise en charge, de connexions et de propriétés pour atteindre le seuil de rubrique.</span><span class="sxs-lookup"><span data-stu-id="b4e82-109">Suggested: A topic has been identified by AI and has enough supporting resources, connections, and properties to meet the topic threshold.</span></span>
- <span data-ttu-id="b4e82-110">Confirmé : une rubrique suggérée par l’IA est validée.</span><span class="sxs-lookup"><span data-stu-id="b4e82-110">Confirmed: A topic that has been suggested by AI is validated.</span></span> <span data-ttu-id="b4e82-111">La validation est effectuée par la confirmation d’un administrateur du savoir. En outre, une rubrique peut être confirmée si au moins deux utilisateurs donnent des commentaires positifs par le biais de commentaires sur la rubrique que la rubrique est valide.</span><span class="sxs-lookup"><span data-stu-id="b4e82-111">Validation is done by confirmation from a knowledge admin. Additionally, a topic can be confirmed if at least two users give positive feedback through topic feedback that the topic is valid.</span></span>
- <span data-ttu-id="b4e82-112">Supprimé : une rubrique est rejetée par un administrateur du savoir et n’est plus visible pour les visiteurs.</span><span class="sxs-lookup"><span data-stu-id="b4e82-112">Removed: A topic is rejected by a knowledge admin and will no longer be visible to viewers.</span></span> <span data-ttu-id="b4e82-113">La rubrique peut être dans n’importe quel état lorsqu’elle est supprimée (suggérée ou confirmée).</span><span class="sxs-lookup"><span data-stu-id="b4e82-113">The topic can be in any state when it is removed (suggested or confirmed).</span></span> 
- <span data-ttu-id="b4e82-114">Publié : rubrique confirmée qui a été mise à jour manuellement.</span><span class="sxs-lookup"><span data-stu-id="b4e82-114">Published: A confirmed topic that has been manually updated.</span></span>

   ![Graphique du cycle de vie des rubriques](../media/knowledge-management/topic-lifecycle.png) </br> 

## <a name="requirements"></a><span data-ttu-id="b4e82-116">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="b4e82-116">Requirements</span></span>

<span data-ttu-id="b4e82-117">Pour gérer des rubriques dans le centre de rubriques, vous devez :</span><span class="sxs-lookup"><span data-stu-id="b4e82-117">To manage topics in the Topic center, you need to:</span></span>
- <span data-ttu-id="b4e82-118">Avoir une licence Expériences de rubrique.</span><span class="sxs-lookup"><span data-stu-id="b4e82-118">Have a Topic Experiences license.</span></span>
- <span data-ttu-id="b4e82-119">Avoir des autorisations sur [**Qui peut gérer les rubriques**](https://docs.microsoft.com/microsoft-365/knowledge/topic-experiences-user-permissions).</span><span class="sxs-lookup"><span data-stu-id="b4e82-119">Have permissions to [**Who can manage topics**](https://docs.microsoft.com/microsoft-365/knowledge/topic-experiences-user-permissions).</span></span> <span data-ttu-id="b4e82-120">Les administrateurs du savoir peuvent accorder cette autorisation aux utilisateurs dans les paramètres d’autorisation de la rubrique Réseau de connaissances.</span><span class="sxs-lookup"><span data-stu-id="b4e82-120">Knowledge admins can give users this permission in the Knowledge Network topic permissions settings.</span></span> 

<span data-ttu-id="b4e82-121">Vous ne pourrez pas afficher la page Gérer les rubriques dans le Centre de rubriques, sauf si vous avez l’autorisation Qui peut gérer **les rubriques.**</span><span class="sxs-lookup"><span data-stu-id="b4e82-121">You will not be able to view the Manage Topics page in the Topic Center unless you have the **Who can manage topics** permission.</span></span>

<span data-ttu-id="b4e82-122">Dans le centre de rubriques, un gestionnaire de connaissances peut consulter les rubriques qui ont été identifiées dans les emplacements sources SharePoint que vous avez spécifiés, et peut les confirmer ou les rejeter.</span><span class="sxs-lookup"><span data-stu-id="b4e82-122">In the topic center, a knowledge manager can review topics that have been identified in the SharePoint source locations you specified, and can either confirm or reject them.</span></span> <span data-ttu-id="b4e82-123">Un gestionnaire de connaissances peut également créer et publier de nouvelles pages de rubriques si aucune page n’a été trouvée dans la découverte de rubrique, ou modifier des pages existantes si elles doivent être mises à jour.</span><span class="sxs-lookup"><span data-stu-id="b4e82-123">A knowledge manager can also create and publish new topic pages if one was not found in topic discovery, or edit existing ones if they need to be updated.</span></span>


## <a name="review-suggested-topics"></a><span data-ttu-id="b4e82-124">Consulter les rubriques suggérées</span><span class="sxs-lookup"><span data-stu-id="b4e82-124">Review suggested topics</span></span>

<span data-ttu-id="b4e82-125">Dans la page Gérer les rubriques du centre de rubriques, les rubriques qui ont été découvertes dans vos emplacements sources SharePoint spécifiés sont répertoriées dans **l’onglet Suggestions.** Un gestionnaire de connaissances peut consulter des rubriques non confirmées et choisir de les confirmer ou de les rejeter.</span><span class="sxs-lookup"><span data-stu-id="b4e82-125">On the Topic center Manage Topics page, topics that were discovered in your specified SharePoint source locations will be listed in the **Suggested** tab. A knowledge manager can review unconfirmed topics and choose to confirm or reject them.</span></span>

<span data-ttu-id="b4e82-126">Pour consulter une rubrique suggérée :</span><span class="sxs-lookup"><span data-stu-id="b4e82-126">To review a suggested topic:</span></span>

1. <span data-ttu-id="b4e82-127">Dans la page Gérer les  **rubriques,** sélectionnez l’onglet Suggestions, sélectionnez la rubrique à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="b4e82-127">On the **Manage topics** page, select the **Suggested** tab, select the topic to open the topic page.</span></span></br>

2. <span data-ttu-id="b4e82-128">Dans la page de rubrique, examinez la page de rubrique, puis sélectionnez **Modifier** si vous devez apporter des modifications à la page.</span><span class="sxs-lookup"><span data-stu-id="b4e82-128">On the topic page, review the topic page, and select **Edit** if you need to make any changes to the page.</span></span>

3. <span data-ttu-id="b4e82-129">Après avoir passé en revue la rubrique, revenir à la page Gérer les rubriques.</span><span class="sxs-lookup"><span data-stu-id="b4e82-129">After reviewing the topic, go back to the Manage topics page.</span></span> <span data-ttu-id="b4e82-130">Pour la rubrique sélectionnée, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="b4e82-130">For the selected topic, you can:</span></span>

   - <span data-ttu-id="b4e82-131">Cochez la coche pour confirmer la rubrique.</span><span class="sxs-lookup"><span data-stu-id="b4e82-131">Select the check mark to confirm the topic.</span></span>
    
   - <span data-ttu-id="b4e82-132">Sélectionnez **le x** si vous souhaitez rejeter la rubrique.</span><span class="sxs-lookup"><span data-stu-id="b4e82-132">Select the **x** if you want to reject the topic.</span></span>

    <span data-ttu-id="b4e82-133">Les rubriques confirmées sont supprimées de la liste **Suggérée** et s’affichent désormais dans **la liste** confirmée.</span><span class="sxs-lookup"><span data-stu-id="b4e82-133">Confirmed topics will be removed from the **Suggested** list and will now display in the **Confirmed** list.</span></span>

    <span data-ttu-id="b4e82-134">Les rubriques rejetées sont supprimées de la liste **Suggérée** et s’affichent désormais sous **l’onglet** Supprimé.</span><span class="sxs-lookup"><span data-stu-id="b4e82-134">Rejected topics will be removed from the **Suggested** list and will now display in the **Removed** tab.</span></span>

   </br> 

## <a name="confirmed-topics"></a><span data-ttu-id="b4e82-135">Rubriques confirmées</span><span class="sxs-lookup"><span data-stu-id="b4e82-135">Confirmed topics</span></span>

<span data-ttu-id="b4e82-136">Dans la page Gérer les rubriques, les rubriques qui ont été découvertes dans les emplacements source SharePoint spécifiés et qui ont été confirmées par  un gestionnaire de connaissances ou « d’autres personnes » confirmées par deux ou plusieurs personnes via le mécanisme de commentaires de carte sont répertoriées dans l’onglet Confirmé. Si nécessaire, un utilisateur autorisé à gérer des rubriques peut passer en revue les rubriques confirmées et choisir de les rejeter.</span><span class="sxs-lookup"><span data-stu-id="b4e82-136">On the Manage topics page, topics that were discovered in your specified SharePoint source locations and have been confirmed by a knowledge manager or "crowd-sourced" confirmed by two or more people through the card feedback mechanism will be listed in the **Confirmed** tab. If needed, a user with permissions to manage topics can review confirmed topics and choose to reject them.</span></span>

<span data-ttu-id="b4e82-137">Pour consulter une rubrique confirmée :</span><span class="sxs-lookup"><span data-stu-id="b4e82-137">To review a confirmed topic:</span></span>

1. <span data-ttu-id="b4e82-138">Sous **l’onglet Confirmé,** sélectionnez la rubrique pour ouvrir la page de rubrique.</span><span class="sxs-lookup"><span data-stu-id="b4e82-138">On the **Confirmed** tab, select the topic to open the topic page.</span></span></br>

2. <span data-ttu-id="b4e82-139">Dans la page de rubrique, examinez la page de rubrique, puis sélectionnez **Modifier** si vous devez apporter des modifications à la page.</span><span class="sxs-lookup"><span data-stu-id="b4e82-139">On the topic page, review the topic page, and select **Edit** if you need to make any changes to the page.</span></span>

<span data-ttu-id="b4e82-140">Notez que vous pouvez toujours choisir de rejeter une rubrique confirmée.</span><span class="sxs-lookup"><span data-stu-id="b4e82-140">Note that you can still chose to reject a confirmed topic.</span></span>  <span data-ttu-id="b4e82-141">Pour ce faire, allez à la rubrique sélectionnée dans la liste confirmée, puis sélectionnez **le x** si vous souhaitez rejeter la rubrique.</span><span class="sxs-lookup"><span data-stu-id="b4e82-141">To do this, go to the selected topic in the Confirmed list, and select the **x** if you want to reject the topic.</span></span>

## <a name="published-topics"></a><span data-ttu-id="b4e82-142">Rubriques publiées</span><span class="sxs-lookup"><span data-stu-id="b4e82-142">Published topics</span></span>
<span data-ttu-id="b4e82-143">Les rubriques publiées ont été modifiées afin que des informations spécifiques apparaissent toujours aux personnes qui rencontrent la page.</span><span class="sxs-lookup"><span data-stu-id="b4e82-143">Published topics have been edited so that specific information will always appear to whoever encounters the page.</span></span> <span data-ttu-id="b4e82-144">Les rubriques créées manuellement sont répertoriées ici.</span><span class="sxs-lookup"><span data-stu-id="b4e82-144">Manually created topics are listed here.</span></span>




