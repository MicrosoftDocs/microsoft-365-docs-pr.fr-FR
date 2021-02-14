---
title: Passer en revue les conversations dans Advanced eDiscovery
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: Découvrez comment utiliser la fonctionnalité reconstruction de conversation dans Advanced eDiscovery pour reconstruire, réviser et exporter des conversations threadées.
ms.custom: seo-marvel-mar2020
ms.openlocfilehash: bf5c39f567240b58546dbeb353e3e461e9b69e48
ms.sourcegitcommit: 9ce9001aa41172152458da27c1c52825355f426d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/03/2020
ms.locfileid: "47358342"
---
# <a name="review-conversations-in-advanced-ediscovery"></a><span data-ttu-id="bfe2d-103">Passer en revue les conversations dans Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="bfe2d-103">Review conversations in Advanced eDiscovery</span></span> 

<span data-ttu-id="bfe2d-104">La messagerie instantanée est un moyen pratique de poser des questions, de partager des idées ou de communiquer rapidement entre de larges publics.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-104">Instant messaging is a convenient way to ask questions, share ideas, or quickly communicate across large audiences.</span></span> <span data-ttu-id="bfe2d-105">Comme les plateformes de messagerie instantanée, telles que Microsoft Teams, sont essentielles à la collaboration d’entreprise, les organisations doivent évaluer la façon dont leur flux de travail eDiscovery traite ces nouvelles formes de communication et de collaboration.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-105">As instant messaging platforms, like Microsoft Teams, become core to enterprise collaboration, organizations must evaluate how their eDiscovery workflow addresses these new forms of communication and collaboration.</span></span> 

<span data-ttu-id="bfe2d-106">La fonctionnalité reconstruction de conversation dans Advanced eDiscovery est conçue pour vous aider à identifier le contenu contextuel et à produire des vues de conversation distinctes.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-106">The Conversation Reconstruction feature in Advanced eDiscovery is designed to help you identify contextual content and produce distinct conversation views.</span></span> <span data-ttu-id="bfe2d-107">Cette fonctionnalité vous permet de passer en revue efficacement et rapidement les conversations par message instantané (également appelées *conversations* threadées) générées sur des plateformes telles que Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-107">This capability allows you to efficiently and rapidly review complete instant message conversations (also called *threaded conversations*) that are generated in platforms like Microsoft Teams.</span></span>

<span data-ttu-id="bfe2d-108">Avec la reconstruction de conversation, vous pouvez utiliser les fonctionnalités intégrées pour reconstruire, réviser et exporter des conversations threadées.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-108">With Conversation Reconstruction, you can use built-in capabilities to reconstruct, review, and export threaded conversations.</span></span> <span data-ttu-id="bfe2d-109">Utilisez la reconstruction de conversation Advanced eDiscovery pour :</span><span class="sxs-lookup"><span data-stu-id="bfe2d-109">Use Advanced eDiscovery Conversation Reconstruction to:</span></span>

- <span data-ttu-id="bfe2d-110">Conserver des métadonnées de niveau message uniques dans tous les messages d’une conversation.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-110">Preserve unique message-level metadata across all messages within a conversation.</span></span>

- <span data-ttu-id="bfe2d-111">Collectez des messages contextuels autour de vos résultats de recherche.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-111">Collect contextual messages around your search results.</span></span>

- <span data-ttu-id="bfe2d-112">Passer en revue, annoter et redessier des conversations threadées.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-112">Review, annotate, and redact threaded conversations.</span></span>

- <span data-ttu-id="bfe2d-113">Exporter des messages individuels ou des conversations threadées</span><span class="sxs-lookup"><span data-stu-id="bfe2d-113">Export individual messages or threaded conversations</span></span>

## <a name="terminology"></a><span data-ttu-id="bfe2d-114">Terminologie</span><span class="sxs-lookup"><span data-stu-id="bfe2d-114">Terminology</span></span>

<span data-ttu-id="bfe2d-115">Voici quelques définitions pour vous aider à commencer à utiliser la reconstruction de conversation.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-115">Here are few definitions to help you get start using Conversation Reconstruction.</span></span>

- <span data-ttu-id="bfe2d-116">**Messages :** Représente la plus petite unité d’une conversation.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-116">**Messages:** Represent the smallest unit of a conversation.</span></span> <span data-ttu-id="bfe2d-117">La taille, la structure et les métadonnées des messages peuvent varier.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-117">Messages may vary in size, structure, and metadata.</span></span> 

- <span data-ttu-id="bfe2d-118">**Conversation :** Représente un regroupement d’un ou plusieurs messages.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-118">**Conversation:** Represents a grouping of one or more messages.</span></span> <span data-ttu-id="bfe2d-119">Dans différentes applications, les conversations peuvent être représentées de différentes manières.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-119">Across different applications, conversations may be represented in different ways.</span></span> <span data-ttu-id="bfe2d-120">Dans certaines applications, il existe une action explicite qui résulte de la réponse à un message existant.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-120">In some applications, there is an explicit action that results from replying to an existing message.</span></span> <span data-ttu-id="bfe2d-121">Les conversations sont formées explicitement à la suite de cette action de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-121">Conversations are formed explicitly as a result of this user action.</span></span> <span data-ttu-id="bfe2d-122">Par exemple, voici une capture d’écran d’une conversation de canal dans Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-122">For example, here is a screenshot of a channel conversation in Microsoft Teams.</span></span>

   ![Conversation du canal Microsoft Teams](../media/threadedchat.png)

   <span data-ttu-id="bfe2d-124">Dans d’autres applications (telles que les messages de conversation 1xN dans Teams), il n’existe pas de chaîne de réponse formelle et les messages apparaissent plutôt comme une « série plate de messages » au sein d’un thread unique.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-124">In other apps (such as 1xN chat messages in Teams), there is not a formal reply chain and instead messages appear as a "flat river of messages" within a single thread.</span></span> <span data-ttu-id="bfe2d-125">Dans ces types d’applications, les conversations sont déduites d’un groupe de messages qui se produisent dans un certain temps.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-125">In these types apps, conversations are inferred from a group of messages that occur within a certain time.</span></span> <span data-ttu-id="bfe2d-126">Ce « groupement souple » de messages (par opposition à une chaîne de réponse) représente la conversation « va-et-vient » sur un sujet spécifique.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-126">This "soft-grouping" of messages (as opposed to a reply chain) represent the "back and forth" conversation about a specific topic of interest.</span></span> 

## <a name="step-1-run-a-search"></a><span data-ttu-id="bfe2d-127">Étape 1 : Exécuter une recherche</span><span class="sxs-lookup"><span data-stu-id="bfe2d-127">Step 1: Run a search</span></span>

<span data-ttu-id="bfe2d-128">Une fois que vous avez identifié les dépositaires et les emplacements de contenu pertinents, vous pouvez créer une recherche pour rechercher du contenu potentiellement pertinent.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-128">After you have identified relevant custodians and content locations, you can create a search to find potentially relevant content.</span></span> <span data-ttu-id="bfe2d-129">Sous **l’onglet Recherches** dans le cas Advanced eDiscovery,  vous pouvez créer une recherche en cliquant sur Nouvelle recherche et en suivant l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-129">On the **Searches** tab in the Advanced eDiscovery case, you can create a search by clicking **New search** and following the wizard.</span></span> <span data-ttu-id="bfe2d-130">Pour plus d’informations sur la création d’une recherche, la création d’une requête de recherche et l’affichage des résultats de la recherche, voir Collecter des données [pour un cas.](create-search-to-collect-data.md)</span><span class="sxs-lookup"><span data-stu-id="bfe2d-130">For information about how you can create a search, build a search query, and view the search results, see [Collect data for a case](create-search-to-collect-data.md).</span></span>

## <a name="step-2-create-a-conversation-review-set"></a><span data-ttu-id="bfe2d-131">Étape 2 : Créer un groupe de révision de conversation</span><span class="sxs-lookup"><span data-stu-id="bfe2d-131">Step 2: Create a conversation review set</span></span>

<span data-ttu-id="bfe2d-132">Dans un jeu à réviser, vous pouvez rechercher, baliser, annoter et écrire des documents, des messages électroniques et des conversations.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-132">In a review set, you can search, tag, annotate, and redact documents, email messages, and chat conversations.</span></span> <span data-ttu-id="bfe2d-133">Dans Advanced eDiscovery, vous pouvez personnaliser votre révision des conversations, en fonction de messages individuels ou de conversations threadées.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-133">In Advanced eDiscovery, you can customize your review of conversations, based in individual messages or threaded conversations.</span></span> <span data-ttu-id="bfe2d-134">Cela est déterminé par le type de jeu à réviser à partir de quel type vous ajoutez les résultats de la recherche créée à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-134">This is determined by the type of review set that you add the results of the search created in Step 1 to.</span></span> <span data-ttu-id="bfe2d-135">Il existe deux types différents d’ensembles de révision :</span><span class="sxs-lookup"><span data-stu-id="bfe2d-135">There are two different types of review sets:</span></span> 
  
  - <span data-ttu-id="bfe2d-136">**Ensembles de révision standard :** Les messages des conversations sont traitées et affichées en tant qu’éléments individuels.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-136">**Standard review sets:** Messages in conversations are processed and displayed as individual items.</span></span> 
  
  -  <span data-ttu-id="bfe2d-137">**Ensembles de révision de conversation :** Les messages dans les conversations sont traitées individuellement mais affichées dans un affichage conversation.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-137">**Conversation review sets:** Messages in conversations are processed individually but displayed in a conversation view.</span></span> <span data-ttu-id="bfe2d-138">Dans un groupe de révision de conversation, vous pouvez annoter, baliser et redacter des messages dans un affichage de conversation thread.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-138">In a conversation review set, you can annotate, tag, and redact messages in a threaded conversation view.</span></span> 

<span data-ttu-id="bfe2d-139">Pour plus d’informations sur la façon de réviser et de gérer le contenu d’un jeu à réviser, voir [Gérer les ensembles de révision.](managing-review-sets.md)</span><span class="sxs-lookup"><span data-stu-id="bfe2d-139">For more information about how to review and manage content in a review set, see [Manage review sets](managing-review-sets.md).</span></span> 

## <a name="step-3-enable-conversation-retrieval-options"></a><span data-ttu-id="bfe2d-140">Étape 3 : Activer les options de récupération des conversations</span><span class="sxs-lookup"><span data-stu-id="bfe2d-140">Step 3: Enable conversation retrieval options</span></span>

<span data-ttu-id="bfe2d-141">Après avoir examiné et finalisé votre requête de recherche, vous pouvez ajouter les résultats de la recherche à un jeu à réviser.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-141">After you have reviewed and finalized your search query, you can add the search results to a review set.</span></span> <span data-ttu-id="bfe2d-142">Lorsque vous ajoutez vos résultats de recherche dans un jeu à réviser, les données d’origine sont copiées dans une zone de stockage Azure pour faciliter le processus de révision et d’analyse.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-142">When you add your search results into a review set, the original data is copied to an Azure Storage area to facilitate the review and analysis process.</span></span> <span data-ttu-id="bfe2d-143">Pour plus d’informations sur l’ajout de résultats de recherche à un jeu à réviser, voir Ajouter des résultats de [recherche à un jeu à réviser.](add-data-to-review-set.md)</span><span class="sxs-lookup"><span data-stu-id="bfe2d-143">For more information about adding search results to a review set, see [Add search results to a review set](add-data-to-review-set.md).</span></span> 

<span data-ttu-id="bfe2d-144">Lorsque vous ajoutez des données de conversations à un jeu à réviser, vous pouvez utiliser les options de récupération de conversation pour développer votre recherche et inclure des messages contextuels.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-144">When you add data from conversations to a review set, you can use the conversation retrieval options to expand your search and include contextual messages.</span></span> <span data-ttu-id="bfe2d-145">Une fois que vous avez définie les options de récupération de conversation, les choses suivantes peuvent se produire :</span><span class="sxs-lookup"><span data-stu-id="bfe2d-145">After you set the conversation retrieval options, the following things can happen:</span></span>

  ![Récupération de conversation](../media/messagesandconversations.png)
  
1. <span data-ttu-id="bfe2d-147">À l’aide d’une requête de mot clé et de plage de dates, la recherche a renvoyé un succès sur *le message 3*.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-147">Using a keyword and date range query, the search returned a hit on *Message 3*.</span></span> <span data-ttu-id="bfe2d-148">Ce message faisait partie d’une conversation plus importante, illustrée par *CRC1*.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-148">This message was part of a larger conversation, illustrated by *CRC1*.</span></span> 
  
2. <span data-ttu-id="bfe2d-149">Lorsque vous ajoutez les données dans un jeu à réviser et activez les options de récupération de conversation, Advanced eDiscovery retourne et collecte d’autres éléments dans *CRC1*.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-149">When you add the data into a review set and enable the conversation retrieval options, Advanced eDiscovery will go back and collect other items in *CRC1*.</span></span> 
  
3. <span data-ttu-id="bfe2d-150">Une fois que les éléments ont été ajoutés au jeu à réviser, vous pouvez passer en revue tous les messages individuels à partir *de CRC1*.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-150">After the items have been added to the review set, you can review all the individual messages from *CRC1*.</span></span> 

<span data-ttu-id="bfe2d-151">Pour activer la récupération de conversation :</span><span class="sxs-lookup"><span data-stu-id="bfe2d-151">To enable conversation retrieval:</span></span>
  
1. <span data-ttu-id="bfe2d-152">Sous **l’onglet Recherches** dans le cas Advanced eDiscovery,  sélectionnez une recherche, puis cliquez sur Ajouter à la révision définie sur la page volante.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-152">On the **Searches** tab in the Advanced eDiscovery case, select a search, and then click **Add to review set** on the flyout page.</span></span>
  
2. <span data-ttu-id="bfe2d-153">Sélectionnez un jeu à réviser existant ou créez-en un.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-153">Select an existing review set or create a review set.</span></span> <span data-ttu-id="bfe2d-154">Vous pouvez configurer les options de récupération lors de l’ajout de résultats de recherche à un jeu à réviser standard ou conversation.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-154">You can configure retrieval options when adding search results to a standard or a conversation review set.</span></span>
  
3. <span data-ttu-id="bfe2d-155">Sous **Options de collecte,** configurez les options de récupération de conversation pour les sources  de contenu que vous souhaitez développer dans votre recherche, puis cliquez sur Ajouter pour démarrer le processus.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-155">Under **Collection options**, configure the conversation retrieval options for the content sources that you want to expand in your search, and then click **Add** to start the process.</span></span>  
  
4. <span data-ttu-id="bfe2d-156">Une fois **que le travail Ajouter à l’ensemble de** révision sous l’onglet **Travaux** est terminé, vous pouvez commencer à examiner les conversations.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-156">After the **Add to review set** job on the **Jobs** tab has finished, you can start reviewing the conversations.</span></span>

## <a name="step-4-review-and-export-conversations-in-a-review-set"></a><span data-ttu-id="bfe2d-157">Étape 4 : Examiner et exporter des conversations dans un jeu à réviser</span><span class="sxs-lookup"><span data-stu-id="bfe2d-157">Step 4: Review and export conversations in a review set</span></span>

<span data-ttu-id="bfe2d-158">Une fois que le contenu a été traitée et ajoutée au jeu à réviser, vous pouvez commencer à examiner les données du jeu à réviser.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-158">After the content has been processed and added to the review set, you can start reviewing the data in the review set.</span></span> <span data-ttu-id="bfe2d-159">Les fonctionnalités de révision sont différentes selon que le contenu a été ajouté à un jeu à réviser standard ou à un groupe de révision de conversation.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-159">The review capabilities are different depending on whether the content was added to a standard review set or a conversation review set.</span></span> 

### <a name="reviewing-conversations-in-a-standard-review-set"></a><span data-ttu-id="bfe2d-160">Examen des conversations dans un jeu à réviser standard</span><span class="sxs-lookup"><span data-stu-id="bfe2d-160">Reviewing conversations in a standard review set</span></span>

<span data-ttu-id="bfe2d-161">Dans un jeu à réviser standard, les messages sont traitées et affichées en tant qu’éléments individuels, comme ils sont stockés dans un dossier de boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-161">In a standard review set, messages are processed and displayed as individual items, similar to how they're stored in a mailbox folder.</span></span> <span data-ttu-id="bfe2d-162">Dans ce flux de travail, chaque message est traitée en tant qu’élément distinct.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-162">In this workflow, each message is processed as a separate item.</span></span> <span data-ttu-id="bfe2d-163">Par conséquent, les options de synthèse de thread et d’exportation ne sont pas disponibles dans un jeu à réviser standard.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-163">As a result, the threaded summary and export options aren't available in a standard review set.</span></span> 

  ![Jeu à réviser standard](../media/standardrs.PNG)

### <a name="reviewing-conversations-in-a-conversation-review-set"></a><span data-ttu-id="bfe2d-165">Examen des conversations dans un groupe de révision de conversation</span><span class="sxs-lookup"><span data-stu-id="bfe2d-165">Reviewing conversations in a conversation review set</span></span>

<span data-ttu-id="bfe2d-166">Dans un groupe de révision de conversation, les messages individuels sont threadés ensemble et présentés en tant que conversations.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-166">In a conversation review set, individual messages are threaded together and presented as conversations.</span></span> <span data-ttu-id="bfe2d-167">Cela vous permet de passer en revue et d’exporter des conversations contextuelles.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-167">This lets you review and export contextual conversations.</span></span> 

  ![Ensemble de révision de conversation](../media/ConversationRSOptions.PNG)

<span data-ttu-id="bfe2d-169">Les sections suivantes décrivent l’examen et l’exportation de conversations dans un groupe de révision de conversation.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-169">The following sections describe reviewing and exporting conversations in a conversation review set.</span></span>

#### <a name="reviewing-conversations"></a><span data-ttu-id="bfe2d-170">Examen des conversations</span><span class="sxs-lookup"><span data-stu-id="bfe2d-170">Reviewing conversations</span></span>

<span data-ttu-id="bfe2d-171">Dans un groupe de révision de conversation, vous pouvez utiliser les options suivantes pour faciliter le processus de révision.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-171">In a conversation review set, you can use the following options to facilitate the review process.</span></span>

- <span data-ttu-id="bfe2d-172">**Grouper par conversation :** Groupe les messages au sein d’une même conversation pour aider les utilisateurs à simplifier et accélérer leur processus de révision.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-172">**Group by conversation:** Groups messages within the same conversation together to help users simplify and expedite their review process.</span></span> 

- <span data-ttu-id="bfe2d-173">**Vue récapitulatif :** Affiche la conversation threadée.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-173">**Summary view:** Displays the threaded conversation.</span></span> <span data-ttu-id="bfe2d-174">Dans cette vue, vous pouvez voir la conversation entière et accéder aux métadonnées de chaque message individuel.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-174">In this view, you can see the entire conversation and also access the metadata for each individual message.</span></span>  
  
   - <span data-ttu-id="bfe2d-175">Afficher les métadonnées des messages individuels</span><span class="sxs-lookup"><span data-stu-id="bfe2d-175">View metadata for individual messages</span></span>
   
   - <span data-ttu-id="bfe2d-176">Télécharger des messages individuels</span><span class="sxs-lookup"><span data-stu-id="bfe2d-176">Download individual messages</span></span>

- <span data-ttu-id="bfe2d-177">**Affichage texte :** Fournit le texte extrait pour l’intégralité de la conversation.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-177">**Text view:** Provides the extracted text for the entire conversation.</span></span> 

- <span data-ttu-id="bfe2d-178">**Affichage annoter :** Vous permet de marquer un affichage thread de la conversation.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-178">**Annotate view:** Lets you markup a threaded view of the conversation.</span></span> <span data-ttu-id="bfe2d-179">Tous les messages de la conversation partagent le même document annoté.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-179">All messages in the conversation share the same annotated document.</span></span>

- <span data-ttu-id="bfe2d-180">**Marquage :** Lorsque vous visualisez des conversations dans un jeu  à réviser, vous pouvez afficher et appliquer des balises en cliquant sur le panneau marquage dans le panneau de codage.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-180">**Tagging:** When viewing conversations in a review set, you can view and apply tags by clicking **Tagging panel** in the Coding panel.</span></span>

- <span data-ttu-id="bfe2d-181">**Réexécutez la conversion de conversation :** Lorsque des messages sont ajoutés à un groupe de révision de conversation, un travail de conversion est automatiquement exécuté pour créer le résumé de thread et annoter des affichages.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-181">**Rerun conversation conversion:** When messages are added to a conversation review set, a conversion job is automatically run to create the threaded summary and annotate views.</span></span> <span data-ttu-id="bfe2d-182">Si le travail de reconstruction de conversation échoue, vous pouvez réexécuter ce travail en cliquant sur Action > Créer des **PDF** de conversation dans le jeu à réviser.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-182">If the Conversation Reconstruction job fails, you can rerun this job by clicking **Action > Create conversation PDFs** in the review set.</span></span>

#### <a name="exporting-conversations"></a><span data-ttu-id="bfe2d-183">Exportation de conversations</span><span class="sxs-lookup"><span data-stu-id="bfe2d-183">Exporting conversations</span></span>

<span data-ttu-id="bfe2d-184">Dans un groupe de révision de conversation, vous pouvez définir les options suivantes pour exporter des conversations :</span><span class="sxs-lookup"><span data-stu-id="bfe2d-184">In a conversation review set, you can set the following options to export conversations:</span></span>

![Exporter les options pour les conversations](../media/export.png)

<span data-ttu-id="bfe2d-186">a.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-186">a.</span></span> <span data-ttu-id="bfe2d-187">Options de métadonnées</span><span class="sxs-lookup"><span data-stu-id="bfe2d-187">Metadata options</span></span>

   - <span data-ttu-id="bfe2d-188">**Charger le fichier :** Les métadonnées sont incluses pour chaque message, message électronique et document.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-188">**Load file:** Metadata is included for each individual message, email, and document.</span></span> <span data-ttu-id="bfe2d-189">Il existe une ligne pour chaque message d’une conversation.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-189">There is one row for each message in a conversation.</span></span> 

   - <span data-ttu-id="bfe2d-190">**Balises :** Les balises de votre processus de révision sont incluses dans le fichier de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-190">**Tags:** Tags from your review process are included in the metadata file.</span></span> <span data-ttu-id="bfe2d-191">Les messages d’une conversation partagent les mêmes balises.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-191">Messages in a conversation share the same tags.</span></span> 

<span data-ttu-id="bfe2d-192">b.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-192">b.</span></span> <span data-ttu-id="bfe2d-193">Options de conversation</span><span class="sxs-lookup"><span data-stu-id="bfe2d-193">Conversation options</span></span>
  
   - <span data-ttu-id="bfe2d-194">**Fichiers de conversation :** Lorsque vous exportez des fichiers de conversation, l’affichage annoté est converti en fichier PDF et téléchargé dans le dossier d’exportation.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-194">**Conversation files:** When you export conversation files, the annotated view is converted to a PDF file and downloaded to the export folder.</span></span> <span data-ttu-id="bfe2d-195">Les messages d’un fichier de conversation pointent vers la version PDF du même fichier de conversation.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-195">Messages in one conversation file point to the PDF version of the same conversation file.</span></span>  
  
   - <span data-ttu-id="bfe2d-196">**Messages de conversation individuels :** Lorsque vous exportez des messages individuels, chaque message unique de la conversation est exporté en tant qu’élément autonome.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-196">**Individual chat messages:** When you export individual messages, each unique message in the conversation is exported as a standalone item.</span></span> <span data-ttu-id="bfe2d-197">Le fichier est exporté au même format que dans la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-197">The file is exported in the same format that it was saved as in the mailbox.</span></span> <span data-ttu-id="bfe2d-198">Pour une conversation spécifique, vous recevez plusieurs fichiers .msg.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-198">For a specific conversation, you receive multiple .msg files.</span></span> 

     >[!NOTE]
     > <span data-ttu-id="bfe2d-199">Si vous avez appliqué des annotations au fichier de conversation, ces annotations ne seront pas transférées vers les messages individuels.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-199">If you applied annotations to the conversation file, these annotations won't be transferred to the individual messages.</span></span> 

<span data-ttu-id="bfe2d-200">c.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-200">c.</span></span> <span data-ttu-id="bfe2d-201">Autres options</span><span class="sxs-lookup"><span data-stu-id="bfe2d-201">Other options</span></span>

   - <span data-ttu-id="bfe2d-202">**Générer des fichiers texte pour tout le contenu exporté :** Génère un fichier texte pour chaque conversation exportée à partir du jeu à réviser.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-202">**Generate text files for all exported content:** Generates a text file for each conversation exported from the review set.</span></span> 

   - <span data-ttu-id="bfe2d-203">**Remplacez le contenu exporté par des PDF rédigés :** Si des fichiers de conversation rédigés sont générés pendant le processus de révision, ces fichiers sont disponibles pendant l’exportation.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-203">**Replace exported content with redacted PDFs:** If redacted conversation files are generated during the review process, then these files are available during export.</span></span> <span data-ttu-id="bfe2d-204">Vous pouvez décider d’exporter uniquement les fichiers natifs (en ne sélectionnant pas cette option) ou de remplacer les fichiers natifs par les versions expurgées des fichiers natifs (en sélectionnant cette option), qui sont exportés en tant que fichiers PDF.</span><span class="sxs-lookup"><span data-stu-id="bfe2d-204">You can decided whether to export only the native files (by not selecting this option) or to replace the native files with the redacted versions of the native files (by selecting this option), which are exported as PDF files.</span></span>

## <a name="more-information"></a><span data-ttu-id="bfe2d-205">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="bfe2d-205">More information</span></span>

<span data-ttu-id="bfe2d-206">Pour en savoir plus sur l’examen des données de cas dans Advanced eDiscovery, consultez les articles suivants :</span><span class="sxs-lookup"><span data-stu-id="bfe2d-206">To learn more about how to review case data in Advanced eDiscovery, see the following articles:</span></span>

- [<span data-ttu-id="bfe2d-207">Afficher les données de cas</span><span class="sxs-lookup"><span data-stu-id="bfe2d-207">View case data</span></span>](view-documents-in-review-set.md)

- [<span data-ttu-id="bfe2d-208">Analyser les données de cas</span><span class="sxs-lookup"><span data-stu-id="bfe2d-208">Analyze case data</span></span>](analyzing-data-in-review-set.md)

- [<span data-ttu-id="bfe2d-209">Exporter les données de cas</span><span class="sxs-lookup"><span data-stu-id="bfe2d-209">Export case data</span></span>](exporting-data-ediscover20.md)
