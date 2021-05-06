---
title: Gestionnaire de conformité Microsoft et RGPD
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
description: Le Gestionnaire de conformité Microsoft est un outil gratuit d’évaluation des risques des flux de travail disponible dans le Portail d’approbation de services de Microsoft. Le Gestionnaire de conformité vous permet de suivre, d’affecter et de vérifier les activités de mise en conformité réglementaires liées aux services de cloud computing Microsoft.
ms.openlocfilehash: 69e6551620fb654cb09d46554e6e3c98b6a2fc60
ms.sourcegitcommit: 1c91b7b24537d0e54d484c3379043db53c1aea65
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2020
ms.locfileid: "41595801"
---
# <a name="microsoft-compliance-manager-and-the-gdpr"></a><span data-ttu-id="867db-104">Gestionnaire de conformité Microsoft et RGPD</span><span class="sxs-lookup"><span data-stu-id="867db-104">Microsoft Compliance Manager and the GDPR</span></span>

<span data-ttu-id="867db-105">Le Règlement général sur la protection des données (RGPD) adopté par l’Union européenne peut affecter votre stratégie de conformité et peut rendre obligatoire des actions spécifiques pour gérer les informations client et utilisateur utilisées dans le Gestionnaire de conformité.</span><span class="sxs-lookup"><span data-stu-id="867db-105">The General Data Protection Regulation (GDPR) enacted by the European Union can impact your compliance strategy and mandate specific actions to manage user and customer information used in Compliance Manager.</span></span>

## <a name="user-privacy-settings"></a><span data-ttu-id="867db-106">Paramètres de confidentialité de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="867db-106">User Privacy settings</span></span>

<span data-ttu-id="867db-107">Certaines réglementations exigent qu’une organisation puisse supprimer les données de l’historique d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="867db-107">Certain regulations require that an organization must be able to delete user history data.</span></span> <span data-ttu-id="867db-108">Le Gestionnaire de conformité fournit des fonctionnalités, les **Paramètres de confidentialité de l’utilisateur**, qui permettent aux administrateurs d’effectuer ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="867db-108">Compliance Manager provides **User Privacy Settings** functions that allow administrators to:</span></span>
  
- [<span data-ttu-id="867db-109">Rechercher un utilisateur</span><span class="sxs-lookup"><span data-stu-id="867db-109">Search for a user</span></span>](#search-for-a-user)
- [<span data-ttu-id="867db-110">Exporter le rapport de l’historique des données d’un compte</span><span class="sxs-lookup"><span data-stu-id="867db-110">Export a report of account data history</span></span>](#export-a-report-of-account-data-history)
- [<span data-ttu-id="867db-111">Supprimer l’historique des données d’un utilisateur</span><span class="sxs-lookup"><span data-stu-id="867db-111">Delete user data history</span></span>](#delete-user-data-history)
  
## <a name="search-for-a-user"></a><span data-ttu-id="867db-112">Rechercher un utilisateur</span><span class="sxs-lookup"><span data-stu-id="867db-112">Search for a user</span></span>

<span data-ttu-id="867db-113">Pour rechercher un compte d’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="867db-113">To search for a user account:</span></span>
  
1. <span data-ttu-id="867db-p103">Entrez l’alias de l’adresse e-mail de l’utilisateur (informations à gauche du symbole @), puis choisissez le nom de domaine à partir de la liste des suffixes de domaine à droite. Pour les organisations ayant plusieurs domaines inscrits, revérifiez le suffixe du nom de domaine pour éviter toute erreur.</span><span class="sxs-lookup"><span data-stu-id="867db-p103">Enter the user email alias (the information to the left of the @ symbol) and choose the domain name from the  domain suffix list on the right. For organizations with multiple registered domains, double check the domain name suffix to ensure that it is correct.</span></span>

2. <span data-ttu-id="867db-116">Une fois que le nom d’utilisateur est correctement entré, sélectionnez **Rechercher**.</span><span class="sxs-lookup"><span data-stu-id="867db-116">When you have the username correctly entered, select **Search**.</span></span>

3. <span data-ttu-id="867db-117">Pour les comptes d’utilisateur non renvoyés, la page affiche **Utilisateur introuvable**.</span><span class="sxs-lookup"><span data-stu-id="867db-117">For user accounts not returned, the page displays **User not found**.</span></span> <span data-ttu-id="867db-118">Vérifiez l’adresse e-mail de l’utilisateur, puis apportez les corrections nécessaires le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="867db-118">Check the user's email address information and make corrections as necessary.</span></span> <span data-ttu-id="867db-119">Pour réessayer, sélectionnez **Rechercher**.</span><span class="sxs-lookup"><span data-stu-id="867db-119">To retry, select **Search**.</span></span>

4. <span data-ttu-id="867db-120">Pour les comptes d’utilisateur renvoyés, le texte du bouton passe de **Rechercher** à **Effacer**.</span><span class="sxs-lookup"><span data-stu-id="867db-120">For user accounts returned, the text of the button changes from **Search** to **Clear**.</span></span> <span data-ttu-id="867db-121">Ceci indique que les comptes d’utilisateur renvoyés est le contexte opérationnel pour les fonctions supplémentaires et que ces dernières s’appliquent à ce compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="867db-121">This indicates that the returned user account is the operating context for the additional functions and that these functions apply to this user account.</span></span>

5. <span data-ttu-id="867db-122">Pour effacer les résultats de la recherche et rechercher un autre utilisateur, sélectionnez **Effacer**.</span><span class="sxs-lookup"><span data-stu-id="867db-122">To clear search results and search for a different user, select **Clear**.</span></span>

## <a name="export-a-report-of-account-data-history"></a><span data-ttu-id="867db-123">Exporter le rapport de l’historique des données d’un compte</span><span class="sxs-lookup"><span data-stu-id="867db-123">Export a report of account data history</span></span>

<span data-ttu-id="867db-p106">Pour chaque compte d’utilisateur identifié, vous pouvez générer un rapport sur les dépendances liées au compte. Ces informations vous permettent de réaffecter des éléments d’action en cours ou de garantir l’accès à des preuves chargées.</span><span class="sxs-lookup"><span data-stu-id="867db-p106">For each user account identified, you can generate a report of dependencies linked to the account. This information allows you to reassign open Action Items or ensure access to previously uploaded evidence.</span></span>
  
 <span data-ttu-id="867db-126">Pour générer et exporter un rapport :</span><span class="sxs-lookup"><span data-stu-id="867db-126">To generate and export a report:</span></span>
  
1. <span data-ttu-id="867db-127">Sélectionnez **Exporter** pour générer et télécharger un rapport sur les éléments d’action de contrôle du Gestionnaire de conformité actuellement attribués au compte d’utilisateur renvoyé, ainsi que la liste des documents chargés par cet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="867db-127">Select **Export** to generate and download a report of the Compliance Manager control Action Items currently assigned to the returned user account, and the list of documents uploaded by that user.</span></span> <span data-ttu-id="867db-128">En l’absence d’actions attribuées ou de documents chargés, un message d’erreur indique « Aucune données pour cet utilisateur ».</span><span class="sxs-lookup"><span data-stu-id="867db-128">If there are no assigned actions or uploaded documents, an error message states "No data for this user".</span></span>

2. <span data-ttu-id="867db-129">Le rapport est téléchargé en arrière-plan de la fenêtre active du navigateur. Si aucune fenêtre contextuelle de téléchargement n’apparaît, vérifiez l’historique de téléchargement de votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="867db-129">The report downloads in the background of the active browser window — if you don't see a download popup that you want to check your browser download history.</span></span>

3. <span data-ttu-id="867db-130">Ouvrez le document pour consulter les données du rapport.</span><span class="sxs-lookup"><span data-stu-id="867db-130">Open the document to review the report data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="867db-p108">Les données du rapport ne sont pas une liste historique qui consigne et affiche les changements d’état de l’historique d’affectation des éléments d’action. Le rapport généré est une capture instantanée des éléments d’action du contrôle affectés pendant l’exécution du rapport (horodateur indiqué dans le rapport). Par exemple, toute réaffectation des éléments d’action génère une autre capture instantanée des données du rapport si ce rapport est généré une nouvelle fois pour le même utilisateur.</span><span class="sxs-lookup"><span data-stu-id="867db-p108">The report data is not a historical list that retains and displays state changes to Action Item assignment history. The generated report is a snapshot of the control Action Items assigned at the time that the report is run (date and time stamp written into the report). For example, any subsequent reassignment of Action Items result in different snapshot report data if the report is generated again for the same user.</span></span>
  
## <a name="delete-user-data-history"></a><span data-ttu-id="867db-134">Supprimer l’historique des données d’un utilisateur</span><span class="sxs-lookup"><span data-stu-id="867db-134">Delete user data history</span></span>

<span data-ttu-id="867db-135">Cette action définit tous les éléments affectés d’action de contrôle sur « non affecté » à l’utilisateur renvoyé.</span><span class="sxs-lookup"><span data-stu-id="867db-135">Sets all control Action Items assigned to the returned user to 'unassigned'.</span></span> <span data-ttu-id="867db-136">Elle définit la valeur **chargé par** sur « utilisateur supprimé » pour tous les documents chargés par l’utilisateur renvoyé.</span><span class="sxs-lookup"><span data-stu-id="867db-136">Sets the **uploaded by** value for any documents uploaded by the returned user to 'user removed'.</span></span>
  
<span data-ttu-id="867db-137">Pour supprimer un élément d’action du compte d’utilisateur et l’historique de chargement des documents :</span><span class="sxs-lookup"><span data-stu-id="867db-137">To delete the user account Action Item and document upload history:</span></span>
  
1. <span data-ttu-id="867db-138">Sélectionnez **Supprimer**.</span><span class="sxs-lookup"><span data-stu-id="867db-138">Select **Delete**.</span></span>

    <span data-ttu-id="867db-139">Une boîte de dialogue de confirmation apparaît, indiquant : *Cette action supprime tous les éléments d’action du contrôle affectés et l’historique de chargement des documents pour l’utilisateur sélectionné. Cette action est définitive. Voulez-vous vraiment continuer ?*  »</span><span class="sxs-lookup"><span data-stu-id="867db-139">A confirmation dialog is displayed: "*This removes all control Action Item assignments and the document upload history for the selected user. This action is permanent. Are you sure you want to continue?*"</span></span>

2. <span data-ttu-id="867db-140">Pour continuer, sélectionnez **OK**. Sinon, sélectionnez **Annuler**.</span><span class="sxs-lookup"><span data-stu-id="867db-140">To continue select **OK**, otherwise select **Cancel**.</span></span>
