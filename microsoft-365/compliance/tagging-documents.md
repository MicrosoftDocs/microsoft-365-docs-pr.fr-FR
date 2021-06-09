---
title: Étiqueter les documents d’un jeu à réviser
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: how-to
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: Le marquage de documents dans un jeu à réviser permet de supprimer le contenu inutile et d’identifier le contenu pertinent dans Advanced eDiscovery cas.
ms.custom: seo-marvel-mar2020
ms.openlocfilehash: 6d6a933f24a034aced99a8eaa70c6ee951765ca0
ms.sourcegitcommit: cc9e3cac6af23f20d7cc5ac6fc6f6e01bc3cc5c5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2021
ms.locfileid: "52736248"
---
# <a name="tag-documents-in-a-review-set-in-advanced-ediscovery"></a><span data-ttu-id="d6baf-103">Baliser des documents dans un jeu à réviser dans Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="d6baf-103">Tag documents in a review set in Advanced eDiscovery</span></span>

<span data-ttu-id="d6baf-104">L’organisation du contenu dans un ensemble de révision est importante pour effectuer différents flux de travail dans le processus eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="d6baf-104">Organizing content in a review set is important to complete various workflows in the eDiscovery process.</span></span> <span data-ttu-id="d6baf-105">Cela inclut les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="d6baf-105">This includes:</span></span>

- <span data-ttu-id="d6baf-106">Élimination de contenu inutile</span><span class="sxs-lookup"><span data-stu-id="d6baf-106">Culling unnecessary content</span></span>

- <span data-ttu-id="d6baf-107">Identification du contenu pertinent</span><span class="sxs-lookup"><span data-stu-id="d6baf-107">Identifying relevant content</span></span>

- <span data-ttu-id="d6baf-108">Identification du contenu qui doit être examiné par un expert ou un avocat</span><span class="sxs-lookup"><span data-stu-id="d6baf-108">Identifying content that must be reviewed by an expert or attorney</span></span>

<span data-ttu-id="d6baf-109">Lorsque des experts, des avocats ou d’autres utilisateurs examinent le contenu d’un groupe de révision, leurs opinions relatives au contenu peuvent être capturées à l’aide de balises.</span><span class="sxs-lookup"><span data-stu-id="d6baf-109">When experts, attorneys, or other users review content in a review set, their opinions related to the content can be captured by using tags.</span></span> <span data-ttu-id="d6baf-110">Par exemple, si l’objectif est d’annuler le contenu inutile, un utilisateur peut baliser des documents avec une balise telle que « non réactif ».</span><span class="sxs-lookup"><span data-stu-id="d6baf-110">For example, if the intent is to cull unnecessary content, a user can tag documents with a tag such as "non-responsive".</span></span> <span data-ttu-id="d6baf-111">Une fois que le contenu a été révisé et balisé, une recherche de jeu à réviser peut être créée pour exclure tout contenu marqué comme « non réactif ».</span><span class="sxs-lookup"><span data-stu-id="d6baf-111">After content has been reviewed and tagged, a review set search can be created to exclude any content tagged as "non-responsive".</span></span> <span data-ttu-id="d6baf-112">Ce processus élimine le contenu non réactif des étapes suivantes du flux de travail eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="d6baf-112">This process eliminates the non-responsive content from the next steps in the eDiscovery workflow.</span></span> <span data-ttu-id="d6baf-113">Le panneau de marquage d’un jeu à réviser peut être personnalisé pour chaque cas afin que les balises de prise en charge du flux de travail de révision prévu pour le cas.</span><span class="sxs-lookup"><span data-stu-id="d6baf-113">The tagging panel in a review set can be customized for every case so that the tags support the intended review workflow for the case.</span></span>

> [!NOTE]
> <span data-ttu-id="d6baf-114">L’étendue des balises est Advanced eDiscovery cas.</span><span class="sxs-lookup"><span data-stu-id="d6baf-114">The scope of tags is an Advanced eDiscovery case.</span></span> <span data-ttu-id="d6baf-115">Cela signifie qu’un cas ne peut avoir qu’un seul ensemble de balises que les réviseurs peuvent utiliser pour baliser des documents de jeu de révision.</span><span class="sxs-lookup"><span data-stu-id="d6baf-115">That means a case can only have one set of tags that reviewers can use to tag review set documents.</span></span> <span data-ttu-id="d6baf-116">Vous ne pouvez pas configurer un ensemble différent de balises pour une utilisation dans différents ensembles de révision dans le même cas.</span><span class="sxs-lookup"><span data-stu-id="d6baf-116">You can't set up a different set of tags for use in different review sets in the same case.</span></span>

## <a name="tag-types"></a><span data-ttu-id="d6baf-117">Types de balises</span><span class="sxs-lookup"><span data-stu-id="d6baf-117">Tag types</span></span>

<span data-ttu-id="d6baf-118">Advanced eDiscovery fournit deux types de balises :</span><span class="sxs-lookup"><span data-stu-id="d6baf-118">Advanced eDiscovery provides two types of tags:</span></span>

- <span data-ttu-id="d6baf-119">**Balises à choix unique**: limite les relecteurs à la sélection d’une seule balise au sein d’un groupe.</span><span class="sxs-lookup"><span data-stu-id="d6baf-119">**Single choice tags**: Restricts reviewers to selecting a single tag within a group.</span></span> <span data-ttu-id="d6baf-120">Ces types de balises peuvent être utiles pour s’assurer que les réviseurs ne sélectionnent pas les balises conflictuelles telles que « réactive » et « non réactive ».</span><span class="sxs-lookup"><span data-stu-id="d6baf-120">These types of tags can be useful to ensure that reviewers don't select conflicting tags such as "responsive" and "non-responsive".</span></span> <span data-ttu-id="d6baf-121">Les balises à choix unique s’affichent sous la mesure des boutons d’option.</span><span class="sxs-lookup"><span data-stu-id="d6baf-121">Single choice tags appear as radio buttons.</span></span>

- <span data-ttu-id="d6baf-122">**Balises de choix multiples**: autoriser les avis à sélectionner plusieurs balises au sein d’un groupe.</span><span class="sxs-lookup"><span data-stu-id="d6baf-122">**Multiple choice tags**: Allow reviews to select multiple tags within a group.</span></span> <span data-ttu-id="d6baf-123">Ces types de balises apparaissent sous forme de case à cocher.</span><span class="sxs-lookup"><span data-stu-id="d6baf-123">These types of tags appear as checkboxes.</span></span>

## <a name="tag-structure"></a><span data-ttu-id="d6baf-124">Structure des balises</span><span class="sxs-lookup"><span data-stu-id="d6baf-124">Tag structure</span></span>

<span data-ttu-id="d6baf-125">Outre les types de balises, la structure de l’organisation des balises dans le panneau de balises peut être utilisée pour rendre les documents de marquage plus intuitifs.</span><span class="sxs-lookup"><span data-stu-id="d6baf-125">In addition to the tag types, the structure of how tags are organized in the tag panel can be used to make tagging documents more intuitive.</span></span> <span data-ttu-id="d6baf-126">Les balises sont regroupées par sections.</span><span class="sxs-lookup"><span data-stu-id="d6baf-126">Tags are grouped by sections.</span></span> <span data-ttu-id="d6baf-127">La recherche de jeu à réviser prend en charge la possibilité de rechercher par balise et par section de balise.</span><span class="sxs-lookup"><span data-stu-id="d6baf-127">Review set search supports the ability to search by tag and by tag section.</span></span> <span data-ttu-id="d6baf-128">Cela signifie que vous pouvez créer une recherche de jeu à réviser pour récupérer les documents marqués avec n’importe quelle balise dans une section.</span><span class="sxs-lookup"><span data-stu-id="d6baf-128">This means you can create a review set search to retrieve documents tagged with any tag in a section.</span></span>

![Sections de balise dans le panneau de balise](../media/TagTypes.png)

<span data-ttu-id="d6baf-130">Vous pouvez organiser davantage les balises en les imbriquer dans une section.</span><span class="sxs-lookup"><span data-stu-id="d6baf-130">You can further organize tags by nesting them within a section.</span></span> <span data-ttu-id="d6baf-131">Par exemple, si l’objectif est d’identifier et de baliser le contenu privilégié, l’imbrmbrage peut être utilisé pour indiquer clairement qu’un réviseur peut marquer un document comme « privilégié » et sélectionner le type de privilège en vérifiant la balise imbrmbrée appropriée.</span><span class="sxs-lookup"><span data-stu-id="d6baf-131">For example, if the intent is to identify and tag privileged content, nesting can be used to make it clear that a reviewer can tag a document as "Privileged" and select the type of privilege by checking the appropriate nested tag.</span></span>

![Balises imbriées dans une section de balise](../media/NestingTags.png)

## <a name="create-tags"></a><span data-ttu-id="d6baf-133">Créer des balises</span><span class="sxs-lookup"><span data-stu-id="d6baf-133">Create tags</span></span>

<span data-ttu-id="d6baf-134">Avant d’appliquer des balises aux documents du jeu à réviser, vous devez créer une structure de balises.</span><span class="sxs-lookup"><span data-stu-id="d6baf-134">Before applying tags to documents in the review set, you need to create a tag structure.</span></span>

1. <span data-ttu-id="d6baf-135">Ouvrez un jeu à réviser, accédez à la barre de commandes et sélectionnez **Baliser par requête.**</span><span class="sxs-lookup"><span data-stu-id="d6baf-135">Open a review set and navigate to the command bar and select **Tag by query**.</span></span>

2. <span data-ttu-id="d6baf-136">Dans le panneau de marquage, sélectionnez **Gérer les options de balise**</span><span class="sxs-lookup"><span data-stu-id="d6baf-136">In the tagging panel, select **Manage tag options**</span></span>

3. <span data-ttu-id="d6baf-137">Sélectionnez **Ajouter une section de balise.**</span><span class="sxs-lookup"><span data-stu-id="d6baf-137">Select **Add tag section**.</span></span>

4. <span data-ttu-id="d6baf-138">Tapez un titre de groupe de balises et une description facultative, puis cliquez sur **Enregistrer.**</span><span class="sxs-lookup"><span data-stu-id="d6baf-138">Type a tag group title and an optional description, and then click **Save**.</span></span>

5. <span data-ttu-id="d6baf-139">Sélectionnez le menu déroulant à trois points en regard du titre du groupe de balises, puis cliquez sur Ajouter une case à **cocher** ou sur **la case d’option Ajouter.**</span><span class="sxs-lookup"><span data-stu-id="d6baf-139">Select the triple dot dropdown menu next to the tag group title and click **Add check box** or **Add option button**.</span></span>

6. <span data-ttu-id="d6baf-140">Tapez un nom et une description pour la case à cocher ou la case d’option.</span><span class="sxs-lookup"><span data-stu-id="d6baf-140">Type a name and description for the checkbox or option button.</span></span>

7. <span data-ttu-id="d6baf-141">Répétez ce processus pour créer des sections de balise, des options de balise et des case à cocher.</span><span class="sxs-lookup"><span data-stu-id="d6baf-141">Repeat this process to create new tag sections, tag options, and checkboxes.</span></span>

   ![Configurer la structure des balises](../media/ManageTagOptions3.png)

## <a name="applying-tags"></a><span data-ttu-id="d6baf-143">Application de balises</span><span class="sxs-lookup"><span data-stu-id="d6baf-143">Applying tags</span></span>

<span data-ttu-id="d6baf-144">Une fois la structure de balises en place, les réviseurs peuvent appliquer des balises aux documents d’un jeu à réviser.</span><span class="sxs-lookup"><span data-stu-id="d6baf-144">With the tag structure in place, reviewers can apply tags to documents in a review set.</span></span> <span data-ttu-id="d6baf-145">Il existe deux façons d’appliquer des balises :</span><span class="sxs-lookup"><span data-stu-id="d6baf-145">There are two different ways to apply tags:</span></span>

- <span data-ttu-id="d6baf-146">Fichiers de balise</span><span class="sxs-lookup"><span data-stu-id="d6baf-146">Tag files</span></span>

- <span data-ttu-id="d6baf-147">Baliser par requête</span><span class="sxs-lookup"><span data-stu-id="d6baf-147">Tag by query</span></span>

### <a name="tag-files"></a><span data-ttu-id="d6baf-148">Fichiers de balise</span><span class="sxs-lookup"><span data-stu-id="d6baf-148">Tag files</span></span>

<span data-ttu-id="d6baf-149">Que vous sélectionniez un ou plusieurs éléments dans un jeu à  réviser, vous pouvez appliquer des balises à leur sélection en cliquant sur Les fichiers de balises dans la barre de commandes.</span><span class="sxs-lookup"><span data-stu-id="d6baf-149">Whether you select a single item or several items in a review set, you can apply tags to their selection by clicking **Tag files** in the command bar.</span></span> <span data-ttu-id="d6baf-150">Dans le panneau de marquage, vous pouvez sélectionner une balise et elle est automatiquement appliquée aux documents sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="d6baf-150">In the tagging panel, you can select a tag and it is automatically applied to the selected documents.</span></span>

![Baliser les fichiers sélectionnés](../media/TagFile2.png)

> [!NOTE]
> <span data-ttu-id="d6baf-152">Les balises sont appliquées uniquement aux éléments sélectionnés dans la liste des éléments.</span><span class="sxs-lookup"><span data-stu-id="d6baf-152">Tags will be applied only to selected items in the list of items.</span></span>

### <a name="tag-by-query"></a><span data-ttu-id="d6baf-153">Baliser par requête</span><span class="sxs-lookup"><span data-stu-id="d6baf-153">Tag by query</span></span>

<span data-ttu-id="d6baf-154">Le marquage par requête vous permet d’appliquer des balises à tous les éléments affichés par une requête de filtre actuellement appliquée dans le jeu à réviser.</span><span class="sxs-lookup"><span data-stu-id="d6baf-154">Tagging by query lets you apply tags to all items displayed by a filter query that's currently applied in the review set.</span></span>

1. <span data-ttu-id="d6baf-155">Désélectionne tous les éléments du jeu à réviser et allez dans la barre de commandes et sélectionnez **Baliser par requête.**</span><span class="sxs-lookup"><span data-stu-id="d6baf-155">Unselect all items in the review set and go to the command bar and select **Tag by query**.</span></span>

2. <span data-ttu-id="d6baf-156">Dans le panneau de marquage, sélectionnez la balise à appliquer.</span><span class="sxs-lookup"><span data-stu-id="d6baf-156">In the tagging panel, select the tag that you want to apply.</span></span>

3. <span data-ttu-id="d6baf-157">Sous la dropdown **de sélection** de balise, trois options déterminent les éléments à appliquer à la balise.</span><span class="sxs-lookup"><span data-stu-id="d6baf-157">Under the **Tag selection** dropdown, there are three options that dictate which items to apply the tag to.</span></span>

   - <span data-ttu-id="d6baf-158">**Éléments qui correspondent à la requête appliquée :** applique des balises à des éléments spécifiques qui correspondent aux conditions de requête de filtre.</span><span class="sxs-lookup"><span data-stu-id="d6baf-158">**Items that match applied query**: Applies tags to specific items that match the filter query conditions.</span></span>

   - <span data-ttu-id="d6baf-159">**Inclure les éléments de famille associés**: applique des balises à des éléments spécifiques qui correspondent aux conditions de requête de filtre et à leurs éléments de famille associés.</span><span class="sxs-lookup"><span data-stu-id="d6baf-159">**Include associated family items**: Applies tags to specific items that match the filter query conditions and their associated family items.</span></span> <span data-ttu-id="d6baf-160">*Les éléments de famille* sont des éléments qui partagent la même valeur de métadonnées FamilyId.</span><span class="sxs-lookup"><span data-stu-id="d6baf-160">*Family items* are items that share the same FamilyId metadata value.</span></span>  

   - <span data-ttu-id="d6baf-161">**Inclure les éléments de conversation associés**: applique des balises aux éléments qui correspondent aux conditions de requête de filtre et à leurs éléments de conversation associés.</span><span class="sxs-lookup"><span data-stu-id="d6baf-161">**Include associated conversation items**: Applies tags to items that match the filter query conditions and their associated conversation items.</span></span> <span data-ttu-id="d6baf-162">*Les éléments de conversation* sont des éléments qui partagent les mêmes valeurs de métadonnées ConversationId.</span><span class="sxs-lookup"><span data-stu-id="d6baf-162">*Conversation items* are items that share the same ConversationId metadata values.</span></span>

   ![Sélection de balise](../media/TagByQuery2.png)

4. <span data-ttu-id="d6baf-164">Cliquez **sur Démarrer le travail de marquage** pour déclencher le travail de marquage.</span><span class="sxs-lookup"><span data-stu-id="d6baf-164">Click **Start tagging job** to trigger the tagging job.</span></span>

## <a name="tag-filter"></a><span data-ttu-id="d6baf-165">Filtre de balise</span><span class="sxs-lookup"><span data-stu-id="d6baf-165">Tag filter</span></span>

<span data-ttu-id="d6baf-166">Utilisez le filtre de balise dans le jeu à réviser pour rechercher ou exclure rapidement des éléments des résultats de la requête en fonction de la façon dont un élément est balisé.</span><span class="sxs-lookup"><span data-stu-id="d6baf-166">Use the tag filter in review set to quickly find or exclude items from the query results based on how an item is tagged.</span></span> 

1. <span data-ttu-id="d6baf-167">Sélectionnez **Filtres** pour développer le panneau de filtrage.</span><span class="sxs-lookup"><span data-stu-id="d6baf-167">Select **Filters** to expand the filter panel.</span></span>

2. <span data-ttu-id="d6baf-168">Sélectionnez et développez **les propriétés de l’élément.**</span><span class="sxs-lookup"><span data-stu-id="d6baf-168">Select and expand **Item properties**.</span></span>

3. <span data-ttu-id="d6baf-169">Faites défiler vers le bas pour trouver le filtre **nommé Balise,** cochez la case, puis cliquez sur **Terminé**.</span><span class="sxs-lookup"><span data-stu-id="d6baf-169">Scroll down to find the filter named **Tag**, select the checkbox, and then click **Done**.</span></span>

4. <span data-ttu-id="d6baf-170">Pour inclure ou exclure des éléments avec une balise spécifique d’une requête, faites l’une des choses suivantes :</span><span class="sxs-lookup"><span data-stu-id="d6baf-170">To include or exclude items with a specific tag from a query, do one of the following:</span></span>

   - <span data-ttu-id="d6baf-171">**Inclure des éléments**: sélectionnez la valeur de la balise et sélectionnez Égal **à l’un** des éléments dans le menu déroulant.</span><span class="sxs-lookup"><span data-stu-id="d6baf-171">**Include items**: Select the tag value and select **Equal any of** in the dropdown menu.</span></span>

      <span data-ttu-id="d6baf-172">Ou</span><span class="sxs-lookup"><span data-stu-id="d6baf-172">Or</span></span>

   - <span data-ttu-id="d6baf-173">**Exclure des** éléments : sélectionnez la valeur de la balise et **sélectionnez** Égal à aucun des éléments du menu déroulant.</span><span class="sxs-lookup"><span data-stu-id="d6baf-173">**Exclude items**: Select the tag value and select **Equals none of** in dropdown menu.</span></span>

     ![Filtre de balise exclure des éléments](../media/TagFilterExclude.png)

> [!NOTE]
> <span data-ttu-id="d6baf-175">Veillez à actualiser la page pour vous assurer que le filtre de balises affiche les dernières modifications apportées à la structure des balises.</span><span class="sxs-lookup"><span data-stu-id="d6baf-175">Be sure to refresh the page to ensure that the tag filter displays the latest changes to the tag structure.</span></span>
