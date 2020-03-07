---
title: Analyser les données d’un ensemble de vérification dans Advanced eDiscovery
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
description: ''
ms.openlocfilehash: 0f9cb386ce57d6581ade5caa05e029511100d9b3
ms.sourcegitcommit: e741930c41abcde61add22d4b773dbf171ed72ac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/07/2020
ms.locfileid: "42556782"
---
# <a name="analyze-data-in-a-review-set-in-advanced-ediscovery"></a><span data-ttu-id="0503d-102">Analyser les données d’un ensemble de vérification dans Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="0503d-102">Analyze data in a review set in Advanced eDiscovery</span></span>

<span data-ttu-id="0503d-103">Lorsque le nombre de documents collectés est important, il peut s’avérer difficile de les examiner tous.</span><span class="sxs-lookup"><span data-stu-id="0503d-103">When the number of collected documents is large, it can be difficult to review them all.</span></span> <span data-ttu-id="0503d-104">Advanced eDiscovery fournit un certain nombre d’outils pour analyser les documents afin de réduire le volume des documents à examiner sans perte de données et pour vous aider à organiser les documents de manière cohérente.</span><span class="sxs-lookup"><span data-stu-id="0503d-104">Advanced eDiscovery provides a number of tools to analyze the documents to reduce the volume of documents to be reviewed without any loss in information, and to help you organize the documents in a coherent manner.</span></span> <span data-ttu-id="0503d-105">Pour en savoir plus sur ces fonctionnalités, consultez les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="0503d-105">To learn more about these capabilities, see:</span></span>

- [<span data-ttu-id="0503d-106">Détecter des quasi-duplicatas</span><span class="sxs-lookup"><span data-stu-id="0503d-106">Near duplicate detection</span></span>](near-duplicates.md)

- [<span data-ttu-id="0503d-107">Threading de messagerie</span><span class="sxs-lookup"><span data-stu-id="0503d-107">Email threading</span></span>](email-threading.md)

- [<span data-ttu-id="0503d-108">Thèmes</span><span class="sxs-lookup"><span data-stu-id="0503d-108">Themes</span></span>](themes.md)

<span data-ttu-id="0503d-109">Pour analyser les données d’un ensemble de révision :</span><span class="sxs-lookup"><span data-stu-id="0503d-109">To analyze data in a review set:</span></span>

1. <span data-ttu-id="0503d-110">Configurez les paramètres d’analyse pour votre cas.</span><span class="sxs-lookup"><span data-stu-id="0503d-110">Configure analytics settings for your case.</span></span> <span data-ttu-id="0503d-111">Pour plus d’informations, consultez la rubrique [configurer les paramètres de recherche et d’analyse](configure-search-analytics-settings.md).</span><span class="sxs-lookup"><span data-stu-id="0503d-111">For more information, see [Configure search and analytics settings](configure-search-analytics-settings.md).</span></span>

2. <span data-ttu-id="0503d-112">Ouvrez l’ensemble de révision à analyser.</span><span class="sxs-lookup"><span data-stu-id="0503d-112">Open the review set you want to analyze.</span></span>

3. <span data-ttu-id="0503d-113">Cliquez sur **gérer le jeu de révision**.</span><span class="sxs-lookup"><span data-stu-id="0503d-113">Click **Manage review set**.</span></span>

4. <span data-ttu-id="0503d-114">Cliquez sur **exécuter l’analyse pour l’ensemble de révision**.</span><span class="sxs-lookup"><span data-stu-id="0503d-114">Click **Run analytics for the review set**.</span></span>

<span data-ttu-id="0503d-115">Vous pouvez vérifier la progression de l’analyse sous l’onglet **tâches** du cas.</span><span class="sxs-lookup"><span data-stu-id="0503d-115">You can check the progress of analysis on the **Jobs** tab of the case.</span></span>

 <span data-ttu-id="0503d-116">Une fois l’analyse terminée, vous pouvez afficher le rapport d’analyse, exécuter des requêtes dans votre ensemble de révision sur les sorties de l’analyse (voir la rubrique relative à la [recherche dans l’ensemble de révision](review-set-search.md)) et consulter les documents connexes d’un document donné (voir [Review Data in Review Set](reviewing-data-in-review-set.md)).</span><span class="sxs-lookup"><span data-stu-id="0503d-116">After analysis is completed, you can view the analytics report, run queries within your review set on outputs of the analysis (see [Query within your review set](review-set-search.md)), and see related documents of a given document (see [Reviewing data in review set](reviewing-data-in-review-set.md)).</span></span>

## <a name="analytics-report"></a><span data-ttu-id="0503d-117">Rapport d’analyse</span><span class="sxs-lookup"><span data-stu-id="0503d-117">Analytics report</span></span>

<span data-ttu-id="0503d-118">Pour afficher un rapport d’analyse pour un jeu de révisions :</span><span class="sxs-lookup"><span data-stu-id="0503d-118">To view an analytics report for a review set:</span></span>

1. <span data-ttu-id="0503d-119">Ouvrez l’ensemble de révision.</span><span class="sxs-lookup"><span data-stu-id="0503d-119">Open the review set.</span></span>

2. <span data-ttu-id="0503d-120">Cliquez sur **gérer le jeu de révision**.</span><span class="sxs-lookup"><span data-stu-id="0503d-120">Click **Manage review set**.</span></span>

3. <span data-ttu-id="0503d-121">Cliquez sur **afficher le rapport**.</span><span class="sxs-lookup"><span data-stu-id="0503d-121">Click **View report**.</span></span>

<span data-ttu-id="0503d-122">Le rapport comprend sept composants de l’analyse :</span><span class="sxs-lookup"><span data-stu-id="0503d-122">The report has seven components from analysis:</span></span>

- <span data-ttu-id="0503d-123">**Population cible :** Le nombre de messages électroniques, de pièces jointes et de documents en vrac trouvés dans l’ensemble de révision.</span><span class="sxs-lookup"><span data-stu-id="0503d-123">**Target population:** The number of email messages, attachments, and loose documents found in the review set.</span></span>

- <span data-ttu-id="0503d-124">**Documents (à l’exception des pièces jointes) :** Nombre de documents en vrac, qui sont des tableaux croisés dynamiques, qui sont des doublons d’un tableau croisé dynamique ou un doublon exact d’un autre document.</span><span class="sxs-lookup"><span data-stu-id="0503d-124">**Documents (excluding attachments):** The number of loose documents that are pivots, unique near duplicates of a pivot, or an exact duplicate of another document.</span></span>

- <span data-ttu-id="0503d-125">**E-mails :** Nombre de messages électroniques inclus, de copies inclusives, inclusifs ou aucun des.</span><span class="sxs-lookup"><span data-stu-id="0503d-125">**Emails:** The number of email messages that are inclusives, inclusive copies, inclusive minuses, or none of the above.</span></span>

- <span data-ttu-id="0503d-126">**Pièces jointes :** Nombre de pièces jointes qui sont uniques ou des doublons d’une autre pièce jointe dans l’ensemble de révision.</span><span class="sxs-lookup"><span data-stu-id="0503d-126">**Attachments:** The number of email attachments that are unique or duplicates of another email attachment in the review set.</span></span>

- <span data-ttu-id="0503d-127">**Nombre de fichiers par type :** Nombre de fichiers identifiés par extension de fichier.</span><span class="sxs-lookup"><span data-stu-id="0503d-127">**Number of files by type:** The number of files, identified by file extension.</span></span>

- <span data-ttu-id="0503d-128">**Documents par source :** Résumé du contenu par sa source de données d’origine.</span><span class="sxs-lookup"><span data-stu-id="0503d-128">**Documents by source:** A summary of content by its original data source.</span></span>

- <span data-ttu-id="0503d-129">**Documents agrégés par processus :** Résumé du contenu en revue les processus de jeu.</span><span class="sxs-lookup"><span data-stu-id="0503d-129">**Documents aggregated by process:** A summary of content by review set processes.</span></span> 
