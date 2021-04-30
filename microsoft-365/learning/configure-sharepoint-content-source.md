---
title: "Bientôt disponible : configurer SharePoint comme source de contenu d'apprentissage pour Microsoft Microsoft Learning (prévisualisation)"
ms.author: chucked
author: chuckedmonson
manager: pamgreen
ms.reviewer: chrisarnoldmsft
ms.date: 04/30/2021
audience: admin
ms.topic: article
ms.service: ''
ms.prod: microsoft-365-enterprise
search.appverid: ''
ms.collection:
- enabler-strategic
- m365initiative-viva-learning
localization_priority: None
description: Découvrez comment configurer SharePoint en tant que source de contenu d'apprentissage pour Microsoft Learning (prévisualisation).
ROBOTS: NOINDEX, NOFOLLOW
ms.openlocfilehash: da75ec0573519ed73507994afeac995c0461de0c
ms.sourcegitcommit: d3f8c69519c593b1580cfa7187ce085a99b8a846
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/30/2021
ms.locfileid: "52100963"
---
# <a name="coming-soon-configure-sharepoint-as-a-learning-content-source-for-microsoft-viva-learning-preview"></a><span data-ttu-id="b6143-103">Bientôt disponible : configurer SharePoint comme source de contenu d'apprentissage pour Microsoft Microsoft Learning (prévisualisation)</span><span class="sxs-lookup"><span data-stu-id="b6143-103">Coming soon: Configure SharePoint as a learning content source for Microsoft Viva Learning (Preview)</span></span>

> [!NOTE]
> <span data-ttu-id="b6143-104">Les informations de cet article concernent un produit d'aperçu qui peut être considérablement modifié avant sa publication commerciale.</span><span class="sxs-lookup"><span data-stu-id="b6143-104">The information in this article relates to a preview product that may be substantially modified before it's commercially released.</span></span> 

<span data-ttu-id="b6143-105">Vous pouvez configurer SharePoint en tant que source de contenu d'apprentissage pour que le contenu de votre organisation soit disponible dans Learning Learning (Prévisualisation).</span><span class="sxs-lookup"><span data-stu-id="b6143-105">You can configure SharePoint as a learning content source to make your organization's own content available in Viva Learning (Preview).</span></span>

## <a name="overview"></a><span data-ttu-id="b6143-106">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="b6143-106">Overview</span></span>

<span data-ttu-id="b6143-107">L'administrateur du savoir (ou administrateur général) fournit une URL de site où le service d'apprentissage peut créer un emplacement centralisé vide(référentiel de contenu d'application d'apprentissage) sous la forme d'une liste SharePoint structurée.</span><span class="sxs-lookup"><span data-stu-id="b6143-107">The knowledge admin (or global administrator) provides a site URL to where the Learning Service can create an empty centralized location—the Learning App Content Repository—in the form of a structured SharePoint list.</span></span> <span data-ttu-id="b6143-108">Cette liste peut être utilisée par votre organisation pour contenir des liens vers des dossiers SharePoint'entreprise contenant du contenu d'apprentissage.</span><span class="sxs-lookup"><span data-stu-id="b6143-108">This list can be used by your organization to house links to cross-company SharePoint folders that contain learning content.</span></span> <span data-ttu-id="b6143-109">Les administrateurs sont chargés de collecter et de organiser une liste d'URL pour les dossiers.</span><span class="sxs-lookup"><span data-stu-id="b6143-109">Admins are responsible for collecting and curating a list of URLs for folders.</span></span> <span data-ttu-id="b6143-110">Ces dossiers doivent inclure uniquement le contenu qui peut être mis à disposition dans Learning (Prévisualisation).</span><span class="sxs-lookup"><span data-stu-id="b6143-110">These folders should only include content that can be made available in Viva Learning (Preview).</span></span>

<span data-ttu-id="b6143-111">Learning (Prévisualisation) prend en charge les types de documents suivants :</span><span class="sxs-lookup"><span data-stu-id="b6143-111">Viva Learning (Preview) supports the following document types:</span></span>

- <span data-ttu-id="b6143-112">Word, PowerPoint, Excel, PDF</span><span class="sxs-lookup"><span data-stu-id="b6143-112">Word, PowerPoint, Excel, PDF</span></span>
- <span data-ttu-id="b6143-113">Audio (.m4a)</span><span class="sxs-lookup"><span data-stu-id="b6143-113">Audio (.m4a)</span></span>
- <span data-ttu-id="b6143-114">Vidéo (.mov, .mp4, .avi)</span><span class="sxs-lookup"><span data-stu-id="b6143-114">Video (.mov, .mp4, .avi)</span></span>

<span data-ttu-id="b6143-115">Pour plus d'informations, voir [la documentation SharePoint Online.](/office365/servicedescriptions/sharepoint-online-service-description/sharepoint-online-limits?redirectSourcePath=%252farticle%252fSharePoint-Online-limits-8f34ff47-b749-408b-abc0-b605e1f6d498)</span><span class="sxs-lookup"><span data-stu-id="b6143-115">For more information, see the [SharePoint Online documentation](/office365/servicedescriptions/sharepoint-online-service-description/sharepoint-online-limits?redirectSourcePath=%252farticle%252fSharePoint-Online-limits-8f34ff47-b749-408b-abc0-b605e1f6d498).</span></span> 

## <a name="permissions"></a><span data-ttu-id="b6143-116">Autorisations</span><span class="sxs-lookup"><span data-stu-id="b6143-116">Permissions</span></span>

<span data-ttu-id="b6143-117">Les URL de dossier de bibliothèque de documents peuvent être collectées à partir de n'importe quel site SharePoint de l'organisation.</span><span class="sxs-lookup"><span data-stu-id="b6143-117">Document library folder URLs can be collected from any SharePoint site in the organization.</span></span> <span data-ttu-id="b6143-118">Learning (Preview) suit toutes les autorisations de contenu existantes.</span><span class="sxs-lookup"><span data-stu-id="b6143-118">Viva Learning (Preview) follows all existing content permissions.</span></span> <span data-ttu-id="b6143-119">Par conséquent, seul le contenu pour lequel un utilisateur a l'autorisation d'accéder est accessible à la recherche et visible dans Learning (Preview).</span><span class="sxs-lookup"><span data-stu-id="b6143-119">Therefore, only content for which a user has permission to access is searchable and visable within Viva Learning (Preview).</span></span> <span data-ttu-id="b6143-120">Tout contenu de ces dossiers est utilisable dans une recherche, mais seul le contenu pour lequel l'employé dispose d'autorisations peut être utilisé.</span><span class="sxs-lookup"><span data-stu-id="b6143-120">Any content within these folders will be searchable, but only content to which the individual employee has permissions can be used.</span></span>

<span data-ttu-id="b6143-121">La suppression de contenu du référentiel de votre organisation n'est actuellement pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="b6143-121">Content deletion from your organization’s repository is not currently supported.</span></span>

<span data-ttu-id="b6143-122">Pour supprimer le contenu accidentellement surface, suivez les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="b6143-122">To remove unintentionally surfaced content, follow these steps:</span></span>

1.  <span data-ttu-id="b6143-123">Pour restreindre l'accès à la bibliothèque de documents, sélectionnez l'option Afficher **les actions,** puis **sélectionnez Gérer l'accès.**</span><span class="sxs-lookup"><span data-stu-id="b6143-123">To restrict access to the document library, select the **Show actions** option, and then select **Manage access**.</span></span>
     
     ![Page bibliothèque de documents dans SharePoint l'option Afficher les actions avec accès Gérer élevé.](../media/learning/learning-sharepoint-permissions2.png)

2.  <span data-ttu-id="b6143-125">Supprimez le document d'origine dans la bibliothèque de documents.</span><span class="sxs-lookup"><span data-stu-id="b6143-125">Delete the original document within the document library.</span></span>

<span data-ttu-id="b6143-126">Pour plus d'informations, [voir Partage et autorisations dans l'SharePoint moderne.](/sharepoint/modern-experience-sharing-permissions)</span><span class="sxs-lookup"><span data-stu-id="b6143-126">For more information, see [Sharing and permissions in the SharePoint modern experience](/sharepoint/modern-experience-sharing-permissions).</span></span> 

## <a name="learning-service"></a><span data-ttu-id="b6143-127">Service d'apprentissage</span><span class="sxs-lookup"><span data-stu-id="b6143-127">Learning Service</span></span>

<span data-ttu-id="b6143-128">Le service d'apprentissage utilise les URL de dossier fournies pour obtenir des métadonnées à partir de tout le contenu stocké dans ces dossiers.</span><span class="sxs-lookup"><span data-stu-id="b6143-128">The Learning Service uses the provided folder URLs to get metadata from all content stored in those folders.</span></span> <span data-ttu-id="b6143-129">Dans un délai de 24 heures après la fourniture de l'URL du dossier dans le référentiel centralisé, les employés peuvent rechercher et utiliser le contenu de votre organisation dans Learning (Preview).</span><span class="sxs-lookup"><span data-stu-id="b6143-129">Within 24 hours of supplying the folder URL in the centralized repository, employees can search for and use your organization’s content within Viva Learning (Preview).</span></span> <span data-ttu-id="b6143-130">Toutes les modifications apportées au contenu, y compris les métadonnées et autorisations mises à jour, seront également appliquées dans le service d'apprentissage dans les 24 heures.</span><span class="sxs-lookup"><span data-stu-id="b6143-130">All changes to content, including updated metadata and permissions, will also be applied in the Learning Service within 24 hours.</span></span>

## <a name="configure-sharepoint-as-a-source"></a><span data-ttu-id="b6143-131">Configurer SharePoint en tant que source</span><span class="sxs-lookup"><span data-stu-id="b6143-131">Configure SharePoint as a source</span></span>

<span data-ttu-id="b6143-132">Vous devez être un administrateur Microsoft 365 général, un administrateur SharePoint ou un administrateur du savoir pour effectuer ces tâches.</span><span class="sxs-lookup"><span data-stu-id="b6143-132">You must be a Microsoft 365 global administrator, SharePoint administrator, or knowledge admin to perform these tasks.</span></span>

<span data-ttu-id="b6143-133">Pour configurer des SharePoint en tant que sources de contenu d'apprentissage dans Le Monde Learning (Prévisualisation), suivez les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="b6143-133">To configure SharePoint as a learning content sources in for Viva Learning (Preview), follow these steps:</span></span>

1.  <span data-ttu-id="b6143-134">Dans le navigation gauche du centre d Microsoft 365'administration, Paramètres   >  **paramètres de l'organisation.**</span><span class="sxs-lookup"><span data-stu-id="b6143-134">In the left navigation of the Microsoft 365 admin center, go to **Settings** > **Org settings**.</span></span>
 
2.  <span data-ttu-id="b6143-135">Dans la page **Paramètres de l'organisation,** sous l'onglet **Services,** sélectionnez **Application d'apprentissage (prévisualisation).**</span><span class="sxs-lookup"><span data-stu-id="b6143-135">On the **Org settings** page, on the **Services** tab, select **Learning app (Preview)**.</span></span>

     ![Paramètres page dans le centre d Microsoft 365 asse qui affiche Le Learning listé.](../media/learning/learning-sharepoint-configure1.png)

3.  <span data-ttu-id="b6143-137">Dans  le panneau Application d'apprentissage (prévisualisation), sous SharePoint, fournit l'URL du site SharePoint où vous souhaitez que Learning crée un référentiel centralisé.</span><span class="sxs-lookup"><span data-stu-id="b6143-137">On the **Learning app (Preview)** panel, under SharePoint, provides the site URL to the SharePoint site where you want Viva Learning to create a centralized repository.</span></span>

     ![Panneau d'apprentissage dans Microsoft 365 centre d'administration affichant SharePoint sélectionné.](../media/learning/learning-sharepoint-configure2.png)

4.  <span data-ttu-id="b6143-139">Une liste SharePoint est créée automatiquement dans le site SharePoint fourni.</span><span class="sxs-lookup"><span data-stu-id="b6143-139">A SharePoint list is created automatically within the provided SharePoint site.</span></span>

     ![Nouvellement créé SharePoint liste dans le site SharePoint site.](../media/learning/learning-sharepoint-configure3.png)

     <span data-ttu-id="b6143-141">Dans le navigation gauche du site SharePoint, sélectionnez Contenu du **site** Référentiel de contenu  >  **d'application d'apprentissage.**</span><span class="sxs-lookup"><span data-stu-id="b6143-141">In the left navigation of the SharePoint site, select **Site contents** > **Learning App Content Repository**.</span></span> 

     ![SharePoint liste affichant la navigation du contenu du site et la section Référentiel de contenu d'application d'apprentissage.](../media/learning/learning-sharepoint-configure4.png) 

5. <span data-ttu-id="b6143-143">Dans la page Référentiel de contenu **d'application** d'apprentissage, SharePoint la liste des url vers les dossiers de contenu d'apprentissage.</span><span class="sxs-lookup"><span data-stu-id="b6143-143">On the **Learning App Content Repository** page, populate the SharePoint list with URLs to the learning content folders.</span></span>

   1. <span data-ttu-id="b6143-144">Sélectionnez **Nouveau** pour afficher le **panneau Nouvel** élément.</span><span class="sxs-lookup"><span data-stu-id="b6143-144">Select **New** to view the **New item** panel.</span></span> 

       ![Page Référentiel de contenu d'apprentissage SharePoint l'option Nouvelle.](../media/learning/learning-sharepoint-configure5.png)
 
   2. <span data-ttu-id="b6143-146">Dans le **panneau Nouvel élément,** dans le champ **Titre,** ajoutez un nom de répertoire de votre choix.</span><span class="sxs-lookup"><span data-stu-id="b6143-146">On the **New item** panel, in the **Title** field, add a directory name of your choice.</span></span> <span data-ttu-id="b6143-147">Dans le champ **URL du** dossier, ajoutez l'URL au dossier de contenu d'apprentissage.</span><span class="sxs-lookup"><span data-stu-id="b6143-147">In the **Folder URL** field, add the URL to the learning content folder.</span></span> <span data-ttu-id="b6143-148">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="b6143-148">Select **Save**.</span></span>

       ![Nouveau panneau d'élément SharePoint affichant les champs d'URL de titre et de dossier.](../media/learning/learning-sharepoint-configure6.png)

   3. <span data-ttu-id="b6143-150">La page **Référentiel de contenu d'application d'apprentissage** est mise à jour avec le nouveau contenu d'apprentissage.</span><span class="sxs-lookup"><span data-stu-id="b6143-150">The **Learning App Content Repository** page is updated with the new learning content.</span></span>

       ![Page Référentiel de contenu d'apprentissage SharePoint affichant les informations mises à jour.](../media/learning/learning-sharepoint-configure7.png)

> [!NOTE]
> <span data-ttu-id="b6143-152">Pour permettre un accès plus large au référentiel de contenu d'application d'apprentissage, un lien vers la liste sera bientôt disponible dans l'interface Learning (Prévisualisation) dans laquelle les utilisateurs peuvent demander l'accès et, en fin de compte, contribuer à remplir la liste.</span><span class="sxs-lookup"><span data-stu-id="b6143-152">To allow for broader access to the Learning App Content Repository, a link to the list soon will be available in the Viva Learning (Preview) interface where users can request access and ultimately help populate the list.</span></span> <span data-ttu-id="b6143-153">Les propriétaires de site et les administrateurs globaux doivent accorder l'accès à la liste.</span><span class="sxs-lookup"><span data-stu-id="b6143-153">Site owners and global administrators will be required to grant access to the list.</span></span> <span data-ttu-id="b6143-154">L'accès est spécifique à la liste uniquement et ne s'applique pas au site où la liste est stockée.</span><span class="sxs-lookup"><span data-stu-id="b6143-154">Access is specific to the list only and does not apply to the site where the list is stored.</span></span> <span data-ttu-id="b6143-155">Pour plus d'informations, [voir Fournir](#provide-your-own-organizations-content) le contenu de votre propre organisation plus loin dans cet article.</span><span class="sxs-lookup"><span data-stu-id="b6143-155">For more information, see [Provide your own organization's content](#provide-your-own-organizations-content) later in this article.</span></span>

### <a name="folder-url-document-library-curation"></a><span data-ttu-id="b6143-156">Curation de bibliothèque de documents d'URL de dossier</span><span class="sxs-lookup"><span data-stu-id="b6143-156">Folder URL document library curation</span></span>

<span data-ttu-id="b6143-157">Les métadonnées par défaut (telles que la date de modification, créées par, le nom du document, le type de contenu et le nom de l'organisation) sont automatiquement extraites dans Learning Learning (Prévisualisation) par l'API Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="b6143-157">Default metadata (such as modified date, created by, document name, content type, and organization name) is automatically pulled into Viva Learning (Preview) by the Microsoft Graph API.</span></span>
 
<span data-ttu-id="b6143-158">Pour améliorer la pertinence globale de la découverte et de la recherche du contenu, nous vous recommandons d'ajouter une **colonne Description.**</span><span class="sxs-lookup"><span data-stu-id="b6143-158">To improve overall discovery and search relevance of the content, we recommend adding a **Description** column.</span></span>

<span data-ttu-id="b6143-159">Pour ajouter une **colonne Description** à la page de bibliothèque de documents, suivez les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="b6143-159">To add a **Description** column to the document library page, follow these steps:</span></span>

1.  <span data-ttu-id="b6143-160">Dans la page **Documents,** sélectionnez **Ajouter une colonne.**</span><span class="sxs-lookup"><span data-stu-id="b6143-160">On the **Documents** page, select **Add column**.</span></span>

2. <span data-ttu-id="b6143-161">Sélectionnez **l'option Afficher les actions,** puis **sélectionnez Une seule ligne de texte.**</span><span class="sxs-lookup"><span data-stu-id="b6143-161">Select the **Show actions** option, and then select **Single line of text**.</span></span>

     ![Page documents dans SharePoint les options Afficher les actions avec une seule ligne de texte en surbrillant.](../media/learning/learning-sharepoint-curation1.png)

3. <span data-ttu-id="b6143-163">Dans le **panneau Créer une colonne,** dans le champ **Nom,** ajoutez un nom descriptif pour la colonne.</span><span class="sxs-lookup"><span data-stu-id="b6143-163">On the **Create a column** panel, in the **Name** field, add a descriptive name for the column.</span></span> <span data-ttu-id="b6143-164">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="b6143-164">Select **Save**.</span></span>

     ![Créez un panneau de colonne SharePoint afficher le nom et d'autres champs.](../media/learning/learning-sharepoint-curation2.png)
 
4. <span data-ttu-id="b6143-166">Dans la page **Documents,** dans la **colonne Description,** ajoutez des descriptions personnalisées pour chaque élément.</span><span class="sxs-lookup"><span data-stu-id="b6143-166">On the **Documents** page, in the **Description** column, add custom descriptions for each item.</span></span> <span data-ttu-id="b6143-167">Si aucune description n'est fournie, Learning (Prévisualisation) fournit un message par défaut qui met en évidence le contenu comme provenant de SharePoint bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="b6143-167">If no description is supplied, Viva Learning (Preview) will provide a default message that highlights the content as being from your own SharePoint library.</span></span> 

     ![Page documents dans SharePoint affichant les descriptions dans la colonne Description.](../media/learning/learning-sharepoint-curation3.png)
 
### <a name="provide-your-own-organizations-content"></a><span data-ttu-id="b6143-169">Fournir le contenu de votre propre organisation</span><span class="sxs-lookup"><span data-stu-id="b6143-169">Provide your own organization's content</span></span>

<span data-ttu-id="b6143-170">Les administrateurs du savoir peuvent accéder au référentiel de contenu des applications d'apprentissage de leur organisation dans SharePoint, où ils peuvent fournir des références à des bibliothèques de documents entre les organisations.</span><span class="sxs-lookup"><span data-stu-id="b6143-170">Knowledge admins can access their organization’s Learning App Content Repository in SharePoint, where they can provide references to cross-organization document libraries.</span></span> <span data-ttu-id="b6143-171">Le contenu de ces bibliothèques sera ensuite présenté comme du contenu d'apprentissage dans Learning (Prévisualisation).</span><span class="sxs-lookup"><span data-stu-id="b6143-171">Content within these libraries will be then surfaced as learning content in Viva Learning (Preview).</span></span>

1. <span data-ttu-id="b6143-172">Dans Learning (Prévisualisation), sélectionnez **Plus d'options** (**...**), puis **sélectionnez Paramètres**.</span><span class="sxs-lookup"><span data-stu-id="b6143-172">In Viva Learning (Preview), select **More options** (**...**), and then select **Settings**.</span></span>

     ![SharePoint page de la bibliothèque affichant l'option Options Paramètres plus.](../media/learning/learning-sharepoint-library-1.png)
     
2. <span data-ttu-id="b6143-174">Sous **Paramètres,** sélectionnez **Autorisations.**</span><span class="sxs-lookup"><span data-stu-id="b6143-174">Under **Settings**, select **Permissions**.</span></span>

     ![Paramètres page d'options SharePoint les options Autorisations et Vérifier l'accès.](../media/learning/learning-sharepoint-library-2.png)

3. <span data-ttu-id="b6143-176">Sélectionnez **Vérifier l'accès** pour vous connecter à la bibliothèque centralisée de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="b6143-176">Select **Check access** to connect to your organization’s centralized library.</span></span>
     
