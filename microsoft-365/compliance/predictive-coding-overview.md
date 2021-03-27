---
title: Module de codage prédictif pour Advanced eDiscovery (aperçu)
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
description: Le nouveau module de codage prédictif dans Advanced eDiscovery utilise l’apprentissage automatique pour analyser les documents d’un jeu à réviser afin de déterminer quels documents sont pertinents pour votre cas ou votre enquête.
ms.openlocfilehash: 6a3f3b502dfe9efedc785ac3b246f60f13466dcb
ms.sourcegitcommit: ef98b8a18d275e5b5961e63d2b0743d046321737
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/26/2021
ms.locfileid: "51382959"
---
# <a name="predictive-coding-module-for-advanced-ediscovery-preview"></a><span data-ttu-id="e653b-103">Module de codage prédictif pour Advanced eDiscovery (aperçu)</span><span class="sxs-lookup"><span data-stu-id="e653b-103">Predictive coding module for Advanced eDiscovery (preview)</span></span>

<span data-ttu-id="e653b-104">À l’aide du nouveau module de codage prédictif dans Advanced eDiscovery, vous pouvez créer et créer un modèle pour hiérarchiser l’examen des documents en commençant par les documents les plus pertinents.</span><span class="sxs-lookup"><span data-stu-id="e653b-104">Using the new predictive coding module in Advanced eDiscovery, you can create and build a model to prioritize review of documents starting with the most relevant documents.</span></span> <span data-ttu-id="e653b-105">To get started, you can create a model, label as few as 50 documents, and then filter documents by model prediction scores to review relevant non-relevant documents.</span><span class="sxs-lookup"><span data-stu-id="e653b-105">To get started, you can create a model, label as few as 50 documents, and then filter documents by model prediction scores to review relevant non-relevant documents.</span></span>

<span data-ttu-id="e653b-106">Voici une vue d’ensemble rapide du flux de travail :</span><span class="sxs-lookup"><span data-stu-id="e653b-106">Here’s a quick overview of the workflow:</span></span>

1. <span data-ttu-id="e653b-107">Ouvrez le module de codage prédictif dans un jeu à réviser.</span><span class="sxs-lookup"><span data-stu-id="e653b-107">Open the predictive coding module in a review set.</span></span>

   ![Cliquez sur la liste de listes d’analyse dans une révision pour aller au module de codage prédictif](..\media\PredictiveCoding1.png)

2. <span data-ttu-id="e653b-109">Dans la page **Modèles de codage** prédictif, cliquez **sur Nouveau modèle** pour créer un modèle de codage prédictif.</span><span class="sxs-lookup"><span data-stu-id="e653b-109">On the **Predictive coding models** page, click **New model** to create a new predictive coding model.</span></span>

   ![Créer un modèle](..\media\PredictiveCoding2.png)

3. <span data-ttu-id="e653b-111">Étiquetez au moins 50 documents comme **pertinents** **ou non pertinents.**</span><span class="sxs-lookup"><span data-stu-id="e653b-111">Label at least 50 documents as **Relevant** or **Not relevant**.</span></span> <span data-ttu-id="e653b-112">Cet étiquetage est utilisé pour former le système.</span><span class="sxs-lookup"><span data-stu-id="e653b-112">This labeling is used to train the system.</span></span>

   ![Étiqueter les documents comme pertinents ou non pertinents pour former le système](..\media\PredictiveCoding3.png)

4. <span data-ttu-id="e653b-114">Appliquez **le filtre de score** de prédiction pour votre modèle au jeu à réviser.</span><span class="sxs-lookup"><span data-stu-id="e653b-114">Apply the **Prediction score** filter for your model to the review set.</span></span> <span data-ttu-id="e653b-115">Pour ce faire :</span><span class="sxs-lookup"><span data-stu-id="e653b-115">To do this:</span></span>

   1. <span data-ttu-id="e653b-116">Dans le jeu à réviser, cliquez sur **Filtres.**</span><span class="sxs-lookup"><span data-stu-id="e653b-116">In the review set, click **Filters**.</span></span>
   2. <span data-ttu-id="e653b-117">Dans la page de programme volant **Filtres,** développez la section **Analyse/ML,** puis cochez la case de **prédiction** pour le modèle que vous souhaitez appliquer.</span><span class="sxs-lookup"><span data-stu-id="e653b-117">In the **Filters** flyout page, expand the **Analytics/ML** section and then select **Prediction score** checkbox for the model you want to apply.</span></span>
   3. <span data-ttu-id="e653b-118">Dans le **filtre de score de prédiction,** spécifiez un score de prédiction.</span><span class="sxs-lookup"><span data-stu-id="e653b-118">In the **Prediction score** filter, specify a prediction score.</span></span> <span data-ttu-id="e653b-119">Le filtre affiche les documents du jeu à réviser qui correspondent au score de prédiction.</span><span class="sxs-lookup"><span data-stu-id="e653b-119">The filter will display the documents in the review set that match the prediction score.</span></span>

      ![Spécifier un score de prédiction pour filtrer des documents](..\media\PredictiveCoding4.png)

5. <span data-ttu-id="e653b-121">Surveillez les performances, l’état et la stabilité de votre modèle.</span><span class="sxs-lookup"><span data-stu-id="e653b-121">Monitor the performance, status, and stability of your model.</span></span>

   ![Surveiller les performances, l’état et la stabilité de votre modèle](..\media\PredictiveCoding5.png)
