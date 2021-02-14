---
title: Gestionnaire de conformité Microsoft et R GDPR
f1.keywords:
- NOCSH
ms.author: robmazz
author: robmazz
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
ROBOTS: NOINDEX, NOFOLLOW
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Le Gestionnaire de conformité Microsoft est un outil gratuit d’évaluation des risques basé sur les flux de travail dans le portail d’approbation de services Microsoft. Le Gestionnaire de conformité vous permet de suivre, d’affecter et de vérifier les activités de conformité réglementaire liées aux services cloud de Microsoft.
ms.openlocfilehash: 69e6551620fb654cb09d46554e6e3c98b6a2fc60
ms.sourcegitcommit: 1c91b7b24537d0e54d484c3379043db53c1aea65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2020
ms.locfileid: "41595801"
---
# <a name="microsoft-compliance-manager-and-the-gdpr"></a><span data-ttu-id="32248-104">Gestionnaire de conformité Microsoft et R GDPR</span><span class="sxs-lookup"><span data-stu-id="32248-104">Microsoft Compliance Manager and the GDPR</span></span>

<span data-ttu-id="32248-105">Le règlement général sur la protection des données (R GDPR) adopté par l’Union européenne peut avoir un impact sur votre stratégie de conformité et rendre obligatoires des actions spécifiques pour gérer les informations utilisateur et client utilisées dans le Gestionnaire de conformité.</span><span class="sxs-lookup"><span data-stu-id="32248-105">The General Data Protection Regulation (GDPR) enacted by the European Union can impact your compliance strategy and mandate specific actions to manage user and customer information used in Compliance Manager.</span></span>

## <a name="user-privacy-settings"></a><span data-ttu-id="32248-106">Paramètres de confidentialité de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="32248-106">User Privacy settings</span></span>

<span data-ttu-id="32248-107">Certaines réglementations exigent qu’une organisation puisse supprimer les données de l’historique des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="32248-107">Certain regulations require that an organization must be able to delete user history data.</span></span> <span data-ttu-id="32248-108">Le Gestionnaire de conformité fournit **des fonctions de paramètres** de confidentialité utilisateur qui permettent aux administrateurs de :</span><span class="sxs-lookup"><span data-stu-id="32248-108">Compliance Manager provides **User Privacy Settings** functions that allow administrators to:</span></span>
  
- [<span data-ttu-id="32248-109">Rechercher un utilisateur</span><span class="sxs-lookup"><span data-stu-id="32248-109">Search for a user</span></span>](#search-for-a-user)
- [<span data-ttu-id="32248-110">Exporter le rapport de l’historique des données d’un compte</span><span class="sxs-lookup"><span data-stu-id="32248-110">Export a report of account data history</span></span>](#export-a-report-of-account-data-history)
- [<span data-ttu-id="32248-111">Supprimer l’historique des données d’un utilisateur</span><span class="sxs-lookup"><span data-stu-id="32248-111">Delete user data history</span></span>](#delete-user-data-history)
  
## <a name="search-for-a-user"></a><span data-ttu-id="32248-112">Rechercher un utilisateur</span><span class="sxs-lookup"><span data-stu-id="32248-112">Search for a user</span></span>

<span data-ttu-id="32248-113">Pour rechercher un compte d’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="32248-113">To search for a user account:</span></span>
  
1. <span data-ttu-id="32248-114">Entrez l’alias de messagerie de l’utilisateur (les informations à gauche du symbole @ ) et choisissez le nom de domaine dans la liste des suffixes de domaine à droite.</span><span class="sxs-lookup"><span data-stu-id="32248-114">Enter the user email alias (the information to the left of the @ symbol) and choose the domain name from the  domain suffix list on the right.</span></span> <span data-ttu-id="32248-115">Pour les organisations avec plusieurs domaines inscrits, vérifiez le suffixe du nom de domaine pour vous assurer qu’il est correct.</span><span class="sxs-lookup"><span data-stu-id="32248-115">For organizations with multiple registered domains, double check the domain name suffix to ensure that it is correct.</span></span>

2. <span data-ttu-id="32248-116">Lorsque vous avez entré correctement le nom d’utilisateur, sélectionnez **Rechercher.**</span><span class="sxs-lookup"><span data-stu-id="32248-116">When you have the username correctly entered, select **Search**.</span></span>

3. <span data-ttu-id="32248-117">Pour les comptes d’utilisateurs qui ne sont pas renvoyés, la page affiche **User in found**.</span><span class="sxs-lookup"><span data-stu-id="32248-117">For user accounts not returned, the page displays **User not found**.</span></span> <span data-ttu-id="32248-118">Vérifiez les informations de l’adresse e-mail de l’utilisateur et a corrections si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="32248-118">Check the user's email address information and make corrections as necessary.</span></span> <span data-ttu-id="32248-119">Pour réessayer, sélectionnez **Rechercher.**</span><span class="sxs-lookup"><span data-stu-id="32248-119">To retry, select **Search**.</span></span>

4. <span data-ttu-id="32248-120">Pour les comptes d’utilisateur renvoyés, le texte du bouton passe de **La** recherche à **Effacer.**</span><span class="sxs-lookup"><span data-stu-id="32248-120">For user accounts returned, the text of the button changes from **Search** to **Clear**.</span></span> <span data-ttu-id="32248-121">Cela indique que le compte d’utilisateur renvoyé est le contexte d’exploitation pour les fonctions supplémentaires et que ces fonctions s’appliquent à ce compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="32248-121">This indicates that the returned user account is the operating context for the additional functions and that these functions apply to this user account.</span></span>

5. <span data-ttu-id="32248-122">Pour effacer les résultats de recherche et rechercher un autre utilisateur, sélectionnez **Effacer.**</span><span class="sxs-lookup"><span data-stu-id="32248-122">To clear search results and search for a different user, select **Clear**.</span></span>

## <a name="export-a-report-of-account-data-history"></a><span data-ttu-id="32248-123">Exporter le rapport de l’historique des données d’un compte</span><span class="sxs-lookup"><span data-stu-id="32248-123">Export a report of account data history</span></span>

<span data-ttu-id="32248-124">Pour chaque compte d’utilisateur identifié, vous pouvez générer un rapport des dépendances liées au compte.</span><span class="sxs-lookup"><span data-stu-id="32248-124">For each user account identified, you can generate a report of dependencies linked to the account.</span></span> <span data-ttu-id="32248-125">Ces informations vous permettent de réaffecter les éléments d’action ouverts ou de garantir l’accès aux preuves précédemment téléchargées.</span><span class="sxs-lookup"><span data-stu-id="32248-125">This information allows you to reassign open Action Items or ensure access to previously uploaded evidence.</span></span>
  
 <span data-ttu-id="32248-126">Pour générer et exporter un rapport :</span><span class="sxs-lookup"><span data-stu-id="32248-126">To generate and export a report:</span></span>
  
1. <span data-ttu-id="32248-127">Sélectionnez **Exporter** pour générer et télécharger un rapport des éléments d’action de contrôle du Gestionnaire de conformité actuellement affectés au compte d’utilisateur renvoyé, ainsi que la liste des documents téléchargés par cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="32248-127">Select **Export** to generate and download a report of the Compliance Manager control Action Items currently assigned to the returned user account, and the list of documents uploaded by that user.</span></span> <span data-ttu-id="32248-128">S’il n’y a pas d’actions affectées ou de documents téléchargés, un message d’erreur indique « Aucune donnée pour cet utilisateur ».</span><span class="sxs-lookup"><span data-stu-id="32248-128">If there are no assigned actions or uploaded documents, an error message states "No data for this user".</span></span>

2. <span data-ttu-id="32248-129">Le rapport est téléchargé en arrière-plan de la fenêtre active du navigateur. Si vous ne voyez pas de fenêtre de téléchargement, vous souhaitez vérifier l’historique de téléchargement de votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="32248-129">The report downloads in the background of the active browser window — if you don't see a download popup that you want to check your browser download history.</span></span>

3. <span data-ttu-id="32248-130">Ouvrez le document pour consulter les données du rapport.</span><span class="sxs-lookup"><span data-stu-id="32248-130">Open the document to review the report data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="32248-131">Les données du rapport ne sont pas une liste historique qui conserve et affiche les modifications d’état apportées à l’historique d’affectation de l’élément d’action.</span><span class="sxs-lookup"><span data-stu-id="32248-131">The report data is not a historical list that retains and displays state changes to Action Item assignment history.</span></span> <span data-ttu-id="32248-132">Le rapport généré est un instantané des éléments d’action de contrôle affectés au moment de l’utilisation du rapport (date et horodaté écrits dans le rapport).</span><span class="sxs-lookup"><span data-stu-id="32248-132">The generated report is a snapshot of the control Action Items assigned at the time that the report is run (date and time stamp written into the report).</span></span> <span data-ttu-id="32248-133">Par exemple, toute réaffectation ultérieure des éléments d’action entraîne des données de rapport de capture instantanée différentes si le rapport est généré à nouveau pour le même utilisateur.</span><span class="sxs-lookup"><span data-stu-id="32248-133">For example, any subsequent reassignment of Action Items result in different snapshot report data if the report is generated again for the same user.</span></span>
  
## <a name="delete-user-data-history"></a><span data-ttu-id="32248-134">Supprimer l’historique des données d’un utilisateur</span><span class="sxs-lookup"><span data-stu-id="32248-134">Delete user data history</span></span>

<span data-ttu-id="32248-135">Définit tous les éléments d’action de contrôle affectés à l’utilisateur renvoyé sur « non affecté ».</span><span class="sxs-lookup"><span data-stu-id="32248-135">Sets all control Action Items assigned to the returned user to 'unassigned'.</span></span> <span data-ttu-id="32248-136">Définit la **valeur téléchargée par valeur** pour tous les documents téléchargés par l’utilisateur renvoyé sur « utilisateur supprimé ».</span><span class="sxs-lookup"><span data-stu-id="32248-136">Sets the **uploaded by** value for any documents uploaded by the returned user to 'user removed'.</span></span>
  
<span data-ttu-id="32248-137">Pour supprimer l’élément d’action du compte d’utilisateur et l’historique de chargement du document :</span><span class="sxs-lookup"><span data-stu-id="32248-137">To delete the user account Action Item and document upload history:</span></span>
  
1. <span data-ttu-id="32248-138">Sélectionnez **Supprimer**.</span><span class="sxs-lookup"><span data-stu-id="32248-138">Select **Delete**.</span></span>

    <span data-ttu-id="32248-139">Une boîte de dialogue de confirmation s’affiche : « Cette action supprime toutes les affectations d’élément d’action de contrôle et l’historique de téléchargement de *document pour l’utilisateur sélectionné. Cette action est permanente. Voulez-vous vraiment continuer ?*»</span><span class="sxs-lookup"><span data-stu-id="32248-139">A confirmation dialog is displayed: "*This removes all control Action Item assignments and the document upload history for the selected user. This action is permanent. Are you sure you want to continue?*"</span></span>

2. <span data-ttu-id="32248-140">Pour continuer, **sélectionnez OK,** sinon **sélectionnez Annuler.**</span><span class="sxs-lookup"><span data-stu-id="32248-140">To continue select **OK**, otherwise select **Cancel**.</span></span>
