---
title: Appliquer le filtre de score de prédiction aux éléments d’un jeu à réviser
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
description: Utilisez un filtre de score de prédiction pour afficher les éléments qu’un modèle de codage prédictif est prévisible comme pertinent ou non pertinent.
ms.openlocfilehash: 0ca2770d5ccbcc3ea5f3dec8394f69d1f5117da5
ms.sourcegitcommit: 50908a93554290ff1157b58d0a868a33e012513c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "52822530"
---
# <a name="apply-a-prediction-score-filter-to-a-review-set-preview"></a><span data-ttu-id="846f8-103">Appliquer un filtre de score de prédiction à un jeu à réviser (aperçu)</span><span class="sxs-lookup"><span data-stu-id="846f8-103">Apply a prediction score filter to a review set (preview)</span></span>

<span data-ttu-id="846f8-104">Après avoir créé un modèle de codage prédictif dans Advanced eDiscovery et l’avoir formé au point où il est stable, vous pouvez appliquer le filtre de score de prédiction pour afficher les éléments de jeu à réviser que le modèle a déterminés pertinents (ou non pertinents).</span><span class="sxs-lookup"><span data-stu-id="846f8-104">After you create a predictive coding model in Advanced eDiscovery and train it to the point where it's stable, you can apply the prediction score filter to display review set items that the model has determined are relevant (or not relevant).</span></span> <span data-ttu-id="846f8-105">Lorsque vous créez un modèle, un filtre de score de prédiction correspondant est également créé.</span><span class="sxs-lookup"><span data-stu-id="846f8-105">When you create a model, a corresponding prediction score filter is also created.</span></span> <span data-ttu-id="846f8-106">Vous pouvez utiliser ce filtre pour afficher les éléments affectés d’un score de prédiction dans une plage spécifiée.</span><span class="sxs-lookup"><span data-stu-id="846f8-106">You can use this filter to display items assigned a prediction score within a specified range.</span></span> <span data-ttu-id="846f8-107">En règle générale, les scores de prédiction entre **0** et **0,5** sont affectés à des éléments que le modèle a prévu ne sont pas pertinents.</span><span class="sxs-lookup"><span data-stu-id="846f8-107">In general, prediction scores between **0** and **.5** are assigned to items that model has predicted are not relevant.</span></span> <span data-ttu-id="846f8-108">Les éléments attribués aux scores de prédiction entre **.5** et **1.0** sont des éléments que le modèle a prévu sont pertinents.</span><span class="sxs-lookup"><span data-stu-id="846f8-108">Items assigned prediction scores between **.5** and **1.0** are items the model has predicted are relevant.</span></span>

<span data-ttu-id="846f8-109">Voici deux façons d’utiliser le filtre de score de prédiction :</span><span class="sxs-lookup"><span data-stu-id="846f8-109">Here are two ways you can use the prediction score filter:</span></span>

- <span data-ttu-id="846f8-110">Hiérarchiser l’examen des éléments d’un jeu à réviser que le modèle a prévu sont pertinents.</span><span class="sxs-lookup"><span data-stu-id="846f8-110">Prioritize the review of items in a review set that the model has predicted are relevant.</span></span>

- <span data-ttu-id="846f8-111">L’annulation des éléments du jeu à réviser que le modèle a prévu n’est pas pertinente.</span><span class="sxs-lookup"><span data-stu-id="846f8-111">Cull items from the review set that the model has predicted are not relevant.</span></span> <span data-ttu-id="846f8-112">Vous pouvez également utiliser le filtre de score de prédiction pour dé hiérarchiser l’examen des éléments non pertinents.</span><span class="sxs-lookup"><span data-stu-id="846f8-112">Alternative, you can use the prediction score filter to de-prioritize the review of non-relevant items.</span></span>

## <a name="before-you-apply-a-prediction-score-filter"></a><span data-ttu-id="846f8-113">Avant d’appliquer un filtre de score de prédiction</span><span class="sxs-lookup"><span data-stu-id="846f8-113">Before you apply a prediction score filter</span></span>

- <span data-ttu-id="846f8-114">Créez un modèle de codage prédictif de sorte qu’un filtre de score de prédiction correspondant soit créé.</span><span class="sxs-lookup"><span data-stu-id="846f8-114">Create a predictive coding model so that a corresponding prediction score filter is created.</span></span>

- <span data-ttu-id="846f8-115">Vous pouvez appliquer un filtre de score de prédiction après l’un des cycles d’entraînement.</span><span class="sxs-lookup"><span data-stu-id="846f8-115">You can apply a prediction score filter after any of the training rounds.</span></span> <span data-ttu-id="846f8-116">Toutefois, vous pouvez attendre après avoir effectué plusieurs séries ou jusqu’à ce que le modèle soit stable avant d’utiliser le filtre de score de prédiction.</span><span class="sxs-lookup"><span data-stu-id="846f8-116">But you may want to wait after performing several rounds or until the model is stable before using the prediction score filter.</span></span>

## <a name="apply-a-prediction-score-filter"></a><span data-ttu-id="846f8-117">Appliquer un filtre de score de prédiction</span><span class="sxs-lookup"><span data-stu-id="846f8-117">Apply a prediction score filter</span></span>

1. <span data-ttu-id="846f8-118">Dans le centre Microsoft 365 conformité, ouvrez le cas  Advanced eDiscovery, sélectionnez l’onglet Ensembles de révision, puis ouvrez le jeu à réviser.</span><span class="sxs-lookup"><span data-stu-id="846f8-118">In the Microsoft 365 compliance center, open the Advanced eDiscovery case, select the **Review sets** tab, and then open the review set.</span></span>

   ![Cliquez sur Filtres pour afficher la page de présentation filtres](..\media\PredictionScoreFilter0.png)   

   <span data-ttu-id="846f8-120">Les filtres par défaut pré-chargés sont affichés en haut de la page de révision.</span><span class="sxs-lookup"><span data-stu-id="846f8-120">The pre-loaded default filters are displayed at the top of the review set page.</span></span> <span data-ttu-id="846f8-121">Vous pouvez laisser ces ensembles sur **Any**.</span><span class="sxs-lookup"><span data-stu-id="846f8-121">You can leave these set to **Any**.</span></span>

2. <span data-ttu-id="846f8-122">Cliquez **sur Filtres** pour afficher la page de présentation **filtres.**</span><span class="sxs-lookup"><span data-stu-id="846f8-122">Click **Filters** to display the **Filters** flyout page.</span></span>

3. <span data-ttu-id="846f8-123">Développez la section Analyse & codage **prédictif** pour afficher un ensemble de filtres.</span><span class="sxs-lookup"><span data-stu-id="846f8-123">Expand the **Analytics & predictive coding** section to display a set of filters.</span></span>

      ![Filtre de score de prédiction dans la section Analyse & codage prédictif](..\media\PredictionScoreFilter1.png)

   <span data-ttu-id="846f8-125">La convention d’attribution de noms pour les filtres de score de prédiction est **le score de prédiction (nom du modèle).**</span><span class="sxs-lookup"><span data-stu-id="846f8-125">The naming convention for prediction score filters is **Prediction score (model name)**.</span></span> <span data-ttu-id="846f8-126">Par exemple, le nom de filtre du score de prédiction pour un modèle nommé **Modèle A** est Le score de **prédiction (modèle A).**</span><span class="sxs-lookup"><span data-stu-id="846f8-126">For example, the prediction score filter name for a model named **Model A** is **Prediction score (Model A)**.</span></span>

4. <span data-ttu-id="846f8-127">Sélectionnez le filtre de score de prédiction à utiliser, puis cliquez sur **Terminé.**</span><span class="sxs-lookup"><span data-stu-id="846f8-127">Select the prediction score filter that you want to use and then click **Done**.</span></span>

5. <span data-ttu-id="846f8-128">Dans la page de jeu à réviser, cliquez sur ladown pour le filtre de score de prédiction et tapez les valeurs minimales et maximales pour la plage de score de prédiction.</span><span class="sxs-lookup"><span data-stu-id="846f8-128">On the review set page, click the dropdown for the prediction score filter and type minimum and maximum values for the prediction score range.</span></span> <span data-ttu-id="846f8-129">Par exemple, la capture d’écran suivante montre une plage de scores de prédiction entre **.5** et **1.0**.</span><span class="sxs-lookup"><span data-stu-id="846f8-129">For example, the following screenshot shows a prediction score range between **.5** and **1.0**.</span></span>

   ![Valeurs minimales et maximales pour le filtre de score de prédiction](..\media\PredictionScoreFilter2.png)

6. <span data-ttu-id="846f8-131">Cliquez en dehors du filtre pour appliquer automatiquement le filtre au jeu à réviser.</span><span class="sxs-lookup"><span data-stu-id="846f8-131">Click outside the filter to automatically apply the filter to the review set.</span></span>

  <span data-ttu-id="846f8-132">Une liste de documents avec un score de prédiction dans la plage que vous avez spécifiée s’affiche sur la page du jeu à réviser.</span><span class="sxs-lookup"><span data-stu-id="846f8-132">A list of documents with a prediction score within the range you specified is displayed on the review set page.</span></span> 

  > [!TIP]
  > <span data-ttu-id="846f8-133">Pour afficher le score de prédiction réel attribué à un document, vous pouvez cliquer sur l’onglet **Métadonnées** dans le volet de lecture.</span><span class="sxs-lookup"><span data-stu-id="846f8-133">To view the actual prediction score assign to a document, you can click the **Metadata** tab in the reading pane.</span></span> <span data-ttu-id="846f8-134">Les scores de prédiction pour tous les modèles du jeu à réviser sont affichés dans la propriété de métadonnées **RelevanceScores.**</span><span class="sxs-lookup"><span data-stu-id="846f8-134">The prediction scores for all models in the review set are displayed in the **RelevanceScores** metadata property.</span></span>

## <a name="more-information"></a><span data-ttu-id="846f8-135">Plus d’informations</span><span class="sxs-lookup"><span data-stu-id="846f8-135">More information</span></span>

- <span data-ttu-id="846f8-136">Pour plus d’informations sur l’utilisation des filtres, voir [Requête et filtrage du contenu dans un jeu à réviser.](review-set-search.md)</span><span class="sxs-lookup"><span data-stu-id="846f8-136">For more information about using filters, see [Query and filter content in a review set](review-set-search.md).</span></span>
