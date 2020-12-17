---
title: 'Gérer les rubriques dans le Centre des rubriques de la rubrique expériences (aperçu) '
description: Comment gérer les rubriques dans le Centre des rubriques.
author: efrene
ms.author: efrene
manager: pamgreen
audience: admin
ms.topic: article
ms.prod: microsoft-365-enterprise
search.appverid: ''
ms.collection: enabler-strategic
ROBOTS: NOINDEX, NOFOLLOW
localization_priority: None
ms.openlocfilehash: 832067d157ed9ffcba1ed9ad514c375cbbdd752b
ms.sourcegitcommit: 884ac262443c50362d0c3ded961d36d6b15d8b73
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/16/2020
ms.locfileid: "49698837"
---
# <a name="manage-topics-in-the-topic-center-preview"></a><span data-ttu-id="fe4d0-103">Gérer les rubriques dans le centre de la rubrique (aperçu)</span><span class="sxs-lookup"><span data-stu-id="fe4d0-103">Manage topics in the Topic center (Preview)</span></span>

> [!Note] 
> <span data-ttu-id="fe4d0-104">Le contenu de cet article est destiné à Project cortex privé preview.</span><span class="sxs-lookup"><span data-stu-id="fe4d0-104">The content in this article is for Project Cortex Private Preview.</span></span> <span data-ttu-id="fe4d0-105">[En savoir plus sur le Projet cortex](https://aka.ms/projectcortex).</span><span class="sxs-lookup"><span data-stu-id="fe4d0-105">[Find out more about Project Cortex](https://aka.ms/projectcortex).</span></span>

<span data-ttu-id="fe4d0-106">Dans le Centre des rubriques, un gestionnaire de connaissances peut afficher la page **gérer les rubriques** pour examiner les rubriques qui ont été identifiées dans les emplacements sources SharePoint, comme indiqué par votre administrateur de connaissances.</span><span class="sxs-lookup"><span data-stu-id="fe4d0-106">In the Topic center, a knowledge manager can view the **Manage topics** page to review topics that have been identified in SharePoint source locations as specified by your knowledge admin.</span></span>  

   ![Centre des rubriques](../media/knowledge-management/topic-center.png) </br> 



<span data-ttu-id="fe4d0-108">Les gestionnaires de connaissances aident à orienter les rubriques découvertes via le cycle de vie des rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="fe4d0-108">Knowledge managers help to guide discovered topics through the topic lifecycle in which topics are:</span></span>

- <span data-ttu-id="fe4d0-109">Suggestion : une rubrique a été identifiée par AI et dispose de suffisamment de ressources de prise en charge, de connexions et de propriétés pour atteindre le seuil de la rubrique.</span><span class="sxs-lookup"><span data-stu-id="fe4d0-109">Suggested: A topic has been identified by AI and has enough supporting resources, connections, and properties to meet the topic threshold.</span></span>
- <span data-ttu-id="fe4d0-110">Confirmation : une rubrique qui a été suggérée par AI est validée.</span><span class="sxs-lookup"><span data-stu-id="fe4d0-110">Confirmed: A topic that has been suggested by AI is validated.</span></span> <span data-ttu-id="fe4d0-111">La validation est réalisée par confirmation à partir d’un administrateur de connaissances. De plus, une rubrique peut être confirmée si au moins deux utilisateurs donnent un feedback positif par le biais de commentaires que la rubrique est valide.</span><span class="sxs-lookup"><span data-stu-id="fe4d0-111">Validation is done by confirmation from a knowledge admin. Additionally, a topic can be confirmed if at least two users give positive feedback through topic feedback that the topic is valid.</span></span>
- <span data-ttu-id="fe4d0-112">Supprimé : une rubrique est rejetée par un administrateur de connaissances et ne sera plus visible par les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="fe4d0-112">Removed: A topic is rejected by a knowledge admin and will no longer be visible to viewers.</span></span> <span data-ttu-id="fe4d0-113">La rubrique peut être dans n’importe quel état lorsqu’elle est supprimée (suggérée ou confirmée).</span><span class="sxs-lookup"><span data-stu-id="fe4d0-113">The topic can be in any state when it is removed (suggested or confirmed).</span></span> 
- <span data-ttu-id="fe4d0-114">Publié : rubrique confirmée qui a été mise à jour manuellement.</span><span class="sxs-lookup"><span data-stu-id="fe4d0-114">Published: A confirmed topic that has been manually updated.</span></span>

   ![Graphique de cycle de vie des rubriques](../media/knowledge-management/topic-lifecycle.png) </br> 

## <a name="requirements"></a><span data-ttu-id="fe4d0-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fe4d0-116">Requirements</span></span>

<span data-ttu-id="fe4d0-117">Pour gérer les rubriques dans le Centre des rubriques, vous devez :</span><span class="sxs-lookup"><span data-stu-id="fe4d0-117">To manage topics in the Topic center, you need to:</span></span>
- <span data-ttu-id="fe4d0-118">Disposer d’une licence pour une rubrique.</span><span class="sxs-lookup"><span data-stu-id="fe4d0-118">Have a Topic Experiences license.</span></span>
- <span data-ttu-id="fe4d0-119">Disposer des autorisations permettant de [**gérer les rubriques**](https://docs.microsoft.com/microsoft-365/knowledge/topic-experiences-user-permissions).</span><span class="sxs-lookup"><span data-stu-id="fe4d0-119">Have permissions to [**Who can manage topics**](https://docs.microsoft.com/microsoft-365/knowledge/topic-experiences-user-permissions).</span></span> <span data-ttu-id="fe4d0-120">Knowledge admins peut donner aux utilisateurs cette autorisation dans la rubrique Knowledge Network topic Permissions.</span><span class="sxs-lookup"><span data-stu-id="fe4d0-120">Knowledge admins can give users this permission in the Knowledge Network topic permissions settings.</span></span> 

<span data-ttu-id="fe4d0-121">Vous ne pouvez pas afficher la page gérer les rubriques dans le Centre des rubriques, sauf si vous disposez de l’autorisation **gérer les rubriques** .</span><span class="sxs-lookup"><span data-stu-id="fe4d0-121">You will not be able to view the Manage Topics page in the Topic Center unless you have the **Who can manage topics** permission.</span></span>

<span data-ttu-id="fe4d0-122">Dans le Centre des rubriques, un gestionnaire de connaissances peut consulter les rubriques qui ont été identifiées dans les emplacements sources SharePoint que vous avez spécifiés et peut les confirmer ou les refuser.</span><span class="sxs-lookup"><span data-stu-id="fe4d0-122">In the topic center, a knowledge manager can review topics that have been identified in the SharePoint source locations you specified, and can either confirm or reject them.</span></span> <span data-ttu-id="fe4d0-123">Un responsable de la connaissance peut également créer et publier de nouvelles pages de rubrique, le cas échéant, si elles ne sont pas disponibles dans la découverte de rubrique, ou en modifier les existantes si elles doivent être mises à jour.</span><span class="sxs-lookup"><span data-stu-id="fe4d0-123">A knowledge manager can also create and publish new topic pages if one was not found in topic discovery, or edit existing ones if they need to be updated.</span></span>


## <a name="review-suggested-topics"></a><span data-ttu-id="fe4d0-124">Consulter les rubriques suggérées</span><span class="sxs-lookup"><span data-stu-id="fe4d0-124">Review suggested topics</span></span>

<span data-ttu-id="fe4d0-125">Sur la page Centre de rubriques gérer les rubriques, les rubriques découvertes dans les emplacements de source SharePoint spécifiés sont répertoriées dans l’onglet **suggéré** . Un responsable de la connaissance peut consulter les rubriques non confirmées et choisir de les confirmer ou de les refuser.</span><span class="sxs-lookup"><span data-stu-id="fe4d0-125">On the Topic center Manage Topics page, topics that were discovered in your specified SharePoint source locations will be listed in the **Suggested** tab. A knowledge manager can review unconfirmed topics and choose to confirm or reject them.</span></span>

<span data-ttu-id="fe4d0-126">Pour passer en revue une rubrique suggérée :</span><span class="sxs-lookup"><span data-stu-id="fe4d0-126">To review a suggested topic:</span></span>

1. <span data-ttu-id="fe4d0-127">Sur la page **gérer les rubriques** , sélectionnez l’onglet **suggéré** , puis la rubrique pour ouvrir la page de la rubrique.</span><span class="sxs-lookup"><span data-stu-id="fe4d0-127">On the **Manage topics** page, select the **Suggested** tab, select the topic to open the topic page.</span></span></br>

2. <span data-ttu-id="fe4d0-128">Sur la page rubrique, passez en revue la page de la rubrique, puis sélectionnez **modifier** si vous devez apporter des modifications à la page.</span><span class="sxs-lookup"><span data-stu-id="fe4d0-128">On the topic page, review the topic page, and select **Edit** if you need to make any changes to the page.</span></span>

3. <span data-ttu-id="fe4d0-129">Après avoir consulté la rubrique, revenez à la page gérer les rubriques.</span><span class="sxs-lookup"><span data-stu-id="fe4d0-129">After reviewing the topic, go back to the Manage topics page.</span></span> <span data-ttu-id="fe4d0-130">Pour la rubrique sélectionnée, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="fe4d0-130">For the selected topic, you can:</span></span>

   - <span data-ttu-id="fe4d0-131">Activez la case à cocher pour confirmer la rubrique.</span><span class="sxs-lookup"><span data-stu-id="fe4d0-131">Select the check mark to confirm the topic.</span></span>
    
   - <span data-ttu-id="fe4d0-132">Sélectionnez le **x** si vous souhaitez rejeter la rubrique.</span><span class="sxs-lookup"><span data-stu-id="fe4d0-132">Select the **x** if you want to reject the topic.</span></span>

    <span data-ttu-id="fe4d0-133">Les rubriques confirmées seront supprimées de la liste **proposée** et s’afficheront désormais dans la liste **confirmée** .</span><span class="sxs-lookup"><span data-stu-id="fe4d0-133">Confirmed topics will be removed from the **Suggested** list and will now display in the **Confirmed** list.</span></span>

    <span data-ttu-id="fe4d0-134">Les sujets rejetés seront supprimés de la liste **proposée** et s’afficheront désormais dans l’onglet **supprimé** .</span><span class="sxs-lookup"><span data-stu-id="fe4d0-134">Rejected topics will be removed from the **Suggested** list and will now display in the **Removed** tab.</span></span>

   </br> 

## <a name="confirmed-topics"></a><span data-ttu-id="fe4d0-135">Rubriques confirmées</span><span class="sxs-lookup"><span data-stu-id="fe4d0-135">Confirmed topics</span></span>

<span data-ttu-id="fe4d0-136">Sur la page gérer les rubriques, les rubriques qui ont été découvertes dans les emplacements sources SharePoint spécifiés et qui ont été confirmées par un gestionnaire de connaissances ou par « sources de foule » confirmées par deux personnes ou plus via le mécanisme de commentaires de carte seront répertoriées sous l’onglet **confirmé** . Si nécessaire, un utilisateur disposant des autorisations pour gérer les rubriques peut consulter les rubriques confirmées et choisir de les refuser.</span><span class="sxs-lookup"><span data-stu-id="fe4d0-136">On the Manage topics page, topics that were discovered in your specified SharePoint source locations and have been confirmed by a knowledge manager or "crowd-sourced" confirmed by two or more people through the card feedback mechanism will be listed in the **Confirmed** tab. If needed, a user with permissions to manage topics can review confirmed topics and choose to reject them.</span></span>

<span data-ttu-id="fe4d0-137">Pour consulter une rubrique confirmée :</span><span class="sxs-lookup"><span data-stu-id="fe4d0-137">To review a confirmed topic:</span></span>

1. <span data-ttu-id="fe4d0-138">Sous l’onglet **confirmation** , sélectionnez la rubrique pour ouvrir la page de rubrique.</span><span class="sxs-lookup"><span data-stu-id="fe4d0-138">On the **Confirmed** tab, select the topic to open the topic page.</span></span></br>

2. <span data-ttu-id="fe4d0-139">Sur la page rubrique, passez en revue la page de la rubrique, puis sélectionnez **modifier** si vous devez apporter des modifications à la page.</span><span class="sxs-lookup"><span data-stu-id="fe4d0-139">On the topic page, review the topic page, and select **Edit** if you need to make any changes to the page.</span></span>

<span data-ttu-id="fe4d0-140">Notez que vous pouvez toujours choisir de refuser une rubrique confirmée.</span><span class="sxs-lookup"><span data-stu-id="fe4d0-140">Note that you can still chose to reject a confirmed topic.</span></span>  <span data-ttu-id="fe4d0-141">Pour ce faire, accédez à la rubrique sélectionnée dans la liste confirmée, puis sélectionnez le **x** si vous souhaitez rejeter la rubrique.</span><span class="sxs-lookup"><span data-stu-id="fe4d0-141">To do this, go to the selected topic in the Confirmed list, and select the **x** if you want to reject the topic.</span></span>

## <a name="published-topics"></a><span data-ttu-id="fe4d0-142">Rubriques publiées</span><span class="sxs-lookup"><span data-stu-id="fe4d0-142">Published topics</span></span>
<span data-ttu-id="fe4d0-143">Les sujets publiés ont été modifiés de sorte que des informations spécifiques apparaissent toujours à l’auteur de la page.</span><span class="sxs-lookup"><span data-stu-id="fe4d0-143">Published topics have been edited so that specific information will always appear to whoever encounters the page.</span></span> <span data-ttu-id="fe4d0-144">Les rubriques créées manuellement sont répertoriées ici.</span><span class="sxs-lookup"><span data-stu-id="fe4d0-144">Manually created topics are listed here.</span></span>




