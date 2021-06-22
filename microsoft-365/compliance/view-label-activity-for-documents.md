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
ms.openlocfilehash: e21bb867044b2a6644b125aad9983ce3518f70ee
ms.sourcegitcommit: 4d26a57c37ff7efbb8d235452c78498b06a59714
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/22/2021
ms.locfileid: "53053338"
---
# <a name="view-label-activity-for-documents"></a><span data-ttu-id="600c1-103">Afficher l’activité liée aux étiquettes des documents</span><span class="sxs-lookup"><span data-stu-id="600c1-103">View label activity for documents</span></span>

<span data-ttu-id="600c1-p101">Après avoir créé vos étiquettes, vérifiez qu’elles sont appliquées au contenu comme vous le souhaitez. Avec l’Explorateur d’activité des étiquettes dans le Centre de sécurité &amp; et conformité, vous pouvez rapidement rechercher et afficher l’activité des étiquettes pour tout le contenu au sein de SharePoint et OneDrive Entreprise au cours des 30 derniers jours. Il s’agit des données en temps réel qui vous offrent une bonne visibilité de ce qui se passe dans votre client.</span><span class="sxs-lookup"><span data-stu-id="600c1-p101">After you create your labels, you'll want to verify that they're being applied to content as you intended. With the Label Activity Explorer in the Security &amp; Compliance Center, you can quickly search and view label activity for all content across SharePoint and OneDrive for Business over the past 30 days. This is real-time data that gives you a clear view into what's happening in your tenant.</span></span>
  
<span data-ttu-id="600c1-107">Par exemple, avec l’Explorateur d’activité des étiquettes, vous pouvez effectuer les actions suivantes :</span><span class="sxs-lookup"><span data-stu-id="600c1-107">For example, with the Label Activity Explorer, you can:</span></span>
  
- <span data-ttu-id="600c1-108">Afficher le nombre de fois où chaque étiquette a été appliquée chaque jour (jusqu’à 30 jours).</span><span class="sxs-lookup"><span data-stu-id="600c1-108">View how many times each label was applied on each day (up to 30 days).</span></span>
    
- <span data-ttu-id="600c1-109">Voir l’utilisateur qui a étiqueté un fichier spécifique et à quelle date, ainsi qu’un lien vers le site où se trouve ce fichier.</span><span class="sxs-lookup"><span data-stu-id="600c1-109">See who labeled exactly which file on which date, along with a link to the site where that file resides.</span></span>
    
- <span data-ttu-id="600c1-110">Afficher les fichiers dont les étiquettes ont été modifiées ou supprimées, les anciennes et nouvelles étiquettes, ainsi que la personne qui a effectué la modification.</span><span class="sxs-lookup"><span data-stu-id="600c1-110">View which files had labels changed or removed, what the old and new labels are, and who made the change.</span></span>
    
- <span data-ttu-id="600c1-p102">Filtrer les données afin d’afficher toute l’activité liée à une étiquette, un fichier ou un utilisateur spécifique. Vous pouvez également filtrer l’activité liée aux étiquettes par emplacement (SharePoint ou OneDrive Entreprise) et voir si l’étiquette a été appliquée manuellement ou automatiquement.</span><span class="sxs-lookup"><span data-stu-id="600c1-p102">Filter the data to see all the label activity for a specific label, file, or user. You can also filter label activity by location (SharePoint or OneDrive for Business) and whether the label was applied manually or auto-applied.</span></span>
    
- <span data-ttu-id="600c1-p103">Consulter l’activité des étiquettes pour des dossiers ainsi que des documents individuels. Vous pourrez bientôt afficher le nombre de fichiers de ce dossier ayant été étiquetés suite à l’étiquetage du dossier en question.</span><span class="sxs-lookup"><span data-stu-id="600c1-p103">View label activity for folders as well as individual documents. Coming soon is the ability to show how many files inside that folder got labeled as a result of the folder getting labeled.</span></span>
    
<span data-ttu-id="600c1-115">Vous trouverez l’explorateur d’activité des étiquettes dans le Centre de sécurité &amp; conformité > **Gouvernance des informations** > **Explorateur d’activité des étiquettes**.</span><span class="sxs-lookup"><span data-stu-id="600c1-115">You can find the Label Activity Explorer in the Security &amp; Compliance Center > **Information governance** > **Label activity explorer**.</span></span>
  
<span data-ttu-id="600c1-116">Notez que l’Explorateur d’activité des étiquettes requiert un abonnement Office 365 Entreprise E5.</span><span class="sxs-lookup"><span data-stu-id="600c1-116">Note that the Label Activity Explorer requires an Office 365 Enterprise E5 subscription.</span></span>
  
![Explorateur d’activité des étiquettes](../media/671ca0cd-1457-40b4-9917-b663360afd95.png)
  
## <a name="view-label-activities-for-files-or-folders"></a><span data-ttu-id="600c1-118">Afficher les activités des étiquettes pour les fichiers ou les dossiers</span><span class="sxs-lookup"><span data-stu-id="600c1-118">View label activities for files or folders</span></span>

<span data-ttu-id="600c1-p104">En haut de l’Explorateur d’activité des étiquettes, vous pouvez choisir d’afficher les activités pour les fichiers ou les dossiers. Notez que l’activité des dossiers inclut uniquement le dossier lui-même, pas les fichiers contenus dans le dossier.</span><span class="sxs-lookup"><span data-stu-id="600c1-p104">At the top of the Label Activity Explorer, you can choose whether to view activities for files or folders. Note that folder activity includes only the folder itself, not the files inside the folder.</span></span>
  
<span data-ttu-id="600c1-p105">Vous voudrez peut-être consulter l’activité des étiquettes pour les dossiers, car si vous étiquetez un dossier, tous les fichiers contenus dans ce dossier sont également étiquetés (à l’exception des fichiers ayant été étiquetés spécifiquement). Par conséquent, l’étiquetage des dossiers risque d’affecter un certain nombre de fichiers. Pour obtenir plus d’informations, consultez la rubrique [Application d’une étiquette de rétention par défaut à tout le contenu d’une bibliothèque, d’un dossier ou d’un ensemble de documents SharePoint](create-apply-retention-labels.md#applying-a-default-retention-label-to-all-content-in-a-sharepoint-library-folder-or-document-set).</span><span class="sxs-lookup"><span data-stu-id="600c1-p105">You might want to see label activity for folders because if you label a folder, all files inside that folder also get that label (except for files that have had a label applied explicitly to them). Therefore, labeling folders might affect a significant number of files. For more information, see [Applying a default retention label to all content in a SharePoint library, folder, or document set](create-apply-retention-labels.md#applying-a-default-retention-label-to-all-content-in-a-sharepoint-library-folder-or-document-set).</span></span>
  
![Menu déroulant affichant les activités des étiquettes pour les fichiers et les dossiers](../media/11030584-f52d-49eb-86f3-7ead16a3b704.png)
  
### <a name="label-activities"></a><span data-ttu-id="600c1-125">Activités des étiquettes</span><span class="sxs-lookup"><span data-stu-id="600c1-125">Label activities</span></span>

 <span data-ttu-id="600c1-p106">L’affichage **Activités des étiquettes** inclut toutes les actions relatives aux étiquettes : **ajout**, **suppression** ou **modification** d’une étiquette. Vous pouvez utiliser cet affichage pour obtenir une vue complète du nombre de fichiers auxquels une étiquette a été appliquée par jour.</span><span class="sxs-lookup"><span data-stu-id="600c1-p106">**Label activities** includes all label actions: **adding**, **removing**, or **changing** a label. You can use this view to get a comprehensive look at how many files each label's been applied to per day.</span></span> 
  
### <a name="label-changes"></a><span data-ttu-id="600c1-128">Modifications des étiquettes</span><span class="sxs-lookup"><span data-stu-id="600c1-128">Label changes</span></span>

 <span data-ttu-id="600c1-p107">L’affichage **Modifications des étiquettes** inclut les actions potentiellement risquées de **suppression** ou de **modification** d’une étiquette. Vous pouvez utiliser cet affichage pour consulter rapidement ces actions risquées et l’utilisateur qui les a effectuées. Dans la liste des activités située sous le graphique, vous pouvez sélectionner un fichier, puis cliquer sur un lien vers ce fichier dans le volet d’informations situé à droite.</span><span class="sxs-lookup"><span data-stu-id="600c1-p107">**Label changes** includes the potentially risky actions of **removing** or **changing** a label. You can use this view to quickly see such risky actions and the user who performed them. In the activity list below the chart, you can select a file, and then click a link to that file in the details pane on the right.</span></span> 
  
![Volet d’informations de l’activité des étiquettes](../media/eb580fd4-b5be-4fda-9ba5-c1256777310d.png)
  
## <a name="filter-label-activity"></a><span data-ttu-id="600c1-133">Filtre de l’activité des étiquettes</span><span class="sxs-lookup"><span data-stu-id="600c1-133">Filter label activity</span></span>

<span data-ttu-id="600c1-p108">Vous pouvez rapidement filtrer les données pour afficher toutes les activités des étiquettes pour une étiquette, un fichier ou un utilisateur en particulier. Vous pouvez également filtrer l’activité des étiquettes par emplacement (SharePoint ou OneDrive Entreprise) et si l’étiquette a été appliquée manuellement ou automatiquement.</span><span class="sxs-lookup"><span data-stu-id="600c1-p108">You can quickly filter the data to see all the label activity for a specific label, file, or user. You can also filter label activity by location (SharePoint or OneDrive for Business) and whether the label was applied manually or auto-applied.</span></span>
  
![Filtres de l’activité des étiquettes](../media/9de92985-120f-48b4-96a7-ef7ec8a71ff0.png)
  

