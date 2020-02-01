---
title: Configuration des balises actives dans Advanced eDiscovery
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
description: Les balises actives vous permettent d’appliquer les fonctionnalités d’apprentissage automatique lors de la révision du contenu dans un cas avancé de découverte électronique. Utilisez des groupes de balises actives pour afficher les résultats des modèles de détection d’apprentissage automatique, tels que le modèle de privilège avocat-client.
ms.openlocfilehash: 9b3e1310baa06f53a3ee1dab5c371fb67d6ab95c
ms.sourcegitcommit: 1c91b7b24537d0e54d484c3379043db53c1aea65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2020
ms.locfileid: "41597401"
---
# <a name="set-up-smart-tags-in-advanced-ediscovery"></a><span data-ttu-id="5d354-104">Configuration des balises actives dans Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="5d354-104">Set up smart tags in Advanced eDiscovery</span></span>

<span data-ttu-id="5d354-105">Les fonctionnalités machine learning (ML) dans Advanced eDiscovery peuvent vous aider à améliorer l’efficacité du processus de décision lors de la révision de documents de cas dans un jeu de révision.</span><span class="sxs-lookup"><span data-stu-id="5d354-105">Machine learning (ML) capabilities in Advanced eDiscovery can help you make the decision process more efficient when reviewing case documents in a review set.</span></span> <span data-ttu-id="5d354-106">Les balises actives permettent de mettre en place les capacités de ML des décisions enregistrées : lors du marquage des documents lors de la révision.</span><span class="sxs-lookup"><span data-stu-id="5d354-106">Smart tags are a way to bring the ML capabilities to where the decisions are recorded: when tagging documents during review.</span></span> <span data-ttu-id="5d354-107">Lorsque vous créez un groupe de balises actives, les décisions qui sont le résultat du modèle ML que vous avez associé au groupe de balises actives s’affichent en ligne avec les balises dans le groupe de balises.</span><span class="sxs-lookup"><span data-stu-id="5d354-107">When you create a smart tag group, then the decisions that are the result of the ML model that you've associated with the smart tag group are displayed in-line with the tags in the tag group.</span></span> <span data-ttu-id="5d354-108">Cela permet d’afficher les informations de résultats ML en ligne lorsque vous examinez des documents spécifiques.</span><span class="sxs-lookup"><span data-stu-id="5d354-108">This helps see the ML results information in-line when you're reviewing specific documents.</span></span>

## <a name="how-to-set-up-a-smart-tag-group"></a><span data-ttu-id="5d354-109">Procédure de configuration d’un groupe de balises actives</span><span class="sxs-lookup"><span data-stu-id="5d354-109">How to set up a smart tag group</span></span>

1. <span data-ttu-id="5d354-110">Dans un jeu de révision, cliquez sur **gérer le jeu de révision** , puis sur gérer les **balises**.</span><span class="sxs-lookup"><span data-stu-id="5d354-110">In a review set, click **Manage review set** and then click **Manage tags**.</span></span>

2. <span data-ttu-id="5d354-111">Cliquez sur **Ajouter un groupe de balises** , puis sélectionnez **Ajouter un groupe de balises actives**.</span><span class="sxs-lookup"><span data-stu-id="5d354-111">Click **Add tag group** and then select **Add smart tag group**.</span></span>

3. <span data-ttu-id="5d354-112">Sélectionnez le modèle ML que vous souhaitez associer au groupe de balises.</span><span class="sxs-lookup"><span data-stu-id="5d354-112">Select the ML model that you want to associate to the tag group.</span></span>
    
   <span data-ttu-id="5d354-113">Cette méthode crée un groupe de balises et *n* balises enfants, où *n* représente le nombre de sorties possibles du modèle.</span><span class="sxs-lookup"><span data-stu-id="5d354-113">This creates a tag group and *N* child tags, where *N* is the number of possible outputs of the model.</span></span> <span data-ttu-id="5d354-114">Par exemple, le [modèle de détection des privilèges du client avocat](attorney-privilege-detection.md) a deux sorties possibles :</span><span class="sxs-lookup"><span data-stu-id="5d354-114">For example, the [attorney-client privilege detection model](attorney-privilege-detection.md) has two possible outputs:</span></span> 

   - <span data-ttu-id="5d354-115">**Positif** : permet de baliser des documents qui contiennent du contenu privilégié par le client.</span><span class="sxs-lookup"><span data-stu-id="5d354-115">**Positive** – Use to tag documents that contain attorney-client privileged content.</span></span>
   
   - <span data-ttu-id="5d354-116">**Négatif** : permet de marquer des documents qui ne contiennent pas de contenu privilégié par le client.</span><span class="sxs-lookup"><span data-stu-id="5d354-116">**Negative** – Use to tag documents that don't contain attorney-client privileged content.</span></span>
    
    <span data-ttu-id="5d354-117">Si vous sélectionnez ce modèle, un groupe de balises avec deux balises enfant est créé (une balise enfant nommée **positive** et l’autre appelée **négatif**) pour l’ensemble de révision.</span><span class="sxs-lookup"><span data-stu-id="5d354-117">If you select this model, a tag group with two child tags is created (one child tag named **Positive** and the other named **Negative**) for the review set.</span></span> <span data-ttu-id="5d354-118">Dans cet exemple, chaque balise enfant correspond à l’une des sorties possibles du modèle de détection des privilèges du client avocat.</span><span class="sxs-lookup"><span data-stu-id="5d354-118">In this example, each child tag corresponds to one of the possible outputs from the attorney-client privilege detection model.</span></span>

4. <span data-ttu-id="5d354-119">Vous pouvez également renommer le groupe de balises et les balises enfants.</span><span class="sxs-lookup"><span data-stu-id="5d354-119">Optionally, you can rename the tag group and the child tags.</span></span> <span data-ttu-id="5d354-120">Par exemple, vous pouvez renommer la balise **positive** en **Privilege** et la balise **négative** pour **ne pas**obtenir de privilèges.</span><span class="sxs-lookup"><span data-stu-id="5d354-120">For example, you could rename the **Positive** tag to **Privileged** and the **Negative** tag to **Not privileged**.</span></span>

## <a name="how-to-use-smart-tags"></a><span data-ttu-id="5d354-121">Utilisation des balises actives</span><span class="sxs-lookup"><span data-stu-id="5d354-121">How to use smart tags</span></span>

<span data-ttu-id="5d354-122">Lors de l’examen d’un document, les résultats du modèle sont affichés en regard de la balise enfant appropriée.</span><span class="sxs-lookup"><span data-stu-id="5d354-122">When reviewing a document, the model's results are displayed next to the appropriate child tag.</span></span> <span data-ttu-id="5d354-123">Par exemple, si vous disposez d’un groupe de balises actives pour la détection des privilèges du client et que vous révisez un document potentiellement privilégié, la raison de cette conclusion s’affiche en regard de la balise appropriée.</span><span class="sxs-lookup"><span data-stu-id="5d354-123">For example, if you have a smart tag group for attorney-client privilege detection and you review a document that is potentially privileged, the reason for that conclusion is displayed next to the appropriate tag.</span></span> <span data-ttu-id="5d354-124">Il est important de noter que la balise n’est pas automatiquement appliquée au document.</span><span class="sxs-lookup"><span data-stu-id="5d354-124">It's important to note that the tag isn't automatically applied to the document.</span></span> <span data-ttu-id="5d354-125">Le relecteur prend la décision de baliser le document.</span><span class="sxs-lookup"><span data-stu-id="5d354-125">The reviewer makes the decision about how to tag the document.</span></span>