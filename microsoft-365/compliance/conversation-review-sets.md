---
title: Examiner les conversations dans Advanced eDiscovery
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: d03df51df3c6314dcec072b5c3b8573a36c279d0
ms.sourcegitcommit: 1162d676b036449ea4220de8a6642165190e3398
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/20/2019
ms.locfileid: "37078759"
---
# <a name="review-conversations-in-advanced-ediscovery"></a><span data-ttu-id="7a8c7-102">Examiner les conversations dans Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="7a8c7-102">Review conversations in Advanced eDiscovery</span></span> 

<span data-ttu-id="7a8c7-103">La messagerie instantanée constitue un moyen pratique de poser des questions, de partager des idées ou de communiquer rapidement entre les grands publics.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-103">Instant messaging is a convenient way to ask questions, share ideas, or quickly communicate across large audiences.</span></span> <span data-ttu-id="7a8c7-104">Comme les plateformes de messagerie instantanée, telles que Microsoft Teams, deviennent essentielles à la collaboration d’entreprise, les organisations doivent évaluer la façon dont leur flux de travail eDiscovery répond à ces nouveaux types de communication et de collaboration.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-104">As instant messaging platforms, like Microsoft Teams, become core to enterprise collaboration, organizations must evaluate how their eDiscovery workflow addresses these new forms of communication and collaboration.</span></span> 

<span data-ttu-id="7a8c7-105">La fonctionnalité de reconstruction de conversation dans Advanced eDiscovery est conçue pour vous aider à identifier le contenu contextuel et à générer des affichages de conversation distincts.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-105">The Conversation Reconstruction feature in Advanced eDiscovery is designed to help you identify contextual content and produce distinct conversation views.</span></span> <span data-ttu-id="7a8c7-106">Cette fonctionnalité vous permet d’examiner efficacement et rapidement les conversations de messagerie instantanée complètes (également appelées « *conversations thématiques*») qui sont générées sur des plateformes telles que Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-106">This capability allows you to efficiently and rapidly review complete instant message conversations (also called *threaded conversations*) that are generated in platforms like Microsoft Teams.</span></span>

<span data-ttu-id="7a8c7-107">Avec la reconstruction des conversations, vous pouvez utiliser les fonctionnalités intégrées pour reconstruire, examiner et exporter les conversations thématiques.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-107">With Conversation Reconstruction, you can use built-in capabilities to reconstruct, review, and export threaded conversations.</span></span> <span data-ttu-id="7a8c7-108">Utilisez la reconstruction avancée de conversation eDiscovery pour :</span><span class="sxs-lookup"><span data-stu-id="7a8c7-108">Use Advanced eDiscovery Conversation Reconstruction to:</span></span>

- <span data-ttu-id="7a8c7-109">Conserver des métadonnées de niveau de message uniques pour tous les messages au sein d’une conversation.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-109">Preserve unique message-level metadata across all messages within a conversation.</span></span>

- <span data-ttu-id="7a8c7-110">Collectez des messages contextuels dans vos résultats de recherche.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-110">Collect contextual messages around your search results.</span></span>

- <span data-ttu-id="7a8c7-111">Vérifier, annoter et biffer les conversations thématiques.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-111">Review, annotate, and redact threaded conversations.</span></span>

- <span data-ttu-id="7a8c7-112">Exporter des messages individuels ou des conversations thématiques</span><span class="sxs-lookup"><span data-stu-id="7a8c7-112">Export individual messages or threaded conversations</span></span>

## <a name="terminology"></a><span data-ttu-id="7a8c7-113">Terminologie</span><span class="sxs-lookup"><span data-stu-id="7a8c7-113">Terminology</span></span>

<span data-ttu-id="7a8c7-114">Voici quelques définitions pour vous aider à commencer à utiliser la reconstruction des conversations.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-114">Here are few definitions to help you get start using Conversation Reconstruction.</span></span>

- <span data-ttu-id="7a8c7-115">**Messages :** Représente la plus petite unité d’une conversation.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-115">**Messages:** Represent the smallest unit of a conversation.</span></span> <span data-ttu-id="7a8c7-116">Les messages peuvent varier en taille, en structure et en métadonnées.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-116">Messages may vary in size, structure, and metadata.</span></span> 

- <span data-ttu-id="7a8c7-117">**Conversation :** Représente un regroupement d’un ou plusieurs messages.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-117">**Conversation:** Represents a grouping of one or more messages.</span></span> <span data-ttu-id="7a8c7-118">Dans différentes applications, les conversations peuvent être représentées de différentes manières.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-118">Across different applications, conversations may be represented in different ways.</span></span> <span data-ttu-id="7a8c7-119">Dans certaines applications, il existe une action explicite qui résulte de la réponse à un message existant.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-119">In some applications, there is an explicit action that results from replying to an existing message.</span></span> <span data-ttu-id="7a8c7-120">Les conversations sont formées de manière explicite à la suite de cette action de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-120">Conversations are formed explicitly as a result of this user action.</span></span> <span data-ttu-id="7a8c7-121">Par exemple, voici une capture d’écran d’une conversation de canal dans Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-121">For example, here is a screenshot of a channel conversation in Microsoft Teams.</span></span>

   ![Conversation de canal Microsoft teams](media/threadedchat.png)

   <span data-ttu-id="7a8c7-123">Dans d’autres applications (telles que les messages de conversation 1xN dans Teams), il n’y a pas de chaîne de réponse formelle et les messages s’affichent en tant que « plates-messages » dans un seul thread.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-123">In other apps (such as 1xN chat messages in Teams), there is not a formal reply chain and instead messages appear as a "flat river of messages" within a single thread.</span></span> <span data-ttu-id="7a8c7-124">Dans ces types d’applications, les conversations sont déduites à partir d’un groupe de messages qui se produisent au cours d’une période donnée.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-124">In these types apps, conversations are inferred from a group of messages that occur within a certain time.</span></span> <span data-ttu-id="7a8c7-125">Ce « regroupement conditionnel » de messages (par opposition à une chaîne de réponse) représente la conversation « en arrière » sur un sujet spécifique.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-125">This "soft-grouping" of messages (as opposed to a reply chain) represent the "back and forth" conversation about a specific topic of interest.</span></span> 

## <a name="step-1-run-a-search"></a><span data-ttu-id="7a8c7-126">Étape 1 : exécution d’une recherche</span><span class="sxs-lookup"><span data-stu-id="7a8c7-126">Step 1: Run a search</span></span>

<span data-ttu-id="7a8c7-127">Une fois que vous avez identifié les dépositaires pertinents et les emplacements de contenu, vous pouvez créer une recherche pour rechercher du contenu potentiellement pertinent.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-127">After you have identified relevant custodians and content locations, you can create a search to find potentially relevant content.</span></span> <span data-ttu-id="7a8c7-128">Sous l’onglet **recherches** du cas Advanced eDiscovery, vous pouvez créer une recherche en cliquant sur **nouvelle recherche** et en suivant l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-128">On the **Searches** tab in the Advanced eDiscovery case, you can create a search by clicking **New search** and following the wizard.</span></span> <span data-ttu-id="7a8c7-129">Pour plus d’informations sur la création d’une recherche, la création d’une requête de recherche et l’affichage des résultats de la recherche, reportez-vous à la rubrique [collecte de données pour un cas](create-search-to-collect-data.md).</span><span class="sxs-lookup"><span data-stu-id="7a8c7-129">For information about how you can create a search, build a search query, and view the search results, see [Collect data for a case](create-search-to-collect-data.md).</span></span>

## <a name="step-2-create-a-conversation-review-set"></a><span data-ttu-id="7a8c7-130">Étape 2 : créer un ensemble de révision de conversation</span><span class="sxs-lookup"><span data-stu-id="7a8c7-130">Step 2: Create a conversation review set</span></span>

<span data-ttu-id="7a8c7-131">Dans un jeu de vérification, vous pouvez rechercher, marquer, annoter et biffer des documents, des messages électroniques et des conversations de conversation.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-131">In a review set, you can search, tag, annotate, and redact documents, email messages, and chat conversations.</span></span> <span data-ttu-id="7a8c7-132">Dans Advanced eDiscovery, vous pouvez personnaliser votre révision des conversations, basée sur des messages individuels ou sur des conversations thématiques.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-132">In Advanced eDiscovery, you can customize your review of conversations, based in individual messages or threaded conversations.</span></span> <span data-ttu-id="7a8c7-133">Cela est déterminé par le type d’ensemble de révision que vous ajoutez les résultats de la recherche créée à l’étape 1 à.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-133">This is determined by the type of review set that you add the results of the search created in Step 1 to.</span></span> <span data-ttu-id="7a8c7-134">Il existe deux types différents de jeux de révision :</span><span class="sxs-lookup"><span data-stu-id="7a8c7-134">There are two different types of review sets:</span></span> 
  
  - <span data-ttu-id="7a8c7-135">**Ensembles de révision standard :** Les messages dans les conversations sont traités et affichés en tant qu’éléments individuels.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-135">**Standard review sets:** Messages in conversations are processed and displayed as individual items.</span></span> 
  
  -  <span data-ttu-id="7a8c7-136">**Ensembles de révision de conversation :** Les messages dans les conversations sont traités individuellement, mais affichés en mode conversation.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-136">**Conversation review sets:** Messages in conversations are processed individually but displayed in a conversation view.</span></span> <span data-ttu-id="7a8c7-137">Dans un ensemble de révision de conversation, vous pouvez annoter, Baliser et biffer des messages dans un affichage de conversation de thème.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-137">In a conversation review set, you can annotate, tag, and redact messages in a threaded conversation view.</span></span> 

<span data-ttu-id="7a8c7-138">Pour plus d’informations sur la révision et la gestion du contenu d’un jeu de révision, voir [Manage Review sets](managing-review-sets.md).</span><span class="sxs-lookup"><span data-stu-id="7a8c7-138">For more information about how to review and manage content in a review set, see [Manage review sets](managing-review-sets.md).</span></span> 

## <a name="step-3-enable-conversation-retrieval-options"></a><span data-ttu-id="7a8c7-139">Étape 3 : activer les options de récupération de conversation</span><span class="sxs-lookup"><span data-stu-id="7a8c7-139">Step 3: Enable conversation retrieval options</span></span>

<span data-ttu-id="7a8c7-140">Une fois que vous avez vérifié et finalisé votre requête de recherche, vous pouvez ajouter les résultats de la recherche à un jeu de révision.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-140">After you have reviewed and finalized your search query, you can add the search results to a review set.</span></span> <span data-ttu-id="7a8c7-141">Lorsque vous ajoutez vos résultats de recherche dans un jeu de révision, les données d’origine sont copiées dans une zone de stockage Azure pour faciliter le processus de révision et d’analyse.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-141">When you add your search results into a review set, the original data is copied to an Azure Storage area to facilitate the review and analysis process.</span></span> <span data-ttu-id="7a8c7-142">Pour plus d’informations sur l’ajout de résultats de recherche à un jeu de révision, voir [Ajouter des résultats de recherche à un jeu de révision](add-data-to-review-set.md).</span><span class="sxs-lookup"><span data-stu-id="7a8c7-142">For more information about adding search results to a review set, see [Add search results to a review set](add-data-to-review-set.md).</span></span> 

<span data-ttu-id="7a8c7-143">Lorsque vous ajoutez des données de conversations à un ensemble de vérification, vous pouvez utiliser les options de récupération de conversation pour étendre votre recherche et inclure des messages contextuels.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-143">When you add data from conversations to a review set, you can use the conversation retrieval options to expand your search and include contextual messages.</span></span> <span data-ttu-id="7a8c7-144">Une fois que vous avez défini les options de récupération de conversation, les opérations suivantes peuvent se produire :</span><span class="sxs-lookup"><span data-stu-id="7a8c7-144">After you set the conversation retrieval options, the following things can happen:</span></span>

  ![Récupération de conversation](media/messagesandconversations.png)
  
1. <span data-ttu-id="7a8c7-146">À l’aide d’une requête de mot clé et de plage de dates, la recherche a renvoyé une correspondance sur le *message 3*.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-146">Using a keyword and date range query, the search returned a hit on *Message 3*.</span></span> <span data-ttu-id="7a8c7-147">Ce message faisait partie d’une conversation plus large, illustrée par *CRC1*.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-147">This message was part of a larger conversation, illustrated by *CRC1*.</span></span> 
  
2. <span data-ttu-id="7a8c7-148">Lorsque vous ajoutez les données à un jeu de révision et activez les options de récupération de conversation, Advanced eDiscovery reviendra et collectera d’autres éléments dans *CRC1*.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-148">When you add the data into a review set and enable the conversation retrieval options, Advanced eDiscovery will go back and collect other items in *CRC1*.</span></span> 
  
3. <span data-ttu-id="7a8c7-149">Une fois que les éléments ont été ajoutés à l’ensemble de vérification, vous pouvez passer en revue tous les messages individuels de *CRC1*.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-149">After the items have been added to the review set, you can review all the individual messages from *CRC1*.</span></span> 



<span data-ttu-id="7a8c7-150">Pour activer la récupération de conversation :</span><span class="sxs-lookup"><span data-stu-id="7a8c7-150">To enable conversation retrieval:</span></span>
  
1. <span data-ttu-id="7a8c7-151">Sous l’onglet **recherches** dans le cas avancé eDiscovery, sélectionnez une recherche, puis cliquez sur **Ajouter pour examiner le jeu** sur la page de menu volant.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-151">On the **Searches** tab in the Advanced eDiscovery case, select a search, and then click **Add to review set** on the flyout page.</span></span>
  
2. <span data-ttu-id="7a8c7-152">Sélectionnez un ensemble de révision existant ou créez un jeu de révision.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-152">Select an existing review set or create a review set.</span></span> <span data-ttu-id="7a8c7-153">Vous pouvez configurer les options de récupération lors de l’ajout de résultats de recherche à un jeu de révision de conversation ou standard.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-153">You can configure retrieval options when adding search results to a standard or a conversation review set.</span></span>
  
3. <span data-ttu-id="7a8c7-154">Sous **options de collection**, configurez les options de récupération de conversation pour les sources de contenu que vous souhaitez développer dans votre recherche, puis cliquez sur **Ajouter** pour démarrer le processus.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-154">Under **Collection options**, configure the conversation retrieval options for the content sources that you want to expand in your search, and then click **Add** to start the process.</span></span>  
  
4. <span data-ttu-id="7a8c7-155">Une fois que le travail **Ajouter au jeu de révision** sous l’onglet **travaux** a terminé, vous pouvez commencer à examiner les conversations.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-155">After the **Add to review set** job on the **Jobs** tab has finished, you can start reviewing the conversations.</span></span>

## <a name="step-4-review-conversations-in-the-review-set"></a><span data-ttu-id="7a8c7-156">Étape 4 : examiner les conversations dans l’ensemble de révision</span><span class="sxs-lookup"><span data-stu-id="7a8c7-156">Step 4: Review conversations in the review set</span></span>

<span data-ttu-id="7a8c7-157">Une fois que le contenu a été traité et ajouté à l’ensemble de vérifications, vous pouvez commencer à examiner les données dans l’ensemble de révision.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-157">After the content has been processed and added to the review set, you can start reviewing the data in the review set.</span></span> <span data-ttu-id="7a8c7-158">Les fonctionnalités de révision sont différentes selon que le contenu a été ajouté à un jeu de révision standard ou à un ensemble de révision de conversation.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-158">The review capabilities are different depending on whether the content was added to a standard review set or a conversation review set.</span></span> 

### <a name="reviewing-conversations-in-a-standard-review-set"></a><span data-ttu-id="7a8c7-159">Examen des conversations dans un jeu de révision standard</span><span class="sxs-lookup"><span data-stu-id="7a8c7-159">Reviewing conversations in a standard review set</span></span>

<span data-ttu-id="7a8c7-160">Dans un ensemble de révision standard, les messages sont traités et affichés en tant qu’éléments individuels, de la même manière qu’ils sont stockés dans un dossier de boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-160">In a standard review set, messages are processed and displayed as individual items, similar to how they're stored in a mailbox folder.</span></span> <span data-ttu-id="7a8c7-161">Dans ce flux de travail, chaque message est traité comme un élément distinct.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-161">In this workflow, each message is processed as a separate item.</span></span> <span data-ttu-id="7a8c7-162">Par conséquent, le résumé lié et les options d’exportation ne sont pas disponibles dans un jeu de révision standard.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-162">As a result, the threaded summary and export options aren't available in a standard review set.</span></span> 

  ![Ensemble de révision standard](media/standardrs.PNG)

### <a name="reviewing-conversations-in-a-conversation-review-set"></a><span data-ttu-id="7a8c7-164">Examen des conversations dans un jeu de révision de conversation</span><span class="sxs-lookup"><span data-stu-id="7a8c7-164">Reviewing conversations in a conversation review set</span></span>

<span data-ttu-id="7a8c7-165">Dans un ensemble de révision de conversation, les messages individuels sont regroupés et présentés sous forme de conversations.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-165">In a conversation review set, individual messages are threaded together and presented as conversations.</span></span> <span data-ttu-id="7a8c7-166">Cela vous permet de passer en revue et d’exporter des conversations contextuelles.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-166">This lets you review and export contextual conversations.</span></span> 

  ![Ensemble de révision de conversation](media/ConversationRSOptions.PNG)

<span data-ttu-id="7a8c7-168">Les sections suivantes décrivent la révision et l’exportation de conversations dans un jeu de révision de conversation.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-168">The following sections describe reviewing and exporting conversations in a conversation review set.</span></span>

#### <a name="reviewing-conversations"></a><span data-ttu-id="7a8c7-169">Examen des conversations</span><span class="sxs-lookup"><span data-stu-id="7a8c7-169">Reviewing conversations</span></span>

<span data-ttu-id="7a8c7-170">Dans un ensemble de révision de conversation, vous pouvez utiliser les options suivantes pour faciliter le processus de révision.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-170">In a conversation review set, you can use the following options to facilitate the review process.</span></span>

- <span data-ttu-id="7a8c7-171">**Regrouper par conversation :** Regroupe les messages au sein d’une même conversation pour aider les utilisateurs à simplifier et accélérer leur processus de révision.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-171">**Group by conversation:** Groups messages within the same conversation together to help users simplify and expedite their review process.</span></span> 

- <span data-ttu-id="7a8c7-172">**Affichage de Résumé :** Affiche la conversation de threads.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-172">**Summary view:** Displays the threaded conversation.</span></span> <span data-ttu-id="7a8c7-173">Dans cet affichage, vous pouvez voir l’intégralité de la conversation et accéder aux métadonnées de chaque message individuel.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-173">In this view, you can see the entire conversation and also access the metadata for each individual message.</span></span>  
  
   - <span data-ttu-id="7a8c7-174">Afficher les métadonnées des messages individuels</span><span class="sxs-lookup"><span data-stu-id="7a8c7-174">View metadata for individual messages</span></span>
   
   - <span data-ttu-id="7a8c7-175">Télécharger des messages individuels</span><span class="sxs-lookup"><span data-stu-id="7a8c7-175">Download individual messages</span></span>

- <span data-ttu-id="7a8c7-176">**Affichage de texte :** Fournit le texte extrait pour l’intégralité de la conversation.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-176">**Text view:** Provides the extracted text for the entire conversation.</span></span> 

- <span data-ttu-id="7a8c7-177">**Annoter :** Vous permet de baliser une vue thématique de la conversation.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-177">**Annotate view:** Lets you markup a threaded view of the conversation.</span></span> <span data-ttu-id="7a8c7-178">Tous les messages de la conversation partagent le même document annoté.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-178">All messages in the conversation share the same annotated document.</span></span>

- <span data-ttu-id="7a8c7-179">**Balisage :** Lors de l’affichage des conversations dans un jeu de vérification, vous pouvez afficher et appliquer des balises en cliquant sur **panneau de marquage** dans le panneau codage.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-179">**Tagging:** When viewing conversations in a review set, you can view and apply tags by clicking **Tagging panel** in the Coding panel.</span></span>

- <span data-ttu-id="7a8c7-180">**Réexécuter la conversion de conversation :** Lorsque des messages sont ajoutés à un jeu de révision de conversation, une tâche de conversion est automatiquement exécutée pour créer le résumé lié aux threads et annoter les vues.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-180">**Rerun conversation conversion:** When messages are added to a conversation review set, a conversion job is automatically run to create the threaded summary and annotate views.</span></span> <span data-ttu-id="7a8c7-181">Si le travail de reconstruction des conversations échoue, vous pouvez réexécuter ce travail en cliquant sur **Action > créer un fichier PDF de conversation** dans l’ensemble de révision.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-181">If the Conversation Reconstruction job fails, you can rerun this job by clicking **Action > Create conversation PDFs** in the review set.</span></span>


#### <a name="exporting-conversations"></a><span data-ttu-id="7a8c7-182">Exportation de conversations</span><span class="sxs-lookup"><span data-stu-id="7a8c7-182">Exporting conversations</span></span>

<span data-ttu-id="7a8c7-183">Dans un ensemble de révision de conversation, vous pouvez définir les options suivantes pour exporter des conversations :</span><span class="sxs-lookup"><span data-stu-id="7a8c7-183">In a conversation review set, you can set the following options to export conversations:</span></span>

![Exporter](media/export.png)

<span data-ttu-id="7a8c7-185">a.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-185">a.</span></span> <span data-ttu-id="7a8c7-186">Options de métadonnées</span><span class="sxs-lookup"><span data-stu-id="7a8c7-186">Metadata options</span></span>

   - <span data-ttu-id="7a8c7-187">**Charger un fichier :** Les métadonnées sont incluses pour chaque message, courrier électronique et document.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-187">**Load file:** Metadata is included for each individual message, email, and document.</span></span> <span data-ttu-id="7a8c7-188">Il y a une ligne pour chaque message dans une conversation.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-188">There is one row for each message in a conversation.</span></span> 

   - <span data-ttu-id="7a8c7-189">**Balises :** Les balises de votre processus de révision sont incluses dans le fichier de métadonnées.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-189">**Tags:** Tags from your review process are included in the metadata file.</span></span> <span data-ttu-id="7a8c7-190">Les messages d’une conversation partagent les mêmes balises.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-190">Messages in a conversation share the same tags.</span></span> 

<span data-ttu-id="7a8c7-191">b.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-191">b.</span></span> <span data-ttu-id="7a8c7-192">Options de conversation</span><span class="sxs-lookup"><span data-stu-id="7a8c7-192">Conversation options</span></span>
  
   - <span data-ttu-id="7a8c7-193">**Fichiers de conversation :** Lorsque vous exportez des fichiers de conversation, l’affichage annoté est converti en fichier PDF et téléchargé dans le dossier d’exportation.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-193">**Conversation files:** When you export conversation files, the annotated view is converted to a PDF file and downloaded to the export folder.</span></span> <span data-ttu-id="7a8c7-194">Les messages d’un fichier de conversation pointent vers la version PDF du même fichier de conversation.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-194">Messages in one conversation file point to the PDF version of the same conversation file.</span></span>  
  
   - <span data-ttu-id="7a8c7-195">**Messages de conversation individuels :** Lorsque vous exportez des messages individuels, chaque message unique de la conversation est exporté en tant qu’élément autonome.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-195">**Individual chat messages:** When you export individual messages, each unique message in the conversation is exported as a standalone item.</span></span> <span data-ttu-id="7a8c7-196">Le fichier est exporté dans le même format que celui dans lequel il a été enregistré dans la boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-196">The file is exported in the same format that it was saved as in the mailbox.</span></span> <span data-ttu-id="7a8c7-197">Pour une conversation spécifique, vous recevez plusieurs fichiers. msg.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-197">For a specific conversation, you receive multiple .msg files.</span></span> 

     >[!NOTE]
     > <span data-ttu-id="7a8c7-198">Si vous avez appliqué des annotations au fichier de conversation, ces annotations ne seront pas transférées vers les messages individuels.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-198">If you applied annotations to the conversation file, these annotations won't be transferred to the individual messages.</span></span> 

<span data-ttu-id="7a8c7-199">c.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-199">c.</span></span> <span data-ttu-id="7a8c7-200">Autres options</span><span class="sxs-lookup"><span data-stu-id="7a8c7-200">Other options</span></span>

   - <span data-ttu-id="7a8c7-201">**Générer des fichiers texte pour tout le contenu exporté :** Génère un fichier texte pour chaque conversation exportée à partir de l’ensemble de révision.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-201">**Generate text files for all exported content:** Generates a text file for each conversation exported from the review set.</span></span> 

   - <span data-ttu-id="7a8c7-202">**Remplacer le contenu exporté par des fichiers PDF biffés :** Si des fichiers de conversation biffée sont générés pendant le processus de révision, ces fichiers sont disponibles pendant l’exportation.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-202">**Replace exported content with redacted PDFs:** If redacted conversation files are generated during the review process, then these files are available during export.</span></span> <span data-ttu-id="7a8c7-203">Vous pouvez décider s’il faut exporter uniquement les fichiers natifs (sans sélectionner cette option) ou remplacer les fichiers natifs par les versions biffées des fichiers natifs (en sélectionnant cette option), qui sont exportées en tant que fichiers PDF.</span><span class="sxs-lookup"><span data-stu-id="7a8c7-203">You can decided whether to export only the native files (by not selecting this option) or to replace the native files with the redacted versions of the native files (by selecting this option), which are exported as PDF files.</span></span>

## <a name="more-information"></a><span data-ttu-id="7a8c7-204">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="7a8c7-204">More information</span></span>

<span data-ttu-id="7a8c7-205">Pour en savoir plus sur l’examen des données de cas dans Advanced eDiscovery, consultez les articles suivants :</span><span class="sxs-lookup"><span data-stu-id="7a8c7-205">To learn more about how to review case data in Advanced eDiscovery, see the following articles:</span></span>

- [<span data-ttu-id="7a8c7-206">Afficher les données d’un incident</span><span class="sxs-lookup"><span data-stu-id="7a8c7-206">View case data</span></span>](view-documents-in-review-set.md) 

- [<span data-ttu-id="7a8c7-207">Analyser les données de cas</span><span class="sxs-lookup"><span data-stu-id="7a8c7-207">Analyze case data</span></span>](analyzing-data-in-review-set.md)

- [<span data-ttu-id="7a8c7-208">Exporter les données de cas</span><span class="sxs-lookup"><span data-stu-id="7a8c7-208">Export case data</span></span>](exporting-data-ediscover20.md)
