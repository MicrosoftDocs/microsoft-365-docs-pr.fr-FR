---
title: Configurer des balises intelligentes dans Advanced eDiscovery
f1.keywords:
- NOCSH
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
ROBOTS: NOINDEX, NOFOLLOW
description: Les balises intelligentes vous permet d’appliquer les fonctionnalités d’apprentissage automatique lors de la révision de contenu dans un cas Advanced eDiscovery. Utilisez des groupes de balises intelligentes pour afficher les résultats des modèles de détection d’apprentissage automatique, tels que le modèle de privilège client-avocat.
ms.openlocfilehash: 3d3852a13410a3aa57932e19031cc5d00ce52a96
ms.sourcegitcommit: 3dd9944a6070a7f35c4bc2b57df397f844c3fe79
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2020
ms.locfileid: "42081081"
---
# <a name="set-up-smart-tags-in-advanced-ediscovery"></a><span data-ttu-id="a93e4-104">Configurer des balises intelligentes dans Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="a93e4-104">Set up smart tags in Advanced eDiscovery</span></span>

<span data-ttu-id="a93e4-105">Les fonctionnalités d’apprentissage automatique (ML) dans Advanced eDiscovery peuvent vous aider à améliorer l’efficacité du processus de décision lors de la révision de documents de cas dans un groupe de révision.</span><span class="sxs-lookup"><span data-stu-id="a93e4-105">Machine learning (ML) capabilities in Advanced eDiscovery can help you make the decision process more efficient when reviewing case documents in a review set.</span></span> <span data-ttu-id="a93e4-106">Les balises intelligentes sont un moyen d’amener les fonctionnalités ML à l’endroit où les décisions sont enregistrées : lors du marquage des documents pendant la révision.</span><span class="sxs-lookup"><span data-stu-id="a93e4-106">Smart tags are a way to bring the ML capabilities to where the decisions are recorded: when tagging documents during review.</span></span> <span data-ttu-id="a93e4-107">Lorsque vous créez un groupe de balises intelligentes, les décisions qui résultent du modèle ML que vous avez associé au groupe de balises intelligentes sont affichées en ligne avec les balises du groupe de balises.</span><span class="sxs-lookup"><span data-stu-id="a93e4-107">When you create a smart tag group, then the decisions that are the result of the ML model that you've associated with the smart tag group are displayed in-line with the tags in the tag group.</span></span> <span data-ttu-id="a93e4-108">Cela vous permet de consulter les résultats ML en ligne lorsque vous examinez des documents spécifiques.</span><span class="sxs-lookup"><span data-stu-id="a93e4-108">This helps see the ML results information in-line when you're reviewing specific documents.</span></span>

## <a name="how-to-set-up-a-smart-tag-group"></a><span data-ttu-id="a93e4-109">Comment configurer un groupe de balises intelligentes</span><span class="sxs-lookup"><span data-stu-id="a93e4-109">How to set up a smart tag group</span></span>

1. <span data-ttu-id="a93e4-110">Dans un jeu à réviser, cliquez sur **Gérer le jeu à réviser,** puis sur Gérer les **balises.**</span><span class="sxs-lookup"><span data-stu-id="a93e4-110">In a review set, click **Manage review set** and then click **Manage tags**.</span></span>

2. <span data-ttu-id="a93e4-111">Cliquez **sur Ajouter un groupe de balises,** puis **sélectionnez Ajouter un groupe de balises intelligentes.**</span><span class="sxs-lookup"><span data-stu-id="a93e4-111">Click **Add tag group** and then select **Add smart tag group**.</span></span>

3. <span data-ttu-id="a93e4-112">Sélectionnez le modèle ML que vous souhaitez associer au groupe de balises.</span><span class="sxs-lookup"><span data-stu-id="a93e4-112">Select the ML model that you want to associate to the tag group.</span></span>
    
   <span data-ttu-id="a93e4-113">Cela crée un groupe de balises et des balises *enfants N,* où *N* est le nombre de sorties possibles du modèle.</span><span class="sxs-lookup"><span data-stu-id="a93e4-113">This creates a tag group and *N* child tags, where *N* is the number of possible outputs of the model.</span></span> <span data-ttu-id="a93e4-114">Par exemple, le modèle [de détection des privilèges client-avocat](attorney-privilege-detection.md) a deux sorties possibles :</span><span class="sxs-lookup"><span data-stu-id="a93e4-114">For example, the [attorney-client privilege detection model](attorney-privilege-detection.md) has two possible outputs:</span></span> 

   - <span data-ttu-id="a93e4-115">**Positif** : utilisez cette balise pour baliser les documents qui contiennent du contenu privilégié client-avocat.</span><span class="sxs-lookup"><span data-stu-id="a93e4-115">**Positive** – Use to tag documents that contain attorney-client privileged content.</span></span>
   
   - <span data-ttu-id="a93e4-116">**Négatif** : utilisez cette balise pour baliser des documents qui ne contiennent pas de contenu privilégié client-avocat.</span><span class="sxs-lookup"><span data-stu-id="a93e4-116">**Negative** – Use to tag documents that don't contain attorney-client privileged content.</span></span>
    
    <span data-ttu-id="a93e4-117">Si vous sélectionnez ce modèle, un groupe de balises avec deux balises enfants est créé (une balise enfant nommée **Positive** et l’autre nommée **Negative**) pour le jeu à réviser.</span><span class="sxs-lookup"><span data-stu-id="a93e4-117">If you select this model, a tag group with two child tags is created (one child tag named **Positive** and the other named **Negative**) for the review set.</span></span> <span data-ttu-id="a93e4-118">Dans cet exemple, chaque balise enfant correspond à l’une des sorties possibles du modèle de détection des privilèges client-avocat.</span><span class="sxs-lookup"><span data-stu-id="a93e4-118">In this example, each child tag corresponds to one of the possible outputs from the attorney-client privilege detection model.</span></span>

4. <span data-ttu-id="a93e4-119">Si vous le souhaitez, vous pouvez renommer le groupe de balises et les balises enfants.</span><span class="sxs-lookup"><span data-stu-id="a93e4-119">Optionally, you can rename the tag group and the child tags.</span></span> <span data-ttu-id="a93e4-120">Par exemple, vous pouvez renommer la balise **Positive** en **Privileged** et la balise **Negative** sur **Not privileged**.</span><span class="sxs-lookup"><span data-stu-id="a93e4-120">For example, you could rename the **Positive** tag to **Privileged** and the **Negative** tag to **Not privileged**.</span></span>

## <a name="how-to-use-smart-tags"></a><span data-ttu-id="a93e4-121">Comment utiliser des balises intelligentes</span><span class="sxs-lookup"><span data-stu-id="a93e4-121">How to use smart tags</span></span>

<span data-ttu-id="a93e4-122">Lors de la révision d’un document, les résultats du modèle s’affichent à côté de la balise enfant appropriée.</span><span class="sxs-lookup"><span data-stu-id="a93e4-122">When reviewing a document, the model's results are displayed next to the appropriate child tag.</span></span> <span data-ttu-id="a93e4-123">Par exemple, si vous avez un groupe de balises intelligentes pour la détection des privilèges client-avocat et que vous examinez un document potentiellement privilégié, la raison de cette conclusion s’affiche à côté de la balise appropriée.</span><span class="sxs-lookup"><span data-stu-id="a93e4-123">For example, if you have a smart tag group for attorney-client privilege detection and you review a document that is potentially privileged, the reason for that conclusion is displayed next to the appropriate tag.</span></span> <span data-ttu-id="a93e4-124">Il est important de noter que la balise n’est pas appliquée automatiquement au document.</span><span class="sxs-lookup"><span data-stu-id="a93e4-124">It's important to note that the tag isn't automatically applied to the document.</span></span> <span data-ttu-id="a93e4-125">Le réviseur prend la décision de baliser le document.</span><span class="sxs-lookup"><span data-stu-id="a93e4-125">The reviewer makes the decision about how to tag the document.</span></span>
