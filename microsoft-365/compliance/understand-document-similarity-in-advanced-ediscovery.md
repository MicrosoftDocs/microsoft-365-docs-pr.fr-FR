---
title: Comprendre la similarité des documents dans Advanced eDiscovery
f1.keywords:
- NOCSH
ms.author: chrfox
author: chrfox
manager: laurawi
titleSuffix: Office 365
ms.date: 09/14/2017
audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 4d4cb381-4c9a-4165-a455-609d525c7a88
description: 'Examinez la valeur similarité des documents, le niveau de ressemblance minimal entre deux fichiers à considérer comme des doublons, fonctionne dans Advanced eDiscovery. '
ms.openlocfilehash: bfce2e3018c690fc0a25bcda8e2c03690a334dc4
ms.sourcegitcommit: 2614f8b81b332f8dab461f4f64f3adaa6703e0d6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2020
ms.locfileid: "43633409"
---
# <a name="understand-document-similarity-in-advanced-ediscovery-classic"></a><span data-ttu-id="b05fa-103">Comprendre la similarité des documents dans Advanced eDiscovery (classique)</span><span class="sxs-lookup"><span data-stu-id="b05fa-103">Understand document similarity in Advanced eDiscovery (classic)</span></span>

> [!NOTE]
> <span data-ttu-id="b05fa-p101">Pour utiliser Advanced eDiscovery, votre organisation doit souscrire un abonnement Office 365 E3 avec le module complémentaire Conformité avancée ou un abonnement E5. Si vous ne disposez pas d’un abonnement et que vous souhaitez essayer Advanced eDiscovery, vous pouvez vous [inscrire pour utiliser une version d’évaluation d’Office 365 Entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="b05fa-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="b05fa-106">Dans Advanced eDiscovery, la similarité des documents est le niveau minimal de ressemblance nécessaire pour que deux documents soient considérés comme des doublons.</span><span class="sxs-lookup"><span data-stu-id="b05fa-106">In Advanced eDiscovery, Document Similarity is the minimal level of resemblance required for two documents to be considered as near-duplicates.</span></span>
  
> [!TIP]
> <span data-ttu-id="b05fa-107">Pour la plupart des applications d’entreprise, il est recommandé d’utiliser une valeur de similarité de 60%-75%.</span><span class="sxs-lookup"><span data-stu-id="b05fa-107">For most business applications, it is recommended to use a Similarity value of 60%-75%.</span></span> <span data-ttu-id="b05fa-108">Pour une grande qualité de la reconnaissance optique des caractères (OCR), il est possible d’appliquer des valeurs inférieures.</span><span class="sxs-lookup"><span data-stu-id="b05fa-108">For very poor quality optical character recognition (OCR) material, lower Similarity values can be applied.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="b05fa-109">Après avoir été définie et exécutée pour un cas donné, la valeur de similarité ne peut pas être modifiée.</span><span class="sxs-lookup"><span data-stu-id="b05fa-109">After it's set and run for a given case, the Similarity value cannot be changed.</span></span> 
  
<span data-ttu-id="b05fa-110">Dans un jeu near-Duplicate (ND), il peut y avoir des documents avec un niveau de ressemblance sous le seuil de similarité.</span><span class="sxs-lookup"><span data-stu-id="b05fa-110">Within a Near-duplicate (ND) set, there may be documents with a level of resemblance below the Similarity threshold.</span></span> <span data-ttu-id="b05fa-111">Pour qu’un document rejoigne un jeu de type ND, il doit y avoir au moins un document dans le paramètre ND avec un niveau de ressemblance dépassant la similarité.</span><span class="sxs-lookup"><span data-stu-id="b05fa-111">For a document to join an ND set, there must be at least one document in the ND set with a level of resemblance exceeding the Similarity.</span></span> 
  
<span data-ttu-id="b05fa-112">Par exemple, supposons que la similarité est définie sur 80%, le document F1 ressemble au document F2 à un niveau de 85% et le document F2 ressemble à un document F3 de 90%.</span><span class="sxs-lookup"><span data-stu-id="b05fa-112">For example, assume the Similarity is set to 80%, document F1 resembles document F2 at a level of 85%, and document F2 resembles document F3 at a level of 90%.</span></span> 
  
<span data-ttu-id="b05fa-113">Toutefois, le document F1 peut ressembler à un document de F3 dont le niveau est de seulement 70%, ce qui est inférieur au seuil.</span><span class="sxs-lookup"><span data-stu-id="b05fa-113">However, document F1 may resemble document F3 at a level of only 70%, which is below the threshold.</span></span> <span data-ttu-id="b05fa-114">Néanmoins, dans cet exemple, les documents F1, F2 et F3 s’affichent dans la plage ND.</span><span class="sxs-lookup"><span data-stu-id="b05fa-114">Nonetheless, in this example, documents F1, F2, and F3 all appear in the one ND set.</span></span> <span data-ttu-id="b05fa-115">De même, à l’aide d’une valeur de similarité de 80%, nous pouvons avoir créé deux jeux, EquiSet-1 et EquiSet-2.</span><span class="sxs-lookup"><span data-stu-id="b05fa-115">Similarly, using a Similarity value of 80%, we may have created two sets, EquiSet-1 and EquiSet-2.</span></span> <span data-ttu-id="b05fa-116">EquiSet-1 contient les documents E1 et E2.</span><span class="sxs-lookup"><span data-stu-id="b05fa-116">EquiSet-1 contains documents E1 and E2.</span></span> <span data-ttu-id="b05fa-117">Equiset-2 contient les documents F1, F2 et F3.</span><span class="sxs-lookup"><span data-stu-id="b05fa-117">Equiset-2 contains documents F1, F2, and F3.</span></span> 
  
<span data-ttu-id="b05fa-118">Les niveaux de ressemblance sont illustrés comme suit :</span><span class="sxs-lookup"><span data-stu-id="b05fa-118">The levels of resemblance are illustrated as follows:</span></span>
  
![Similitude du document](../media/3907ea7d-e28a-4027-8fc3-be090dd39144.gif)
  
<span data-ttu-id="b05fa-120">Supposons qu’un autre document, x1, est maintenant inséré.</span><span class="sxs-lookup"><span data-stu-id="b05fa-120">Assume that another document, X1, is now inserted.</span></span> <span data-ttu-id="b05fa-121">La ressemblance entre x1 et E3 est de 87%.</span><span class="sxs-lookup"><span data-stu-id="b05fa-121">The resemblance between X1 and E3 is 87%.</span></span> <span data-ttu-id="b05fa-122">De même, la ressemblance entre x1 et F1 est de 92%.</span><span class="sxs-lookup"><span data-stu-id="b05fa-122">Similarly, the resemblance between X1 and F1 is 92%.</span></span> <span data-ttu-id="b05fa-123">Par conséquent, EquiSet-1, EquiSet-2 et x1 sont désormais combinés en un seul jeu ND.</span><span class="sxs-lookup"><span data-stu-id="b05fa-123">As a result, EquiSet -1, EquiSet -2, and X1 are now combined into one ND set.</span></span>
  
![Similitude du document](../media/d140d347-33d5-475a-af04-594a0f2ab13d.gif)
  
> [!NOTE]
> <span data-ttu-id="b05fa-125">Si deux documents sont affectés à un seul jeu, ils restent ensemble dans le même ensemble ND, même si des documents supplémentaires sont ajoutés à l’ensemble ou si les jeux sont fusionnés.</span><span class="sxs-lookup"><span data-stu-id="b05fa-125">If any two documents are assigned to one ND set, they will remain together in the same ND set, even if additional documents are added to the set or if the sets are merged.</span></span> 
  
<span data-ttu-id="b05fa-126">Une fois les ensembles fusionnés, le document croisé dynamique peut changer lorsque de nouveaux documents sont ajoutés à un jeu.</span><span class="sxs-lookup"><span data-stu-id="b05fa-126">After sets are merged, the Pivot document can change when new documents are added to a set.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b05fa-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b05fa-127">See also</span></span>

[<span data-ttu-id="b05fa-128">Advanced eDiscovery (classique)</span><span class="sxs-lookup"><span data-stu-id="b05fa-128">Advanced eDiscovery (classic)</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="b05fa-129">Définition des options d’analyse</span><span class="sxs-lookup"><span data-stu-id="b05fa-129">Setting Analyze options</span></span>](set-analyze-options-in-advanced-ediscovery.md)
  
[<span data-ttu-id="b05fa-130">Définition d’un texte ignoré</span><span class="sxs-lookup"><span data-stu-id="b05fa-130">Setting ignore text</span></span>](set-ignore-text-in-advanced-ediscovery.md)
  
[<span data-ttu-id="b05fa-131">Définition des paramètres avancés d’analyse</span><span class="sxs-lookup"><span data-stu-id="b05fa-131">Setting Analyze advanced settings</span></span>](set-analyze-advanced-settings-in-advanced-ediscovery.md)
  
[<span data-ttu-id="b05fa-132">Affichage des résultats de l’analyse</span><span class="sxs-lookup"><span data-stu-id="b05fa-132">Viewing Analyze results</span></span>](view-analyze-results-in-advanced-ediscovery.md)

