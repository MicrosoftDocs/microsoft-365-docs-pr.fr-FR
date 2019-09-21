---
title: Exécuter les données d’analyse pour investiguer plus rapidement
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
ms.openlocfilehash: 7462b415c2e5b0a66c08bb9b5abb647f366e9785
ms.sourcegitcommit: 1162d676b036449ea4220de8a6642165190e3398
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/20/2019
ms.locfileid: "37079773"
---
# <a name="run-analytics-to-investigate-faster"></a><span data-ttu-id="19dde-102">Exécuter les données d’analyse pour investiguer plus rapidement</span><span class="sxs-lookup"><span data-stu-id="19dde-102">Run analytics to investigate faster</span></span>

<span data-ttu-id="19dde-103">Lorsqu’une collection de preuves est volumineuse, il peut s’avérer difficile de les examiner tous.</span><span class="sxs-lookup"><span data-stu-id="19dde-103">When an evidence collection is large, it can be difficult to review them all.</span></span> <span data-ttu-id="19dde-104">Un ensemble de preuves inclut souvent plusieurs copies de messages ou de documents de courrier identiques ou similaires.</span><span class="sxs-lookup"><span data-stu-id="19dde-104">A set of evidence often includes multiple copies of the same or similar email messages or documents.</span></span> <span data-ttu-id="19dde-105">Les enquêtes de données (préversion) fournissent un certain nombre d’outils d’analyse qui peuvent vous aider à réduire le volume des documents qui doivent être analysés sans aucune perte de données.</span><span class="sxs-lookup"><span data-stu-id="19dde-105">Data Investigations (Preview) provides a number of analytics tools that can help you reduce the volume of documents that need to be reviewed without any loss in information.</span></span> <span data-ttu-id="19dde-106">Pour en savoir plus sur ces fonctionnalités, consultez les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="19dde-106">To learn more about these capabilities, see:</span></span>

- [<span data-ttu-id="19dde-107">Détecter des quasi-duplicatas</span><span class="sxs-lookup"><span data-stu-id="19dde-107">Near duplicate detection</span></span>](near-duplicates.md)

- [<span data-ttu-id="19dde-108">Threading de messagerie</span><span class="sxs-lookup"><span data-stu-id="19dde-108">Email threading</span></span>](email-threading.md)

- [<span data-ttu-id="19dde-109">Thèmes</span><span class="sxs-lookup"><span data-stu-id="19dde-109">Themes</span></span>](themes.md)

<span data-ttu-id="19dde-110">Pour analyser les données d’un ensemble de preuves :</span><span class="sxs-lookup"><span data-stu-id="19dde-110">To analyze data in an evidence set:</span></span>

1. <span data-ttu-id="19dde-111">Configurez les paramètres d’analyse pour votre enquête.</span><span class="sxs-lookup"><span data-stu-id="19dde-111">Configure the analytics settings for your investigation.</span></span> <span data-ttu-id="19dde-112">Pour plus d’informations, consultez la rubrique [configurer les paramètres de recherche et d’analyse](configure-search-analytics-settings.md).</span><span class="sxs-lookup"><span data-stu-id="19dde-112">For more information, see [Configure search and analytics settings](configure-search-analytics-settings.md).</span></span>

2. <span data-ttu-id="19dde-113">Ouvrez l’ensemble de preuves.</span><span class="sxs-lookup"><span data-stu-id="19dde-113">Open the evidence set.</span></span>

3. <span data-ttu-id="19dde-114">Cliquez sur **gérer les preuves**.</span><span class="sxs-lookup"><span data-stu-id="19dde-114">Click **Manage evidence**.</span></span>

4. <span data-ttu-id="19dde-115">Sous **analyse**, cliquez sur **analyser**.</span><span class="sxs-lookup"><span data-stu-id="19dde-115">Under **Analytics**, click **Analyze**.</span></span>

<span data-ttu-id="19dde-116">Vous pouvez vérifier la progression de l’analyse dans l’onglet **travaux** de votre enquête.</span><span class="sxs-lookup"><span data-stu-id="19dde-116">You can check the progress of analysis on the **Jobs** tab in your investigation.</span></span> <span data-ttu-id="19dde-117">Le type de travail déclenché est nommé **analyse en cours d’exécution**.</span><span class="sxs-lookup"><span data-stu-id="19dde-117">The job type that's triggered is named **Running analytics**.</span></span>

 <span data-ttu-id="19dde-118">Une fois l’analyse terminée, vous pouvez afficher la liste des doublons ou des doublons exacts du document que vous examinez dans le volet droit.</span><span class="sxs-lookup"><span data-stu-id="19dde-118">After analysis is completed, you can see a list of exact duplicates or near-duplicates of the document that you're reviewing located in the panel on the right.</span></span> <span data-ttu-id="19dde-119">Pour sélectionner tous les doublons du document que vous affichez, vous pouvez facilement le faire à l’aide de ce panneau.</span><span class="sxs-lookup"><span data-stu-id="19dde-119">To select all duplicates of the document you're viewing, you can easily do so using this panel.</span></span> <span data-ttu-id="19dde-120">Pour en savoir plus sur les autres fonctionnalités de ce panneau, voir [examiner les données dans les preuves](review-data-in-evidence.md).</span><span class="sxs-lookup"><span data-stu-id="19dde-120">To learn more about other features on this panel, see [Review data in evidence](review-data-in-evidence.md).</span></span> 

<span data-ttu-id="19dde-121">Vous pouvez également exécuter des requêtes supplémentaires dans votre preuve à l’aide des sorties de l’analyse comme themes.</span><span class="sxs-lookup"><span data-stu-id="19dde-121">You can also run additional queries within your evidence using the outputs of the analysis such as themes.</span></span> <span data-ttu-id="19dde-122">Pour plus d’informations, consultez [la rubrique Query the Data in Evidence](evidence-query.md).</span><span class="sxs-lookup"><span data-stu-id="19dde-122">For more information, see [Query the data in evidence](evidence-query.md).</span></span>

## <a name="analytics-report"></a><span data-ttu-id="19dde-123">Rapport d’analyse</span><span class="sxs-lookup"><span data-stu-id="19dde-123">Analytics report</span></span>

<span data-ttu-id="19dde-124">Pour afficher un rapport d’analyse pour vos preuves :</span><span class="sxs-lookup"><span data-stu-id="19dde-124">To view an analytics report for your evidence:</span></span>

1. <span data-ttu-id="19dde-125">Ouvrez l’ensemble de preuves.</span><span class="sxs-lookup"><span data-stu-id="19dde-125">Open the evidence set.</span></span>

2. <span data-ttu-id="19dde-126">Cliquez sur **gérer les preuves**.</span><span class="sxs-lookup"><span data-stu-id="19dde-126">Click **Manage evidence**.</span></span>

3. <span data-ttu-id="19dde-127">Sous **analyse**, cliquez sur **afficher le rapport**.</span><span class="sxs-lookup"><span data-stu-id="19dde-127">Under **Analytics**, click **View report**.</span></span>

<span data-ttu-id="19dde-128">L’État comprend quatre composants de l’analyse :</span><span class="sxs-lookup"><span data-stu-id="19dde-128">The report has four components from analysis:</span></span>

- <span data-ttu-id="19dde-129">**Répartition** : nombre de messages électroniques bruts, de pièces jointes et de documents trouvés dans l’ensemble de preuves.</span><span class="sxs-lookup"><span data-stu-id="19dde-129">**Breakdown** - The number of raw emails, attachments, and documents found in the evidence set.</span></span>

- <span data-ttu-id="19dde-130">**E-mails** : nombre de messages eamil inclusifs, inclusifs, moins de copies inclusives ou aucun des éléments ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="19dde-130">**Emails** - The number of eamil messages that are inclusives, inclusive minuses, inclusive copies, or none of the above.</span></span>
   - <span data-ttu-id="19dde-131">Inclusif : dernier message dans le thread de courrier électronique qui contient l’historique précédent et nécessite une révision.</span><span class="sxs-lookup"><span data-stu-id="19dde-131">Inclusives: The last message in the email thread that contains all previous history and requires review.</span></span>
   - <span data-ttu-id="19dde-132">Inclusif : le message dans le fil de discussion qui contient une ou plusieurs pièces jointes qui doivent être réexaminées.</span><span class="sxs-lookup"><span data-stu-id="19dde-132">Inclusive minuses: The message in the thread that contains one or more different attachments that requires review.</span></span>
   - <span data-ttu-id="19dde-133">Copies inclusives : message qui est une copie d’un autre message moins inclusive ou inclusif (Subject and Body).</span><span class="sxs-lookup"><span data-stu-id="19dde-133">Inclusive copies: The message that is a copy of another inclusive or inclusive minus message (subject and body).</span></span>

- <span data-ttu-id="19dde-134">**Pièces jointes** : nombre de pièces jointes qui sont uniques ou des doublons d’une autre pièce jointe dans la même preuve.</span><span class="sxs-lookup"><span data-stu-id="19dde-134">**Attachments** - The number of email attachments that are unique or duplicates of a different email attachment within the same evidence same.</span></span>

- <span data-ttu-id="19dde-135">**Documents (à l’exception des pièces jointes)** : le nombre de documents uniques qui nécessitent une révision, par exemple, le document le plus représentatif de l’ensemble presque dupliqué ou un doublon exact d’un autre document).</span><span class="sxs-lookup"><span data-stu-id="19dde-135">**Documents (excluding email attachments)** - The number of unique documents that require review, for example, the most representative document of the near-duplicate set or an exact duplicate of another document).</span></span>