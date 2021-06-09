---
title: Retrait du module de pertinence dans Advanced eDiscovery
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ROBOTS: NOINDEX, NOFOLLOW
ms.collection: M365-security-compliance
description: Le module de pertinence Advanced eDiscovery sera retiré le 10 mars 2021. Cet article explique ce qu’il faut faire avant que la pertinence ne soit retirée. Plus précisément, terminez les modèles non terminés en exécutant le calcul Par lot afin de pouvoir conserver les métadonnées du modèle.
ms.openlocfilehash: 0719c2cb1b6b0d867ffc045fe02d57e1e2f32a61
ms.sourcegitcommit: 50908a93554290ff1157b58d0a868a33e012513c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "52821996"
---
# <a name="retirement-of-the-relevance-module-in-advanced-ediscovery"></a><span data-ttu-id="b0b7a-105">Retrait du module Pertinence dans Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="b0b7a-105">Retirement of the Relevance module in Advanced eDiscovery</span></span>

<span data-ttu-id="b0b7a-106">Le 10 mars 2021, nous allons retirer le module Pertinence dans Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="b0b7a-106">On March 10, 2021, we are retiring the Relevance module in Advanced eDiscovery.</span></span> <span data-ttu-id="b0b7a-107">Ce retrait signifie que les organisations n’auront plus accès au module Pertinence (en accédant à Gérer le jeu à réviser Pertinence dans un cas Advanced eDiscovery) ou ne pourront plus accéder aux modèles  >   Pertinence existants.</span><span class="sxs-lookup"><span data-stu-id="b0b7a-107">This retirement means that organizations will no longer have access to the Relevance module (by going to **Manage review set** > **Relevance** in an Advanced eDiscovery case) or be able to access any existing Relevance models.</span></span> <span data-ttu-id="b0b7a-108">Le module de pertinence actuel qui est retiré sera remplacé par une nouvelle solution de codage prédictif au T2 CY 2021.</span><span class="sxs-lookup"><span data-stu-id="b0b7a-108">The current Relevance module that is being retired will be replaced with a new predictive coding solution in Q2 CY 2021.</span></span> <span data-ttu-id="b0b7a-109">Cette nouvelle fonctionnalité permettra aux organisations de créer leurs propres modèles de codage prédictifs dans un flux de travail plus simple et plus intuitif.</span><span class="sxs-lookup"><span data-stu-id="b0b7a-109">This new functionality will let organizations build their own predictive coding models in an easier and more intuitive workflow.</span></span>

<span data-ttu-id="b0b7a-110">Pour préparer ce retrait à venir, nous recommandons aux organisations qui utilisent le module Pertinence d’exporter la sortie de leur modèle avant la date de retrait en exécutant un calcul Par lot pour tous les modèles existants.</span><span class="sxs-lookup"><span data-stu-id="b0b7a-110">To prepare for this upcoming retirement, we recommend that organizations who use the Relevance module export their model’s output before the retirement date by running a Batch calculation for all existing models.</span></span> <span data-ttu-id="b0b7a-111">Tous les scores de pertinence de votre modèle sont stockés définitivement dans le jeu à réviser correspondant et accessibles lorsque des documents sont exportés.</span><span class="sxs-lookup"><span data-stu-id="b0b7a-111">All Relevance scores from your model will be permanently stored in the corresponding review set and accessible when documents are exported.</span></span> <span data-ttu-id="b0b7a-112">Les scores de pertinence sont également conservés en tant que métadonnées dans le fichier de chargement.</span><span class="sxs-lookup"><span data-stu-id="b0b7a-112">Relevance scores are also retained as metadata in the load file.</span></span> <span data-ttu-id="b0b7a-113">En outre, vous pourrez toujours filtrer le contenu du jeu à réviser en fonction du score de pertinence et avoir accès à toutes les métadonnées produites par vos modèles de pertinence.</span><span class="sxs-lookup"><span data-stu-id="b0b7a-113">Also, you will still be able to filter content in the review set based on relevance score and have access to all metadata produced by your Relevance models.</span></span>

## <a name="complete-unfinished-models"></a><span data-ttu-id="b0b7a-114">Modèles inachevés complets</span><span class="sxs-lookup"><span data-stu-id="b0b7a-114">Complete unfinished models</span></span>

<span data-ttu-id="b0b7a-115">Pour les modèles de pertinence non terminés, veuillez effectuer une évaluation, une formation et un calcul par lot afin de pouvoir appliquer le modèle aux documents d’un jeu à réviser.</span><span class="sxs-lookup"><span data-stu-id="b0b7a-115">For any unfinished Relevance models, please complete assessment, training, and Batch calculation so that you can apply the model to the documents in a review set.</span></span> <span data-ttu-id="b0b7a-116">L’exécution du calcul batch permet de conserver les informations après la date de retrait du module de pertinence.</span><span class="sxs-lookup"><span data-stu-id="b0b7a-116">Completing the Batch calculation will preserve the information after the retirement date of the Relevance module.</span></span>

<span data-ttu-id="b0b7a-117">Voici les étapes à suivre pour effectuer les modèles non terminés :</span><span class="sxs-lookup"><span data-stu-id="b0b7a-117">Here are the steps to complete any unfinished models:</span></span>

1. <span data-ttu-id="b0b7a-118">Formez votre modèle jusqu’à ce qu’il soit stabilisé et prêt pour le calcul par lots.</span><span class="sxs-lookup"><span data-stu-id="b0b7a-118">Train your model until it is stabilized and ready for Batch calculation.</span></span> <span data-ttu-id="b0b7a-119">Voir [Formation au marquage et à la pertinence.](tagging-and-relevance-training-in-advanced-ediscovery.md)</span><span class="sxs-lookup"><span data-stu-id="b0b7a-119">See [Tagging and Relevance training](tagging-and-relevance-training-in-advanced-ediscovery.md).</span></span>

   <span data-ttu-id="b0b7a-120">La capture d’écran suivante montre un module prêt pour un calcul par lot.</span><span class="sxs-lookup"><span data-stu-id="b0b7a-120">The following screenshot shows a module that is ready for a Batch calculation.</span></span> <span data-ttu-id="b0b7a-121">Notez que l’évaluation et la formation sont terminées et que l’étape suivante consiste à exécuter le calcul par lots.</span><span class="sxs-lookup"><span data-stu-id="b0b7a-121">Notice that the Assessment and Training is complete, and the next step is to run Batch calculation.</span></span>

   ![Capture d’écran du modèle prêt pour le calcul par lots](../media/ReadyForBatchCalculation.png)

2. <span data-ttu-id="b0b7a-123">Exécutez le calcul par lots.</span><span class="sxs-lookup"><span data-stu-id="b0b7a-123">Run the Batch calculation.</span></span> <span data-ttu-id="b0b7a-124">Voir [Effectuer le calcul par lots.](track-relevance-analysis-in-advanced-ediscovery.md#performing-batch-calculation)</span><span class="sxs-lookup"><span data-stu-id="b0b7a-124">See [Performing Batch calculation](track-relevance-analysis-in-advanced-ediscovery.md#performing-batch-calculation).</span></span>

3. <span data-ttu-id="b0b7a-125">Vérifiez que le calcul par lots a réussi.</span><span class="sxs-lookup"><span data-stu-id="b0b7a-125">Verify that Batch calculation was successful.</span></span> <span data-ttu-id="b0b7a-126">Voir [les résultats de calcul par lot.](track-relevance-analysis-in-advanced-ediscovery.md#batch-calculation-results)</span><span class="sxs-lookup"><span data-stu-id="b0b7a-126">See [Batch calculation results](track-relevance-analysis-in-advanced-ediscovery.md#batch-calculation-results).</span></span>

<span data-ttu-id="b0b7a-127">Pour obtenir de l’aide sur la réalisation de modèles de pertinence non terminés, contactez le Support Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b0b7a-127">For help with completing unfinished Relevance models, contact Microsoft Support.</span></span>
