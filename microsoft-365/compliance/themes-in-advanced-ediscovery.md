---
title: Thèmes-eDiscovery
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
description: Utilisez des thèmes dans Advanced eDiscovery pour organiser les ensembles de révision en recherchant le thème dominant dans chaque document.
ms.custom: seo-marvel-mar2020
ms.openlocfilehash: eb008e091cd8c8330d1cdd5b388e252af70922da
ms.sourcegitcommit: a45cf8b887587a1810caf9afa354638e68ec5243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/05/2020
ms.locfileid: "44034518"
---
# <a name="themes"></a><span data-ttu-id="efe59-103">Thèmes</span><span class="sxs-lookup"><span data-stu-id="efe59-103">Themes</span></span>

<span data-ttu-id="efe59-104">Comment une personne écrit-t-elle un document ?</span><span class="sxs-lookup"><span data-stu-id="efe59-104">How does a person write a document?</span></span> <span data-ttu-id="efe59-105">Elles commencent généralement par une ou plusieurs idées qu’elles souhaitent transférer dans le document, et composent des mots qui s’alignent sur les idées.</span><span class="sxs-lookup"><span data-stu-id="efe59-105">They generally start with one or more ideas they want to convey in the document, and compose using words that align with the ideas.</span></span> <span data-ttu-id="efe59-106">Plus l’idée est fréquente, plus le nombre de mots liés à cette idée est important.</span><span class="sxs-lookup"><span data-stu-id="efe59-106">The more prevalent an idea is, the more frequent the words that are related to that idea tend to be.</span></span> <span data-ttu-id="efe59-107">Cela indique le mode d’utilisation des documents par les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="efe59-107">This informs how people consume documents as well.</span></span> <span data-ttu-id="efe59-108">Il est important de comprendre la lecture d’un document, à savoir les idées que le document tente de transmettre, les idées qui apparaissent où et les relations entre les idées.</span><span class="sxs-lookup"><span data-stu-id="efe59-108">The important thing to understand from reading a document is the ideas that the document is trying to convey, which ideas appear where, and what the relationships between the ideas are.</span></span>

<span data-ttu-id="efe59-109">Cela peut être étendu à la manière dont une personne souhaite utiliser un ensemble de documents.</span><span class="sxs-lookup"><span data-stu-id="efe59-109">This can be extended to how a person wants to consume a set of documents.</span></span> <span data-ttu-id="efe59-110">Ils veulent voir quelles idées sont présentes dans les ensembles et quels documents parlent de ces idées.</span><span class="sxs-lookup"><span data-stu-id="efe59-110">They want to see which ideas are present in the sets, and which documents are talking about those ideas.</span></span> <span data-ttu-id="efe59-111">En outre, si elle trouve un document d’intérêt particulier, elle souhaite pouvoir consulter des documents qui abordent des idées similaires.</span><span class="sxs-lookup"><span data-stu-id="efe59-111">Also, if they find a particular document of interest, they want to be able to see documents that discuss similar ideas.</span></span>

<span data-ttu-id="efe59-112">La fonctionnalité de thèmes dans Advanced eDiscovery tente de reproduire la raison pour les êtres humains des documents en analysant les *thèmes* présentés dans un jeu de révision et en affectant un thème aux documents dans l’ensemble de révision.</span><span class="sxs-lookup"><span data-stu-id="efe59-112">The Themes functionality in Advanced eDiscovery attempts to mimic how humans reason about documents, by analyzing the *themes* that are discussed in a review set and assigning a theme to documents in the review set.</span></span> <span data-ttu-id="efe59-113">Dans Advanced eDiscovery, les thèmes se déplacent d’une étape supplémentaire et identifient le *thème dominant* dans chaque document.</span><span class="sxs-lookup"><span data-stu-id="efe59-113">In Advanced eDiscovery, Themes goes one step further and identifies the *dominant theme* in each document.</span></span> <span data-ttu-id="efe59-114">Le thème dominant est celui qui apparaît le plus souvent dans un document.</span><span class="sxs-lookup"><span data-stu-id="efe59-114">The dominant theme is the one that appears the most often in a document.</span></span>

## <a name="how-does-themes-work"></a><span data-ttu-id="efe59-115">Comment fonctionne le thème ?</span><span class="sxs-lookup"><span data-stu-id="efe59-115">How does Themes work?</span></span>

<span data-ttu-id="efe59-116">La fonctionnalité de thèmes analyse les documents avec du texte dans un ensemble de révision pour analyser les thèmes communs qui apparaissent dans tous les documents de l’ensemble de révision.</span><span class="sxs-lookup"><span data-stu-id="efe59-116">The Themes functionality analyzes documents with text in a review set to parse out common themes that appear across all the documents in the review set.</span></span> <span data-ttu-id="efe59-117">Advanced eDiscovery affecte ces thèmes aux documents dans lesquels ils apparaissent.</span><span class="sxs-lookup"><span data-stu-id="efe59-117">Advanced eDiscovery assigns those themes to the documents in which they appear.</span></span> <span data-ttu-id="efe59-118">Il étiquette également chaque thème avec les mots utilisés dans les documents représentatifs du thème.</span><span class="sxs-lookup"><span data-stu-id="efe59-118">It also labels each theme with the words used in the documents that are representative of the theme.</span></span> <span data-ttu-id="efe59-119">Étant donné qu’un document peut contenir différents types d’objets, Advanced eDiscovery affecte souvent plusieurs thèmes à des documents.</span><span class="sxs-lookup"><span data-stu-id="efe59-119">Because a document can contain various types of subject matter, Advanced eDiscovery often assigns multiple themes to documents.</span></span> <span data-ttu-id="efe59-120">Le thème qui apparaît le plus en évidence dans un document est désigné comme son thème dominant.</span><span class="sxs-lookup"><span data-stu-id="efe59-120">The theme that appears most prominently in a document is designated as its dominant theme.</span></span>
