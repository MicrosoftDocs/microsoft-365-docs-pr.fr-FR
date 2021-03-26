---
title: Présentation de la compréhension de document
ms.author: efrene
author: efrene
manager: pamgreen
audience: admin
ms.topic: article
ms.prod: microsoft-365-enterprise
search.appverid: ''
ms.collection:
- enabler-strategic
- m365initiative-syntex
localization_priority: Priority
description: Obtenez une vue d’ensemble de la compréhension des documents dans Microsoft SharePoint Syntex.
ms.openlocfilehash: 73e217e458fb9e1ccad8b64ffc81a6c9522a04f4
ms.sourcegitcommit: 1244bbc4a3d150d37980cab153505ca462fa7ddc
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/26/2021
ms.locfileid: "51222754"
---
# <a name="document-understanding-overview"></a><span data-ttu-id="3a488-103">Présentation de la compréhension de document</span><span class="sxs-lookup"><span data-stu-id="3a488-103">Document understanding overview</span></span>


</br>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4CSu7] 

</br>

<span data-ttu-id="3a488-104">La compréhension de document utilise les modèles de renseignements artificiels pour automatiser la classification des fichiers et l’extraction des informations.</span><span class="sxs-lookup"><span data-stu-id="3a488-104">Document understanding uses artificial intelligence (AI) models to automate classification of files and extraction of information.</span></span> <span data-ttu-id="3a488-105">Il fonctionne de façon optimale avec les documents non structurés, tels que les lettres ou les contrats.</span><span class="sxs-lookup"><span data-stu-id="3a488-105">It works best with unstructured documents, such as letters or contracts.</span></span> <span data-ttu-id="3a488-106">Ces documents doivent comporter du texte qui peut être identifié sur la base de phrases ou de modèles.</span><span class="sxs-lookup"><span data-stu-id="3a488-106">These documents must have text that can be identified based on phrases or patterns.</span></span> <span data-ttu-id="3a488-107">Le texte identifié désigne à la fois le type de fichier (sa classification) et ce que vous voulez extraire (ses extracteurs).</span><span class="sxs-lookup"><span data-stu-id="3a488-107">The identified text designates both the type of file it is (its classification) and what you'd like to extract (its extractors).</span></span>

> [!NOTE]
> <span data-ttu-id="3a488-108">Pour plus d’informations sur les exemples de scénarios relatifs aux exemples de scénarios, consultez l’article [SharePoint Syntex adoption : Guide de démarrage](./adoption-getstarted.md).</span><span class="sxs-lookup"><span data-stu-id="3a488-108">See the [SharePoint Syntex adoption: Get started guide](./adoption-getstarted.md) for more information about document understanding scenario examples.</span></span>

<span data-ttu-id="3a488-109">Les modèles de compréhension de document sont créés et gérés dans un site de type SharePoint appelé un *centre de contenu* .</span><span class="sxs-lookup"><span data-stu-id="3a488-109">Document understanding models are created and managed in a type of SharePoint site called a *content center*.</span></span> <span data-ttu-id="3a488-110">Lorsqu’il est appliqué à une bibliothèque de documents SharePoint, le modèle associé à un type de contenu inclut des colonnes pour stocker les informations extraites.</span><span class="sxs-lookup"><span data-stu-id="3a488-110">When applied to a SharePoint document library, the model is associated with a content type has columns to store the information being extracted.</span></span> <span data-ttu-id="3a488-111">Le type de contenu que vous créez est stocké dans la Galerie de types de contenu SharePoint.</span><span class="sxs-lookup"><span data-stu-id="3a488-111">The content type you create is stored in the SharePoint content type gallery.</span></span> <span data-ttu-id="3a488-112">Vous pouvez également choisir d’utiliser des types de contenu existants pour utiliser leur schéma.</span><span class="sxs-lookup"><span data-stu-id="3a488-112">You can also choose to use existing content types to use their schema.</span></span>

> [!NOTE]
> <span data-ttu-id="3a488-113">Les types de contenus scellés ou en lecture seule ne peuvent pas être mis à jour. Ils ne peuvent donc pas être utilisés dans un modèle.</span><span class="sxs-lookup"><span data-stu-id="3a488-113">Read-only or sealed content types cannot be updated, so they cannot be used in a model.</span></span>

<span data-ttu-id="3a488-114">Ajoutez des *classificateurs* et des *extracteurs* à votre document présentation des modèles pour effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="3a488-114">Add *classifiers* and *extractors* to your document understanding models to do the following:</span></span> 

- <span data-ttu-id="3a488-115">Les classificateurs sont utilisés pour identifier et classer les documents téléchargés vers la bibliothèque de documents.</span><span class="sxs-lookup"><span data-stu-id="3a488-115">Classifiers are used to identify and classify documents that are uploaded to the document library.</span></span> <span data-ttu-id="3a488-116">Par exemple, un classifieur peut être « exercé » pour identifier tous les documents *renouvellement de contrat* qui sont chargés dans la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="3a488-116">For example, a classifier can be "trained" to identify all *contract renewal* documents that are uploaded to the library.</span></span> <span data-ttu-id="3a488-117">Le type de contenu renouvellement contrat est défini par vous lorsque vous créez votre classifieur.</span><span class="sxs-lookup"><span data-stu-id="3a488-117">The contract renewal content type is defined by you when you create your classifier.</span></span>

- <span data-ttu-id="3a488-118">Les extracteurs extraient des informations de ces documents.</span><span class="sxs-lookup"><span data-stu-id="3a488-118">Extractors pull information from these documents.</span></span> <span data-ttu-id="3a488-119">Par exemple, pour tous les documents de renouvellement de contrat identifiés dans votre bibliothèque de documents, les colonnes s’affichent dans votre affichage qui indiquent également la *date de début du service* et *client* pour chaque document de renouvellement de contrat.</span><span class="sxs-lookup"><span data-stu-id="3a488-119">For example, for all contract renewal documents identified in your document library, columns display in your view that also show the *Service Start Date* and  *Client* for each contract renewal document.</span></span> 

<span data-ttu-id="3a488-120">Vous pouvez utiliser des fichiers d’exemple pour former et tester vos classificateurs et extracteurs de votre modèle.</span><span class="sxs-lookup"><span data-stu-id="3a488-120">You can use example files to train and test your classifiers and extractors in your model.</span></span> <span data-ttu-id="3a488-121">Les exemples de fichiers fournissent vos exemples de modèles à rechercher lorsque vous essayez d’identifier et d’extraire des données de fichiers.</span><span class="sxs-lookup"><span data-stu-id="3a488-121">Example files provide your model examples of what to look for when trying to identify and extract data from files.</span></span> <span data-ttu-id="3a488-122">Par exemple, vous devez former vos classificateurs et extracteurs de renouvellement de contrat avec des exemples de documents de renouvellement de contrat que votre entreprise utilise.</span><span class="sxs-lookup"><span data-stu-id="3a488-122">For example, you would train your contract renewal classifiers and extractors with examples of contract renewal documents your company works with.</span></span> <span data-ttu-id="3a488-123">Vous pouvez également utiliser des exemples de fichiers pour tester l’efficacité de votre modèle.</span><span class="sxs-lookup"><span data-stu-id="3a488-123">You can also use example files to test the effectiveness of your model.</span></span>

<span data-ttu-id="3a488-124">Une fois que vous avez publié votre modèle, utilisez le centre de contenu pour l’appliquer à toute bibliothèque de documents SharePoint à laquelle vous avez accès.</span><span class="sxs-lookup"><span data-stu-id="3a488-124">After publishing your model, use the content center to apply it to any SharePoint document library that you have access to.</span></span>  

### <a name="file-limitations"></a><span data-ttu-id="3a488-125">Limitations de fichier</span><span class="sxs-lookup"><span data-stu-id="3a488-125">File limitations</span></span>

<span data-ttu-id="3a488-126">Les modèles de compréhension des documents utilisent la technologie OCR (Optical Character Recognition) pour analyser les fichiers PDF, images et TIFF, à la fois lorsque vous entraînez un modèle avec des exemples de fichiers et lorsque vous l’exécutez sur des fichiers dans une bibliothèque de documents.</span><span class="sxs-lookup"><span data-stu-id="3a488-126">Document understanding models use Optical Character Recognition (OCR) technology to scan PDFs, images, and TIFF files, both when you train a model with example files and when you run the model against files in a document library.</span></span>

<span data-ttu-id="3a488-127">Notez les différences suivantes en ce qui concerne les fichiers texte Microsoft Office et les fichiers OCR numérisés (PDF, image ou TIFF) :</span><span class="sxs-lookup"><span data-stu-id="3a488-127">Note the following differences in regards to Microsoft Office text-based files and OCR-scanned files (PDF, image, or TIFF):</span></span>

- <span data-ttu-id="3a488-128">Fichiers Office : nous tronquons à 64 000 caractères (lors de la formation et de l’exécuter sur des fichiers dans une bibliothèque de documents).</span><span class="sxs-lookup"><span data-stu-id="3a488-128">Office files: We truncate at 64K characters (in training and when run against files in a document library).</span></span>
- <span data-ttu-id="3a488-129">Fichiers numérisés par OCR : la limite est de 20 pages.</span><span class="sxs-lookup"><span data-stu-id="3a488-129">OCR-scanned files: There is a 20 page limit.</span></span>  

#### <a name="supported-file-types"></a><span data-ttu-id="3a488-130">Types de fichiers pris en charge</span><span class="sxs-lookup"><span data-stu-id="3a488-130">Supported file types</span></span>

<span data-ttu-id="3a488-131">Les modèles de compréhension des documents suivent les types de fichiers suivants :</span><span class="sxs-lookup"><span data-stu-id="3a488-131">Document understanding models support the following file types:</span></span>

- <span data-ttu-id="3a488-132">doc</span><span class="sxs-lookup"><span data-stu-id="3a488-132">doc</span></span>
- <span data-ttu-id="3a488-133">docx</span><span class="sxs-lookup"><span data-stu-id="3a488-133">docx</span></span>
- <span data-ttu-id="3a488-134">eml</span><span class="sxs-lookup"><span data-stu-id="3a488-134">eml</span></span>
- <span data-ttu-id="3a488-135">heic</span><span class="sxs-lookup"><span data-stu-id="3a488-135">heic</span></span>
- <span data-ttu-id="3a488-136">heif</span><span class="sxs-lookup"><span data-stu-id="3a488-136">heif</span></span>
- <span data-ttu-id="3a488-137">htm</span><span class="sxs-lookup"><span data-stu-id="3a488-137">htm</span></span>
- <span data-ttu-id="3a488-138">html</span><span class="sxs-lookup"><span data-stu-id="3a488-138">html</span></span>
- <span data-ttu-id="3a488-139">jpeg</span><span class="sxs-lookup"><span data-stu-id="3a488-139">jpeg</span></span>
- <span data-ttu-id="3a488-140">jpg</span><span class="sxs-lookup"><span data-stu-id="3a488-140">jpg</span></span>
- <span data-ttu-id="3a488-141">Markdown</span><span class="sxs-lookup"><span data-stu-id="3a488-141">markdown</span></span>
- <span data-ttu-id="3a488-142">md</span><span class="sxs-lookup"><span data-stu-id="3a488-142">md</span></span>
- <span data-ttu-id="3a488-143">msg</span><span class="sxs-lookup"><span data-stu-id="3a488-143">msg</span></span>
- <span data-ttu-id="3a488-144">pdf</span><span class="sxs-lookup"><span data-stu-id="3a488-144">pdf</span></span>
- <span data-ttu-id="3a488-145">png</span><span class="sxs-lookup"><span data-stu-id="3a488-145">png</span></span>
- <span data-ttu-id="3a488-146">ppt</span><span class="sxs-lookup"><span data-stu-id="3a488-146">ppt</span></span>
- <span data-ttu-id="3a488-147">pptx</span><span class="sxs-lookup"><span data-stu-id="3a488-147">pptx</span></span>
- <span data-ttu-id="3a488-148">rtf</span><span class="sxs-lookup"><span data-stu-id="3a488-148">rtf</span></span>
- <span data-ttu-id="3a488-149">tif</span><span class="sxs-lookup"><span data-stu-id="3a488-149">tif</span></span>
- <span data-ttu-id="3a488-150">tiff</span><span class="sxs-lookup"><span data-stu-id="3a488-150">tiff</span></span>
- <span data-ttu-id="3a488-151">txt</span><span class="sxs-lookup"><span data-stu-id="3a488-151">txt</span></span>
- <span data-ttu-id="3a488-152">xls</span><span class="sxs-lookup"><span data-stu-id="3a488-152">xls</span></span>
- <span data-ttu-id="3a488-153">xlsx</span><span class="sxs-lookup"><span data-stu-id="3a488-153">xlsx</span></span>



## <a name="see-also"></a><span data-ttu-id="3a488-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a488-154">See Also</span></span>
[<span data-ttu-id="3a488-155">Créer un classificateur</span><span class="sxs-lookup"><span data-stu-id="3a488-155">Create a classifier</span></span>](create-a-classifier.md)

[<span data-ttu-id="3a488-156">Créer un extracteur</span><span class="sxs-lookup"><span data-stu-id="3a488-156">Create an extractor</span></span>](create-an-extractor.md)

[<span data-ttu-id="3a488-157">Créer un centre de contenu</span><span class="sxs-lookup"><span data-stu-id="3a488-157">Create a content center</span></span>](create-a-content-center.md)

[<span data-ttu-id="3a488-158">Créer un modèle de traitement de formulaire</span><span class="sxs-lookup"><span data-stu-id="3a488-158">Create a form processing model</span></span>](create-a-form-processing-model.md)

[<span data-ttu-id="3a488-159">Appliquer un modèle</span><span class="sxs-lookup"><span data-stu-id="3a488-159">Apply a model</span></span>](apply-a-model.md)   

[<span data-ttu-id="3a488-160">Différence entre la compréhension de document et les modèles de traitement de formulaire</span><span class="sxs-lookup"><span data-stu-id="3a488-160">Difference between a document understanding and a form processing model</span></span>](difference-between-document-understanding-and-form-processing-model.md)
  
[<span data-ttu-id="3a488-161">Vue d’ensemble du traitement des formulaires</span><span class="sxs-lookup"><span data-stu-id="3a488-161">Form processing overview</span></span>](form-processing-overview.md)

[<span data-ttu-id="3a488-162">Mode d’accessibilité Syntex de SharePoint</span><span class="sxs-lookup"><span data-stu-id="3a488-162">SharePoint Syntex Accessibility Mode</span></span>](accessibility-mode.md)