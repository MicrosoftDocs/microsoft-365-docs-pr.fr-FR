---
title: La rubrique rencontre un filtrage de sécurité (aperçu)
ms.author: efrene
author: efrene
manager: pamgreen
audience: admin
ms.topic: article
ms.service: ''
ms.prod: microsoft-365-enterprise
search.appverid: ''
ms.collection: enabler-strategic
localization_priority: None
ROBOTS: NOINDEX, NOFOLLOW
description: Vue d’ensemble de l’utilisation de la sécurité pour afficher les rubriques.
ms.openlocfilehash: 7e503082494d27f9418b8e09b8d20d01e4708fe9
ms.sourcegitcommit: 884ac262443c50362d0c3ded961d36d6b15d8b73
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/16/2020
ms.locfileid: "49698954"
---
# <a name="topic-experiences-security-trimming-preview"></a><span data-ttu-id="82935-103">La rubrique rencontre un filtrage de sécurité (aperçu)</span><span class="sxs-lookup"><span data-stu-id="82935-103">Topic Experiences security trimming (Preview)</span></span>

> [!Note] 
> <span data-ttu-id="82935-104">Le contenu de cet article est destiné à Project cortex privé preview.</span><span class="sxs-lookup"><span data-stu-id="82935-104">The content in this article is for Project Cortex Private Preview.</span></span> <span data-ttu-id="82935-105">[En savoir plus sur le Projet cortex](https://aka.ms/projectcortex).</span><span class="sxs-lookup"><span data-stu-id="82935-105">[Find out more about Project Cortex](https://aka.ms/projectcortex).</span></span>

<span data-ttu-id="82935-106">Rubrique Experience les utilisateurs ne peuvent pas afficher les informations dans les rubriques que leurs autorisations Office 365 existantes les empêchent de voir.</span><span class="sxs-lookup"><span data-stu-id="82935-106">Topic experiences users will not be able to view information in topics that their existing Office 365 permissions prevents them from seeing.</span></span> <span data-ttu-id="82935-107">Tout ce qu’un utilisateur voit sur une page de rubrique (par exemple, des sites SharePoint, des documents, des fichiers) sera des informations qu’il est déjà autorisé à voir.</span><span class="sxs-lookup"><span data-stu-id="82935-107">Everything a user sees on a topic page (for example, SharePoint sites, documents, files) will be information they are already allowed to see.</span></span> <span data-ttu-id="82935-108">Les expériences de rubrique ne modifient pas les autorisations existantes.</span><span class="sxs-lookup"><span data-stu-id="82935-108">Topic experiences does not make changes to any existing permissions.</span></span>

## <a name="why-two-users-may-have-different-views-of-the-same-topic"></a><span data-ttu-id="82935-109">Pourquoi deux utilisateurs peuvent-ils avoir différentes vues du même sujet ?</span><span class="sxs-lookup"><span data-stu-id="82935-109">Why two users may have different views of the same topic</span></span>

<span data-ttu-id="82935-110">Lorsqu’une rubrique est créée via AI ou une opération manuelle, elle peut contenir une description de la rubrique, des noms de substitution, des personnes associées à la rubrique, ainsi que des sites, des pages et des fichiers liés à la rubrique.</span><span class="sxs-lookup"><span data-stu-id="82935-110">When a topic is created through AI or manual curation, it can contain a description of the topic, alternative names, people associated with the topic, as well as sites, pages, and files related to the topic.</span></span> <span data-ttu-id="82935-111">Lorsque ces informations s’affichent sur une page de rubrique, il est possible que deux utilisateurs qui visualisent le même sujet ne voient pas les mêmes informations.</span><span class="sxs-lookup"><span data-stu-id="82935-111">When this information is viewed on a topic page, it is possible that two users who are viewing the same topic my not see the same information.</span></span>
  
<span data-ttu-id="82935-112">Par exemple, lorsque l’utilisateur 1 affiche la page de la rubrique Neptune, il s’agit de ce qu’il peut voir.</span><span class="sxs-lookup"><span data-stu-id="82935-112">For example, when User 1 views the Neptune topic page, this is what they might see.</span></span>

![Rubrique Neptune pour l’utilisateur 1](../media/knowledge-management/user2-topic-view.png) </br> 

<span data-ttu-id="82935-114">Toutefois, lorsque l’utilisateur 2 regarde sur la même page de rubrique Neptune, son affichage diffère de l’utilisateur 1.</span><span class="sxs-lookup"><span data-stu-id="82935-114">However, when User 2 looks at the same Neptune topic page, her view differs from User 1.</span></span>  <span data-ttu-id="82935-115">L’utilisateur 2 est en mesure de voir le fichier de *vue d’ensemble du produit DG-2000* dans la section **fichiers et pages épinglés** de la page de rubrique, qui ne s’affiche pas pour l’utilisateur 1.</span><span class="sxs-lookup"><span data-stu-id="82935-115">User 2 is able to see the *DG-2000 Product Overview* file in the **Pinned files and pages** section of the topic page, which does not appear for User 1.</span></span> 

![Rubrique Neptune pour l’utilisateur 2](../media/knowledge-management/user1-topic-view.png) </br> 

<span data-ttu-id="82935-117">La différence entre ce que les utilisateurs peuvent voir dans la même rubrique est que les utilisateurs ne disposent pas des autorisations Office 365 pour afficher un site ou un fichier associé.</span><span class="sxs-lookup"><span data-stu-id="82935-117">The difference in what users may see on the same topic is because users may not have the Office 365 permissions to view a related site or file.</span></span>  <span data-ttu-id="82935-118">Les expériences de rubrique respectent les autorisations définies sur les éléments d’une rubrique et ne peuvent pas modifier l’accès à celles-ci.</span><span class="sxs-lookup"><span data-stu-id="82935-118">Topic experiences respects the permissions that are set on items in a topic, and cannot change access to them.</span></span> <span data-ttu-id="82935-119">Dans notre exemple, l’utilisateur 1 ne peut pas afficher le fichier de *vue d’ensemble du produit DG-2000* dans sa page de rubrique pour Neptune, car l’utilisateur 1 ne dispose pas des autorisations Office 365 pour afficher le fichier.</span><span class="sxs-lookup"><span data-stu-id="82935-119">In our example, User 1 is not able to view the *DG-2000 Product Overview* file in their topic page for Neptune because User 1 does not have Office 365 permissions to view the file.</span></span>

<span data-ttu-id="82935-120">Si un utilisateur ne parvient pas à voir suffisamment d’informations dans une rubrique pour qu’il soit utile, la rubrique ne sera pas disponible pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="82935-120">If a user is not able to see enough information in a topic for it to be useful, the topic will not be available to the user.</span></span> <span data-ttu-id="82935-121">Dans ce cas, l’utilisateur ne voit pas la rubrique en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="82935-121">In this instance, the user will not see the highlighted topic.</span></span> <span data-ttu-id="82935-122">Toutefois, un autre utilisateur disposant d’autorisations pour accéder à des informations supplémentaires dans la rubrique pour qu’il soit utile, sera en mesure de voir la rubrique.</span><span class="sxs-lookup"><span data-stu-id="82935-122">However, a different user who has permissions to more information in the topic for it to be useful, will be able to see the topic.</span></span>


## <a name="topic-permissions-for-knowledge-managers-and-topic-contributors"></a><span data-ttu-id="82935-123">Rubriques d’autorisations pour les responsables du savoir et les contributeurs</span><span class="sxs-lookup"><span data-stu-id="82935-123">Topic permissions for knowledge managers and topic contributors</span></span>

<span data-ttu-id="82935-124">Les utilisateurs auxquels sont attribués des autorisations pour gérer les rubriques-gestionnaires de connaissances-seront en mesure d’afficher les informations qu’ils sont autorisés à voir dans les rubriques.</span><span class="sxs-lookup"><span data-stu-id="82935-124">Users that are assigned permissions to manage topics - knowledge managers - will only be able to view information they have permissions to see within topics.</span></span>

<span data-ttu-id="82935-125">De même, les utilisateurs qui disposent des autorisations de création et de modification de rubrique-Contributor de rubrique-seront uniquement en mesure d’afficher les informations qu’ils sont autorisés à voir dans les rubriques.</span><span class="sxs-lookup"><span data-stu-id="82935-125">Similarly, users who have create and edit topic permissions - topic contributors - will only be able to view information they have permissions to see within topics.</span></span> 


## <a name="ai-versus-manually-curated-topic-information"></a><span data-ttu-id="82935-126">Informations sur les rubriques de la préversion et la facilité organisée manuellement</span><span class="sxs-lookup"><span data-stu-id="82935-126">AI versus manually curated topic information</span></span>

<span data-ttu-id="82935-127">Les rubriques peuvent contenir des informations générées par les IA et des informations ajoutées ou modifiées par des collaborateurs ou des responsables du savoir.</span><span class="sxs-lookup"><span data-stu-id="82935-127">Topics can contain information generated by AI and information added or edited by topic contributors or knowledge managers.</span></span>

 - <span data-ttu-id="82935-128">Les informations d’une rubrique qui a été ajoutée par AI sont visibles uniquement pour les personnes ayant accès au contenu source.</span><span class="sxs-lookup"><span data-stu-id="82935-128">Information in a topic that was added by AI is only visible to people who have access to the source content.</span></span>
 - <span data-ttu-id="82935-129">Les informations qui ont été ajoutées ou modifiées manuellement par un collaborateur de rubrique ou le gestionnaire de connaissances sont visibles par tous les utilisateurs qui peuvent voir la rubrique.</span><span class="sxs-lookup"><span data-stu-id="82935-129">Information that has been manually added or edited by a topic contributor or knowledge manager is visible to everyone who can see the topic.</span></span>

<span data-ttu-id="82935-130">Le tableau suivant décrit ce que les utilisateurs-consultants, contributeurs et gestionnaires de connaissances peuvent voir dans un sujet donné en fonction de leurs autorisations.</span><span class="sxs-lookup"><span data-stu-id="82935-130">The following table describes what users - topic viewers, contributors, and knowledge managers - can see in a given topic based on their permissions.</span></span>

|<span data-ttu-id="82935-131">Élément de rubrique</span><span class="sxs-lookup"><span data-stu-id="82935-131">Topic item</span></span>|<span data-ttu-id="82935-132">Ce que les utilisateurs peuvent voir</span><span class="sxs-lookup"><span data-stu-id="82935-132">What users can see</span></span>|
|:---------|:------------------|
|<span data-ttu-id="82935-133">Nom de la rubrique</span><span class="sxs-lookup"><span data-stu-id="82935-133">Topic name</span></span>|<span data-ttu-id="82935-134">Les utilisateurs peuvent voir le nom de toutes les rubriques dans le Centre des rubriques.</span><span class="sxs-lookup"><span data-stu-id="82935-134">Users can see the topic name of all topics in the topic center.</span></span> <span data-ttu-id="82935-135">Il se peut que certaines rubriques ne soient pas visibles si elles ont une faible pertinence pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="82935-135">Some topics may not be visible if they have a low relevancy to the user.</span></span>|
|<span data-ttu-id="82935-136">Description de la rubrique</span><span class="sxs-lookup"><span data-stu-id="82935-136">Topic description</span></span>|<span data-ttu-id="82935-137">Les descriptions générées par les IA sont visibles uniquement pour les utilisateurs qui disposent d’autorisations sur le contenu source.</span><span class="sxs-lookup"><span data-stu-id="82935-137">AI-generated descriptions are visible only to users who have permissions to the source content.</span></span> <span data-ttu-id="82935-138">Les descriptions entrées ou modifiées manuellement sont visibles par tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="82935-138">Manually entered or edited descriptions are visible to all users.</span></span>|
|<span data-ttu-id="82935-139">Personnes</span><span class="sxs-lookup"><span data-stu-id="82935-139">People</span></span>|<span data-ttu-id="82935-140">Les personnes en attente sont visibles par tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="82935-140">Pinned people are visible to all users.</span></span> <span data-ttu-id="82935-141">Les personnes suggérées sont uniquement visibles par les utilisateurs disposant d’autorisations sur le contenu source.</span><span class="sxs-lookup"><span data-stu-id="82935-141">Suggested people are only visible to users who have permissions to the source content.</span></span>|
|<span data-ttu-id="82935-142">Fichiers</span><span class="sxs-lookup"><span data-stu-id="82935-142">Files</span></span>|<span data-ttu-id="82935-143">Les fichiers ne sont visibles que pour les utilisateurs qui disposent d’autorisations sur le contenu source.</span><span class="sxs-lookup"><span data-stu-id="82935-143">Files are only visible to users who have permissions to the source content.</span></span>|
|<span data-ttu-id="82935-144">Pages</span><span class="sxs-lookup"><span data-stu-id="82935-144">Pages</span></span>|<span data-ttu-id="82935-145">Les pages sont visibles uniquement pour les utilisateurs qui disposent d’autorisations sur le contenu source.</span><span class="sxs-lookup"><span data-stu-id="82935-145">Pages are only visible to users who have permissions to the source content.</span></span>|
|<span data-ttu-id="82935-146">Sites</span><span class="sxs-lookup"><span data-stu-id="82935-146">Sites</span></span>|<span data-ttu-id="82935-147">Les sites sont visibles uniquement pour les utilisateurs qui disposent d’autorisations sur le contenu source.</span><span class="sxs-lookup"><span data-stu-id="82935-147">Sites are only visible to users who have permissions to the source content.</span></span>|




## <a name="see-also"></a><span data-ttu-id="82935-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="82935-148">See also</span></span>

