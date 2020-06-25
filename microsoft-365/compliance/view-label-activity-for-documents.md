---
title: Afficher l’activité liée aux étiquettes des documents
f1.keywords:
- NOCSH
ms.author: cabailey
author: cabailey
manager: laurawi
ms.date: 5/9/2018
audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.collection:
- M365-security-compliance
- SPO_Content
localization_priority: Priority
search.appverid:
- MOE150
- MET150
ms.custom: seo-marvel-apr2020
description: Découvrez comment utiliser l’Explorateur des activités d’étiquettes dans le Centre de conformité et de sécurité Microsoft 365 pour rechercher et consulter l’activité des étiquettes.
ms.openlocfilehash: 9cf505575a17c8f6eb4d48e609d358f9c988965f
ms.sourcegitcommit: 973f5449784cb70ce5545bc3cf57bf1ce5209218
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2020
ms.locfileid: "44819024"
---
# <a name="view-label-activity-for-documents"></a><span data-ttu-id="651c6-103">Afficher l’activité liée aux étiquettes des documents</span><span class="sxs-lookup"><span data-stu-id="651c6-103">View label activity for documents</span></span>

<span data-ttu-id="651c6-104">After you create your labels, you'll want to verify that they're being applied to content as you intended.</span><span class="sxs-lookup"><span data-stu-id="651c6-104">After you create your labels, you'll want to verify that they're being applied to content as you intended.</span></span> <span data-ttu-id="651c6-105">With the Label Activity Explorer in the Security &amp; Compliance Center, you can quickly search and view label activity for all content across SharePoint and OneDrive for Business over the past 30 days.</span><span class="sxs-lookup"><span data-stu-id="651c6-105">With the Label Activity Explorer in the Security &amp; Compliance Center, you can quickly search and view label activity for all content across SharePoint and OneDrive for Business over the past 30 days.</span></span> <span data-ttu-id="651c6-106">This is real-time data that gives you a clear view into what's happening in your tenant.</span><span class="sxs-lookup"><span data-stu-id="651c6-106">This is real-time data that gives you a clear view into what's happening in your tenant.</span></span>
  
<span data-ttu-id="651c6-107">Par exemple, avec l’Explorateur d’activité des étiquettes, vous pouvez effectuer les actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="651c6-107">For example, with the Label Activity Explorer, you can:</span></span>
  
- <span data-ttu-id="651c6-108">Afficher le nombre de fois où chaque étiquette a été appliquée chaque jour (jusqu’à 30 jours).</span><span class="sxs-lookup"><span data-stu-id="651c6-108">View how many times each label was applied on each day (up to 30 days).</span></span>
    
- <span data-ttu-id="651c6-109">Voir l’utilisateur qui a étiqueté un fichier spécifique et à quelle date, ainsi qu’un lien vers le site où se trouve ce fichier.</span><span class="sxs-lookup"><span data-stu-id="651c6-109">See who labeled exactly which file on which date, along with a link to the site where that file resides.</span></span>
    
- <span data-ttu-id="651c6-110">Afficher les fichiers dont les étiquettes ont été modifiées ou supprimées, les anciennes et nouvelles étiquettes, ainsi que la personne qui a effectué la modification.</span><span class="sxs-lookup"><span data-stu-id="651c6-110">View which files had labels changed or removed, what the old and new labels are, and who made the change.</span></span>
    
- <span data-ttu-id="651c6-111">Filter the data to see all the label activity for a specific label, file, or user.</span><span class="sxs-lookup"><span data-stu-id="651c6-111">Filter the data to see all the label activity for a specific label, file, or user.</span></span> <span data-ttu-id="651c6-112">You can also filter label activity by location (SharePoint or OneDrive for Business) and whether the label was applied manually or auto-applied.</span><span class="sxs-lookup"><span data-stu-id="651c6-112">You can also filter label activity by location (SharePoint or OneDrive for Business) and whether the label was applied manually or auto-applied.</span></span>
    
- <span data-ttu-id="651c6-113">View label activity for folders as well as individual documents.</span><span class="sxs-lookup"><span data-stu-id="651c6-113">View label activity for folders as well as individual documents.</span></span> <span data-ttu-id="651c6-114">Coming soon is the ability to show how many files inside that folder got labeled as a result of the folder getting labeled.</span><span class="sxs-lookup"><span data-stu-id="651c6-114">Coming soon is the ability to show how many files inside that folder got labeled as a result of the folder getting labeled.</span></span>
    
<span data-ttu-id="651c6-115">Vous trouverez l’explorateur d’activité des étiquettes dans le Centre de sécurité &amp; conformité > **Gouvernance des informations** > **Explorateur d’activité des étiquettes**.</span><span class="sxs-lookup"><span data-stu-id="651c6-115">You can find the Label Activity Explorer in the Security &amp; Compliance Center > **Information governance** > **Label activity explorer**.</span></span>
  
<span data-ttu-id="651c6-116">Notez que l’Explorateur d’activité des étiquettes requiert un abonnement Office 365 Entreprise E5.</span><span class="sxs-lookup"><span data-stu-id="651c6-116">Note that the Label Activity Explorer requires an Office 365 Enterprise E5 subscription.</span></span>
  
![Explorateur d’activité des étiquettes](../media/671ca0cd-1457-40b4-9917-b663360afd95.png)
  
## <a name="view-label-activities-for-files-or-folders"></a><span data-ttu-id="651c6-118">Afficher les activités des étiquettes pour les fichiers ou les dossiers</span><span class="sxs-lookup"><span data-stu-id="651c6-118">View label activities for files or folders</span></span>

<span data-ttu-id="651c6-119">At the top of the Label Activity Explorer, you can choose whether to view activities for files or folders.</span><span class="sxs-lookup"><span data-stu-id="651c6-119">At the top of the Label Activity Explorer, you can choose whether to view activities for files or folders.</span></span> <span data-ttu-id="651c6-120">Note that folder activity includes only the folder itself, not the files inside the folder.</span><span class="sxs-lookup"><span data-stu-id="651c6-120">Note that folder activity includes only the folder itself, not the files inside the folder.</span></span>
  
<span data-ttu-id="651c6-121">You might want to see label activity for folders because if you label a folder, all files inside that folder also get that label (except for files that have had a label applied explicitly to them).</span><span class="sxs-lookup"><span data-stu-id="651c6-121">You might want to see label activity for folders because if you label a folder, all files inside that folder also get that label (except for files that have had a label applied explicitly to them).</span></span> <span data-ttu-id="651c6-122">Therefore, labeling folders might affect a significant number of files.</span><span class="sxs-lookup"><span data-stu-id="651c6-122">Therefore, labeling folders might affect a significant number of files.</span></span> <span data-ttu-id="651c6-123">For more information, see [Applying a default retention label to all content in a SharePoint library, folder, or document set](labels.md#applying-a-default-retention-label-to-all-content-in-a-sharepoint-library-folder-or-document-set).</span><span class="sxs-lookup"><span data-stu-id="651c6-123">For more information, see [Applying a default retention label to all content in a SharePoint library, folder, or document set](labels.md#applying-a-default-retention-label-to-all-content-in-a-sharepoint-library-folder-or-document-set).</span></span>
  
![Menu déroulant affichant les activités des étiquettes pour les fichiers et les dossiers](../media/11030584-f52d-49eb-86f3-7ead16a3b704.png)
  
### <a name="label-activities"></a><span data-ttu-id="651c6-125">Activités des étiquettes</span><span class="sxs-lookup"><span data-stu-id="651c6-125">Label activities</span></span>

 <span data-ttu-id="651c6-126">**Label activities** includes all label actions: **adding**, **removing**, or **changing** a label.</span><span class="sxs-lookup"><span data-stu-id="651c6-126">**Label activities** includes all label actions: **adding**, **removing**, or **changing** a label.</span></span> <span data-ttu-id="651c6-127">You can use this view to get a comprehensive look at how many files each label's been applied to per day.</span><span class="sxs-lookup"><span data-stu-id="651c6-127">You can use this view to get a comprehensive look at how many files each label's been applied to per day.</span></span> 
  
### <a name="label-changes"></a><span data-ttu-id="651c6-128">Modifications des étiquettes</span><span class="sxs-lookup"><span data-stu-id="651c6-128">Label changes</span></span>

 <span data-ttu-id="651c6-129">**Label changes** includes the potentially risky actions of **removing** or **changing** a label.</span><span class="sxs-lookup"><span data-stu-id="651c6-129">**Label changes** includes the potentially risky actions of **removing** or **changing** a label.</span></span> <span data-ttu-id="651c6-130">You can use this view to quickly see such risky actions and the user who performed them.</span><span class="sxs-lookup"><span data-stu-id="651c6-130">You can use this view to quickly see such risky actions and the user who performed them.</span></span> <span data-ttu-id="651c6-131">In the activity list below the chart, you can select a file, and then click a link to that file in the details pane on the right.</span><span class="sxs-lookup"><span data-stu-id="651c6-131">In the activity list below the chart, you can select a file, and then click a link to that file in the details pane on the right.</span></span> 
  
![Volet d’informations de l’activité des étiquettes](../media/eb580fd4-b5be-4fda-9ba5-c1256777310d.png)
  
## <a name="filter-label-activity"></a><span data-ttu-id="651c6-133">Filtre de l’activité des étiquettes</span><span class="sxs-lookup"><span data-stu-id="651c6-133">Filter label activity</span></span>

<span data-ttu-id="651c6-134">You can quickly filter the data to see all the label activity for a specific label, file, or user.</span><span class="sxs-lookup"><span data-stu-id="651c6-134">You can quickly filter the data to see all the label activity for a specific label, file, or user.</span></span> <span data-ttu-id="651c6-135">You can also filter label activity by location (SharePoint or OneDrive for Business) and whether the label was applied manually or auto-applied.</span><span class="sxs-lookup"><span data-stu-id="651c6-135">You can also filter label activity by location (SharePoint or OneDrive for Business) and whether the label was applied manually or auto-applied.</span></span>
  
![Filtres de l’activité des étiquettes](../media/9de92985-120f-48b4-96a7-ef7ec8a71ff0.png)
  

