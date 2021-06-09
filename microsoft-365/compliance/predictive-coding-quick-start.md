---
title: Codage prédictif dans Advanced eDiscovery - Démarrage rapide
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
ms.reviewer: jefwan
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection: M365-security-compliance
description: Découvrez comment commencer à utiliser le module de codage prédictif dans Advanced eDiscovery. Cet article vous explique le processus de bout en bout d’utilisation du codage prédictif pour identifier le contenu d’un jeu à réviser le plus pertinent pour votre enquête.
ms.openlocfilehash: 16fb92af5048ae6cd953e522b2e5e5d8f5a7256f
ms.sourcegitcommit: 50908a93554290ff1157b58d0a868a33e012513c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "52822562"
---
# <a name="quick-start-predictive-coding-in-advanced-ediscovery-preview"></a><span data-ttu-id="f852e-104">Démarrage rapide : codage prédictif dans Advanced eDiscovery (aperçu)</span><span class="sxs-lookup"><span data-stu-id="f852e-104">Quick start: Predictive coding in Advanced eDiscovery (preview)</span></span>

<span data-ttu-id="f852e-105">Cet article présente un démarrage rapide pour l’utilisation du codage prédictif dans Advanced eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="f852e-105">This article presents a quick start for using predictive coding in Advanced eDiscovery.</span></span> <span data-ttu-id="f852e-106">Le module de codage prédictif dans Advanced eDiscovery utilise les fonctionnalités intelligentes d’apprentissage automatique dans Advanced eDiscovery pour vous aider à réduire la quantité de contenu à réviser.</span><span class="sxs-lookup"><span data-stu-id="f852e-106">The predictive coding module in Advanced eDiscovery uses the intelligent, machine learning capabilities in Advanced eDiscovery to help you reduce the amount of content to review.</span></span> <span data-ttu-id="f852e-107">Le codage prédictif vous permet de réduire et de réduire les volumes importants de contenu de cas à un ensemble pertinent d’éléments que vous pouvez hiérarchiser pour révision.</span><span class="sxs-lookup"><span data-stu-id="f852e-107">Predictive coding helps you reduce and cull large volumes of case content to a relevant set of items that you can prioritize for review.</span></span> <span data-ttu-id="f852e-108">Pour ce faire, vous devez créer et former vos propres modèles de codage prédictifs qui vous aident à hiérarchiser l’examen des éléments les plus pertinents d’un jeu à réviser.</span><span class="sxs-lookup"><span data-stu-id="f852e-108">This is accomplished by creating and training your own predictive coding models that help you prioritize the review of the most relevant items in a review set.</span></span>

<span data-ttu-id="f852e-109">Voici un aperçu rapide du processus de codage prédictif :</span><span class="sxs-lookup"><span data-stu-id="f852e-109">Here's an a quick overview of the predictive coding process:</span></span>

![Processus de démarrage rapide pour le codage de prédiction](..\media\PredictiveCodingQuickStartProcess.png)

<span data-ttu-id="f852e-111">Pour commencer, vous créez un modèle, étiqueter aussi peu que 50 éléments comme pertinents ou non pertinents.</span><span class="sxs-lookup"><span data-stu-id="f852e-111">To get started, you create a model, label as few as 50 items as relevant or not relevant.</span></span> <span data-ttu-id="f852e-112">Le système utilise ensuite cette formation pour appliquer des scores de prédiction à chaque élément du jeu à réviser.</span><span class="sxs-lookup"><span data-stu-id="f852e-112">The system then uses this training to apply prediction scores to every item in the review set.</span></span> <span data-ttu-id="f852e-113">Cela vous permet de filtrer les éléments en fonction du score de prédiction, ce qui vous permet d’examiner d’abord les éléments les plus pertinents (ou non pertinents).</span><span class="sxs-lookup"><span data-stu-id="f852e-113">This lets you filter items based on the prediction score, which  allows you to review the most relevant (or non-relevant) items first.</span></span> <span data-ttu-id="f852e-114">Si vous souhaitez entraîner des modèles avec des taux de rappel et des nombres de rappels plus élevés, vous pouvez continuer à étiqueter des éléments dans les séries de formation suivantes jusqu’à ce que le modèle se stabilise.</span><span class="sxs-lookup"><span data-stu-id="f852e-114">If you want to train models with higher accuracies and recall rates, you can continue labeling items in subsequent training rounds until the model stabilizes.</span></span> <span data-ttu-id="f852e-115">Une fois le modèle stabilisé, vous pouvez appliquer le filtre de prédiction final pour hiérarchiser les éléments à réviser.</span><span class="sxs-lookup"><span data-stu-id="f852e-115">Once the model is stabilized, you can apply the final prediction filter to prioritize items to review.</span></span>

<span data-ttu-id="f852e-116">Pour une vue d’ensemble détaillée du codage prédictif, voir En savoir plus sur le codage prédictif [dans Advanced eDiscovery](predictive-coding-overview.md).</span><span class="sxs-lookup"><span data-stu-id="f852e-116">For a detailed overview of predictive coding, see [Learn about predictive coding in Advanced eDiscovery](predictive-coding-overview.md).</span></span>

## <a name="step-1-create-a-new-predictive-coding-model"></a><span data-ttu-id="f852e-117">Étape 1 : Créer un modèle de codage prédictif</span><span class="sxs-lookup"><span data-stu-id="f852e-117">Step 1: Create a new predictive coding model</span></span>

<span data-ttu-id="f852e-118">La première étape consiste à créer un modèle de codage prédictif dans le jeu à réviser</span><span class="sxs-lookup"><span data-stu-id="f852e-118">The first step is to create a new predictive coding model in the review set</span></span>

1. <span data-ttu-id="f852e-119">Dans le centre Microsoft 365 conformité, ouvrez un Advanced eDiscovery, puis sélectionnez l’onglet Ensembles **de révision.**</span><span class="sxs-lookup"><span data-stu-id="f852e-119">In the Microsoft 365 compliance center, open an Advanced eDiscovery case and then select the **Review sets** tab.</span></span>

2. <span data-ttu-id="f852e-120">Ouvrez un jeu à réviser, puis cliquez sur **Analyse** Gérer le  >  **codage prédictif (prévisualisation).**</span><span class="sxs-lookup"><span data-stu-id="f852e-120">Open a review set and then click **Analytics** > **Manage predictive coding (preview)**.</span></span>

   ![Cliquez sur le menu déroulant Analyser dans le jeu à réviser pour aller à la page Codage prédictif](..\media\ManagePredictiveCoding.png)

3. <span data-ttu-id="f852e-122">Dans la page **Modèles de codage prédictif (prévisualisation),** cliquez **sur Nouveau modèle.**</span><span class="sxs-lookup"><span data-stu-id="f852e-122">On the **Predictive coding models (preview)** page, click **New model**.</span></span>

4. <span data-ttu-id="f852e-123">Dans la page volante, tapez un nom pour le modèle et une description facultative.</span><span class="sxs-lookup"><span data-stu-id="f852e-123">On the flyout page, type a name for the model and an optional description.</span></span>

5. <span data-ttu-id="f852e-124">Cliquez **sur Enregistrer** pour créer le modèle.</span><span class="sxs-lookup"><span data-stu-id="f852e-124">Click **Save** to create the model.</span></span>

   <span data-ttu-id="f852e-125">La préparation de votre modèle prendra quelques minutes.</span><span class="sxs-lookup"><span data-stu-id="f852e-125">It will take a couple minutes for the system to prepare your model.</span></span> <span data-ttu-id="f852e-126">Une fois prêt, vous pouvez effectuer la première série de formations.</span><span class="sxs-lookup"><span data-stu-id="f852e-126">After it's ready, you can perform the first round of training.</span></span>

<span data-ttu-id="f852e-127">Pour obtenir des instructions plus détaillées, voir [Créer un modèle de codage prédictif.](predictive-coding-create-model.md)</span><span class="sxs-lookup"><span data-stu-id="f852e-127">For more detailed instructions, see [Create a predictive coding model](predictive-coding-create-model.md).</span></span>

## <a name="step-2-perform-the-first-training-round"></a><span data-ttu-id="f852e-128">Étape 2 : Effectuer la première série de formations</span><span class="sxs-lookup"><span data-stu-id="f852e-128">Step 2: Perform the first training round</span></span>

<span data-ttu-id="f852e-129">Après avoir créé le modèle, l’étape suivante consiste à effectuer la première série de formations en étiqueter les éléments comme pertinents ou non pertinents.</span><span class="sxs-lookup"><span data-stu-id="f852e-129">After you create the model, the next step is to complete the first training round by labeling items as relevant or not relevant.</span></span>

1. <span data-ttu-id="f852e-130">Ouvrez le jeu à réviser, puis cliquez sur **Analyse** Gérer le  >  **codage prédictif (prévisualisation).**</span><span class="sxs-lookup"><span data-stu-id="f852e-130">Open the review set and then click **Analytics** > **Manage predictive coding (preview)**.</span></span>

2. <span data-ttu-id="f852e-131">Dans la page **Modèles de codage prédictif (prévisualisation),** sélectionnez le modèle que vous souhaitez entraîner.</span><span class="sxs-lookup"><span data-stu-id="f852e-131">On the **Predictive coding models (preview)** page, select the model that you want to train.</span></span>

3. <span data-ttu-id="f852e-132">Sous **l’onglet** Vue d’ensemble, sous **La première** série, cliquez **sur Démarrer la série de formation suivante.**</span><span class="sxs-lookup"><span data-stu-id="f852e-132">On the **Overview** tab, under **Round 1**, click **Start next training round**.</span></span>

   <span data-ttu-id="f852e-133">**L’onglet** Formation s’affiche et contient 50 éléments à étiqueter.</span><span class="sxs-lookup"><span data-stu-id="f852e-133">The **Training** tab is displayed and contains 50 items for you to label.</span></span>

4. <span data-ttu-id="f852e-134">Examinez chaque document, puis  **sélectionnez** le bouton Pertinent ou Non pertinent en bas du volet de lecture pour l’étiqueter.</span><span class="sxs-lookup"><span data-stu-id="f852e-134">Review each document and then select the **Relevant** or **Not relevant** button at the bottom of the reading pane to label it.</span></span>

   ![Étiqueter chaque document comme pertinent ou non pertinent](..\media\TrainModel1.png)

5. <span data-ttu-id="f852e-136">Une fois que vous avez étiqueté les 50 éléments, cliquez sur **Terminer.**</span><span class="sxs-lookup"><span data-stu-id="f852e-136">After you've labeled all 50 items, click **Finish**.</span></span>

    <span data-ttu-id="f852e-137">Il faudra quelques minutes au système pour « apprendre » de votre étiquetage et mettre à jour le modèle.</span><span class="sxs-lookup"><span data-stu-id="f852e-137">It will take a couple minutes for the system to "learn" from your labeling and update the model.</span></span> <span data-ttu-id="f852e-138">Une fois ce processus terminé, l’état **Prêt** s’affiche pour le modèle sur la page Modèles de codage prédictif **(prévisualisation).**</span><span class="sxs-lookup"><span data-stu-id="f852e-138">When this process is complete, a status of **Ready** is displayed for the model on the **Predictive coding models (preview)** page.</span></span>

<span data-ttu-id="f852e-139">Pour obtenir des instructions plus détaillées, voir [La formation d’un modèle de codage prédictif.](predictive-coding-train-model.md)</span><span class="sxs-lookup"><span data-stu-id="f852e-139">For more detailed instructions, see [Train a predictive coding model](predictive-coding-train-model.md).</span></span>

## <a name="step-3-apply-the-prediction-score-filter-to-items-in-review-set"></a><span data-ttu-id="f852e-140">Étape 3 : Appliquer le filtre de score de prédiction aux éléments du jeu à réviser</span><span class="sxs-lookup"><span data-stu-id="f852e-140">Step 3: Apply the prediction score filter to items in review set</span></span>

<span data-ttu-id="f852e-141">Après avoir effectué une série de formation en bail, vous pouvez appliquer le filtre de score de prédiction aux éléments du jeu à réviser.</span><span class="sxs-lookup"><span data-stu-id="f852e-141">After you perform at lease one training round, you can apply the prediction score filter to items in review set.</span></span> <span data-ttu-id="f852e-142">Cela vous permet de passer en revue les éléments que le modèle a prévu comme pertinents ou non pertinents.</span><span class="sxs-lookup"><span data-stu-id="f852e-142">This lets you review the items the model has predicted as relevant or not relevant.</span></span>   

1. <span data-ttu-id="f852e-143">Ouvrez le jeu à réviser.</span><span class="sxs-lookup"><span data-stu-id="f852e-143">Open the review set.</span></span>

   ![Cliquez sur Filtres pour afficher la page de présentation filtres](..\media\PredictionScoreFilter0.png)

   <span data-ttu-id="f852e-145">Les filtres par défaut pré-chargés sont affichés en haut de la page de révision.</span><span class="sxs-lookup"><span data-stu-id="f852e-145">The pre-loaded default filters are displayed at the top of the review set page.</span></span> <span data-ttu-id="f852e-146">Vous pouvez laisser ces ensembles sur **Any**.</span><span class="sxs-lookup"><span data-stu-id="f852e-146">You can leave these set to **Any**.</span></span>

2. <span data-ttu-id="f852e-147">Cliquez **sur Filtres** pour afficher la page de présentation **filtres.**</span><span class="sxs-lookup"><span data-stu-id="f852e-147">Click **Filters** to display the **Filters** flyout page.</span></span>

3. <span data-ttu-id="f852e-148">Développez la section Analyse & codage **prédictif** pour afficher un ensemble de filtres.</span><span class="sxs-lookup"><span data-stu-id="f852e-148">Expand the **Analytics & predictive coding** section to display a set of filters.</span></span>

      ![Filtre de score de prédiction dans la section Analyse & codage prédictif](..\media\PredictionScoreFilter1.png)

   <span data-ttu-id="f852e-150">La convention d’attribution de noms pour les filtres de score de prédiction est **le score de prédiction (nom du modèle).**</span><span class="sxs-lookup"><span data-stu-id="f852e-150">The naming convention for prediction score filters is **Prediction score (model name)**.</span></span> <span data-ttu-id="f852e-151">Par exemple, le nom de filtre du score de prédiction pour un modèle nommé **Modèle A** est Le score de **prédiction (modèle A).**</span><span class="sxs-lookup"><span data-stu-id="f852e-151">For example, the prediction score filter name for a model named **Model A** is **Prediction score (Model A)**.</span></span>

4. <span data-ttu-id="f852e-152">Sélectionnez le filtre de score de prédiction à utiliser, puis cliquez sur **Terminé.**</span><span class="sxs-lookup"><span data-stu-id="f852e-152">Select the prediction score filter that you want to use and then click **Done**.</span></span>

5. <span data-ttu-id="f852e-153">Dans la page de jeu à réviser, cliquez sur ladown pour le filtre de score de prédiction et tapez les valeurs minimales et maximales pour la plage de score de prédiction.</span><span class="sxs-lookup"><span data-stu-id="f852e-153">On the review set page, click the dropdown for the prediction score filter and type minimum and maximum values for the prediction score range.</span></span> <span data-ttu-id="f852e-154">Par exemple, la capture d’écran suivante montre une plage de scores de prédiction entre **.5** et **1.0**.</span><span class="sxs-lookup"><span data-stu-id="f852e-154">For example, the following screenshot shows a prediction score range between **.5** and **1.0**.</span></span>

   ![Valeurs minimales et maximales pour le filtre de score de prédiction](..\media\PredictionScoreFilter2.png)

6. <span data-ttu-id="f852e-156">Cliquez en dehors du filtre pour appliquer automatiquement le filtre au jeu à réviser.</span><span class="sxs-lookup"><span data-stu-id="f852e-156">Click outside the filter to automatically apply the filter to the review set.</span></span>

  <span data-ttu-id="f852e-157">Une liste de documents avec un score de prédiction dans la plage que vous avez spécifiée s’affiche sur la page du jeu à réviser.</span><span class="sxs-lookup"><span data-stu-id="f852e-157">A list of documents with a prediction score within the range you specified is displayed on the review set page.</span></span>

<span data-ttu-id="f852e-158">Pour obtenir des instructions plus détaillées, voir Appliquer un filtre de prédiction [à un jeu à réviser.](predictive-coding-apply-prediction-filter.md)</span><span class="sxs-lookup"><span data-stu-id="f852e-158">For more detailed instructions, see [Apply a prediction filter to a review set](predictive-coding-apply-prediction-filter.md).</span></span>

## <a name="step-4-perform-more-training-rounds"></a><span data-ttu-id="f852e-159">Étape 4 : Effectuer d’autres séries de formation</span><span class="sxs-lookup"><span data-stu-id="f852e-159">Step 4: Perform more training rounds</span></span>

<span data-ttu-id="f852e-160">Il est plus probable que vous dedessiez plusieurs séries de formation pour former le module afin de mieux prévoir les éléments pertinents et non pertinents dans l’ensemble de révision.</span><span class="sxs-lookup"><span data-stu-id="f852e-160">More than likely, you'll have to perform more training rounds to train the module to better predict relevant and non-relevant items in the review set.</span></span> <span data-ttu-id="f852e-161">En règle générale, vous allez entraîner le modèle suffisamment de fois jusqu’à ce qu’il soit suffisamment stabilisé pour répondre à vos besoins.</span><span class="sxs-lookup"><span data-stu-id="f852e-161">In general, you'll train the model enough times until it stabilizes enough to meet your requirements.</span></span>

<span data-ttu-id="f852e-162">Pour plus d’informations, voir [Effectuer des séries de formation supplémentaires](predictive-coding-train-model.md#perform-additional-training-rounds)</span><span class="sxs-lookup"><span data-stu-id="f852e-162">For more information, see [Perform additional training rounds](predictive-coding-train-model.md#perform-additional-training-rounds)</span></span>

## <a name="step-5-apply-the-final-prediction-score-filter-to-prioritize-review"></a><span data-ttu-id="f852e-163">Étape 5 : Appliquer le filtre de score de prédiction final pour hiérarchiser l’examen</span><span class="sxs-lookup"><span data-stu-id="f852e-163">Step 5: Apply the final prediction score filter to prioritize review</span></span>

<span data-ttu-id="f852e-164">Répétez les instructions de l’étape 3 pour appliquer le score de prédiction final au jeu à réviser afin de hiérarchiser l’examen des éléments pertinents et non pertinents une fois que vous avez terminé toutes les séries de formation et stabilisé le modèle.</span><span class="sxs-lookup"><span data-stu-id="f852e-164">Repeat the instructions in Step 3 to apply the final prediction score to the review set to prioritize the review of relevant and non-relevant items after you complete all the training rounds and stabilize the model.</span></span>
