---
title: Consulter les données dans des preuves
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: how-to
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Découvrez les méthodes permettant de passer en revue les données de vos preuves, telles que l’affichage dans un format natif, texte ou presque natif.
ms.custom: seo-marvel-mar2020
ms.openlocfilehash: 9335b95cc57add69660b707577829caef1ad8183
ms.sourcegitcommit: 2160e7cf373f992dd4d11793a59cb8c44f8d587e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/26/2020
ms.locfileid: "48285380"
---
# <a name="review-the-data-in-evidence"></a><span data-ttu-id="698b8-103">Consulter les données dans des preuves</span><span class="sxs-lookup"><span data-stu-id="698b8-103">Review the data in evidence</span></span>

<span data-ttu-id="698b8-104">Les données d’un ensemble de preuves dans une enquête sur les données sont un instantané des résultats de la recherche que vous avez collectés et ajoutés à l’ensemble de preuves.</span><span class="sxs-lookup"><span data-stu-id="698b8-104">The data in an evidence set in a data investigation is a snapshot of the search results that you collected and added to the evidence set.</span></span> <span data-ttu-id="698b8-105">Lorsque vous ajoutez des résultats de recherche à une preuve, un processus est déclenché pour extraire les fichiers, les métadonnées et le texte des éléments renvoyés par la recherche.</span><span class="sxs-lookup"><span data-stu-id="698b8-105">When you add search results to evidence, a process is triggered to extract files, metadata, and text from the items returned by the search.</span></span> <span data-ttu-id="698b8-106">Ensuite, l’outil enquêtes de données (aperçu) crée un nouvel index (par un processus appelé *indexation avancée*) de toutes les données et ajoute un ensemble de preuves sur l’onglet **preuve** .</span><span class="sxs-lookup"><span data-stu-id="698b8-106">Then the Data Investigations (preview) tool then builds a new index (by a process called *Advanced indexing*) of all the data and adds to an evidence set on the **Evidence** tab.</span></span> 

<span data-ttu-id="698b8-107">Pour les analyses urgentes, cela vous permet de contenir rapidement l’environnement en supprimant les données propagées ou involontaires dans la source de données d’origine, tout en vous permettant d’examiner la preuve recréée dans un environnement en quarantaine, dans ce cas les données copiées dans l’ensemble de preuves.</span><span class="sxs-lookup"><span data-stu-id="698b8-107">For time-sensitive investigations, this allows you to quickly contain the environment by deleting the actual spilled or malicious data located in the at original data source, while at the same time allowing you to investigate the re-created evidence in a quarantined environment, which in this case is the data copied to the evidence set).</span></span> <span data-ttu-id="698b8-108">Une fois que la preuve a été collectée et ajoutée à l’ensemble de preuves, vous pouvez passer en revue des documents individuels au format natif, au format texte ou à un format quasi natif que vous pouvez utiliser pour annoter et biffer des documents.</span><span class="sxs-lookup"><span data-stu-id="698b8-108">After the evidence is collected and added to the evidence set, you can review individual documents in their native format, text format, or a near-native format that you can use to annotate and redact documents.</span></span> <span data-ttu-id="698b8-109">En outre, vous pouvez exécuter des requêtes pour affiner les données définies par plage de temps, types de fichiers, propriétaires de données, ainsi que de nombreuses autres propriétés et conditions de recherche.</span><span class="sxs-lookup"><span data-stu-id="698b8-109">Additionally, you can run queries to narrow the data set by time range, file types, data owners, and many other properties and search conditions.</span></span> <span data-ttu-id="698b8-110">Par exemple, à l’aide des conditions auteur, expéditeur ou destinataire, vous pouvez identifier rapidement les personnes impliquées dans l’incident et si les données de votre organisation ont été partagées avec des utilisateurs externes.</span><span class="sxs-lookup"><span data-stu-id="698b8-110">For example, by using the Author, Sender, or Recipient conditions, you can quickly identify the people are involved in the incident and if any data from your organization has been shared with external users.</span></span> <span data-ttu-id="698b8-111">Pour plus d’informations sur la recherche dans les données d’un ensemble de preuves, voir [query the Data in Evidence](evidence-query.md).</span><span class="sxs-lookup"><span data-stu-id="698b8-111">For more information about searching through data in an evidence set, see [Query the data in evidence](evidence-query.md).</span></span>

<span data-ttu-id="698b8-112">Pour regrouper des documents et obtenir de l’aide supplémentaire pour votre révision, sélectionnez un ensemble de preuves sous l’onglet **preuve** , puis cliquez sur **gérer les preuves**.</span><span class="sxs-lookup"><span data-stu-id="698b8-112">To group documents and get more assistance for your review, select an evidence set on the **Evidence** tab, and then click **Manage evidence**.</span></span> <span data-ttu-id="698b8-113">Dans la vignette **analyse** , cliquez sur **reconstruire l’analyse pour l’ensemble du jeu**.</span><span class="sxs-lookup"><span data-stu-id="698b8-113">In the **Analytics** tile, click **Rebuild analytics for the whole set**.</span></span> <span data-ttu-id="698b8-114">Cette opération exécute des analyses avancées, telles que la détection des doublons, le Threading de messagerie électronique et l’analyse de thème.</span><span class="sxs-lookup"><span data-stu-id="698b8-114">This will run advanced analytics such as duplicate detection, email threading, and theme analysis.</span></span> <span data-ttu-id="698b8-115">Par la suite, vous pouvez voir les thèmes généraux des données, ainsi qu’organiser les documents par des threads de messagerie, des doublons et des doublons exacts pour faciliter votre examen.</span><span class="sxs-lookup"><span data-stu-id="698b8-115">Afterwards, you can see the general themes of the data and also organize documents by email threads, near duplicates, and exact duplicates to help your investigation.</span></span> <span data-ttu-id="698b8-116">Pour plus d’informations, reportez-vous [à exécuter Analytics pour effectuer des recherches plus rapidement](run-analytics-to-investigate-faster.md).</span><span class="sxs-lookup"><span data-stu-id="698b8-116">For more information, see [Run analytics to investigate faster](run-analytics-to-investigate-faster.md).</span></span>

## <a name="view-documents-in-evidence"></a><span data-ttu-id="698b8-117">Afficher les documents dans les preuves</span><span class="sxs-lookup"><span data-stu-id="698b8-117">View documents in evidence</span></span>

<span data-ttu-id="698b8-118">L’outil enquêtes sur les données (aperçu) vous permet d’afficher du contenu dans plusieurs visionneuses, chaque afficheur ayant un objectif différent.</span><span class="sxs-lookup"><span data-stu-id="698b8-118">The Data Investigations (preview) tool allows you to display content in several different viewers, with each viewer having a different purpose.</span></span> <span data-ttu-id="698b8-119">Ces utilisateurs sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="698b8-119">These viewers are:</span></span>

- <span data-ttu-id="698b8-120">Métadonnées de fichier</span><span class="sxs-lookup"><span data-stu-id="698b8-120">File metadata</span></span>
- <span data-ttu-id="698b8-121">Affichage natif</span><span class="sxs-lookup"><span data-stu-id="698b8-121">Native view</span></span>
- <span data-ttu-id="698b8-122">Affichage de texte</span><span class="sxs-lookup"><span data-stu-id="698b8-122">Text view</span></span>
- <span data-ttu-id="698b8-123">Mode annotation</span><span class="sxs-lookup"><span data-stu-id="698b8-123">Annotate view</span></span>

<span data-ttu-id="698b8-124">Pour accéder à l’un de ces utilisateurs, il vous suffit de sélectionner un document dans un jeu de preuves.</span><span class="sxs-lookup"><span data-stu-id="698b8-124">To access any of these viewers, just select a document in an evidence set.</span></span>

## <a name="file-metadata"></a><span data-ttu-id="698b8-125">Métadonnées de fichier</span><span class="sxs-lookup"><span data-stu-id="698b8-125">File metadata</span></span>

<span data-ttu-id="698b8-126">Cette vue affiche diverses propriétés de métadonnées associées au document sélectionné.</span><span class="sxs-lookup"><span data-stu-id="698b8-126">This view displays various metadata properties associated with the selected document.</span></span> <span data-ttu-id="698b8-127">Vous pouvez activer ou désactiver cette vue en cliquant sur **métadonnées de fichier**.</span><span class="sxs-lookup"><span data-stu-id="698b8-127">You can toggle this view on and off by clicking **File metadata**.</span></span> <span data-ttu-id="698b8-128">Lors de l’examen d’un document, vous pouvez afficher les métadonnées du fichier et continuer à modifier les différentes visionneuses.</span><span class="sxs-lookup"><span data-stu-id="698b8-128">When reviewing a document, you can view the file metadata and still change between the different viewers.</span></span>

<span data-ttu-id="698b8-129">Voici un exemple de métadonnées de fichier pour un document.</span><span class="sxs-lookup"><span data-stu-id="698b8-129">Here's an example of the file metadata for a document.</span></span> <span data-ttu-id="698b8-130">Pour plus d’informations sur les champs de métadonnées, voir [document Metadata Fields in Data investigations (Preview)](document-metadata-fields.md).</span><span class="sxs-lookup"><span data-stu-id="698b8-130">For more information about the metadata fields, see [Document metadata fields in Data Investigations (preview)](document-metadata-fields.md).</span></span>

![Panneau métadonnées de fichier](../media/Reviewimage2.png)

## <a name="native-view"></a><span data-ttu-id="698b8-132">Affichage natif</span><span class="sxs-lookup"><span data-stu-id="698b8-132">Native view</span></span>

<span data-ttu-id="698b8-133">La visionneuse Native affiche l’affichage le plus précis d’un document dans son format natif.</span><span class="sxs-lookup"><span data-stu-id="698b8-133">The Native viewer displays the most accurate view of a document in its native format.</span></span> <span data-ttu-id="698b8-134">L’affichage natif est pris en charge pour des centaines de types de fichiers et est destiné à afficher des documents dans l’expérience Native la plus réelle possible.</span><span class="sxs-lookup"><span data-stu-id="698b8-134">Native view is supported for hundreds of file types and is meant to display documents in the truest native experience possible.</span></span> <span data-ttu-id="698b8-135">Pour les fichiers Microsoft Office, la visionneuse Native utilise la version Web des applications Office.</span><span class="sxs-lookup"><span data-stu-id="698b8-135">For Microsoft Office files, the Native viewer uses the web version of Office apps.</span></span> <span data-ttu-id="698b8-136">Cela vous permet d’afficher du contenu tel que des commentaires dans différents documents Office, formules et lignes/colonnes masquées dans Excel, ainsi que l’affichage notes dans PowerPoint.</span><span class="sxs-lookup"><span data-stu-id="698b8-136">This allows you to view content such as comments in different Office documents, formulas and hidden rows/columns in Excel, and the Notes view in PowerPoint.</span></span>

![<span data-ttu-id="698b8-137">Affichage natif</span><span class="sxs-lookup"><span data-stu-id="698b8-137">Native view</span></span>
](../media/Reviewimage3.png)

## <a name="text-view"></a><span data-ttu-id="698b8-138">Affichage de texte</span><span class="sxs-lookup"><span data-stu-id="698b8-138">Text view</span></span>

<span data-ttu-id="698b8-139">La visionneuse de texte donne un aperçu du texte extrait d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="698b8-139">The Text viewer provides a view of the extracted text of a file.</span></span> <span data-ttu-id="698b8-140">Elle ignore toutes les images incorporées et la mise en forme, mais cet affichage est utile si vous essayez d’examiner et de comprendre rapidement le contenu d’un document.</span><span class="sxs-lookup"><span data-stu-id="698b8-140">It ignores any embedded images and formatting, but this view is useful if you're trying to quickly review and understand the content in a document.</span></span> <span data-ttu-id="698b8-141">L’affichage de texte inclut également les fonctionnalités suivantes :</span><span class="sxs-lookup"><span data-stu-id="698b8-141">Text view also includes these features:</span></span>

  - <span data-ttu-id="698b8-142">Un compteur de ligne, qui facilite la référence à des parties spécifiques d’un document.</span><span class="sxs-lookup"><span data-stu-id="698b8-142">A line counter, which makes it easier to reference specific portions of a document.</span></span>

  - <span data-ttu-id="698b8-143">Mise en surbrillance des résultats de recherche mettant en surbrillance les termes dans le document, ainsi que sur la barre de défilement</span><span class="sxs-lookup"><span data-stu-id="698b8-143">Search hit highlighting that highlight terms in the document as well as on the scrollbar</span></span>

  - <span data-ttu-id="698b8-144">Une vue diff fournit un affichage de comparaison qui met en évidence les différences de texte lors de l’affichage des documents à l’aide du panneau **presque des doublons** .</span><span class="sxs-lookup"><span data-stu-id="698b8-144">A diff view provides a comparison view that highlights the text differences when viewing documents using the **Near duplicates** panel.</span></span>

<span data-ttu-id="698b8-145">**Exemple de mise en surbrillance des compteurs de ligne et de recherche dans le texte et la barre de défilement**</span><span class="sxs-lookup"><span data-stu-id="698b8-145">**Example of line counter and search hit highlighting in text and scrollbar**</span></span>

![<span data-ttu-id="698b8-146">Affichage de texte</span><span class="sxs-lookup"><span data-stu-id="698b8-146">Text view</span></span>
](../media/Reviewimage4.png)

<span data-ttu-id="698b8-147">**Exemple de vue diff**</span><span class="sxs-lookup"><span data-stu-id="698b8-147">**Example of the diff view**</span></span>

![<span data-ttu-id="698b8-148">Vue diff</span><span class="sxs-lookup"><span data-stu-id="698b8-148">Diff view</span></span>
](../media/Reviewimage5.png)

## <a name="annotate-view"></a><span data-ttu-id="698b8-149">Mode annotation</span><span class="sxs-lookup"><span data-stu-id="698b8-149">Annotate view</span></span>

<span data-ttu-id="698b8-150">L’affichage Annoted propose des fonctionnalités qui vous permettent d’appliquer un balisage à un document pendant le processus de révision ; ces outils sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="698b8-150">The Annotate view provides features that allow you to apply markup on a document during the review process; this  includes these tools:</span></span>

  - <span data-ttu-id="698b8-151">**Zone Redactions** : vous pouvez dessiner une zone opaque sur le document qui masque le contenu sensible.</span><span class="sxs-lookup"><span data-stu-id="698b8-151">**Area redactions** – You can draw an opaque box on the document that hides sensitive content.</span></span>

  - <span data-ttu-id="698b8-152">**Crayon** : vous pouvez dessiner manuellement sur un document pour attirer l’attention sur certaines parties du contenu</span><span class="sxs-lookup"><span data-stu-id="698b8-152">**Pencil** – You can free-hand draw on a document to bring attention to certain portions of the content</span></span>

  - <span data-ttu-id="698b8-153">**Sélectionner des annotations** : vous pouvez sélectionner et supprimer des annotations dans un document.</span><span class="sxs-lookup"><span data-stu-id="698b8-153">**Select annotations** - You can select and delete annotations in a document.</span></span>

  - <span data-ttu-id="698b8-154">**Activer/désactiver la transparence** des annotations : vous pouvez activer/désactiver la transparence des annotations (entre opaque et semi-transparent) de sorte que vous puissiez visualiser le contenu derrière l’annotation.</span><span class="sxs-lookup"><span data-stu-id="698b8-154">**Toggle annotation transparency** – You can toggle the transparency of annotations (between opaque and semi-transparent) so you can view the content behind the annotation.</span></span> <span data-ttu-id="698b8-155">Cela inclut le basculement de la transparence des annotations et des annotations Redactions.</span><span class="sxs-lookup"><span data-stu-id="698b8-155">This includes toggling the transparency of pencil annotations and redactions.</span></span>

<span data-ttu-id="698b8-156">La vue Annoted fournit également les fonctionnalités de navigation suivantes :</span><span class="sxs-lookup"><span data-stu-id="698b8-156">The Annotate view also provides the following navigation functionality:</span></span>

  - <span data-ttu-id="698b8-157">**Page précédente**, **page suivante**et **accéder aux** contrôles de navigation de page à utiliser pour les documents de plusieurs pages.</span><span class="sxs-lookup"><span data-stu-id="698b8-157">**Previous page**, **Next page**, and **Go to page** - Navigation controls to use for multi-page documents.</span></span>

  - <span data-ttu-id="698b8-158">**Zoom** : augmente ou réduit la taille des documents en mode annotation.</span><span class="sxs-lookup"><span data-stu-id="698b8-158">**Zoom** – Increases or decreases the size of documents in Annotate view.</span></span>

  - <span data-ttu-id="698b8-159">**Rotation** : rotation des documents dans le sens des aiguilles d’une montre.</span><span class="sxs-lookup"><span data-stu-id="698b8-159">**Rotate** – Rotate documents clockwise.</span></span>

  - <span data-ttu-id="698b8-160">**Search** : recherchez des mots clés dans un document, puis utilisez les contrôles Previous et Next pour afficher les résultats (qui sont mis en surbrillance) dans le document.</span><span class="sxs-lookup"><span data-stu-id="698b8-160">**Search** – Search for keywords in a document, and then use Previous and Next controls to view the hits (which are highlighted) within the document.</span></span>

<span data-ttu-id="698b8-161">**Exemple d’affichage annoter**</span><span class="sxs-lookup"><span data-stu-id="698b8-161">**Example of Annotate view**</span></span>

![Mode annotation](../media/Reviewimage1.png)

> [!NOTE]
> <span data-ttu-id="698b8-163">Les annotations sont appliquées à une copie du document qui a été ajouté à l’ensemble de preuves.</span><span class="sxs-lookup"><span data-stu-id="698b8-163">Annotations are applied to a copy of the document that was added to the evidence set.</span></span> <span data-ttu-id="698b8-164">Les documents d’origine dans le service actif ne sont pas annotés.</span><span class="sxs-lookup"><span data-stu-id="698b8-164">The original documents in the live service aren't annotated.</span></span>
