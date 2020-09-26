---
title: Détection quasi-doublons-eDiscovery
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
description: Utilisez la détection presque en double pour regrouper des documents textuellement similaires lors de l’analyse des données de cas dans Advanced eDiscovery.
ms.custom: seo-marvel-mar2020
ms.openlocfilehash: 255531897a1706904005034c56cab00d0032b7f3
ms.sourcegitcommit: 2160e7cf373f992dd4d11793a59cb8c44f8d587e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/26/2020
ms.locfileid: "48286020"
---
# <a name="near-duplicate-detection-in-advanced-ediscovery"></a><span data-ttu-id="d3dea-103">Quasi-détection des doublons dans Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="d3dea-103">Near duplicate detection in Advanced eDiscovery</span></span>

<span data-ttu-id="d3dea-104">Considérez un ensemble de documents à examiner dans lequel un sous-ensemble est basé sur le même modèle et qui possède essentiellement le même langage, avec quelques différences ici et là.</span><span class="sxs-lookup"><span data-stu-id="d3dea-104">Consider a set of documents to be reviewed in which a subset is based on the same template and has mostly the same boilerplate language, with a few differences here and there.</span></span> <span data-ttu-id="d3dea-105">Si un réviseur peut identifier ce sous-ensemble, passer en revue l’une d’entre elles de façon approfondie et passer en revue les différences pour le reste, il n’aurait pas manqué d’informations uniques pendant une période de temps qui aurait été utilisée pour lire tous les documents.</span><span class="sxs-lookup"><span data-stu-id="d3dea-105">If a reviewer could identify this subset, review one of them thoroughly, and review the differences for the rest, they would not have missed any unique information while taking only a fraction of time that would have taken them to read all documents cover to cover.</span></span> <span data-ttu-id="d3dea-106">La détection des quasi-doublons regroupe les documents textuellement similaires afin de renforcer l’efficacité du processus d’examen.</span><span class="sxs-lookup"><span data-stu-id="d3dea-106">Near duplicate detection groups textually similar documents together to help you make your review process more efficient.</span></span>

## <a name="how-does-it-work"></a><span data-ttu-id="d3dea-107">Comment cela fonctionne-t-il ?</span><span class="sxs-lookup"><span data-stu-id="d3dea-107">How does it work?</span></span>

<span data-ttu-id="d3dea-108">Lorsqu’il procède à la détection des quasi-doublons, le système analyse tous les documents contenant du texte.</span><span class="sxs-lookup"><span data-stu-id="d3dea-108">When near duplicate detection is run, the system parses every document with text.</span></span> <span data-ttu-id="d3dea-109">Il les compare ensuite afin de déterminer si leur niveau de similarité est supérieur à un seuil défini.</span><span class="sxs-lookup"><span data-stu-id="d3dea-109">Then, it compares every document against each other to determine whether their similarity is greater than the set threshold.</span></span> <span data-ttu-id="d3dea-110">Si c’est le cas, les documents sont regroupés.</span><span class="sxs-lookup"><span data-stu-id="d3dea-110">If it is, the documents are grouped together.</span></span> <span data-ttu-id="d3dea-111">Une fois tous les documents comparés et regroupés, un document de chaque groupe est désigné comme « pivot ». Lorsque vous procédez par la suite à l’examen des documents, vous pouvez commencer par le pivot avant de vous pencher sur les autres documents du groupe de quasi-doublons, en vous attachant à chaque fois à repérer la différence entre le pivot et l’autre document examiné.</span><span class="sxs-lookup"><span data-stu-id="d3dea-111">Once all documents have been compared and grouped, a document from each group is marked as the "pivot"; in reviewing your documents, you can review a pivot first and review the other documents in the same near duplicate set, focusing on the difference between the pivot and the document that is in review.</span></span>
