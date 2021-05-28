---
title: Présentation de la compréhension de document
ms.author: chucked
author: chuckedmonson
manager: pamgreen
ms.reviewer: ssquires
audience: admin
ms.topic: article
ms.prod: microsoft-365-enterprise
search.appverid: ''
ms.collection:
- enabler-strategic
- m365initiative-syntex
localization_priority: Priority
description: Obtenez une vue d’ensemble de la compréhension des documents dans Microsoft SharePoint Syntex.
ms.openlocfilehash: 7e5818a929fa0f4554a7ee4ece460b4fe0d691aa
ms.sourcegitcommit: a6fb731fdf726d7d9fe4232cf69510013f2b54ce
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2021
ms.locfileid: "52683822"
---
# <a name="document-understanding-overview"></a><span data-ttu-id="d2e23-103">Présentation de la compréhension de document</span><span class="sxs-lookup"><span data-stu-id="d2e23-103">Document understanding overview</span></span>


</br>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4CSu7] 

</br>

<span data-ttu-id="d2e23-104">La compréhension de document utilise les modèles de renseignements artificiels pour automatiser la classification des fichiers et l’extraction des informations.</span><span class="sxs-lookup"><span data-stu-id="d2e23-104">Document understanding uses artificial intelligence (AI) models to automate classification of files and extraction of information.</span></span> <span data-ttu-id="d2e23-105">Il fonctionne de façon optimale avec les documents non structurés, tels que les lettres ou les contrats.</span><span class="sxs-lookup"><span data-stu-id="d2e23-105">It works best with unstructured documents, such as letters or contracts.</span></span> <span data-ttu-id="d2e23-106">Ces documents doivent comporter du texte qui peut être identifié sur la base de phrases ou de modèles.</span><span class="sxs-lookup"><span data-stu-id="d2e23-106">These documents must have text that can be identified based on phrases or patterns.</span></span> <span data-ttu-id="d2e23-107">Le texte identifié désigne à la fois le type de fichier (sa classification) et ce que vous voulez extraire (ses extracteurs).</span><span class="sxs-lookup"><span data-stu-id="d2e23-107">The identified text designates both the type of file it is (its classification) and what you'd like to extract (its extractors).</span></span>

> [!NOTE]
> <span data-ttu-id="d2e23-108">Pour plus d’informations sur les exemples de scénarios relatifs aux exemples de scénarios, consultez l’article [SharePoint Syntex adoption : Guide de démarrage](./adoption-getstarted.md).</span><span class="sxs-lookup"><span data-stu-id="d2e23-108">See the [SharePoint Syntex adoption: Get started guide](./adoption-getstarted.md) for more information about document understanding scenario examples.</span></span>

<span data-ttu-id="d2e23-109">Les modèles de compréhension de document sont créés et gérés dans un site de type SharePoint appelé un *centre de contenu* .</span><span class="sxs-lookup"><span data-stu-id="d2e23-109">Document understanding models are created and managed in a type of SharePoint site called a *content center*.</span></span> <span data-ttu-id="d2e23-110">Lorsqu’il est appliqué à une bibliothèque de documents SharePoint, le modèle associé à un type de contenu inclut des colonnes pour stocker les informations extraites.</span><span class="sxs-lookup"><span data-stu-id="d2e23-110">When applied to a SharePoint document library, the model is associated with a content type has columns to store the information being extracted.</span></span> <span data-ttu-id="d2e23-111">Le type de contenu que vous créez est stocké dans la Galerie de types de contenu SharePoint.</span><span class="sxs-lookup"><span data-stu-id="d2e23-111">The content type you create is stored in the SharePoint content type gallery.</span></span> <span data-ttu-id="d2e23-112">Vous pouvez également choisir d’utiliser des types de contenu existants pour utiliser leur schéma.</span><span class="sxs-lookup"><span data-stu-id="d2e23-112">You can also choose to use existing content types to use their schema.</span></span>

> [!NOTE]
> <span data-ttu-id="d2e23-113">Les types de contenus scellés ou en lecture seule ne peuvent pas être mis à jour. Ils ne peuvent donc pas être utilisés dans un modèle.</span><span class="sxs-lookup"><span data-stu-id="d2e23-113">Read-only or sealed content types cannot be updated, so they can't be used in a model.</span></span>

<span data-ttu-id="d2e23-114">Ajoutez des *classificateurs* et des *extracteurs* à votre document présentation des modèles pour effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="d2e23-114">Add *classifiers* and *extractors* to your document understanding models to do the following:</span></span> 

- <span data-ttu-id="d2e23-115">Les classificateurs sont utilisés pour identifier et classer les documents téléchargés vers la bibliothèque de documents.</span><span class="sxs-lookup"><span data-stu-id="d2e23-115">Classifiers are used to identify and classify documents that are uploaded to the document library.</span></span> <span data-ttu-id="d2e23-116">Par exemple, un classifieur peut être « exercé » pour identifier tous les documents *renouvellement de contrat* qui sont chargés dans la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="d2e23-116">For example, a classifier can be "trained" to identify all *contract renewal* documents that are uploaded to the library.</span></span> <span data-ttu-id="d2e23-117">Le type de contenu renouvellement contrat est défini par vous lorsque vous créez votre classifieur.</span><span class="sxs-lookup"><span data-stu-id="d2e23-117">The contract renewal content type is defined by you when you create your classifier.</span></span>

- <span data-ttu-id="d2e23-118">Les extracteurs extraient des informations de ces documents.</span><span class="sxs-lookup"><span data-stu-id="d2e23-118">Extractors pull information from these documents.</span></span> <span data-ttu-id="d2e23-119">Par exemple, pour tous les documents de renouvellement de contrat identifiés dans votre bibliothèque de documents, les colonnes s’affichent dans votre affichage qui indiquent également la *date de début du service* et *client* pour chaque document de renouvellement de contrat.</span><span class="sxs-lookup"><span data-stu-id="d2e23-119">For example, for all contract renewal documents identified in your document library, columns display in your view that also show the *Service Start Date* and  *Client* for each contract renewal document.</span></span> 

<span data-ttu-id="d2e23-120">Vous pouvez utiliser des fichiers d’exemple pour former et tester vos classificateurs et extracteurs de votre modèle.</span><span class="sxs-lookup"><span data-stu-id="d2e23-120">You can use example files to train and test your classifiers and extractors in your model.</span></span> <span data-ttu-id="d2e23-121">Les exemples de fichiers fournissent vos exemples de modèles à rechercher lorsque vous essayez d’identifier et d’extraire des données de fichiers.</span><span class="sxs-lookup"><span data-stu-id="d2e23-121">Example files provide your model examples of what to look for when trying to identify and extract data from files.</span></span> <span data-ttu-id="d2e23-122">Par exemple, vous devez former vos classificateurs et extracteurs de renouvellement de contrat avec des exemples de documents de renouvellement de contrat que votre entreprise utilise.</span><span class="sxs-lookup"><span data-stu-id="d2e23-122">For example, you would train your contract renewal classifiers and extractors with examples of contract renewal documents your company works with.</span></span> <span data-ttu-id="d2e23-123">Vous pouvez également utiliser des exemples de fichiers pour tester l’efficacité de votre modèle.</span><span class="sxs-lookup"><span data-stu-id="d2e23-123">You can also use example files to test the effectiveness of your model.</span></span>

<span data-ttu-id="d2e23-124">Une fois que vous avez publié votre modèle, utilisez le centre de contenu pour l’appliquer à toute bibliothèque de documents SharePoint à laquelle vous avez accès.</span><span class="sxs-lookup"><span data-stu-id="d2e23-124">After publishing your model, use the content center to apply it to any SharePoint document library that you have access to.</span></span>  

## <a name="file-limitations"></a><span data-ttu-id="d2e23-125">Limitations de fichier</span><span class="sxs-lookup"><span data-stu-id="d2e23-125">File limitations</span></span>

<span data-ttu-id="d2e23-126">Les modèles de compréhension des documents utilisent la technologie OCR (Optical Character Recognition) pour analyser les fichiers PDF, images et TIFF, à la fois lorsque vous entraînez un modèle avec des exemples de fichiers et lorsque vous l’exécutez sur des fichiers dans une bibliothèque de documents.</span><span class="sxs-lookup"><span data-stu-id="d2e23-126">Document understanding models use Optical Character Recognition (OCR) technology to scan PDFs, images, and TIFF files, both when you train a model with example files and when you run the model against files in a document library.</span></span>

<span data-ttu-id="d2e23-127">Notez les différences suivantes en ce qui concerne les fichiers texte Microsoft Office et les fichiers numérisés par OCR (PDF, image ou TIFF) :</span><span class="sxs-lookup"><span data-stu-id="d2e23-127">Note the following differences with regard to Microsoft Office text-based files and OCR-scanned files (PDF, image, or TIFF):</span></span>

- <span data-ttu-id="d2e23-128">Fichiers Office : nous avons tronqué à 64 000 caractères (lors de la formation et de l’exécution sur des fichiers dans une bibliothèque de documents).</span><span class="sxs-lookup"><span data-stu-id="d2e23-128">Office files: Truncated at 64,000 characters (in training and when run against files in a document library).</span></span>

- <span data-ttu-id="d2e23-129">Fichiers numérisés par OCR : la limite est de 20 pages.</span><span class="sxs-lookup"><span data-stu-id="d2e23-129">OCR-scanned files: There's a 20-page limit.</span></span>  

### <a name="requirements"></a><span data-ttu-id="d2e23-130">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="d2e23-130">Requirements</span></span>

<span data-ttu-id="d2e23-131">Le traitement OCR fonctionne mieux sur des documents respectant les conditions requises suivantes :</span><span class="sxs-lookup"><span data-stu-id="d2e23-131">OCR processing works best on documents that meet the following requirements:</span></span>

- <span data-ttu-id="d2e23-132">Format JPG, PNG ou PDF (texte ou numérisé).</span><span class="sxs-lookup"><span data-stu-id="d2e23-132">JPG, PNG, or PDF format (text or scanned).</span></span> <span data-ttu-id="d2e23-133">Les PDF à texte incorporé sont meilleurs car il n’existe aucune erreur d’emplacement et d’extraction de caractères.</span><span class="sxs-lookup"><span data-stu-id="d2e23-133">Text-embedded PDFs are better, because there won't be any errors in character extraction and location.</span></span>

- <span data-ttu-id="d2e23-134">Si vos PDF sont verrouillés par mot de passe, vous devez supprimer le verrou avant de les envoyer.</span><span class="sxs-lookup"><span data-stu-id="d2e23-134">If your PDFs are password-locked, you must remove the lock before submitting them.</span></span>

- <span data-ttu-id="d2e23-135">La taille de fichier combinée des documents par collection utilisés pour la formation ne doit pas dépasser 50 Mo et les documents PDF ne doivent pas contenir plus de 500 pages.</span><span class="sxs-lookup"><span data-stu-id="d2e23-135">The combined file size of the documents used for training per collection must not exceed 50 MB, and PDF documents shouldn't have more than 500 pages.</span></span>

- <span data-ttu-id="d2e23-136">Pour les images, les dimensions doivent se situer entre 50 x 50 et 10 000 x 10 000 pixels.</span><span class="sxs-lookup"><span data-stu-id="d2e23-136">For images, dimensions must be between 50 × 50 and 10,000 × 10,000 pixels.</span></span>
   > [!NOTE]
   > <span data-ttu-id="d2e23-137">Les images très larges ou ayant des dimensions spéciales (par exemple, des plans au sol) peuvent être tronquées dans le processus OCR et perdre en précision.</span><span class="sxs-lookup"><span data-stu-id="d2e23-137">Images that are very wide or have odd dimensions (for example, floor plans) might get truncated in the OCR process and lose accuracy.</span></span>
 
- <span data-ttu-id="d2e23-138">Pour les fichiers PDF, les dimensions doivent se situer à 17 x 17 pouces au maximum, ce qui correspond à des tailles de papier A3 ou Légal, ou plus petites.</span><span class="sxs-lookup"><span data-stu-id="d2e23-138">For PDF files, dimensions must be at most 17 x 17 inches, corresponding to Legal or A3 paper sizes and smaller.</span></span>

- <span data-ttu-id="d2e23-139">S’ils sont numérisés à partir de documents sur papier, les numérisations devraient être des images de qualité supérieure.</span><span class="sxs-lookup"><span data-stu-id="d2e23-139">If scanned from paper documents, scans should be high-quality images.</span></span>

- <span data-ttu-id="d2e23-140">Doit utiliser l’alphabet latin (caractères anglais).</span><span class="sxs-lookup"><span data-stu-id="d2e23-140">Must use the Latin alphabet (English characters).</span></span>

> [!NOTE]
> <span data-ttu-id="d2e23-141">Le générateur d’intelligence artificielle ne prend actuellement pas en charge les types suivants de formulaires traitant des données entrantes :</span><span class="sxs-lookup"><span data-stu-id="d2e23-141">AI Builder doesn't currently support the following types of form processing input data:</span></span><br><span data-ttu-id="d2e23-142">– Case à cocher ou cases d’option</span><span class="sxs-lookup"><span data-stu-id="d2e23-142">- Check boxes or radio buttons</span></span><br><span data-ttu-id="d2e23-143">– Signatures</span><span class="sxs-lookup"><span data-stu-id="d2e23-143">- Signatures</span></span><br><span data-ttu-id="d2e23-144">– PDF à remplir</span><span class="sxs-lookup"><span data-stu-id="d2e23-144">- Fillable PDFs</span></span>

### <a name="supported-file-types"></a><span data-ttu-id="d2e23-145">Types de fichiers pris en charge</span><span class="sxs-lookup"><span data-stu-id="d2e23-145">Supported file types</span></span>

<span data-ttu-id="d2e23-146">Les modèles de compréhension des documents suivent les types de fichiers suivants :</span><span class="sxs-lookup"><span data-stu-id="d2e23-146">Document understanding models support the following file types:</span></span>

- <span data-ttu-id="d2e23-147">doc</span><span class="sxs-lookup"><span data-stu-id="d2e23-147">doc</span></span>
- <span data-ttu-id="d2e23-148">docx</span><span class="sxs-lookup"><span data-stu-id="d2e23-148">docx</span></span>
- <span data-ttu-id="d2e23-149">eml</span><span class="sxs-lookup"><span data-stu-id="d2e23-149">eml</span></span>
- <span data-ttu-id="d2e23-150">heic</span><span class="sxs-lookup"><span data-stu-id="d2e23-150">heic</span></span>
- <span data-ttu-id="d2e23-151">heif</span><span class="sxs-lookup"><span data-stu-id="d2e23-151">heif</span></span>
- <span data-ttu-id="d2e23-152">htm</span><span class="sxs-lookup"><span data-stu-id="d2e23-152">htm</span></span>
- <span data-ttu-id="d2e23-153">html</span><span class="sxs-lookup"><span data-stu-id="d2e23-153">html</span></span>
- <span data-ttu-id="d2e23-154">jpeg</span><span class="sxs-lookup"><span data-stu-id="d2e23-154">jpeg</span></span>
- <span data-ttu-id="d2e23-155">jpg</span><span class="sxs-lookup"><span data-stu-id="d2e23-155">jpg</span></span>
- <span data-ttu-id="d2e23-156">Markdown</span><span class="sxs-lookup"><span data-stu-id="d2e23-156">markdown</span></span>
- <span data-ttu-id="d2e23-157">md</span><span class="sxs-lookup"><span data-stu-id="d2e23-157">md</span></span>
- <span data-ttu-id="d2e23-158">msg</span><span class="sxs-lookup"><span data-stu-id="d2e23-158">msg</span></span>
- <span data-ttu-id="d2e23-159">pdf</span><span class="sxs-lookup"><span data-stu-id="d2e23-159">pdf</span></span>
- <span data-ttu-id="d2e23-160">png</span><span class="sxs-lookup"><span data-stu-id="d2e23-160">png</span></span>
- <span data-ttu-id="d2e23-161">ppt</span><span class="sxs-lookup"><span data-stu-id="d2e23-161">ppt</span></span>
- <span data-ttu-id="d2e23-162">pptx</span><span class="sxs-lookup"><span data-stu-id="d2e23-162">pptx</span></span>
- <span data-ttu-id="d2e23-163">rtf</span><span class="sxs-lookup"><span data-stu-id="d2e23-163">rtf</span></span>
- <span data-ttu-id="d2e23-164">tif</span><span class="sxs-lookup"><span data-stu-id="d2e23-164">tif</span></span>
- <span data-ttu-id="d2e23-165">tiff</span><span class="sxs-lookup"><span data-stu-id="d2e23-165">tiff</span></span>
- <span data-ttu-id="d2e23-166">txt</span><span class="sxs-lookup"><span data-stu-id="d2e23-166">txt</span></span>
- <span data-ttu-id="d2e23-167">xls</span><span class="sxs-lookup"><span data-stu-id="d2e23-167">xls</span></span>
- <span data-ttu-id="d2e23-168">xlsx</span><span class="sxs-lookup"><span data-stu-id="d2e23-168">xlsx</span></span>



## <a name="see-also"></a><span data-ttu-id="d2e23-169">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d2e23-169">See Also</span></span>
[<span data-ttu-id="d2e23-170">Créer un classificateur</span><span class="sxs-lookup"><span data-stu-id="d2e23-170">Create a classifier</span></span>](create-a-classifier.md)

[<span data-ttu-id="d2e23-171">Créer un extracteur</span><span class="sxs-lookup"><span data-stu-id="d2e23-171">Create an extractor</span></span>](create-an-extractor.md)

[<span data-ttu-id="d2e23-172">Créer un centre de contenu</span><span class="sxs-lookup"><span data-stu-id="d2e23-172">Create a content center</span></span>](create-a-content-center.md)

[<span data-ttu-id="d2e23-173">Créer un modèle de traitement de formulaire</span><span class="sxs-lookup"><span data-stu-id="d2e23-173">Create a form processing model</span></span>](create-a-form-processing-model.md)

[<span data-ttu-id="d2e23-174">Appliquer un modèle</span><span class="sxs-lookup"><span data-stu-id="d2e23-174">Apply a model</span></span>](apply-a-model.md)   

[<span data-ttu-id="d2e23-175">Différence entre la compréhension de document et les modèles de traitement de formulaire</span><span class="sxs-lookup"><span data-stu-id="d2e23-175">Difference between a document understanding and a form processing model</span></span>](difference-between-document-understanding-and-form-processing-model.md)
  
[<span data-ttu-id="d2e23-176">Vue d’ensemble du traitement des formulaires</span><span class="sxs-lookup"><span data-stu-id="d2e23-176">Form processing overview</span></span>](form-processing-overview.md)

[<span data-ttu-id="d2e23-177">Mode d’accessibilité Syntex de SharePoint</span><span class="sxs-lookup"><span data-stu-id="d2e23-177">SharePoint Syntex Accessibility Mode</span></span>](accessibility-mode.md)