---
title: Afficher les résultats de l’analyse dans Office 365 Advanced eDiscovery
f1.keywords:
- NOCSH
ms.author: chrfox
author: chrfox
manager: laurawi
titleSuffix: Office 365
ms.date: 9/14/2017
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 5974f3c2-89fe-4c5f-ac7b-57f214437f7e
description: 'Comprendre où afficher les résultats du processus d’analyse dans Office 365 Advanced eDiscovery, y compris les définitions des options de tâche affichées.  '
ms.openlocfilehash: adee00d2b7826827cc14f4ca945952f4892511a1
ms.sourcegitcommit: e741930c41abcde61add22d4b773dbf171ed72ac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/07/2020
ms.locfileid: "42557622"
---
# <a name="view-analyze-results-in-advanced-ediscovery-classic"></a><span data-ttu-id="7c8cb-103">Afficher les résultats de l’analyse dans Advanced eDiscovery (classique)</span><span class="sxs-lookup"><span data-stu-id="7c8cb-103">View Analyze results in Advanced eDiscovery (classic)</span></span>

> [!NOTE]
> <span data-ttu-id="7c8cb-p101">Pour utiliser Advanced eDiscovery, votre organisation doit souscrire un abonnement Office 365 E3 avec le module complémentaire Conformité avancée ou un abonnement E5. Si vous ne disposez pas d’un abonnement et que vous souhaitez essayer Advanced eDiscovery, vous pouvez vous [inscrire pour utiliser une version d’évaluation d’Office 365 Entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="7c8cb-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="7c8cb-106">Dans Advanced eDiscovery, la progression et les résultats du processus d’analyse peuvent être affichés dans un grand nombre d’écrans, comme décrit ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="7c8cb-106">In Advanced eDiscovery, progress and results for the Analyze process can be viewed in a variety of displays as described below.</span></span>
  
## <a name="view-analyze-task-status"></a><span data-ttu-id="7c8cb-107">Afficher l’état de la tâche d’analyse</span><span class="sxs-lookup"><span data-stu-id="7c8cb-107">View Analyze task status</span></span>

<span data-ttu-id="7c8cb-108">Dans **préparer \> l' \> analyse \> des résultats**de la tâche, l’État est affiché pendant et après l’exécution de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="7c8cb-108">In **Prepare \> Analyze \> Results \> Task status**, the status is displayed during and after Analyze process execution.</span></span> 
  
![Analyser l’état des tâches](../media/d0372978-ce08-4f4e-a1fc-aa918ae44364.png)
  
<span data-ttu-id="7c8cb-110">Les tâches affichées peuvent varier en fonction des options sélectionnées.</span><span class="sxs-lookup"><span data-stu-id="7c8cb-110">The tasks displayed may vary depending on the options selected.</span></span> 
  
- <span data-ttu-id="7c8cb-111">**ND/et : configuration**: prépare l’exécution, par exemple, définit les paramètres Run et case.</span><span class="sxs-lookup"><span data-stu-id="7c8cb-111">**ND/ET: setup**: Prepares for the run, for example, sets run and case parameters.</span></span>
    
- <span data-ttu-id="7c8cb-112">**ND/tout : calcul de ND**: traite les analyses de fichiers presque en double.</span><span class="sxs-lookup"><span data-stu-id="7c8cb-112">**ND/ET: ND calculation**: Processes Near-duplicate analysis of files.</span></span>
    
- <span data-ttu-id="7c8cb-113">**ND/et : et calcul**: effectue une analyse des threads de messagerie sur l’ensemble du message.</span><span class="sxs-lookup"><span data-stu-id="7c8cb-113">**ND/ET: ET calculation**: Performs Email Thread analysis on the entire email set.</span></span>
    
- <span data-ttu-id="7c8cb-114">**ND/et : tableaux croisés dynamiques et similitudes**: effectue un traitement de type tableau croisé dynamique et similarité des fichiers.</span><span class="sxs-lookup"><span data-stu-id="7c8cb-114">**ND/ET: pivots and similarities**: Performs pivot and file similarity processing.</span></span>
    
- <span data-ttu-id="7c8cb-115">**ND/et : mise à jour des métadonnées**: finalise les nouvelles données collectées sur les fichiers de la base de données.</span><span class="sxs-lookup"><span data-stu-id="7c8cb-115">**ND/ET: metadata update**: Finalizes the new data collected on the files in the database.</span></span>
    
- <span data-ttu-id="7c8cb-116">**Themes : calculation des thèmes**: exécute l’analyse des thèmes.</span><span class="sxs-lookup"><span data-stu-id="7c8cb-116">**Themes: themes calculation**: Runs themes analysis.</span></span> <span data-ttu-id="7c8cb-117">(Affiché uniquement s’il est sélectionné.)</span><span class="sxs-lookup"><span data-stu-id="7c8cb-117">(Displayed only if selected.)</span></span>
    
- <span data-ttu-id="7c8cb-118">**État**de la tâche : cette ligne s’affiche une fois la tâche terminée.</span><span class="sxs-lookup"><span data-stu-id="7c8cb-118">**Task status**: This line is displayed after task completion.</span></span> <span data-ttu-id="7c8cb-119">Pendant l’exécution des tâches, la durée de l’exécution s’affiche.</span><span class="sxs-lookup"><span data-stu-id="7c8cb-119">While tasks are running, run duration is displayed.</span></span>
    
> [!NOTE]
> <span data-ttu-id="7c8cb-120">Les résultats d’analyse des doublons et des threads de messagerie (ND et ED) s’appliquent au nombre de documents à traiter.</span><span class="sxs-lookup"><span data-stu-id="7c8cb-120">The Analyze results of Near-duplicates and Email Threads (ND and ED) applies to the number of documents to be processed.</span></span> <span data-ttu-id="7c8cb-121">Il n’inclut pas les fichiers en double exact.</span><span class="sxs-lookup"><span data-stu-id="7c8cb-121">It does not include Exact duplicate files.</span></span> 
  
## <a name="view-near-duplicates-and-email-threads-status"></a><span data-ttu-id="7c8cb-122">Afficher l’état des doublons et des threads de messagerie</span><span class="sxs-lookup"><span data-stu-id="7c8cb-122">View Near-duplicates and Email Threads status</span></span>

<span data-ttu-id="7c8cb-123">Les résultats de la population **cible** affichent le nombre de documents, d’e-mails, de pièces jointes et d’erreurs dans la population cible.</span><span class="sxs-lookup"><span data-stu-id="7c8cb-123">The **Target** population results display the number of documents, emails, attachments, and errors in the target population.</span></span> 
  
<span data-ttu-id="7c8cb-124">Les résultats des **documents** affichent le nombre de tableaux croisés dynamiques, de doublons uniques et de fichiers en double exact.</span><span class="sxs-lookup"><span data-stu-id="7c8cb-124">The **Documents** results display the number of pivots, unique near-duplicates, and exact duplicate files.</span></span> 
  
<span data-ttu-id="7c8cb-125">Les résultats des **courriers électroniques** affichent le nombre de copies inclusives, inclusives et non incluses, ainsi que le reste des messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="7c8cb-125">The **Emails** results display the number of inclusive, inclusive minus, unique inclusive copies, and the rest of the email messages.</span></span> <span data-ttu-id="7c8cb-126">Les différents types de résultats de messagerie sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="7c8cb-126">The different types of email results are:</span></span> 
  
- <span data-ttu-id="7c8cb-127">**Inclus**: un message électronique Inclusive est le nœud de terminaison dans un fil de messagerie et contient l’historique précédent de ce thread.</span><span class="sxs-lookup"><span data-stu-id="7c8cb-127">**Inclusive**: An inclusive email is the terminating node in an email thread and contains all the previous history of that thread.</span></span> <span data-ttu-id="7c8cb-128">Par conséquent, le réviseur peut se concentrer en toute sécurité sur le courrier inclusif, sans avoir à lire les messages précédents dans le fil de discussion.</span><span class="sxs-lookup"><span data-stu-id="7c8cb-128">As a result, the reviewer can safely focus on the inclusive email, without the need to read the previous messages in the thread.</span></span> 
    
- <span data-ttu-id="7c8cb-129">**Moins inclusive**: un message électronique inclusif est désigné sous la forme non inclusive, moins s’il y a une ou plusieurs pièces jointes différentes associées aux parents du message inclusif.</span><span class="sxs-lookup"><span data-stu-id="7c8cb-129">**Inclusive minus**: An inclusive email is designated as inclusive minus if there are one or more different attachments associated with the parents of the inclusive message.</span></span> <span data-ttu-id="7c8cb-130">Dans ce contexte, le terme parent est utilisé pour les messages situés vers le haut sur le thread de courrier électronique ou les conversations incluses dans ce message électronique inclus spécifique.</span><span class="sxs-lookup"><span data-stu-id="7c8cb-130">In this context, the term Parent is used for messages located upwards on the email thread or conversations included in that specific inclusive email.</span></span> <span data-ttu-id="7c8cb-131">Un réviseur peut utiliser l’indication moins inclusive comme un signal qui, bien qu’il ne soit pas nécessaire de revoir le contenu des parents du courrier électronique inclus, il peut être utile de vérifier les pièces jointes associées aux parents de chemin d’accès inclusifs.</span><span class="sxs-lookup"><span data-stu-id="7c8cb-131">A reviewer can use the inclusive minus indication as a signal that although it might not be necessary to review the content of the inclusive email parents, it may be useful to review the attachments associated with the inclusive path parents.</span></span> 
    
- <span data-ttu-id="7c8cb-132">**Copie inclusive**: un message électronique inclusif est désigné comme copie inclusive s’il s’agit de la copie d’un autre message marqué comme étant inclusive ou inclusive.</span><span class="sxs-lookup"><span data-stu-id="7c8cb-132">**Inclusive copy**: An inclusive email is designated as inclusive copy if it's the copy of another message marked as inclusive or inclusive minus.</span></span> <span data-ttu-id="7c8cb-133">En d’autres termes, ce message a le même objet et le même corps qu’un autre message inclusif et, en tant que tel, réside dans le même nœud.</span><span class="sxs-lookup"><span data-stu-id="7c8cb-133">In other words, this message has the same subject and body as another inclusive message and, as such, co-resides in the same node.</span></span> <span data-ttu-id="7c8cb-134">Étant donné que les messages de copie inclusive contiennent le même contenu, ils peuvent généralement être ignorés lors du processus de révision.</span><span class="sxs-lookup"><span data-stu-id="7c8cb-134">Because inclusive copy messages contain the same content, they can usually be skipped in the review process.</span></span> 
    
- <span data-ttu-id="7c8cb-135">**Le reste**: indique qu’il s’agit d’un courrier électronique qui ne contient pas de contenu unique et, par conséquent, qu’il n’est pas inclus dans les trois catégories précédentes.</span><span class="sxs-lookup"><span data-stu-id="7c8cb-135">**The rest**: This indicates email that doesn't contain any unique content, and therefore doesn't fall into any of the previous three categories.</span></span> <span data-ttu-id="7c8cb-136">Ces messages électroniques n’ont pas besoin d’être vérifiés.</span><span class="sxs-lookup"><span data-stu-id="7c8cb-136">These email messages don't need to be reviewed.</span></span> <span data-ttu-id="7c8cb-137">Si un message contient une pièce jointe qui ne se trouve pas dans un message électronique plus inclusive, il se peut que la pièce jointe doive être révisée.</span><span class="sxs-lookup"><span data-stu-id="7c8cb-137">If a message contains an attachment that isn't on a later inclusive email, then the attachment might need to be reviewed.</span></span> <span data-ttu-id="7c8cb-138">Cela est indiqué par l’existence d’un courrier inclusif moins le message dans le fil de discussion.</span><span class="sxs-lookup"><span data-stu-id="7c8cb-138">This is indicated by the existence of an inclusive minus email within the thread.</span></span>
    
<span data-ttu-id="7c8cb-139">Les résultats des **pièces jointes** affichent le nombre de pièces jointes, en fonction de ce type comme uniques et des doublons.</span><span class="sxs-lookup"><span data-stu-id="7c8cb-139">The **Attachments** results display the number of attachments, according to such type as unique and duplicates.</span></span> 
  
![Doublons à proximité et Threads de messagerie](../media/54491303-0ee3-4739-b42e-d1ee486842fd.png)
  
## <a name="see-also"></a><span data-ttu-id="7c8cb-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7c8cb-141">See also</span></span>

[<span data-ttu-id="7c8cb-142">Découverte électronique avancée (classique)</span><span class="sxs-lookup"><span data-stu-id="7c8cb-142">Advanced eDiscovery (classic)</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="7c8cb-143">Présentation de la similarité des documents</span><span class="sxs-lookup"><span data-stu-id="7c8cb-143">Understanding document similarity</span></span>](understand-document-similarity-in-advanced-ediscovery.md)
  
[<span data-ttu-id="7c8cb-144">Définition des options d’analyse</span><span class="sxs-lookup"><span data-stu-id="7c8cb-144">Setting Analyze options</span></span>](set-analyze-options-in-advanced-ediscovery.md)
  
[<span data-ttu-id="7c8cb-145">Définition d’un texte ignoré</span><span class="sxs-lookup"><span data-stu-id="7c8cb-145">Setting ignore text</span></span>](set-ignore-text-in-advanced-ediscovery.md)
  
[<span data-ttu-id="7c8cb-146">Définition des paramètres avancés d’analyse</span><span class="sxs-lookup"><span data-stu-id="7c8cb-146">Setting Analyze advanced settings</span></span>](view-analyze-results-in-advanced-ediscovery.md)

