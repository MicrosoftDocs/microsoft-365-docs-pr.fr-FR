---
title: Trimming de sécurité des rubriques Microsoft
ms.author: efrene
author: efrene
manager: pamgreen
ms.reviewer: cjtan
audience: admin
ms.topic: article
ms.service: ''
ms.prod: microsoft-365-enterprise
search.appverid: ''
ms.collection: enabler-strategic
localization_priority: None
description: Vue d’ensemble de l’utilisation de la sécurité pour afficher les rubriques.
ms.openlocfilehash: a7146592edb356b4d46a5a178b5754dc0de6a7c0
ms.sourcegitcommit: 30c3054004ddc9d6059c11d55577552aa2464810
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/20/2021
ms.locfileid: "50939622"
---
# <a name="microsoft-viva-topics-security-trimming"></a><span data-ttu-id="ba128-103">Trimming de sécurité des rubriques Microsoft</span><span class="sxs-lookup"><span data-stu-id="ba128-103">Microsoft Viva Topics security trimming</span></span> 

<span data-ttu-id="ba128-104">Les utilisateurs de rubriques Topics ne peuvent pas afficher les informations dans les rubriques que leurs autorisations Office 365 existantes les empêchent de voir.</span><span class="sxs-lookup"><span data-stu-id="ba128-104">Viva Topics users can't view information in topics that their existing Office 365 permissions prevent them from seeing.</span></span> <span data-ttu-id="ba128-105">Tout ce qu’un utilisateur voit sur une page de rubrique (par exemple, des sites SharePoint, des documents, des fichiers) sera des informations qu’il est déjà autorisé à voir.</span><span class="sxs-lookup"><span data-stu-id="ba128-105">Everything a user sees on a topic page (for example, SharePoint sites, documents, files) will be information they are already allowed to see.</span></span> <span data-ttu-id="ba128-106">Topics ne modifie pas les autorisations existantes.</span><span class="sxs-lookup"><span data-stu-id="ba128-106">Viva Topics does not make changes to any existing permissions.</span></span>

## <a name="why-two-users-may-have-different-views-of-the-same-topic"></a><span data-ttu-id="ba128-107">Pourquoi deux utilisateurs peuvent avoir des vues différentes de la même rubrique</span><span class="sxs-lookup"><span data-stu-id="ba128-107">Why two users may have different views of the same topic</span></span>

<span data-ttu-id="ba128-108">Lorsqu’une rubrique est créée par le biais d’une IA ou d’une curation manuelle, elle peut contenir une description de la rubrique, d’autres noms, des personnes associées à la rubrique, ainsi que des sites, des pages et des fichiers associés à la rubrique.</span><span class="sxs-lookup"><span data-stu-id="ba128-108">When a topic is created through AI or manual curation, it can contain a description of the topic, alternative names, people associated with the topic, as well as sites, pages, and files related to the topic.</span></span> <span data-ttu-id="ba128-109">Lorsque ces informations sont visualées sur une page de rubrique, il est possible que deux utilisateurs qui visualisent la même rubrique ne voient pas les mêmes informations.</span><span class="sxs-lookup"><span data-stu-id="ba128-109">When this information is viewed on a topic page, it is possible that two users who are viewing the same topic my not see the same information.</span></span>
  
<span data-ttu-id="ba128-110">Par exemple, lorsque l’utilisateur 1 affiche la page de rubriqueSoe, il peut voir cet affichage de la page de rubrique.</span><span class="sxs-lookup"><span data-stu-id="ba128-110">For example, when User 1 views the Neptune topic page, they might see this view of the topic page.</span></span>

![Rubrique de l’utilisateur 1](../media/knowledge-management/user2-topic-view.png) </br> 

<span data-ttu-id="ba128-112">Toutefois, lorsque l’utilisateur 2 examine la même page de rubriques, son affichage diffère de celui de l’utilisateur 1.</span><span class="sxs-lookup"><span data-stu-id="ba128-112">However, when User 2 looks at the same Neptune topic page, their view differs from User 1.</span></span>  <span data-ttu-id="ba128-113">L’utilisateur 2 peut voir le fichier de présentation du produit *DG-2000* dans la section Des fichiers et **des pages** épinglés de la page de rubrique, qui n’apparaît pas pour l’utilisateur 1.</span><span class="sxs-lookup"><span data-stu-id="ba128-113">User 2 is able to see the *DG-2000 Product Overview* file in the **Pinned files and pages** section of the topic page, which does not appear for User 1.</span></span> 

![Rubrique de Rubrique pour l’utilisateur 2](../media/knowledge-management/user1-topic-view.png) </br> 

<span data-ttu-id="ba128-115">La différence entre ce que les utilisateurs peuvent voir dans la même rubrique est que les utilisateurs n’ont peut-être pas les autorisations Office 365 pour afficher un site ou un fichier associé.</span><span class="sxs-lookup"><span data-stu-id="ba128-115">The difference in what users may see on the same topic is because users may not have the Office 365 permissions to view a related site or file.</span></span>  <span data-ttu-id="ba128-116">Cette rubrique respecte les autorisations définies sur les éléments d’une rubrique et ne peut pas modifier l’accès à ces derniers.</span><span class="sxs-lookup"><span data-stu-id="ba128-116">Viva Topics respects the permissions that are set on items in a topic, and cannot change access to them.</span></span> <span data-ttu-id="ba128-117">Dans notre exemple, l’utilisateur 1 n’est pas en mesure d’afficher le fichier de présentation du produit *DG-2000* dans sa page de rubriques, car l’utilisateur 1 n’a pas les autorisations Office 365 pour afficher le fichier.</span><span class="sxs-lookup"><span data-stu-id="ba128-117">In our example, User 1 is not able to view the *DG-2000 Product Overview* file in their topic page for Neptune because User 1 does not have Office 365 permissions to view the file.</span></span>

<span data-ttu-id="ba128-118">Si un utilisateur ne peut pas voir suffisamment d’informations dans une rubrique pour qu’elle soit utile, la rubrique ne sera pas disponible pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ba128-118">If a user is not able to see enough information in a topic for it to be useful, the topic will not be available to the user.</span></span> <span data-ttu-id="ba128-119">Lorsque cela se produit, l’utilisateur ne voit pas la rubrique mise en surbrillvient.</span><span class="sxs-lookup"><span data-stu-id="ba128-119">When this happens, the user will not see the highlighted topic.</span></span> <span data-ttu-id="ba128-120">Un autre utilisateur qui dispose d’autorisations pour plus d’informations dans la rubrique afin qu’elle soit utile, pourra voir la rubrique.</span><span class="sxs-lookup"><span data-stu-id="ba128-120">A different user who has permissions to more information in the topic for it to be useful, will be able to see the topic.</span></span>


## <a name="topic-permissions-for-knowledge-managers-and-topic-contributors"></a><span data-ttu-id="ba128-121">Autorisations de rubrique pour les gestionnaires de connaissances et les contributeurs de rubriques</span><span class="sxs-lookup"><span data-stu-id="ba128-121">Topic permissions for knowledge managers and topic contributors</span></span>

<span data-ttu-id="ba128-122">Les utilisateurs qui se voient attribuer des autorisations pour gérer des rubriques (gestionnaires de connaissances) pourront uniquement afficher les informations qu’ils sont autorisés à consulter dans les rubriques.</span><span class="sxs-lookup"><span data-stu-id="ba128-122">Users that are assigned permissions to manage topics - knowledge managers - will only be able to view information they have permissions to see within topics.</span></span>

<span data-ttu-id="ba128-123">De même, les utilisateurs qui ont des autorisations de création et de modification de rubriques (collaborateurs de rubriques) pourront uniquement afficher les informations qu’ils sont autorisés à consulter dans les rubriques.</span><span class="sxs-lookup"><span data-stu-id="ba128-123">Similarly, users who have create and edit topic permissions - topic contributors - will only be able to view information they have permissions to see within topics.</span></span> 


## <a name="ai-versus-manually-curated-topic-information"></a><span data-ttu-id="ba128-124">Informations sur l’IA par rapport aux rubriques organisées manuellement</span><span class="sxs-lookup"><span data-stu-id="ba128-124">AI versus manually curated topic information</span></span>

<span data-ttu-id="ba128-125">Les rubriques peuvent contenir des informations générées par l’IA et des informations ajoutées ou modifiées par des collaborateurs de rubriques ou des gestionnaires de connaissances.</span><span class="sxs-lookup"><span data-stu-id="ba128-125">Topics can contain information generated by AI and information added or edited by topic contributors or knowledge managers.</span></span>

 - <span data-ttu-id="ba128-126">Les informations d’une rubrique ajoutée par l’IA sont visibles uniquement pour les personnes qui ont accès au contenu source.</span><span class="sxs-lookup"><span data-stu-id="ba128-126">Information in a topic that was added by AI is only visible to people who have access to the source content.</span></span>
 - <span data-ttu-id="ba128-127">La description de la rubrique et les informations sur les personnes qui ont été manuellement ajoutées ou modifiées par un collaborateur de rubrique ou un gestionnaire de connaissances sont visibles par tous les utilisateurs qui peuvent consulter cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="ba128-127">Topic description and people information that has been manually added or edited by a topic contributor or knowledge manager is visible to everyone who can see the topic.</span></span>
 - <span data-ttu-id="ba128-128">Les fichiers, pages et sites sont visibles uniquement pour les utilisateurs qui ont des autorisations sur le contenu source, qu’ils soient ajoutés ou ajoutés manuellement par l’IA.</span><span class="sxs-lookup"><span data-stu-id="ba128-128">Files, pages, and sites are only visible to users who have permissions to the source content, whether manually added or added by AI.</span></span>

<span data-ttu-id="ba128-129">Le tableau suivant décrit ce que les utilisateurs (visiteurs de rubriques, collaborateurs et gestionnaires de connaissances) peuvent voir dans une rubrique donnée en fonction de leurs autorisations.</span><span class="sxs-lookup"><span data-stu-id="ba128-129">The following table describes what users - topic viewers, contributors, and knowledge managers - can see in a given topic based on their permissions.</span></span>

|<span data-ttu-id="ba128-130">Élément de rubrique</span><span class="sxs-lookup"><span data-stu-id="ba128-130">Topic item</span></span>|<span data-ttu-id="ba128-131">Ce que les utilisateurs peuvent voir</span><span class="sxs-lookup"><span data-stu-id="ba128-131">What users can see</span></span>|
|:---------|:------------------|
|<span data-ttu-id="ba128-132">Nom de la rubrique</span><span class="sxs-lookup"><span data-stu-id="ba128-132">Topic name</span></span>|<span data-ttu-id="ba128-133">Les utilisateurs peuvent voir le nom des rubriques dans le centre de rubriques.</span><span class="sxs-lookup"><span data-stu-id="ba128-133">Users can see the topic name of topics in the topic center.</span></span> <span data-ttu-id="ba128-134">Certaines rubriques peuvent ne pas être visibles si les utilisateurs n’ont pas d’autorisations pour le contenu source ou ont une faible pertinence pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ba128-134">Some topics may not be visible if users don't have permissions to the source content or have a low relevancy to the user.</span></span>|
|<span data-ttu-id="ba128-135">Description du sujet</span><span class="sxs-lookup"><span data-stu-id="ba128-135">Topic description</span></span>|<span data-ttu-id="ba128-136">Les descriptions générées par l’IA sont visibles uniquement pour les utilisateurs qui ont des autorisations sur le contenu source.</span><span class="sxs-lookup"><span data-stu-id="ba128-136">AI-generated descriptions are visible only to users who have permissions to the source content.</span></span> <span data-ttu-id="ba128-137">Les descriptions entrées ou modifiées manuellement sont visibles pour tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="ba128-137">Manually entered or edited descriptions are visible to all users.</span></span>|
|<span data-ttu-id="ba128-138">Personnes</span><span class="sxs-lookup"><span data-stu-id="ba128-138">People</span></span>|<span data-ttu-id="ba128-139">Les personnes épinglées sont visibles par tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="ba128-139">Pinned people are visible to all users.</span></span> <span data-ttu-id="ba128-140">Les personnes suggérées sont visibles uniquement pour les utilisateurs qui ont des autorisations sur le contenu source.</span><span class="sxs-lookup"><span data-stu-id="ba128-140">Suggested people are only visible to users who have permissions to the source content.</span></span>|
|<span data-ttu-id="ba128-141">Fichiers</span><span class="sxs-lookup"><span data-stu-id="ba128-141">Files</span></span>|<span data-ttu-id="ba128-142">Les fichiers sont visibles uniquement pour les utilisateurs qui ont des autorisations sur le contenu source.</span><span class="sxs-lookup"><span data-stu-id="ba128-142">Files are only visible to users who have permissions to the source content.</span></span>|
|<span data-ttu-id="ba128-143">Pages</span><span class="sxs-lookup"><span data-stu-id="ba128-143">Pages</span></span>|<span data-ttu-id="ba128-144">Les pages sont visibles uniquement pour les utilisateurs qui ont des autorisations sur le contenu source.</span><span class="sxs-lookup"><span data-stu-id="ba128-144">Pages are only visible to users who have permissions to the source content.</span></span>|
|<span data-ttu-id="ba128-145">Sites</span><span class="sxs-lookup"><span data-stu-id="ba128-145">Sites</span></span>|<span data-ttu-id="ba128-146">Les sites sont visibles uniquement pour les utilisateurs qui ont des autorisations sur le contenu source.</span><span class="sxs-lookup"><span data-stu-id="ba128-146">Sites are only visible to users who have permissions to the source content.</span></span>|




## <a name="see-also"></a><span data-ttu-id="ba128-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ba128-147">See also</span></span>

