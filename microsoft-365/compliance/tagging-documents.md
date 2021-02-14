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
description: Le marquage de documents dans un jeu à réviser permet de supprimer du contenu inutile et d’identifier le contenu pertinent dans un cas Advanced eDiscovery.
ms.custom: seo-marvel-mar2020
ms.openlocfilehash: 83e7a3c9c097968c4d773e6e2092bb3c50154cc3
ms.sourcegitcommit: 2160e7cf373f992dd4d11793a59cb8c44f8d587e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/26/2020
ms.locfileid: "48285280"
---
# <a name="tag-documents-in-a-review-set-in-advanced-ediscovery"></a><span data-ttu-id="fb419-103">Baliser des documents dans un jeu à réviser dans Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="fb419-103">Tag documents in a review set in Advanced eDiscovery</span></span>

<span data-ttu-id="fb419-104">L’organisation du contenu dans un ensemble de révision est importante pour effectuer différents flux de travail dans le processus eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="fb419-104">Organizing content in a review set is important to complete various workflows in the eDiscovery process.</span></span> <span data-ttu-id="fb419-105">Cela inclut les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="fb419-105">This includes:</span></span>

- <span data-ttu-id="fb419-106">Élimination de contenu inutile</span><span class="sxs-lookup"><span data-stu-id="fb419-106">Culling unnecessary content</span></span>

- <span data-ttu-id="fb419-107">Identification du contenu pertinent</span><span class="sxs-lookup"><span data-stu-id="fb419-107">Identifying relevant content</span></span>
 
- <span data-ttu-id="fb419-108">Identification du contenu qui doit être examiné par un expert ou un avocat</span><span class="sxs-lookup"><span data-stu-id="fb419-108">Identifying content that must be reviewed by an expert or an attorney</span></span>

<span data-ttu-id="fb419-109">Lorsque des experts, des avocats ou d’autres utilisateurs examinent le contenu d’un groupe de révision, leurs opinions relatives au contenu peuvent être capturées à l’aide de balises.</span><span class="sxs-lookup"><span data-stu-id="fb419-109">When experts, attorneys, or other users review content in a review set, their opinions related to the content can be captured by using tags.</span></span> <span data-ttu-id="fb419-110">Par exemple, si l’objectif est d’annuler le contenu inutile, un utilisateur peut baliser des documents avec une balise telle que « non réactif ».</span><span class="sxs-lookup"><span data-stu-id="fb419-110">For example, if the intent is to cull unnecessary content, a user can tag documents with a tag such as "non-responsive".</span></span> <span data-ttu-id="fb419-111">Une fois que le contenu a été révisé et balisé, une recherche de jeu à réviser peut être créée pour exclure tout contenu marqué comme « non réactif », ce qui élimine ce contenu des étapes suivantes du flux de travail eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="fb419-111">After content has been reviewed and tagged, a review set search can be created to exclude any content tagged as "non-responsive", which eliminates this content from the next steps in the eDiscovery workflow.</span></span> <span data-ttu-id="fb419-112">Le panneau de balises peut être personnalisé pour chaque cas afin que les balises peuvent prendre en charge le flux de travail de révision prévu.</span><span class="sxs-lookup"><span data-stu-id="fb419-112">The tag panel can be customized for every case so that the tags can support the intended review workflow.</span></span>

## <a name="tag-types"></a><span data-ttu-id="fb419-113">Types de balises</span><span class="sxs-lookup"><span data-stu-id="fb419-113">Tag types</span></span>

<span data-ttu-id="fb419-114">Advanced eDiscovery fournit deux types de balises :</span><span class="sxs-lookup"><span data-stu-id="fb419-114">Advanced eDiscovery provides two types of tags:</span></span>

- <span data-ttu-id="fb419-115">**Balises à choix unique** : limite la sélection d’une seule balise au sein d’un groupe.</span><span class="sxs-lookup"><span data-stu-id="fb419-115">**Single choice tags** - Restricts users to select a single tag within a group.</span></span> <span data-ttu-id="fb419-116">Cela peut être utile pour s’assurer que les utilisateurs ne sélectionnent pas de balises conflictuelles telles que « réactive » et « non réactive ».</span><span class="sxs-lookup"><span data-stu-id="fb419-116">This can be useful to ensure users don't select conflicting tags such as "responsive" and "non-responsive".</span></span> <span data-ttu-id="fb419-117">Celles-ci s’affichent sous la mesure des boutons d’radio.</span><span class="sxs-lookup"><span data-stu-id="fb419-117">These will appear as radio buttons.</span></span>

- <span data-ttu-id="fb419-118">**Balises de choix multiples** : autoriser les utilisateurs à sélectionner plusieurs balises au sein d’un groupe.</span><span class="sxs-lookup"><span data-stu-id="fb419-118">**Multiple choice tags** - Allow users to select multiple tags within a group.</span></span> <span data-ttu-id="fb419-119">Celles-ci s’affichent sous la mesure des case à cocher.</span><span class="sxs-lookup"><span data-stu-id="fb419-119">These will appear as checkboxes.</span></span>

## <a name="tag-structure"></a><span data-ttu-id="fb419-120">Structure des balises</span><span class="sxs-lookup"><span data-stu-id="fb419-120">Tag structure</span></span>

<span data-ttu-id="fb419-121">Outre les types de balises, la structure de l’organisation des balises dans le panneau de balises peut être utilisée pour rendre les documents de marquage plus intuitifs.</span><span class="sxs-lookup"><span data-stu-id="fb419-121">In addition to the tag types, the structure of how tags are organized in the tag panel can be used to make tagging documents more intuitive.</span></span> <span data-ttu-id="fb419-122">Les balises sont regroupées par sections.</span><span class="sxs-lookup"><span data-stu-id="fb419-122">Tags are grouped by sections.</span></span> <span data-ttu-id="fb419-123">La recherche de jeu à réviser prend en charge la possibilité de rechercher par balise et par section de balise.</span><span class="sxs-lookup"><span data-stu-id="fb419-123">Review set search supports the ability to search by tag and by tag section.</span></span> <span data-ttu-id="fb419-124">Cela signifie que vous pouvez créer une recherche de jeu à réviser pour récupérer les documents marqués avec n’importe quelle balise dans une section.</span><span class="sxs-lookup"><span data-stu-id="fb419-124">This means you can create a review set search to retrieve documents tagged with any tag in a section.</span></span>

![Sections de balise dans le panneau de balise](../media/Tagtypes.png)

<span data-ttu-id="fb419-126">Les balises peuvent être davantage organisées en les imbriquent dans une section.</span><span class="sxs-lookup"><span data-stu-id="fb419-126">Tags can be further organized by nesting them within a section.</span></span> <span data-ttu-id="fb419-127">Par exemple, si l’objectif est d’identifier et de baliser le contenu privilégié, l’imbrmbrage peut être utilisé pour indiquer clairement qu’un utilisateur peut marquer un document comme « privilégié » et sélectionner le type de privilège en vérifiant la balise imbrmbrée appropriée.</span><span class="sxs-lookup"><span data-stu-id="fb419-127">For example, if the intent is to identify and tag privileged content, nesting can be used to make it clear that a user can tag a document as "Privileged" and select the type of privilege by checking the appropriate nested tag.</span></span>

![Balises imbriées dans une section de balise](../media/Nestingtags.png)

## <a name="applying-tags"></a><span data-ttu-id="fb419-129">Application de balises</span><span class="sxs-lookup"><span data-stu-id="fb419-129">Applying tags</span></span>

<span data-ttu-id="fb419-130">Il existe plusieurs façons d’appliquer une balise au contenu.</span><span class="sxs-lookup"><span data-stu-id="fb419-130">There are several ways to apply a tag to content.</span></span>

### <a name="tagging-a-single-document"></a><span data-ttu-id="fb419-131">Marquage d’un document unique</span><span class="sxs-lookup"><span data-stu-id="fb419-131">Tagging a single document</span></span>

<span data-ttu-id="fb419-132">Lorsque vous affichez un document dans un jeu à réviser, vous pouvez afficher les balises qu’un avis peut utiliser en cliquant sur **le panneau de marquage.**</span><span class="sxs-lookup"><span data-stu-id="fb419-132">When viewing a document in a review set, you can display the tags that a review can use by clicking **Tagging panel**.</span></span>

![Cliquez sur Le panneau Balise pour afficher le panneau de balises](../media/Singledoctag.png)

<span data-ttu-id="fb419-134">Cela vous permet d’appliquer des balises au document affiché dans la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="fb419-134">This will enable you to apply tags to the document displayed in the viewer.</span></span>

### <a name="bulk-tagging"></a><span data-ttu-id="fb419-135">Marquage en bloc</span><span class="sxs-lookup"><span data-stu-id="fb419-135">Bulk tagging</span></span>

<span data-ttu-id="fb419-136">Le marquage en bloc peut être effectué en sélectionnant plusieurs fichiers  dans la grille des résultats, puis en utilisant les balises du panneau de marquage similaires au marquage de documents simples.</span><span class="sxs-lookup"><span data-stu-id="fb419-136">Bulk tagging can be done by selecting multiple files in the results grid and then using the tags in the **Tagging panel** similar to tagging single documents.</span></span> <span data-ttu-id="fb419-137">L’un-marquage en bloc peut être effectué en sélectionnant deux fois des balises . Le premier clic applique la balise, et la deuxième sélection garantit que la balise est effacée pour tous les fichiers sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="fb419-137">Bulk un-tagging can be done by selecting tags twice; the first click will apply the tag, and the second selection will ensure that tag is cleared for all selected files.</span></span>

![Capture d’écran d’une description de téléphone portable générée automatiquement](../media/Bulktag.png)

> [!NOTE]
> <span data-ttu-id="fb419-139">Lors du marquage en bloc, le panneau de marquage affiche le nombre de fichiers marqués pour chaque balise du panneau.</span><span class="sxs-lookup"><span data-stu-id="fb419-139">When bulk tagging, the tagging panel will display a count of files that are tagged for each tag in the panel.</span></span>

### <a name="tagging-in-other-review-panels"></a><span data-ttu-id="fb419-140">Marquage dans d’autres panneaux d’avis</span><span class="sxs-lookup"><span data-stu-id="fb419-140">Tagging in other review panels</span></span>

<span data-ttu-id="fb419-141">Lorsque vous examinez des documents, vous pouvez utiliser les autres panneaux de révision pour examiner d’autres caractéristiques des documents dans la grille des résultats.</span><span class="sxs-lookup"><span data-stu-id="fb419-141">When reviewing documents, you can use the other review panels to review other characteristics of documents in the results grid.</span></span> <span data-ttu-id="fb419-142">Cela inclut la révision d’autres documents connexes, threads de messagerie, quasi-doublons et hachages.</span><span class="sxs-lookup"><span data-stu-id="fb419-142">This includes reviewing other related documents, email threads, near duplicates, and hash duplicates.</span></span> <span data-ttu-id="fb419-143">Par exemple, lorsque vous examinez des documents  connexes (à l’aide du Panneau de révision de la famille de documents), vous pouvez réduire considérablement le temps de révision en balisé en bloc les documents associés.</span><span class="sxs-lookup"><span data-stu-id="fb419-143">For example, when you're reviewing related documents (by using the **Document family** review panel), you can significantly reduce review time by bulk tagging related documents.</span></span> <span data-ttu-id="fb419-144">Par exemple, si un message électronique a plusieurs pièces jointes et que vous souhaitez vous assurer que toute la famille est marquée de façon cohérente.</span><span class="sxs-lookup"><span data-stu-id="fb419-144">For example, if an email message has several attachments and you want to ensure that the entire family is tagged consistently.</span></span>

<span data-ttu-id="fb419-145">Par exemple, voici comment afficher  le panneau marquage lors de l’utilisation du panneau de révision de la famille **de** documents :</span><span class="sxs-lookup"><span data-stu-id="fb419-145">For example, here's how to display the **Tagging panel** when using the **Document family** review panel:</span></span>

1. <span data-ttu-id="fb419-146">Avec le panneau de révision ouvert pour un document sélectionné (par  exemple, affichage de la liste du contenu connexe dans le panneau révision de la famille de documents), cliquez sur **Baliser** les documents sous le panneau de révision de la famille de documents.</span><span class="sxs-lookup"><span data-stu-id="fb419-146">With the review panel open for a selected document (for example, displaying the list of related content in the **Document family** review panel, click **Tag documents** under the document family review panel.</span></span>

   <span data-ttu-id="fb419-147">Le panneau de marquage s’affiche en tant que fenêtre indépendant.</span><span class="sxs-lookup"><span data-stu-id="fb419-147">The tagging panel is displayed as a pop-up window.</span></span>

2. <span data-ttu-id="fb419-148">Choisissez une ou plusieurs balises pour appliquer le document sélectionné.</span><span class="sxs-lookup"><span data-stu-id="fb419-148">Choose one or more tags to apply the selected document.</span></span> 

3. <span data-ttu-id="fb419-149">Pour baliser tous les documents, sélectionnez tous les documents dans le panneau Famille de documents, cliquez sur Baliser les **documents,** puis choisissez les balises à appliquer à toute la famille de documents. </span><span class="sxs-lookup"><span data-stu-id="fb419-149">To tag all documents, select all documents in the **Document family** panel, click **Tag documents**, and then choose the tags to apply to the entire family of documents.</span></span>

![Capture d’écran d’un billet de réseau social Description généré automatiquement](../media/Relatedtag.png)
