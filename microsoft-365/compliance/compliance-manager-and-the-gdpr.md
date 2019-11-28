---
title: Gestionnaire de conformité Microsoft et RGPD
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
description: Le gestionnaire de conformité Microsoft est un outil d’évaluation des risques gratuit basé sur un flux de travail dans le portail d’approbation de service Microsoft. Le gestionnaire de conformité vous permet de suivre, d’affecter et de vérifier les activités de conformité réglementaire liées aux services Cloud de Microsoft.
ms.openlocfilehash: 0d2edb2f7362fa8e8bea6ae82c417f61072bccff
ms.sourcegitcommit: e386037c9cc335c86896dc153344850735afbccd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/27/2019
ms.locfileid: "39633613"
---
# <a name="microsoft-compliance-manager-and-the-gdpr"></a><span data-ttu-id="39f44-104">Gestionnaire de conformité Microsoft et RGPD</span><span class="sxs-lookup"><span data-stu-id="39f44-104">Microsoft Compliance Manager and the GDPR</span></span>

<span data-ttu-id="39f44-105">Le règlement général sur la protection des données (RGPD), traité par l’Union européenne, peut avoir un impact sur votre stratégie de conformité et imposer des actions spécifiques pour gérer les informations utilisateur et client utilisées dans le gestionnaire de conformité.</span><span class="sxs-lookup"><span data-stu-id="39f44-105">The General Data Protection Regulation (GDPR) enacted by the European Union can impact your compliance strategy and mandate specific actions to manage user and customer information used in Compliance Manager.</span></span>

## <a name="user-privacy-settings"></a><span data-ttu-id="39f44-106">Paramètres de confidentialité de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="39f44-106">User Privacy settings</span></span>

<span data-ttu-id="39f44-107">Dans certaines réglementations, une organisation doit être en mesure de supprimer les données d’historique de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="39f44-107">Certain regulations require that an organization must be able to delete user history data.</span></span> <span data-ttu-id="39f44-108">Le gestionnaire de conformité fournit des fonctions de **paramètres de confidentialité** de l’utilisateur qui permettent aux administrateurs :</span><span class="sxs-lookup"><span data-stu-id="39f44-108">Compliance Manager provides **User Privacy Settings** functions that allow administrators to:</span></span>
  
- [<span data-ttu-id="39f44-109">Rechercher un utilisateur</span><span class="sxs-lookup"><span data-stu-id="39f44-109">Search for a user</span></span>](#search-for-a-user)
- [<span data-ttu-id="39f44-110">Exporter le rapport de l’historique des données d’un compte</span><span class="sxs-lookup"><span data-stu-id="39f44-110">Export a report of account data history</span></span>](#export-a-report-of-account-data-history)
- [<span data-ttu-id="39f44-111">Supprimer l’historique des données d’un utilisateur</span><span class="sxs-lookup"><span data-stu-id="39f44-111">Delete user data history</span></span>](#delete-user-data-history)
  
## <a name="search-for-a-user"></a><span data-ttu-id="39f44-112">Rechercher un utilisateur</span><span class="sxs-lookup"><span data-stu-id="39f44-112">Search for a user</span></span>

<span data-ttu-id="39f44-113">Pour rechercher un compte d’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="39f44-113">To search for a user account:</span></span>
  
1. <span data-ttu-id="39f44-114">Entrez l’alias de messagerie de l’utilisateur (les informations à gauche du symbole @) et choisissez le nom de domaine dans la liste de suffixe de domaine à droite.</span><span class="sxs-lookup"><span data-stu-id="39f44-114">Enter the user email alias (the information to the left of the @ symbol) and choose the domain name from the  domain suffix list on the right.</span></span> <span data-ttu-id="39f44-115">Pour les organisations disposant de plusieurs domaines inscrits, vérifiez que le suffixe du nom de domaine est correct.</span><span class="sxs-lookup"><span data-stu-id="39f44-115">For organizations with multiple registered domains, double check the domain name suffix to ensure that it is correct.</span></span>

2. <span data-ttu-id="39f44-116">Une fois le nom d’utilisateur correctement entré, sélectionnez **recherche**.</span><span class="sxs-lookup"><span data-stu-id="39f44-116">When you have the username correctly entered, select **Search**.</span></span>

3. <span data-ttu-id="39f44-117">Pour les comptes d’utilisateur qui ne sont pas renvoyés, la page affiche « **utilisateur introuvable**».</span><span class="sxs-lookup"><span data-stu-id="39f44-117">For user accounts not returned, the page displays **User not found**.</span></span> <span data-ttu-id="39f44-118">Vérifiez les informations de l’adresse de messagerie de l’utilisateur et effectuez les corrections nécessaires.</span><span class="sxs-lookup"><span data-stu-id="39f44-118">Check the user's email address information and make corrections as necessary.</span></span> <span data-ttu-id="39f44-119">Pour réessayer, sélectionnez **recherche**.</span><span class="sxs-lookup"><span data-stu-id="39f44-119">To retry, select **Search**.</span></span>

4. <span data-ttu-id="39f44-120">Pour les comptes d’utilisateur renvoyés, le texte du bouton passe de la **recherche** à **Effacer**.</span><span class="sxs-lookup"><span data-stu-id="39f44-120">For user accounts returned, the text of the button changes from **Search** to **Clear**.</span></span> <span data-ttu-id="39f44-121">Cela indique que le compte d’utilisateur renvoyé est le contexte d’exploitation pour les fonctions supplémentaires et que ces fonctions s’appliquent à ce compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="39f44-121">This indicates that the returned user account is the operating context for the additional functions and that these functions apply to this user account.</span></span>

5. <span data-ttu-id="39f44-122">Pour effacer les résultats de la recherche et Rechercher un autre utilisateur, sélectionnez **Effacer**.</span><span class="sxs-lookup"><span data-stu-id="39f44-122">To clear search results and search for a different user, select **Clear**.</span></span>

## <a name="export-a-report-of-account-data-history"></a><span data-ttu-id="39f44-123">Exporter le rapport de l’historique des données d’un compte</span><span class="sxs-lookup"><span data-stu-id="39f44-123">Export a report of account data history</span></span>

<span data-ttu-id="39f44-124">Pour chaque compte d’utilisateur identifié, vous pouvez générer un rapport des dépendances liées au compte.</span><span class="sxs-lookup"><span data-stu-id="39f44-124">For each user account identified, you can generate a report of dependencies linked to the account.</span></span> <span data-ttu-id="39f44-125">Ces informations vous permettent de réaffecter des éléments d’action ouverts ou de vous assurer de l’accès à des preuves précédemment téléchargées.</span><span class="sxs-lookup"><span data-stu-id="39f44-125">This information allows you to reassign open Action Items or ensure access to previously uploaded evidence.</span></span>
  
 <span data-ttu-id="39f44-126">Pour générer et exporter un rapport :</span><span class="sxs-lookup"><span data-stu-id="39f44-126">To generate and export a report:</span></span>
  
1. <span data-ttu-id="39f44-127">Sélectionnez **Exporter** pour générer et télécharger un rapport des éléments d’action de contrôle du gestionnaire de conformité actuellement attribués au compte d’utilisateur renvoyé, ainsi que la liste des documents téléchargés par cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="39f44-127">Select **Export** to generate and download a report of the Compliance Manager control Action Items currently assigned to the returned user account, and the list of documents uploaded by that user.</span></span> <span data-ttu-id="39f44-128">S’il n’y a pas d’actions affectées ou de documents téléchargés, un message d’erreur indique « pas de données pour cet utilisateur ».</span><span class="sxs-lookup"><span data-stu-id="39f44-128">If there are no assigned actions or uploaded documents, an error message states "No data for this user".</span></span>

2. <span data-ttu-id="39f44-129">Le rapport est téléchargé en arrière-plan de la fenêtre active du navigateur — si vous ne voyez pas de menu contextuel de téléchargement dans lequel vous souhaitez vérifier l’historique de téléchargement de votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="39f44-129">The report downloads in the background of the active browser window — if you don't see a download popup that you want to check your browser download history.</span></span>

3. <span data-ttu-id="39f44-130">Ouvrez le document pour consulter les données du rapport.</span><span class="sxs-lookup"><span data-stu-id="39f44-130">Open the document to review the report data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="39f44-131">Les données de rapport ne sont pas une liste historique qui conserve et affiche les modifications d’État apportées à l’historique des affectations d’éléments d’action.</span><span class="sxs-lookup"><span data-stu-id="39f44-131">The report data is not a historical list that retains and displays state changes to Action Item assignment history.</span></span> <span data-ttu-id="39f44-132">Le rapport généré est une capture instantanée des éléments d’action de contrôle affectés lors de l’exécution du rapport (horodatage écrit dans le rapport).</span><span class="sxs-lookup"><span data-stu-id="39f44-132">The generated report is a snapshot of the control Action Items assigned at the time that the report is run (date and time stamp written into the report).</span></span> <span data-ttu-id="39f44-133">Par exemple, toute réaffectation ultérieure d’éléments d’action entraîne des données de rapport de capture instantanée différentes si le rapport est régénéré pour le même utilisateur.</span><span class="sxs-lookup"><span data-stu-id="39f44-133">For example, any subsequent reassignment of Action Items result in different snapshot report data if the report is generated again for the same user.</span></span>
  
## <a name="delete-user-data-history"></a><span data-ttu-id="39f44-134">Supprimer l’historique des données d’un utilisateur</span><span class="sxs-lookup"><span data-stu-id="39f44-134">Delete user data history</span></span>

<span data-ttu-id="39f44-135">Définit tous les éléments d’action de contrôle affectés à l’utilisateur renvoyé comme étant « non attribué ».</span><span class="sxs-lookup"><span data-stu-id="39f44-135">Sets all control Action Items assigned to the returned user to 'unassigned'.</span></span> <span data-ttu-id="39f44-136">Définit la valeur **chargée par** pour tous les documents téléchargés par l’utilisateur retourné sur « utilisateur supprimé ».</span><span class="sxs-lookup"><span data-stu-id="39f44-136">Sets the **uploaded by** value for any documents uploaded by the returned user to 'user removed'.</span></span>
  
<span data-ttu-id="39f44-137">Pour supprimer l’élément d’action du compte d’utilisateur et l’historique de chargement des documents :</span><span class="sxs-lookup"><span data-stu-id="39f44-137">To delete the user account Action Item and document upload history:</span></span>
  
1. <span data-ttu-id="39f44-138">Sélectionnez **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="39f44-138">Select **Delete**.</span></span>

    <span data-ttu-id="39f44-139">Une boîte de dialogue de confirmation s’affiche : «*cette option supprime toutes les affectations d’éléments d’action de contrôle et l’historique de téléchargement de documents de l’utilisateur sélectionné. Cette action est permanente. Êtes-vous sûr de vouloir continuer ?*</span><span class="sxs-lookup"><span data-stu-id="39f44-139">A confirmation dialog is displayed: "*This removes all control Action Item assignments and the document upload history for the selected user. This action is permanent. Are you sure you want to continue?*"</span></span>

2. <span data-ttu-id="39f44-140">Pour continuer, sélectionnez **OK**, sinon cliquez sur **Annuler**.</span><span class="sxs-lookup"><span data-stu-id="39f44-140">To continue select **OK**, otherwise select **Cancel**.</span></span>
