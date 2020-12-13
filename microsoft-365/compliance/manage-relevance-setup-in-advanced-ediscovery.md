---
title: Gestion de la configuration de Pertinence dans Advanced eDiscovery
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
titleSuffix: Office 365
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MOE150
- MET150
ms.assetid: fd6be6d3-2e8d-449d-9851-03ab7546e6aa
description: Lisez les recommandations pour configurer l’entraînement Pertinence dans Advanced eDiscovery pour qu’il note les fichiers selon leur pertinence et génère des résultats.
ms.openlocfilehash: a6bec149e11fa80fb57cb811120218fa7f2cc45b
ms.sourcegitcommit: 47de4402174c263ae8d70c910ca068a7581d04ae
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "49662869"
---
# <a name="manage-relevance-setup-in-advanced-ediscovery-classic"></a><span data-ttu-id="f16bb-103">Gestion de la configuration de Pertinence dans Advanced eDiscovery (classique)</span><span class="sxs-lookup"><span data-stu-id="f16bb-103">Manage Relevance setup in Advanced eDiscovery (classic)</span></span>

> [!NOTE]
> <span data-ttu-id="f16bb-p101">Pour utiliser Advanced eDiscovery, votre organisation doit souscrire un abonnement Office 365 E3 avec le module complémentaire Conformité avancée ou un abonnement E5. Si vous ne disposez pas d’un abonnement et que vous souhaitez essayer Advanced eDiscovery, vous pouvez vous [inscrire pour utiliser une version d’évaluation d’Office 365 Entreprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="f16bb-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
 <span data-ttu-id="f16bb-p102">La technologie Pertinence d’Advanced eDiscovery emploie des logiciels utilisés par des experts pour noter les fichiers selon leur pertinence. Elle peut être utilisée dans les processus d’évaluation rapide des cas, de sélection et de révision des échantillons de fichier.</span><span class="sxs-lookup"><span data-stu-id="f16bb-p102">Advanced eDiscovery Relevance technology employs expert-guided software for scoring files by their relevance. Advanced eDiscovery Relevance can be used for Early Case Assessment (ECA), culling, and file sample review.</span></span> 
  
 <span data-ttu-id="f16bb-p103">Advanced eDiscovery comprend des composants adaptés à l’entraînement Pertinence et à l’étiquetage des fichiers liés à un cas. Il collecte des informations sur les échantillons de fichiers pertinents et non pertinents entraînés pour noter chaque fichier selon leur pertinence, puis il génère des résultats qui peuvent servir pendant et après le processus de révision des fichiers.</span><span class="sxs-lookup"><span data-stu-id="f16bb-p103">Advanced eDiscovery includes components for the Relevance training and tagging of files relevant to a case. Advanced eDiscovery learns from the trained samples of Relevant and Not Relevant files to provide Relevance scores for each file, and generates analytical results that can be used during and after the file review process.</span></span> 
  
## <a name="guidelines-for-setting-up-relevance-training"></a><span data-ttu-id="f16bb-110">Conseils de configuration de l’entraînement Pertinence</span><span class="sxs-lookup"><span data-stu-id="f16bb-110">Guidelines for setting up Relevance training</span></span>

 <span data-ttu-id="f16bb-p104">Dans Advanced eDiscovery, dans la fenêtre **Cas**, sélectionnez un cas et cliquez sur **Atteindre le cas**. Cliquez sur **Pertinence** \> **Installation de Pertinence**. Suivez ces conseils pour configurer Pertinence.</span><span class="sxs-lookup"><span data-stu-id="f16bb-p104">In Advance eDiscovery, in the **Cases** window, select a case and click **Go to case**. Click **Relevance** \> **Relevance setup**. Follow these recommended guidelines to set up Relevance.</span></span> 
  
- <span data-ttu-id="f16bb-114">**Étiquetage** : l’efficacité du processus d’entraînement itératif Pertinence dépend de la capacité de l’expert à étiqueter les échantillons de fichier avec précision et cohérence.</span><span class="sxs-lookup"><span data-stu-id="f16bb-114">**Tagging**: The effectiveness of the iterative Relevance training process is dependent on the ability of the expert to tag the file samples with precision and consistency.</span></span>

- <span data-ttu-id="f16bb-115">**Sujets des cas** :</span><span class="sxs-lookup"><span data-stu-id="f16bb-115">**Case issues**:</span></span>
  
  - <span data-ttu-id="f16bb-p105">Pour chaque sujet, faites appel au même expert tout au long de l’entraînement Pertinence. Plusieurs experts ne peuvent pas étiqueter le même sujet en même temps.</span><span class="sxs-lookup"><span data-stu-id="f16bb-p105">For each issue, use the same expert throughout the entire Relevance training process. Simultaneous tagging of the same issue by multiple experts is not permitted.</span></span>
  
  - <span data-ttu-id="f16bb-118">Déterminez si chaque groupe de fichiers est pertinent par rapport à un sujet spécifique.</span><span class="sxs-lookup"><span data-stu-id="f16bb-118">Determine if each group of files is pertinent only to a specific issue.</span></span>

  - <span data-ttu-id="f16bb-p106">Si un sujet est défini de façon trop générale, Advanced eDiscovery peut générer un nombre excessif de fichiers non pertinents. Si un sujet est défini de façon trop restrictive, le processus d’entraînement Pertinence peut durer plus longtemps.</span><span class="sxs-lookup"><span data-stu-id="f16bb-p106">If an issue is defined too generally, Advanced eDiscovery may yield too many files that are not relevant. If an issue is defined too narrowly, the Relevance training process may take more time.</span></span> 

  - <span data-ttu-id="f16bb-121">À chaque cycle d’entraînement Pertinence, Advanced eDiscovery se concentre sur un seul sujet actif et des exemples de résultats temporaires sont affichés.</span><span class="sxs-lookup"><span data-stu-id="f16bb-121">During each Relevance training cycle, Advanced eDiscovery focuses on a single active issue and interim sample results are displayed accordingly.</span></span>

  - <span data-ttu-id="f16bb-p107">Dans un scénario à sujets multiples, le mode Échantillonnage permet de sélectionner des sujets à inclure dans le processus. Les sujets marqués « Inactif » ne sont pas traités tant que le mode Échantillonnage n’est pas modifié. Un sujet peut apparaître « Inactif » ou « Actif » pour un seul expert.</span><span class="sxs-lookup"><span data-stu-id="f16bb-p107">In a multiple-issue scenario, the Sampling mode enables the selection of issues to be included in processing. Issues defined as "off" are not handled until their Sampling mode is changed. An issue can be "idle" or "on" for only one expert.</span></span>

  - <span data-ttu-id="f16bb-p108">Advanced eDiscovery peut servir à générer des fichiers de privilège des candidats. Configurez un autre sujet selon son privilège. Si possible, entraînez et sélectionnez les fichiers selon leur pertinence, puis entraînez les fichiers selon leur privilège parmi les fichiers sélectionnés uniquement (rechargez les fichiers sélectionnés dans un cas distinct).</span><span class="sxs-lookup"><span data-stu-id="f16bb-p108">Advanced eDiscovery can be used to generate candidate privilege files. Set up a separate issue for privilege. If possible, train and cull for relevance first, and then train for privilege on the culled set only (reload the culled set as a separate case).</span></span> 

  - <span data-ttu-id="f16bb-p109">Vous pouvez uniquement effectuer un traitement par lots si aucun échantillon n’est ouvert (quand vous cliquez sur Traitement par lots, une liste d’utilisateurs contenant des échantillons ouverts s’affiche). Un administrateur peut « fermer » les échantillons d’autres utilisateurs (seulement si ces utilisateurs ne sont pas en train d’étiqueter ces échantillons), en utilisant l’utilitaire « Modifier la pertinence » avec l’option « Tous les échantillons des utilisateurs ».</span><span class="sxs-lookup"><span data-stu-id="f16bb-p109">Batch calculation can be performed only when there are no open samples (when clicking Batch Calculation, there will be a list displayed of users with open samples). To "close" samples of other users (this should be performed only if these users are not tagging these samples), an Administrator can use the "Modify relevance" utility with the "All users sample" option.</span></span>

- <span data-ttu-id="f16bb-p110">**Métadonnées** : Advanced eDiscovery se concentre sur le contenu. Il ne tient pas compte des métadonnées dans les critères de pertinence.</span><span class="sxs-lookup"><span data-stu-id="f16bb-p110">**Metadata**: Advanced eDiscovery focuses on content. It does not consider metadata as part of the relevance criteria.</span></span>

- <span data-ttu-id="f16bb-132">**Richesse** : si la richesse d’un sujet est inférieure à 3 % après évaluation, prévoyez d’alimenter l’entraînement Pertinence avec des fichiers pertinents et non pertinents connus.</span><span class="sxs-lookup"><span data-stu-id="f16bb-132">**Richness**: If the Richness for an issue is less than 3% after Assessment, consider seeding the Relevance training with known Relevant and Not Relevant files.</span></span>

- <span data-ttu-id="f16bb-p111">**Taille de fichier** : les fichiers volumineux (plus de 5 242 880 caractères de texte extrait) sont ignorés dans Pertinence. Ces fichiers ne participent pas au processus d’entraînement Pertinence et ne reçoivent pas de note de pertinence après le traitement par lots. Les fichiers de plus de 5 Mo peuvent être inclus dans le jeu d’évaluation.</span><span class="sxs-lookup"><span data-stu-id="f16bb-p111">**File size**: Large files (over 5,242,880 characters of extracted text) are ignored in Relevance. The files do not participate in the Relevance training process and do not receive a Relevance score after Batch Calculation. Files over 5 MB can be included in the Assessment set.</span></span>

## <a name="setting-up-case-issues"></a><span data-ttu-id="f16bb-136">Configuration des sujets des cas</span><span class="sxs-lookup"><span data-stu-id="f16bb-136">Setting up case issues</span></span>

<span data-ttu-id="f16bb-137">Les paramètres décrits dans cette section sont disponibles dans Advanced eDiscovery **Pertinence** \> **Configuration de Pertinence**.</span><span class="sxs-lookup"><span data-stu-id="f16bb-137">The parameters described in this section are available in the Advanced eDiscovery **Relevance** \> **Relevance setup**.</span></span>
  
- <span data-ttu-id="f16bb-138">Les sujets doivent être affectés à un utilisateur qui entraînera les fichiers.</span><span class="sxs-lookup"><span data-stu-id="f16bb-138">Issues must be assigned to a user who will train the files.</span></span>

- <span data-ttu-id="f16bb-139">Les fichiers importés doivent ensuite être ajoutés au chargement en cours de traitement.</span><span class="sxs-lookup"><span data-stu-id="f16bb-139">Imported files must then be added to the load being processed.</span></span>

- <span data-ttu-id="f16bb-140">Définissez et organisez les sujets attentivement, car cela peut influer sur les résultats de l’entraînement Pertinence.</span><span class="sxs-lookup"><span data-stu-id="f16bb-140">Define and organize issues carefully, as this can impact the Relevance training results.</span></span>

<span data-ttu-id="f16bb-141">Une fois les paramètres définis, le réviseur-expert peut commencer à entraîner les fichiers dans l’onglet **Pertinence**.</span><span class="sxs-lookup"><span data-stu-id="f16bb-141">After parameters are set, the reviewer / expert can start training the files in the **Relevance** tab.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f16bb-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f16bb-142">See also</span></span>

[<span data-ttu-id="f16bb-143">Advanced eDiscovery (classique)</span><span class="sxs-lookup"><span data-stu-id="f16bb-143">Advanced eDiscovery (classic)</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="f16bb-144">Définition des sujets et affectation des utilisateurs</span><span class="sxs-lookup"><span data-stu-id="f16bb-144">Defining issues and assigning users</span></span>](define-issues-and-assign-users.md)
  
[<span data-ttu-id="f16bb-145">Configuration des chargements pour ajouter des fichiers importés</span><span class="sxs-lookup"><span data-stu-id="f16bb-145">Setting up loads to add imported files</span></span>](set-up-loads-to-add-imported-files.md)
  
[<span data-ttu-id="f16bb-146">Définition des mots clés surlignés et des options avancées</span><span class="sxs-lookup"><span data-stu-id="f16bb-146">Defining highlighted keywords and advanced options</span></span>](define-highlighted-keywords-and-advanced-options.md)

