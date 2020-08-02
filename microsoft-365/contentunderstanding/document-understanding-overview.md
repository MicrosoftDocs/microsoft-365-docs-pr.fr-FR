---
title: Vue d’ensemble du document de présentation (aperçu)
ms.author: efrene
author: efrene
manager: pamgreen
ms.date: 08/1/2020
audience: admin
ms.topic: article
ms.service: ''
search.appverid: ''
localization_priority: Normal
ROBOTS: NOINDEX, NOFOLLOW
description: Obtenez une vue d’ensemble de la compréhension des documents dans le projet cortex.
ms.openlocfilehash: 13b0aa3742c6cf1c0c1123996c683d13c6577876
ms.sourcegitcommit: ea5e2f85bd6b609658545b120c7e08789b9686fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/01/2020
ms.locfileid: "46537134"
---
# <a name="document-understanding-overview-preview"></a><span data-ttu-id="11497-103">Vue d’ensemble du document de présentation (aperçu)</span><span class="sxs-lookup"><span data-stu-id="11497-103">Document understanding overview (Preview)</span></span>
> [!Note] 
> <span data-ttu-id="11497-104">Le projet cortex est actuellement en préversion.</span><span class="sxs-lookup"><span data-stu-id="11497-104">Project Cortex is currently in Preview.</span></span> <span data-ttu-id="11497-105">Pour [plus d’informations sur le projet cortex](https://aka.ms/projectcortex).</span><span class="sxs-lookup"><span data-stu-id="11497-105">[Find out more about Project Cortex](https://aka.ms/projectcortex).</span></span>

</br>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4CSu7] 

</br>

<span data-ttu-id="11497-106">Document comprendre utilise les modèles AI pour automatiser la classification des fichiers et l’extraction des informations.</span><span class="sxs-lookup"><span data-stu-id="11497-106">Document understanding uses AI models to automate classification of files and extraction of information.</span></span> <span data-ttu-id="11497-107">Elle fonctionne mieux avec des documents non structurés, tels que des lettres ou des contrats.</span><span class="sxs-lookup"><span data-stu-id="11497-107">It works best with unstructured documents, like letters or contracts.</span></span> <span data-ttu-id="11497-108">Les documents doivent contenir du texte qui peut être identifié en fonction d’expressions ou de modèles.</span><span class="sxs-lookup"><span data-stu-id="11497-108">The documents should have text that can be identified based on phrases or patterns.</span></span> <span data-ttu-id="11497-109">Le texte identifié peut désigner à la fois le type de fichier dont il est (sa classification) et ce que vous souhaitez extraire (ses extracteurs).</span><span class="sxs-lookup"><span data-stu-id="11497-109">The identified text can designate both the type of file it is (its classification) and what you'd like to extract (its extractors).</span></span>

<span data-ttu-id="11497-110">Les modèles de présentation des documents sont créés et gérés dans un type de site SharePoint appelé centre de contenu.</span><span class="sxs-lookup"><span data-stu-id="11497-110">Document understanding models are created and managed in a type of SharePoint site called a content center.</span></span> <span data-ttu-id="11497-111">Lorsqu’il est appliqué à une bibliothèque de documents SharePoint, le modèle est associé à un type de contenu qui contient des colonnes pour stocker les informations extraites.</span><span class="sxs-lookup"><span data-stu-id="11497-111">When applied to a SharePoint document library, the model is associated with a content type which has columns to store the information extracted.</span></span> <span data-ttu-id="11497-112">Le type de contenu que vous créez est stocké dans la Galerie de types de contenu SharePoint.</span><span class="sxs-lookup"><span data-stu-id="11497-112">The content type you create is stored in the SharePoint content type gallery.</span></span> <span data-ttu-id="11497-113">Vous pouvez également choisir d’utiliser des types de contenu existants afin d’utiliser leur schéma.</span><span class="sxs-lookup"><span data-stu-id="11497-113">You can also choose to use existing content types in order to use their schema.</span></span>

<span data-ttu-id="11497-114">Vous pouvez ajouter des *classifieurs* et des *extracteurs* à vos modèles de présentation de documents pour effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="11497-114">You can add *classifiers* and *extractors* to your document understanding models to do the following:</span></span> 

- <span data-ttu-id="11497-115">Les classifieurs sont utilisés pour identifier et classer les documents qui sont chargés dans la bibliothèque de documents.</span><span class="sxs-lookup"><span data-stu-id="11497-115">Classifiers are used to identify and classify documents that are uploaded to the document library.</span></span> <span data-ttu-id="11497-116">Par exemple, un classifieur peut être « formé » pour identifier tous les documents de *renouvellement de contrat* téléchargés dans la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="11497-116">For example, a classifier can be "trained" to identify all *contract renewal* documents that are uploaded to the library.</span></span> <span data-ttu-id="11497-117">Le type de contenu renouvellement de contrat est défini par vous lors de la création de votre classifieur.</span><span class="sxs-lookup"><span data-stu-id="11497-117">The contract renewal content type is defined by you when you create your classifier.</span></span>

- <span data-ttu-id="11497-118">Les extracteurs extraient des informations de ces documents.</span><span class="sxs-lookup"><span data-stu-id="11497-118">Extractors pull information from these documents.</span></span> <span data-ttu-id="11497-119">Par exemple, pour tous les documents de renouvellement de contrat identifiés dans votre bibliothèque de documents, les colonnes s’affichent dans votre affichage qui indique également la *Date de début du service* et le *client* pour chaque document de renouvellement de contrat.</span><span class="sxs-lookup"><span data-stu-id="11497-119">For example, for all contract renewal documents that are identified in your document library, columns will display in your view that will also show the *Service Start Date* and  *Client* for each contract renewal document.</span></span> 

<span data-ttu-id="11497-120">Vous utilisez des exemples de fichiers pour former et tester vos classifieurs et extracteurs dans votre modèle.</span><span class="sxs-lookup"><span data-stu-id="11497-120">You use example files to train and test your classifiers and extractors in your model.</span></span> <span data-ttu-id="11497-121">Les exemples de fichiers fournissent des exemples de modèles de ce que vous pouvez rechercher lorsque vous essayez d’identifier et d’extraire des données à partir de fichiers.</span><span class="sxs-lookup"><span data-stu-id="11497-121">Example files provide your model examples of what to look for when trying to identify and extract data from files.</span></span> <span data-ttu-id="11497-122">Par exemple, vous allez former vos classifieurs et extracteurs de renouvellement de contrat avec des exemples de documents de renouvellement de contrat avec lesquels votre société travaille.</span><span class="sxs-lookup"><span data-stu-id="11497-122">For example, you would train your contract renewal classifiers and extractors with examples of contract renewal documents your company works with.</span></span> <span data-ttu-id="11497-123">Vous pouvez également utiliser des exemples de fichiers pour tester l’efficacité de votre modèle.</span><span class="sxs-lookup"><span data-stu-id="11497-123">You can also use example files to test the effectiveness of your model.</span></span>

<span data-ttu-id="11497-124">Après avoir publié votre modèle, utilisez le centre de contenu pour l’appliquer à n’importe quelle bibliothèque de documents SharePoint à laquelle vous avez accès.</span><span class="sxs-lookup"><span data-stu-id="11497-124">After publishing your model, use the content center to apply it to any SharePoint document library that you have access to.</span></span>  


## <a name="see-also"></a><span data-ttu-id="11497-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="11497-125">See Also</span></span>
[<span data-ttu-id="11497-126">Créer un classifieur</span><span class="sxs-lookup"><span data-stu-id="11497-126">Create a classifier</span></span>](create-a-classifier.md)</br>
[<span data-ttu-id="11497-127">Créer un extracteur</span><span class="sxs-lookup"><span data-stu-id="11497-127">Create an extractor</span></span>](create-an-extractor.md)</br>
<span data-ttu-id="11497-128">[Créer un centre](create-a-content-center.md) 
 de contenu [Créer un modèle de traitement de formulaire](create-a-form-processing-model.md)</span><span class="sxs-lookup"><span data-stu-id="11497-128">[Create a content center](create-a-content-center.md)
[Create a form processing model](create-a-form-processing-model.md)</span></span></br>
<span data-ttu-id="11497-129">[Appliquer un modèle](apply-a-model.md) </span><span class="sxs-lookup"><span data-stu-id="11497-129">[Apply a model](apply-a-model.md) </span></span>  
[<span data-ttu-id="11497-130">Différence entre une présentation de document et un modèle de traitement de formulaire</span><span class="sxs-lookup"><span data-stu-id="11497-130">Difference between a document understanding and a form processing model</span></span>](difference-between-document-understanding-and-form-processing-model.md)  
[<span data-ttu-id="11497-131">Vue d’ensemble du traitement des formulaires</span><span class="sxs-lookup"><span data-stu-id="11497-131">Form processing overview</span></span>](form-processing-overview.md)




