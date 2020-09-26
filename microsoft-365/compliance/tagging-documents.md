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
description: Le marquage des documents dans un jeu de révision permet de supprimer le contenu inutile et d’identifier le contenu pertinent dans un cas avancé de découverte électronique.
ms.custom: seo-marvel-mar2020
ms.openlocfilehash: 83e7a3c9c097968c4d773e6e2092bb3c50154cc3
ms.sourcegitcommit: 2160e7cf373f992dd4d11793a59cb8c44f8d587e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/26/2020
ms.locfileid: "48285280"
---
# <a name="tag-documents-in-a-review-set-in-advanced-ediscovery"></a><span data-ttu-id="09bab-103">Baliser des documents dans un ensemble de révision dans Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="09bab-103">Tag documents in a review set in Advanced eDiscovery</span></span>

<span data-ttu-id="09bab-104">L’organisation du contenu dans un jeu de révision est importante pour effectuer plusieurs flux de travail dans le processus de découverte électronique.</span><span class="sxs-lookup"><span data-stu-id="09bab-104">Organizing content in a review set is important to complete various workflows in the eDiscovery process.</span></span> <span data-ttu-id="09bab-105">Cela inclut les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="09bab-105">This includes:</span></span>

- <span data-ttu-id="09bab-106">Élimination de contenu inutile</span><span class="sxs-lookup"><span data-stu-id="09bab-106">Culling unnecessary content</span></span>

- <span data-ttu-id="09bab-107">Identification du contenu pertinent</span><span class="sxs-lookup"><span data-stu-id="09bab-107">Identifying relevant content</span></span>
 
- <span data-ttu-id="09bab-108">Identification du contenu qui doit être révisé par un expert ou un avocat</span><span class="sxs-lookup"><span data-stu-id="09bab-108">Identifying content that must be reviewed by an expert or an attorney</span></span>

<span data-ttu-id="09bab-109">Lorsque des experts, des avocats ou d’autres utilisateurs consultent le contenu d’un ensemble de révision, leurs opinions liées au contenu peuvent être capturées à l’aide de balises.</span><span class="sxs-lookup"><span data-stu-id="09bab-109">When experts, attorneys, or other users review content in a review set, their opinions related to the content can be captured by using tags.</span></span> <span data-ttu-id="09bab-110">Par exemple, si l’intention est d’effectuer une élimination de contenu inutile, un utilisateur peut marquer des documents avec une balise telle que « non réactif ».</span><span class="sxs-lookup"><span data-stu-id="09bab-110">For example, if the intent is to cull unnecessary content, a user can tag documents with a tag such as "non-responsive".</span></span> <span data-ttu-id="09bab-111">Une fois que le contenu a été révisé et balisé, une recherche de jeu de réexamen peut être créée pour exclure le contenu marqué comme « non réactif », ce qui élimine ce contenu des étapes suivantes dans le flux de travail de découverte électronique.</span><span class="sxs-lookup"><span data-stu-id="09bab-111">After content has been reviewed and tagged, a review set search can be created to exclude any content tagged as "non-responsive", which eliminates this content from the next steps in the eDiscovery workflow.</span></span> <span data-ttu-id="09bab-112">Le panneau des balises peut être personnalisé pour chaque cas afin que les balises puissent prendre en charge le flux de travail de révision prévu.</span><span class="sxs-lookup"><span data-stu-id="09bab-112">The tag panel can be customized for every case so that the tags can support the intended review workflow.</span></span>

## <a name="tag-types"></a><span data-ttu-id="09bab-113">Types de balises</span><span class="sxs-lookup"><span data-stu-id="09bab-113">Tag types</span></span>

<span data-ttu-id="09bab-114">Advanced eDiscovery propose deux types de balises :</span><span class="sxs-lookup"><span data-stu-id="09bab-114">Advanced eDiscovery provides two types of tags:</span></span>

- <span data-ttu-id="09bab-115">**Balises à choix unique** : limite les utilisateurs à la sélection d’une balise unique au sein d’un groupe.</span><span class="sxs-lookup"><span data-stu-id="09bab-115">**Single choice tags** - Restricts users to select a single tag within a group.</span></span> <span data-ttu-id="09bab-116">Cela peut être utile pour s’assurer que les utilisateurs ne sélectionnent pas les balises conflictuelles telles que « réactif » et « ne répond pas ».</span><span class="sxs-lookup"><span data-stu-id="09bab-116">This can be useful to ensure users don't select conflicting tags such as "responsive" and "non-responsive".</span></span> <span data-ttu-id="09bab-117">Celles-ci s’affichent sous forme de cases d’option.</span><span class="sxs-lookup"><span data-stu-id="09bab-117">These will appear as radio buttons.</span></span>

- <span data-ttu-id="09bab-118">**Balises Choice multiples** : permet aux utilisateurs de sélectionner plusieurs balises au sein d’un groupe.</span><span class="sxs-lookup"><span data-stu-id="09bab-118">**Multiple choice tags** - Allow users to select multiple tags within a group.</span></span> <span data-ttu-id="09bab-119">Celles-ci s’affichent sous forme de cases à cocher.</span><span class="sxs-lookup"><span data-stu-id="09bab-119">These will appear as checkboxes.</span></span>

## <a name="tag-structure"></a><span data-ttu-id="09bab-120">Structure des balises</span><span class="sxs-lookup"><span data-stu-id="09bab-120">Tag structure</span></span>

<span data-ttu-id="09bab-121">En plus des types de balises, la structure de la manière dont les balises sont organisées dans le panneau des balises peut être utilisée pour faciliter l’utilisation de documents de marquage.</span><span class="sxs-lookup"><span data-stu-id="09bab-121">In addition to the tag types, the structure of how tags are organized in the tag panel can be used to make tagging documents more intuitive.</span></span> <span data-ttu-id="09bab-122">Les balises sont regroupées par sections.</span><span class="sxs-lookup"><span data-stu-id="09bab-122">Tags are grouped by sections.</span></span> <span data-ttu-id="09bab-123">Review Set search prend en charge la fonctionnalité de recherche par balise et par section tag.</span><span class="sxs-lookup"><span data-stu-id="09bab-123">Review set search supports the ability to search by tag and by tag section.</span></span> <span data-ttu-id="09bab-124">Cela signifie que vous pouvez créer une recherche de jeu de réexamen pour récupérer des documents marqués avec une balise dans une section.</span><span class="sxs-lookup"><span data-stu-id="09bab-124">This means you can create a review set search to retrieve documents tagged with any tag in a section.</span></span>

![Sections de balise dans le panneau des balises](../media/Tagtypes.png)

<span data-ttu-id="09bab-126">Les balises peuvent être organisées de manière plus approfondie en les imbriquant dans une section.</span><span class="sxs-lookup"><span data-stu-id="09bab-126">Tags can be further organized by nesting them within a section.</span></span> <span data-ttu-id="09bab-127">Par exemple, si l’intention est d’identifier et de baliser un contenu privilégié, l’imbrication peut être utilisée pour indiquer clairement qu’un utilisateur peut marquer un document comme « privilégié » et sélectionner le type de privilège en vérifiant la balise imbriquée appropriée.</span><span class="sxs-lookup"><span data-stu-id="09bab-127">For example, if the intent is to identify and tag privileged content, nesting can be used to make it clear that a user can tag a document as "Privileged" and select the type of privilege by checking the appropriate nested tag.</span></span>

![Balises imbriquées dans une section de balise](../media/Nestingtags.png)

## <a name="applying-tags"></a><span data-ttu-id="09bab-129">Application de balises</span><span class="sxs-lookup"><span data-stu-id="09bab-129">Applying tags</span></span>

<span data-ttu-id="09bab-130">Il existe plusieurs façons d’appliquer une balise au contenu.</span><span class="sxs-lookup"><span data-stu-id="09bab-130">There are several ways to apply a tag to content.</span></span>

### <a name="tagging-a-single-document"></a><span data-ttu-id="09bab-131">Marquage d’un document unique</span><span class="sxs-lookup"><span data-stu-id="09bab-131">Tagging a single document</span></span>

<span data-ttu-id="09bab-132">Lors de l’affichage d’un document dans un jeu de vérification, vous pouvez afficher les balises qu’une révision peut utiliser en cliquant sur **panneau de marquage**.</span><span class="sxs-lookup"><span data-stu-id="09bab-132">When viewing a document in a review set, you can display the tags that a review can use by clicking **Tagging panel**.</span></span>

![Cliquez sur panneau des balises pour afficher le panneau Balises.](../media/Singledoctag.png)

<span data-ttu-id="09bab-134">Cela vous permet d’appliquer des balises au document affiché dans la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="09bab-134">This will enable you to apply tags to the document displayed in the viewer.</span></span>

### <a name="bulk-tagging"></a><span data-ttu-id="09bab-135">Balisage en bloc</span><span class="sxs-lookup"><span data-stu-id="09bab-135">Bulk tagging</span></span>

<span data-ttu-id="09bab-136">L’étiquetage en bloc peut être réalisé en sélectionnant plusieurs fichiers dans la grille de résultats, puis en utilisant les balises dans le **panneau balisage** de la même manière que pour le marquage des documents uniques.</span><span class="sxs-lookup"><span data-stu-id="09bab-136">Bulk tagging can be done by selecting multiple files in the results grid and then using the tags in the **Tagging panel** similar to tagging single documents.</span></span> <span data-ttu-id="09bab-137">L’annulation de balisage en bloc peut être réalisée en sélectionnant deux fois les balises ; le premier clic applique la balise, et la deuxième sélection garantit que la balise est effacée pour tous les fichiers sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="09bab-137">Bulk un-tagging can be done by selecting tags twice; the first click will apply the tag, and the second selection will ensure that tag is cleared for all selected files.</span></span>

![Capture d’écran d’une description de téléphone de cellule générée automatiquement](../media/Bulktag.png)

> [!NOTE]
> <span data-ttu-id="09bab-139">Lors de l’étiquetage en bloc, le panneau balisage affiche un nombre de fichiers balisés pour chaque balise dans le panneau.</span><span class="sxs-lookup"><span data-stu-id="09bab-139">When bulk tagging, the tagging panel will display a count of files that are tagged for each tag in the panel.</span></span>

### <a name="tagging-in-other-review-panels"></a><span data-ttu-id="09bab-140">Balisage dans d’autres panneaux de révision</span><span class="sxs-lookup"><span data-stu-id="09bab-140">Tagging in other review panels</span></span>

<span data-ttu-id="09bab-141">Lors de l’examen des documents, vous pouvez utiliser les autres panneaux de révision pour examiner les autres caractéristiques des documents dans la grille de résultats.</span><span class="sxs-lookup"><span data-stu-id="09bab-141">When reviewing documents, you can use the other review panels to review other characteristics of documents in the results grid.</span></span> <span data-ttu-id="09bab-142">Cela inclut l’examen d’autres documents connexes, des threads de messagerie, des doublons de doublons et des doublons de hachage.</span><span class="sxs-lookup"><span data-stu-id="09bab-142">This includes reviewing other related documents, email threads, near duplicates, and hash duplicates.</span></span> <span data-ttu-id="09bab-143">Par exemple, lorsque vous consultez des documents connexes (à l’aide du panneau de vérification de la **famille de documents** ), vous pouvez réduire considérablement le temps d’examen en bloc des documents associés.</span><span class="sxs-lookup"><span data-stu-id="09bab-143">For example, when you're reviewing related documents (by using the **Document family** review panel), you can significantly reduce review time by bulk tagging related documents.</span></span> <span data-ttu-id="09bab-144">Par exemple, si un message électronique comporte plusieurs pièces jointes et que vous souhaitez vous assurer que toute la famille est marquée de manière cohérente.</span><span class="sxs-lookup"><span data-stu-id="09bab-144">For example, if an email message has several attachments and you want to ensure that the entire family is tagged consistently.</span></span>

<span data-ttu-id="09bab-145">Par exemple, voici comment afficher le panneau de **marquage** lors de l’utilisation du panneau de vérification de la **famille de documents** :</span><span class="sxs-lookup"><span data-stu-id="09bab-145">For example, here's how to display the **Tagging panel** when using the **Document family** review panel:</span></span>

1. <span data-ttu-id="09bab-146">Lorsque le panneau vérifier est ouvert pour un document sélectionné (par exemple, affichage de la liste du contenu associé dans le panneau de vérification de la **famille de documents** , cliquez sur **documents de balise** sous le panneau examen de la famille de documents.</span><span class="sxs-lookup"><span data-stu-id="09bab-146">With the review panel open for a selected document (for example, displaying the list of related content in the **Document family** review panel, click **Tag documents** under the document family review panel.</span></span>

   <span data-ttu-id="09bab-147">Le panneau de marquage est affiché sous la forme d’une fenêtre contextuelle.</span><span class="sxs-lookup"><span data-stu-id="09bab-147">The tagging panel is displayed as a pop-up window.</span></span>

2. <span data-ttu-id="09bab-148">Choisissez une ou plusieurs balises à appliquer au document sélectionné.</span><span class="sxs-lookup"><span data-stu-id="09bab-148">Choose one or more tags to apply the selected document.</span></span> 

3. <span data-ttu-id="09bab-149">Pour baliser tous les documents, sélectionnez tous les documents dans le panneau de la **famille** de documents, cliquez sur **documents de balises**, puis sélectionnez les balises à appliquer à l’ensemble de la famille de documents.</span><span class="sxs-lookup"><span data-stu-id="09bab-149">To tag all documents, select all documents in the **Document family** panel, click **Tag documents**, and then choose the tags to apply to the entire family of documents.</span></span>

![Capture d’écran d’une description de publication de réseau social générée automatiquement](../media/Relatedtag.png)
