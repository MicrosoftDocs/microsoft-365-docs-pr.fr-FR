---
title: Vue d’ensemble de la gestion des connaissances (aperçu)
ms.author: efrene
author: efrene
manager: pamgreen
ms.date: 8/1/2020
audience: admin
ms.topic: article
ms.service: o365-administration
search.appverid: ''
localization_priority: None
ROBOTS: NOINDEX, NOFOLLOW
description: Vue d’ensemble de la gestion des connaissances dans le projet cortex.
ms.openlocfilehash: d422b54bb7991fb5fd61465cd0428ab586d10bf5
ms.sourcegitcommit: 7355cc8871cde5fac6d7d6dcecc3e41e35601623
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "48906940"
---
# <a name="knowledge-management-overview-preview"></a><span data-ttu-id="235c6-103">Vue d’ensemble de la gestion des connaissances (aperçu)</span><span class="sxs-lookup"><span data-stu-id="235c6-103">Knowledge management Overview (Preview)</span></span>

> [!Note] 
> <span data-ttu-id="235c6-104">Le contenu de cet article est destiné à Project cortex privé preview.</span><span class="sxs-lookup"><span data-stu-id="235c6-104">The content in this article is for Project Cortex Private Preview.</span></span> <span data-ttu-id="235c6-105">[En savoir plus sur le Projet cortex](https://aka.ms/projectcortex).</span><span class="sxs-lookup"><span data-stu-id="235c6-105">[Find out more about Project Cortex](https://aka.ms/projectcortex).</span></span>

<span data-ttu-id="235c6-106">Knowledge Management utilise la technologie Microsoft AI, Microsoft 365, Delve, Search, ainsi que d’autres composants et services pour créer un réseau de connaissances dans votre environnement Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="235c6-106">Knowledge management uses Microsoft AI technology, Microsoft 365, Delve, Search, and other components and services to build a knowledge network in your Microsoft 365 environment.</span></span> 

   ![Flux de gestion des connaissances](../media/content-understanding/knowledge-management-flowchart.png) </br> 

<span data-ttu-id="235c6-108">L’objectif est de fournir des informations aux utilisateurs dans les applications qu’ils utilisent quotidiennement, telles qu’Outlook, teams et SharePoint.</span><span class="sxs-lookup"><span data-stu-id="235c6-108">It's goal is to deliver information to you users in apps they use everyday, such as Outlook, Teams, and SharePoint.</span></span>

<span data-ttu-id="235c6-109">Par exemple, les utilisateurs voient des termes inconnus dans leurs courriers électroniques, leurs sites SharePoint ou dans les conversations Teams, pour lesquelles ils souhaitent en savoir plus.</span><span class="sxs-lookup"><span data-stu-id="235c6-109">For example, users see unfamiliar terms in their emails, SharePoint sites, or in Teams conversations, that they want to know more about.</span></span> <span data-ttu-id="235c6-110">Knowledge Management utilise AI pour rechercher et identifier automatiquement ces **rubriques** , ainsi que pour compiler des informations les concernant, telles qu’une brève description, des experts techniques sur le sujet, ainsi que des sites, des fichiers et des pages qui y sont associés.</span><span class="sxs-lookup"><span data-stu-id="235c6-110">Knowledge management uses AI to automatically searches for and identifies these **topics** , and compiles information about them, such as a short description, subject matter experts on the topic, and sites, files, and pages that are related to it.</span></span> <span data-ttu-id="235c6-111">Vous pouvez choisir de mettre à jour les informations de la rubrique selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="235c6-111">You can choose to update the topic information as needed.</span></span> <span data-ttu-id="235c6-112">Vous pouvez ensuite mettre les rubriques à la disposition des utilisateurs, ce qui signifie que, pour chaque instance de la rubrique qui apparaît dans les applications telles qu’Outlook, teams et SharePoint, le texte est mis en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="235c6-112">You can then make the topics available to your users, which means that for every instance of the topic that appears in apps such as Outlook, Teams, and SharePoint, the text will be highlighted.</span></span> <span data-ttu-id="235c6-113">Les utilisateurs peuvent choisir la rubrique pour en savoir plus à ce sujet dans la rubrique Détails.</span><span class="sxs-lookup"><span data-stu-id="235c6-113">Users can choose to select the topic to learn more about it through the topic details.</span></span>


## <a name="topic-indexing"></a><span data-ttu-id="235c6-114">Indexation des rubriques</span><span class="sxs-lookup"><span data-stu-id="235c6-114">Topic indexing</span></span>

<span data-ttu-id="235c6-115">Knowledge Management utilise la technologie Microsoft AI pour identifier les **rubriques** de votre environnement Office 365.</span><span class="sxs-lookup"><span data-stu-id="235c6-115">Knowledge Management uses Microsoft AI technology to identify **topics** in your Office 365 environment.</span></span>

<span data-ttu-id="235c6-116">Une rubrique est une expression ou un terme qui est significatif ou important au sein de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="235c6-116">A topic is a phrase or term that is organizationally significant or important.</span></span> <span data-ttu-id="235c6-117">Il a une signification spécifique pour l’organisation et a des ressources qui lui sont associées, qui peuvent aider les utilisateurs à comprendre ce qu’ils sont et à trouver plus d’informations à leur sujet.</span><span class="sxs-lookup"><span data-stu-id="235c6-117">It has a specific meaning to the organization, and has resources related to it that can help people understand what it is and find more information about it.</span></span>

<span data-ttu-id="235c6-118">Lorsqu’une rubrique est identifiée, une **page de rubrique** est créée pour celle-ci qui contient des informations collectées par le biais de l’indexation des rubriques, telles que :</span><span class="sxs-lookup"><span data-stu-id="235c6-118">When a topic is identified, a **topic page** is created for it that contains information that was gathered through topic indexing, such as:</span></span>

- <span data-ttu-id="235c6-119">Autres noms et/ou acronymes.</span><span class="sxs-lookup"><span data-stu-id="235c6-119">Alternate names and/or acronyms.</span></span>
- <span data-ttu-id="235c6-120">Brève description de la rubrique.</span><span class="sxs-lookup"><span data-stu-id="235c6-120">A short description of the topic.</span></span>
- <span data-ttu-id="235c6-121">Utilisateurs pouvant être informé de la rubrique.</span><span class="sxs-lookup"><span data-stu-id="235c6-121">Users who might be knowledgeable about the topic.</span></span>
- <span data-ttu-id="235c6-122">Fichiers, pages et sites associés à la rubrique.</span><span class="sxs-lookup"><span data-stu-id="235c6-122">Files, pages, and sites that are related to the topic.</span></span>


## <a name="topic-discovery"></a><span data-ttu-id="235c6-123">Découverte de rubrique</span><span class="sxs-lookup"><span data-stu-id="235c6-123">Topic discovery</span></span>
<span data-ttu-id="235c6-124">Lorsqu’une rubrique est mentionnée dans contenu sur les actualités et pages SharePoint, elle apparaît en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="235c6-124">When a topic is mentioned in content on SharePoint news and pages, you'll see it highlighted.</span></span> <span data-ttu-id="235c6-125">Ouvrez le résumé de la rubrique à partir de la mise en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="235c6-125">Open the topic summary from the highlight.</span></span> <span data-ttu-id="235c6-126">Ouvrez les détails de la rubrique à partir du titre du résumé.</span><span class="sxs-lookup"><span data-stu-id="235c6-126">Open the topic details from the title of the summary.</span></span> <!--(msg for Efren: not sure if I should use discovery for this; we use discovered in-product for indexing?)--> <span data-ttu-id="235c6-127">La rubrique mentionnée peut être identifiée automatiquement ou avoir été ajoutée à la page à l’aide d’une référence directe à la rubrique par l’auteur de la page.</span><span class="sxs-lookup"><span data-stu-id="235c6-127">The mentioned topic could be identified automatically or have been added to the page with a direct reference to the topic by the page author.</span></span>

<span data-ttu-id="235c6-128">Vous pouvez également découvrir des rubriques via Microsoft Search.</span><span class="sxs-lookup"><span data-stu-id="235c6-128">You can also discover topics through Microsoft Search.</span></span>


## <a name="topic-management"></a><span data-ttu-id="235c6-129">Gestion des rubriques</span><span class="sxs-lookup"><span data-stu-id="235c6-129">Topic management</span></span>

<span data-ttu-id="235c6-130">La gestion des rubriques est réalisée dans le **Centre** de la rubrique de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="235c6-130">Topic management is done in your organization's **topic center**.</span></span> <span data-ttu-id="235c6-131">Le site Centre de rubrique est créé lors de l’installation et sert de centre de connaissances pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="235c6-131">The topic center site is created during setup and serves as your center of knowledge for your organization.</span></span> <span data-ttu-id="235c6-132">Elle contient une liste de toutes les rubriques découvertes dans votre environnement, ainsi que toutes les pages de rubrique créées pour ces rubriques.</span><span class="sxs-lookup"><span data-stu-id="235c6-132">It will contain a list of all topics that were discovered in your environment, as well as all topic pages that were created for these topics.</span></span> 

<span data-ttu-id="235c6-133">Les utilisateurs qui disposent des autorisations appropriées peuvent effectuer les opérations suivantes dans le centre de la rubrique :</span><span class="sxs-lookup"><span data-stu-id="235c6-133">Users who are provided the correct permissions will be able to do the following in the topic center:</span></span>

- <span data-ttu-id="235c6-134">Confirmez ou rejetez des rubriques qui ont été découvertes dans votre client.</span><span class="sxs-lookup"><span data-stu-id="235c6-134">Confirm or reject topics that were discovered in your tenant.</span></span>
- <span data-ttu-id="235c6-135">Créez de nouvelles rubriques manuellement en fonction de vos besoins (par exemple, si vous n’avez pas suffisamment d’informations pour qu’elles soient découvertes via AI).</span><span class="sxs-lookup"><span data-stu-id="235c6-135">Create new topics manually as needed (for example, if not enough information was provided for it to be discovered through AI).</span></span>
- <span data-ttu-id="235c6-136">Modifier des pages de rubrique existantes.</span><span class="sxs-lookup"><span data-stu-id="235c6-136">Edit existing topic pages.</span></span></br>

<span data-ttu-id="235c6-137">Pour plus d’informations, voir [travailler avec une rubrique dans le Centre des rubriques](work-with-topics.md) .</span><span class="sxs-lookup"><span data-stu-id="235c6-137">See [Work with topic in the topic center](work-with-topics.md) for more information.</span></span>  


## <a name="admin-controls"></a><span data-ttu-id="235c6-138">Contrôles d’administration</span><span class="sxs-lookup"><span data-stu-id="235c6-138">Admin controls</span></span>

<span data-ttu-id="235c6-139">Les contrôles d’administration dans le centre d’administration Microsoft 365 vous permettent de gérer votre réseau de connaissances.</span><span class="sxs-lookup"><span data-stu-id="235c6-139">Admin controls in the Microsoft 365 admin center  allow you to manage your knowledge network.</span></span> <span data-ttu-id="235c6-140">Ils permettent à un administrateur global ou SharePoint de Microsoft 365 de :</span><span class="sxs-lookup"><span data-stu-id="235c6-140">They allow a Microsoft 365 global or SharePoint admin to:</span></span>

- <span data-ttu-id="235c6-141">Contrôlez les utilisateurs de votre organisation autorisés à voir les rubriques dans leurs applications clientes ou dans les résultats de la recherche SharePoint.</span><span class="sxs-lookup"><span data-stu-id="235c6-141">Control which users in your organization are allowed to see topics in their client apps or in SharePoint search results.</span></span>
- <span data-ttu-id="235c6-142">Contrôlez les sites SharePoint qui seront analysés pour rechercher des rubriques.</span><span class="sxs-lookup"><span data-stu-id="235c6-142">Control which SharePoint sites will be crawled to search for topics.</span></span>
- <span data-ttu-id="235c6-143">Configurez la découverte de rubrique pour exclure des termes spécifiques qui ne doivent pas être une rubrique.</span><span class="sxs-lookup"><span data-stu-id="235c6-143">Configure topic discovery to exclude specific terms that you don't want to be a topic.</span></span>
- <span data-ttu-id="235c6-144">Contrôlez les utilisateurs qui peuvent confirmer ou rejeter des rubriques dans le centre de la rubrique.</span><span class="sxs-lookup"><span data-stu-id="235c6-144">Control which users can to confirm or reject topics in the topic center.</span></span>
- <span data-ttu-id="235c6-145">Contrôler les utilisateurs qui peuvent créer et modifier des rubriques dans le Centre des rubriques.</span><span class="sxs-lookup"><span data-stu-id="235c6-145">Control which users can create and edit topics in the topic center.</span></span>

<span data-ttu-id="235c6-146">Pour plus d’informations, consultez [la rubrique gérer votre réseau de connaissances](manage-knowledge-network.md) .</span><span class="sxs-lookup"><span data-stu-id="235c6-146">See [Manage your knowledge network](manage-knowledge-network.md) for more information.</span></span> 

## <a name="topic-curation--feedback"></a><span data-ttu-id="235c6-147">& des commentaires sur les de la rubrique</span><span class="sxs-lookup"><span data-stu-id="235c6-147">Topic curation & feedback</span></span>

<span data-ttu-id="235c6-148">AI continue de fournir des suggestions pour améliorer vos rubriques lorsque des modifications sont apportées dans votre environnement.</span><span class="sxs-lookup"><span data-stu-id="235c6-148">AI will continually work to provide you suggestions to improve your topics as changes occur in your environment.</span></span>

<span data-ttu-id="235c6-149">Les utilisateurs qui autorisent l’accès à consulter les rubriques de leur travail quotidien sont autorisés à formuler des suggestions pour les améliorer.</span><span class="sxs-lookup"><span data-stu-id="235c6-149">Users who you allow access to see topics in their daily work are allowed to make suggestions to improve them.</span></span> <span data-ttu-id="235c6-150">Par exemple, si un utilisateur consulte la page de rubrique et qu’il voit des informations incorrectes ou devant être ajoutées, un lien sur la page de rubrique leur permet de modifier directement les informations.</span><span class="sxs-lookup"><span data-stu-id="235c6-150">For example, if a user views the topic page and sees information that is incorrect or needs to be added, a link on the topic page allows them to edit the information directly.</span></span> <span data-ttu-id="235c6-151">Un autre exemple, si un utilisateur affiche une mise en surbrillance sur une page d’actualités SharePoint, vous trouverez des questions qui vous demanderont si la mise en surbrillance est appropriée ou si la rubrique suggérée est appropriée pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="235c6-151">Another example, if a user views a a highlight on a SharePoint news page, you will find questions asking whether or not the highlight is appropriate or the suggested topic is appropriate for your organization.</span></span> <span data-ttu-id="235c6-152">Votre réponse vous aidera à déterminer ce qui est affiché sur les résumés des rubriques et dans les détails de la rubrique.</span><span class="sxs-lookup"><span data-stu-id="235c6-152">Your answer will help determine what's shown on topic summaries and in topic details.</span></span>

<span data-ttu-id="235c6-153">En outre, les utilisateurs disposant des autorisations appropriées peuvent baliser des éléments tels que la conversation Yammer qui concernent une rubrique, et les ajouter à une rubrique spécifique.</span><span class="sxs-lookup"><span data-stu-id="235c6-153">Additionally, users with proper permissions can tag items such as Yammer conversation that are relevant to a topic, and add them to a specific topic.</span></span> <!--(msg for Efren: changed to Yammer, because we will not have shipped Teams yet)-->


## <a name="see-also"></a><span data-ttu-id="235c6-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="235c6-154">See also</span></span>
[<span data-ttu-id="235c6-155">Configurer la gestion des connaissances</span><span class="sxs-lookup"><span data-stu-id="235c6-155">Set up knowledge management</span></span>](set-up-knowledge-network.md)</br>
[<span data-ttu-id="235c6-156">Présentation du centre de rubriques</span><span class="sxs-lookup"><span data-stu-id="235c6-156">Topic center overview</span></span>](topic-center-overview.md)
