---
title: Thèmes - eDiscovery
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: Utilisez des thèmes dans Advanced eDiscovery pour organiser les ensembles de révision en trouvant le thème dominant dans chaque document.
ms.custom: seo-marvel-mar2020
ms.openlocfilehash: 3dfc0dca0c6ed62e3ce8384efa2fd3ea407c3ce8
ms.sourcegitcommit: 2160e7cf373f992dd4d11793a59cb8c44f8d587e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/26/2020
ms.locfileid: "48285530"
---
# <a name="themes-in-advanced-ediscovery"></a><span data-ttu-id="6bebc-103">Thèmes dans Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="6bebc-103">Themes in Advanced eDiscovery</span></span>

<span data-ttu-id="6bebc-104">Comment une personne écrit-elle un document ?</span><span class="sxs-lookup"><span data-stu-id="6bebc-104">How does a person write a document?</span></span> <span data-ttu-id="6bebc-105">Ils commencent généralement par une ou plusieurs idées qu’ils souhaitent transmettre dans le document et composent à l’aide de mots qui s’alignent sur les idées.</span><span class="sxs-lookup"><span data-stu-id="6bebc-105">They generally start with one or more ideas they want to convey in the document, and compose using words that align with the ideas.</span></span> <span data-ttu-id="6bebc-106">Plus une idée est répandue, plus les mots associés à cette idée sont fréquents.</span><span class="sxs-lookup"><span data-stu-id="6bebc-106">The more prevalent an idea is, the more frequent the words that are related to that idea tend to be.</span></span> <span data-ttu-id="6bebc-107">Cela vous informe également sur la façon dont les personnes utilisent des documents.</span><span class="sxs-lookup"><span data-stu-id="6bebc-107">This informs how people consume documents as well.</span></span> <span data-ttu-id="6bebc-108">L’élément important à comprendre lors de la lecture d’un document est les idées que le document tente de transmettre, les idées qui apparaissent où et quelles sont les relations entre les idées.</span><span class="sxs-lookup"><span data-stu-id="6bebc-108">The important thing to understand from reading a document is the ideas that the document is trying to convey, which ideas appear where, and what the relationships between the ideas are.</span></span>

<span data-ttu-id="6bebc-109">Cela peut être étendu à la façon dont une personne souhaite consommer un ensemble de documents.</span><span class="sxs-lookup"><span data-stu-id="6bebc-109">This can be extended to how a person wants to consume a set of documents.</span></span> <span data-ttu-id="6bebc-110">Ils souhaitent voir quelles idées sont présentes dans les ensembles et quels documents les présentent.</span><span class="sxs-lookup"><span data-stu-id="6bebc-110">They want to see which ideas are present in the sets, and which documents are talking about those ideas.</span></span> <span data-ttu-id="6bebc-111">En outre, s’ils trouvent un document particulier intéressant, ils souhaitent être en mesure de voir des documents qui discutent d’idées similaires.</span><span class="sxs-lookup"><span data-stu-id="6bebc-111">Also, if they find a particular document of interest, they want to be able to see documents that discuss similar ideas.</span></span>

<span data-ttu-id="6bebc-112">La fonctionnalité Thèmes dans Advanced eDiscovery tente d’imiter la  raison humaine des documents, en analysant les thèmes abordés dans un jeu à réviser et en attribuant un thème aux documents du jeu à réviser.</span><span class="sxs-lookup"><span data-stu-id="6bebc-112">The Themes functionality in Advanced eDiscovery attempts to mimic how humans reason about documents, by analyzing the *themes* that are discussed in a review set and assigning a theme to documents in the review set.</span></span> <span data-ttu-id="6bebc-113">Dans Advanced eDiscovery, les thèmes vont plus loin et identifient le *thème dominant* dans chaque document.</span><span class="sxs-lookup"><span data-stu-id="6bebc-113">In Advanced eDiscovery, Themes goes one step further and identifies the *dominant theme* in each document.</span></span> <span data-ttu-id="6bebc-114">Le thème dominant est celui qui apparaît le plus souvent dans un document.</span><span class="sxs-lookup"><span data-stu-id="6bebc-114">The dominant theme is the one that appears the most often in a document.</span></span>

## <a name="how-does-themes-work"></a><span data-ttu-id="6bebc-115">Comment fonctionnent les thèmes ?</span><span class="sxs-lookup"><span data-stu-id="6bebc-115">How does Themes work?</span></span>

<span data-ttu-id="6bebc-116">La fonctionnalité Thèmes analyse les documents d’un jeu à réviser qui incluent du texte afin d’identifier les thèmes communs qui apparaissent dans tous les documents du jeu à réviser.</span><span class="sxs-lookup"><span data-stu-id="6bebc-116">The Themes functionality analyzes documents with text in a review set to parse out common themes that appear across all the documents in the review set.</span></span> <span data-ttu-id="6bebc-117">Advanced eDiscovery attribue les thèmes identifiés aux documents dans lesquels ils apparaissent.</span><span class="sxs-lookup"><span data-stu-id="6bebc-117">Advanced eDiscovery assigns those themes to the documents in which they appear.</span></span> <span data-ttu-id="6bebc-118">Il associe par ailleurs les thèmes aux mots utilisés dans les documents représentatifs du thème.</span><span class="sxs-lookup"><span data-stu-id="6bebc-118">It also labels each theme with the words used in the documents that are representative of the theme.</span></span> <span data-ttu-id="6bebc-119">Les documents pouvant contenir différents types de sujets, Advanced eDiscovery leur attribue souvent plusieurs thèmes.</span><span class="sxs-lookup"><span data-stu-id="6bebc-119">Because a document can contain various types of subject matter, Advanced eDiscovery often assigns multiple themes to documents.</span></span> <span data-ttu-id="6bebc-120">Le thème le plus évident dans un document est désigné comme thème dominant.</span><span class="sxs-lookup"><span data-stu-id="6bebc-120">The theme that appears most prominently in a document is designated as its dominant theme.</span></span>
