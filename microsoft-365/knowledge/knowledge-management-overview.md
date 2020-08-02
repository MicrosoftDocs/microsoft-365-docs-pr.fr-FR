---
title: Vue d’ensemble de la gestion des connaissances (aperçu)
ms.author: efrene
author: efrene
manager: pamgreen
ms.date: 8/1/2020
audience: admin
ms.topic: article
ms.service: ''
search.appverid: ''
localization_priority: Normal
ROBOTS: NOINDEX, NOFOLLOW
description: Vue d’ensemble de la gestion des connaissances dans le projet cortex.
ms.openlocfilehash: 99b0d0ece9ef8271666b1978db7947f3e3f2a4e8
ms.sourcegitcommit: 3a47efcbdf3d2b39caa2798ea5be806839b05ed1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/01/2020
ms.locfileid: "46540072"
---
# <a name="knowledge-management-0verview-preview"></a><span data-ttu-id="6ae0a-103">0verview de gestion des informations (aperçu)</span><span class="sxs-lookup"><span data-stu-id="6ae0a-103">Knowledge management 0verview (Preview)</span></span>

> [!Note] 
> <span data-ttu-id="6ae0a-104">Le contenu de cet article est destiné à Project cortex privé preview.</span><span class="sxs-lookup"><span data-stu-id="6ae0a-104">The content in this article is for Project Cortex Private Preview.</span></span> [<span data-ttu-id="6ae0a-105">En savoir plus sur le projet cortex</span><span class="sxs-lookup"><span data-stu-id="6ae0a-105">Find out more about Project Cortex</span></span>](https://aka.ms/projectcortex) 

<span data-ttu-id="6ae0a-106">Knowledge Management utilise la technologie Microsoft AI, Microsoft 365, Delve, Search, ainsi que d’autres composants et services pour créer un réseau de connaissances dans votre environnement Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="6ae0a-106">Knowledge management uses Microsoft AI technology, Microsoft 365, Delve, Search, and other components and services to build a knowledge network in your Microsoft 365 environment.</span></span> 

   ![Flux de gestion des connaissances](../media/content-understanding/knowledge-management-flowchart.png) </br> 

<span data-ttu-id="6ae0a-108">L’objectif est de fournir des informations aux utilisateurs dans les applications qu’ils utilisent quotidiennement, telles qu’Outlook, teams et SharePoint.</span><span class="sxs-lookup"><span data-stu-id="6ae0a-108">It's goal is to deliver information to you users in apps they use everyday, such as Outlook, Teams, and SharePoint.</span></span>

<span data-ttu-id="6ae0a-109">Par exemple, les utilisateurs voient des termes inconnus dans leurs courriers électroniques, leurs sites SharePoint ou dans les conversations Teams, pour lesquelles ils souhaitent en savoir plus.</span><span class="sxs-lookup"><span data-stu-id="6ae0a-109">For example, users see unfamiliar terms in their emails, SharePoint sites, or in Teams conversations, that they want to know more about.</span></span> <span data-ttu-id="6ae0a-110">Knowledge Management utilise AI pour rechercher et identifier automatiquement ces **rubriques**, ainsi que pour compiler des informations les concernant, telles qu’une brève description, des experts techniques sur le sujet, ainsi que des sites, des fichiers et des pages qui y sont associés.</span><span class="sxs-lookup"><span data-stu-id="6ae0a-110">Knowledge management uses AI to automatically searches for and identifies these **topics**, and compiles information about them, such as a short description, subject matter experts on the topic, and sites, files, and pages that are related to it.</span></span> <span data-ttu-id="6ae0a-111">Vous pouvez choisir de mettre à jour les informations de la rubrique selon vos besoins.</span><span class="sxs-lookup"><span data-stu-id="6ae0a-111">You can choose to update the topic information as needed.</span></span> <span data-ttu-id="6ae0a-112">Vous pouvez ensuite mettre les rubriques à la disposition des utilisateurs, ce qui signifie que, pour chaque instance de la rubrique qui apparaît dans les applications telles qu’Outlook, teams et SharePoint, le texte est mis en surbrillance.</span><span class="sxs-lookup"><span data-stu-id="6ae0a-112">You can then make the topics available to your users, which means that for every instance of the topic that appears in apps such as Outlook, Teams, and SharePoint, the text will be highlighted.</span></span> <span data-ttu-id="6ae0a-113">Les utilisateurs peuvent choisir la rubrique pour en savoir plus à ce sujet dans la rubrique Détails.</span><span class="sxs-lookup"><span data-stu-id="6ae0a-113">Users can choose to select the topic to learn more about it through the topic details.</span></span>


## <a name="topic-discovery"></a><span data-ttu-id="6ae0a-114">Découverte de rubrique</span><span class="sxs-lookup"><span data-stu-id="6ae0a-114">Topic discovery</span></span>

<span data-ttu-id="6ae0a-115">Knowledge Management utilise la technologie Microsoft AI pour rechercher des **rubriques** dans votre environnement Office 365.</span><span class="sxs-lookup"><span data-stu-id="6ae0a-115">Knowledge Management uses Microsoft AI technology to search for **topics** in your Office 365 environment.</span></span>

<span data-ttu-id="6ae0a-116">Une rubrique est une expression ou un terme qui est significatif ou important au sein de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="6ae0a-116">A topic is a phrase or term that is organizationally significant or important.</span></span> <span data-ttu-id="6ae0a-117">Il a une signification spécifique pour l’organisation et a des ressources qui lui sont associées, qui peuvent aider les utilisateurs à comprendre ce qu’ils sont et à trouver plus d’informations à leur sujet.</span><span class="sxs-lookup"><span data-stu-id="6ae0a-117">It has a specific meaning to the organization, and has resources related to it that can help people understand what it is and find more information about it.</span></span>

<span data-ttu-id="6ae0a-118">Lorsqu’une rubrique est découverte, une **page de rubrique** est créée pour celle-ci qui contient des informations collectées par le biais de la découverte de rubrique, telles que :</span><span class="sxs-lookup"><span data-stu-id="6ae0a-118">When a topic is discovered, a **topic page** is created for it that contains information that was gathered through topic discovery, such as:</span></span>

- <span data-ttu-id="6ae0a-119">Brève description de la rubrique.</span><span class="sxs-lookup"><span data-stu-id="6ae0a-119">A short description of the topic.</span></span>
- <span data-ttu-id="6ae0a-120">Utilisateurs pouvant être informé de la rubrique.</span><span class="sxs-lookup"><span data-stu-id="6ae0a-120">Users who might be knowledgeable about the topic.</span></span>
- <span data-ttu-id="6ae0a-121">Fichiers, pages et sites associés à la rubrique.</span><span class="sxs-lookup"><span data-stu-id="6ae0a-121">Files, pages, and sites that are related to the topic.</span></span>


## <a name="topic-management"></a><span data-ttu-id="6ae0a-122">Gestion des rubriques</span><span class="sxs-lookup"><span data-stu-id="6ae0a-122">Topic management</span></span>

<span data-ttu-id="6ae0a-123">La gestion des rubriques est réalisée dans le **Centre**de la rubrique de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="6ae0a-123">Topic management is done in your organization's **topic center**.</span></span> <span data-ttu-id="6ae0a-124">Le site Centre de rubrique est créé lors de l’installation et sert de centre de connaissances pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="6ae0a-124">The topic center site is created during setup and serves as your center of knowledge for your organization.</span></span> <span data-ttu-id="6ae0a-125">Elle contient une liste de toutes les rubriques découvertes dans votre environnement, ainsi que toutes les pages de rubrique créées pour ces rubriques.</span><span class="sxs-lookup"><span data-stu-id="6ae0a-125">It will contain a list of all topics that were discovered in your environment, as well as all topic pages that were created for these topics.</span></span> 

<span data-ttu-id="6ae0a-126">Les utilisateurs qui disposent des autorisations appropriées peuvent effectuer les opérations suivantes dans le centre de la rubrique :</span><span class="sxs-lookup"><span data-stu-id="6ae0a-126">Users who are provided the correct permissions will be able to do the following in the topic center:</span></span>

- <span data-ttu-id="6ae0a-127">Confirmez ou rejetez des rubriques qui ont été découvertes dans votre client.</span><span class="sxs-lookup"><span data-stu-id="6ae0a-127">Confirm or reject topics that were discovered in your tenant.</span></span>
- <span data-ttu-id="6ae0a-128">Créez de nouvelles rubriques manuellement en fonction de vos besoins (par exemple, si vous n’avez pas suffisamment d’informations pour qu’elles soient découvertes via AI).</span><span class="sxs-lookup"><span data-stu-id="6ae0a-128">Create new topics manually as needed (for example, if not enough information was provided for it to be discovered through AI).</span></span>
- <span data-ttu-id="6ae0a-129">Modifier des pages de rubrique existantes.</span><span class="sxs-lookup"><span data-stu-id="6ae0a-129">Edit existing topic pages.</span></span></br>

<span data-ttu-id="6ae0a-130">Pour plus d’informations, voir [travailler avec une rubrique dans le Centre des rubriques](work-with-topics.md) .</span><span class="sxs-lookup"><span data-stu-id="6ae0a-130">See [Work with topic in the topic center](work-with-topics.md) for more information.</span></span>  


## <a name="admin-controls"></a><span data-ttu-id="6ae0a-131">Contrôles d’administration</span><span class="sxs-lookup"><span data-stu-id="6ae0a-131">Admin controls</span></span>

<span data-ttu-id="6ae0a-132">Les contrôles d’administration dans le centre d’administration Microsoft 365 vous permettent de gérer votre réseau de connaissances.</span><span class="sxs-lookup"><span data-stu-id="6ae0a-132">Admin controls in the Microsoft 365 admin center  allow you to manage your knowledge network.</span></span> <span data-ttu-id="6ae0a-133">Ils permettent à un administrateur global ou SharePoint de Microsoft 365 de :</span><span class="sxs-lookup"><span data-stu-id="6ae0a-133">They allow a Microsoft 365 global or SharePoint admin to:</span></span>

- <span data-ttu-id="6ae0a-134">Contrôlez les utilisateurs de votre organisation autorisés à voir les rubriques dans leurs applications clientes ou dans les résultats de la recherche SharePoint.</span><span class="sxs-lookup"><span data-stu-id="6ae0a-134">Control which users in your organization are allowed to see topics in their client apps or in SharePoint search results.</span></span>
- <span data-ttu-id="6ae0a-135">Contrôlez les sites SharePoint qui seront analysés pour rechercher des rubriques.</span><span class="sxs-lookup"><span data-stu-id="6ae0a-135">Control which SharePoint sites will be crawled to search for topics.</span></span>
- <span data-ttu-id="6ae0a-136">Configurez la découverte de rubrique pour exclure des termes spécifiques qui ne doivent pas être une rubrique.</span><span class="sxs-lookup"><span data-stu-id="6ae0a-136">Configure topic discovery to exclude specific terms that you don't want to be a topic.</span></span>
- <span data-ttu-id="6ae0a-137">Contrôlez les utilisateurs qui peuvent confirmer ou rejeter des rubriques dans le centre de la rubrique.</span><span class="sxs-lookup"><span data-stu-id="6ae0a-137">Control which users can to confirm or reject topics in the topic center.</span></span>
- <span data-ttu-id="6ae0a-138">Contrôler les utilisateurs qui peuvent créer et modifier des rubriques dans le Centre des rubriques.</span><span class="sxs-lookup"><span data-stu-id="6ae0a-138">Control which users can create and edit topics in the topic center.</span></span>

<span data-ttu-id="6ae0a-139">Pour plus d’informations, consultez [la rubrique gérer votre réseau de connaissances](manage-knowledge-network.md) .</span><span class="sxs-lookup"><span data-stu-id="6ae0a-139">See [Manage your knowledge network](manage-knowledge-network.md) for more information.</span></span> 

## <a name="topic-curation"></a><span data-ttu-id="6ae0a-140">Section curative</span><span class="sxs-lookup"><span data-stu-id="6ae0a-140">Topic curation</span></span>

<span data-ttu-id="6ae0a-141">AI continue de fournir des suggestions pour améliorer vos rubriques lorsque des modifications sont apportées dans votre environnement.</span><span class="sxs-lookup"><span data-stu-id="6ae0a-141">AI will continually work to provide you suggestions to improve your topics as changes occur in your environment.</span></span>

<span data-ttu-id="6ae0a-142">Les utilisateurs qui autorisent l’accès à consulter les rubriques de leur travail quotidien sont autorisés à formuler des suggestions pour les améliorer.</span><span class="sxs-lookup"><span data-stu-id="6ae0a-142">Users who you allow access to see topics in their daily work are allowed to make suggestions to improve them.</span></span> <span data-ttu-id="6ae0a-143">Par exemple, si un utilisateur consulte la page de rubrique et qu’il constate des informations incorrectes ou devant être ajoutées, un lien sur la page de rubrique leur permet de soumettre une demande pour mettre à jour les informations.</span><span class="sxs-lookup"><span data-stu-id="6ae0a-143">For example, if a user views the topic page and sees information that is incorrect or needs to be added, a link on the topic page allows them to submit a request to update the information.</span></span>

<span data-ttu-id="6ae0a-144">En outre, les utilisateurs disposant des autorisations appropriées peuvent baliser des éléments tels que la conversation de teams qui s’appliquent à une rubrique, et les ajouter à une rubrique spécifique.</span><span class="sxs-lookup"><span data-stu-id="6ae0a-144">Additionally, users with proper permissions can tag items such as Teams conversation that are relevant to a topic, and add them to a specific topic.</span></span>




## <a name="see-also"></a><span data-ttu-id="6ae0a-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6ae0a-145">See also</span></span>
[<span data-ttu-id="6ae0a-146">Configurer la gestion des connaissances</span><span class="sxs-lookup"><span data-stu-id="6ae0a-146">Set up knowledge management</span></span>](set-up-knowledge-network.md)</br>
[<span data-ttu-id="6ae0a-147">Présentation du centre de rubriques</span><span class="sxs-lookup"><span data-stu-id="6ae0a-147">Topic center overview</span></span>](topic-center-overview.md)