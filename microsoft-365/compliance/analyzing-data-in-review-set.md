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
ms.openlocfilehash: fbc2ad99433e2bf296e2891b6f3e85e22b6af6df
ms.sourcegitcommit: 3dd9944a6070a7f35c4bc2b57df397f844c3fe79
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2020
ms.locfileid: "42079931"
---
# <a name="analyze-data-in-a-review-set-in-advanced-ediscovery"></a><span data-ttu-id="98f69-102">Analyser les données d’un ensemble de vérification dans Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="98f69-102">Analyze data in a review set in Advanced eDiscovery</span></span>

<span data-ttu-id="98f69-103">Lorsque le nombre de documents collectés est important, il peut s’avérer difficile de les examiner tous.</span><span class="sxs-lookup"><span data-stu-id="98f69-103">When the number of collected documents is large, it can be difficult to review them all.</span></span> <span data-ttu-id="98f69-104">Advanced eDiscovery fournit un certain nombre d’outils pour analyser les documents afin de réduire le volume des documents à examiner sans perte de données et pour vous aider à organiser les documents de manière cohérente.</span><span class="sxs-lookup"><span data-stu-id="98f69-104">Advanced eDiscovery provides a number of tools to analyze the documents to reduce the volume of documents to be reviewed without any loss in information, and to help you organize the documents in a coherent manner.</span></span> <span data-ttu-id="98f69-105">Pour en savoir plus sur ces fonctionnalités, consultez les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="98f69-105">To learn more about these capabilities, see:</span></span>

- [<span data-ttu-id="98f69-106">Détecter des quasi-duplicatas</span><span class="sxs-lookup"><span data-stu-id="98f69-106">Near duplicate detection</span></span>](near-duplicates.md)

- [<span data-ttu-id="98f69-107">Threading de messagerie</span><span class="sxs-lookup"><span data-stu-id="98f69-107">Email threading</span></span>](email-threading.md)

- [<span data-ttu-id="98f69-108">Thèmes</span><span class="sxs-lookup"><span data-stu-id="98f69-108">Themes</span></span>](themes.md)

<span data-ttu-id="98f69-109">Pour analyser les données d’un ensemble de révision :</span><span class="sxs-lookup"><span data-stu-id="98f69-109">To analyze data in a review set:</span></span>

1. <span data-ttu-id="98f69-110">Configurez les paramètres d’analyse pour votre cas.</span><span class="sxs-lookup"><span data-stu-id="98f69-110">Configure analytics settings for your case.</span></span> <span data-ttu-id="98f69-111">Pour plus d’informations, consultez la rubrique [configurer les paramètres de recherche et d’analyse](configure-search-analytics-settings.md).</span><span class="sxs-lookup"><span data-stu-id="98f69-111">For more information, see [Configure search and analytics settings](configure-search-analytics-settings.md).</span></span>

2. <span data-ttu-id="98f69-112">Ouvrez l’ensemble de révision à analyser.</span><span class="sxs-lookup"><span data-stu-id="98f69-112">Open the review set you want to analyze.</span></span>

3. <span data-ttu-id="98f69-113">Cliquez sur **gérer le jeu de révision**.</span><span class="sxs-lookup"><span data-stu-id="98f69-113">Click **Manage review set**.</span></span>

4. <span data-ttu-id="98f69-114">Cliquez sur **exécuter l’analyse pour l’ensemble de révision**.</span><span class="sxs-lookup"><span data-stu-id="98f69-114">Click **Run analytics for the review set**.</span></span>

<span data-ttu-id="98f69-115">Vous pouvez vérifier la progression de l’analyse sous l’onglet **tâches** du cas.</span><span class="sxs-lookup"><span data-stu-id="98f69-115">You can check the progress of analysis on the **Jobs** tab of the case.</span></span>

 <span data-ttu-id="98f69-116">Une fois l’analyse terminée, vous pouvez afficher le rapport d’analyse, exécuter des requêtes dans votre ensemble de révision sur les sorties de l’analyse (voir la rubrique relative à la [recherche dans l’ensemble de révision](review-set-search.md)) et consulter les documents connexes d’un document donné (voir [Review Data in Review Set](reviewing-data-in-review-set.md)).</span><span class="sxs-lookup"><span data-stu-id="98f69-116">After analysis is completed, you can view the analytics report, run queries within your review set on outputs of the analysis (see [Query within your review set](review-set-search.md)), and see related documents of a given document (see [Reviewing data in review set](reviewing-data-in-review-set.md)).</span></span>

## <a name="analytics-report"></a><span data-ttu-id="98f69-117">Rapport d’analyse</span><span class="sxs-lookup"><span data-stu-id="98f69-117">Analytics report</span></span>

<span data-ttu-id="98f69-118">Pour afficher un rapport d’analyse pour un jeu de révisions :</span><span class="sxs-lookup"><span data-stu-id="98f69-118">To view an analytics report for a review set:</span></span>

1. <span data-ttu-id="98f69-119">Ouvrez l’ensemble de révision.</span><span class="sxs-lookup"><span data-stu-id="98f69-119">Open the review set.</span></span>

2. <span data-ttu-id="98f69-120">Cliquez sur **gérer le jeu de révision**.</span><span class="sxs-lookup"><span data-stu-id="98f69-120">Click **Manage review set**.</span></span>

3. <span data-ttu-id="98f69-121">Cliquez sur **afficher le rapport**.</span><span class="sxs-lookup"><span data-stu-id="98f69-121">Click **View report**.</span></span>

<span data-ttu-id="98f69-122">L’État comprend quatre composants de l’analyse :</span><span class="sxs-lookup"><span data-stu-id="98f69-122">The report has four components from analysis:</span></span>

- <span data-ttu-id="98f69-123">**Répartition** : le nombre de messages électroniques, de pièces jointes et de documents en vrac a été trouvé dans l’ensemble de révision.</span><span class="sxs-lookup"><span data-stu-id="98f69-123">**Breakdown** - How many email messages, attachments, and loose documents were found in the review set.</span></span>

- <span data-ttu-id="98f69-124">**Documents (à l’exception des pièces jointes)** : le nombre de documents en vrac était des tableaux croisés dynamiques, des doublons uniques proches d’un tableau croisé dynamique ou un doublon exact d’un autre document.</span><span class="sxs-lookup"><span data-stu-id="98f69-124">**Documents (excluding attachments)** - How many loose documents were pivots, unique near duplicates of a pivot, or an exact duplicate of another document.</span></span>

- <span data-ttu-id="98f69-125">**E-mails** : nombre de messages électroniques inclus, copies inclusives, déductions inclusives ou aucun des éléments ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="98f69-125">**Emails** - How many email messages were inclusives, inclusive copies, inclusive minuses, or none of the above.</span></span>

- <span data-ttu-id="98f69-126">**Pièces jointes** : le nombre de pièces jointes de courrier électronique sont uniques ou des doublons d’une autre pièce jointe dans l’ensemble de révision.</span><span class="sxs-lookup"><span data-stu-id="98f69-126">**Attachments** - How many email attachments were unique or duplicates of another email attachment in the review set.</span></span>
