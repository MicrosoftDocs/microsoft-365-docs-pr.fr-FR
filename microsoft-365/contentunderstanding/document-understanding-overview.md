---
title: Présentation de l’explication des documents
ms.author: efrene
author: efrene
manager: pamgreen
ms.date: 08/1/2020
audience: admin
ms.topic: article
ms.prod: microsoft-365-enterprise
search.appverid: ''
localization_priority: None
ROBOTS: NOINDEX, NOFOLLOW
description: Obtenir une vue d’ensemble de la compréhension des documents dans Microsoft SharePoint Syntex.
ms.openlocfilehash: dd8731759d8f1cbea57d171fa7a803ffc4f1baa7
ms.sourcegitcommit: 15be7822220041c25fc52565f1c64d252e442d89
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/28/2020
ms.locfileid: "48294759"
---
# <a name="document-understanding-overview"></a><span data-ttu-id="d6ea8-103">Présentation de l’explication des documents</span><span class="sxs-lookup"><span data-stu-id="d6ea8-103">Document understanding overview</span></span>


</br>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4CSu7] 

</br>

<span data-ttu-id="d6ea8-104">Le mémorandum d’accord sur les documents utilise les modèles d’intelligence artificielle pour automatiser la classification des fichiers et l’extraction des informations.</span><span class="sxs-lookup"><span data-stu-id="d6ea8-104">Document understanding uses artificial intelligence (AI) models to automate classification of files and extraction of information.</span></span> <span data-ttu-id="d6ea8-105">Il fonctionne de manière optimale avec des documents non structurés, tels que des lettres ou des contrats.</span><span class="sxs-lookup"><span data-stu-id="d6ea8-105">It works best with unstructured documents, such as letters or contracts.</span></span> <span data-ttu-id="d6ea8-106">Ces documents doivent contenir du texte qui peut être identifié en fonction d’expressions ou de modèles.</span><span class="sxs-lookup"><span data-stu-id="d6ea8-106">These documents must have text that can be identified based on phrases or patterns.</span></span> <span data-ttu-id="d6ea8-107">Le texte identifié désigne à la fois le type de fichier dont il est (sa classification) et ce que vous souhaitez extraire (ses extracteurs).</span><span class="sxs-lookup"><span data-stu-id="d6ea8-107">The identified text designates both the type of file it is (its classification) and what you'd like to extract (its extractors).</span></span>

<span data-ttu-id="d6ea8-108">Les modèles de présentation des documents sont créés et gérés dans un type de site SharePoint appelé *Centre de contenu*.</span><span class="sxs-lookup"><span data-stu-id="d6ea8-108">Document understanding models are created and managed in a type of SharePoint site called a *content center*.</span></span> <span data-ttu-id="d6ea8-109">Lorsqu’il est appliqué à une bibliothèque de documents SharePoint, le modèle associé à un type de contenu comporte des colonnes pour stocker les informations extraites.</span><span class="sxs-lookup"><span data-stu-id="d6ea8-109">When applied to a SharePoint document library, the model is associated with a content type has columns to store the information being extracted.</span></span> <span data-ttu-id="d6ea8-110">Le type de contenu que vous créez est stocké dans la Galerie de types de contenu SharePoint.</span><span class="sxs-lookup"><span data-stu-id="d6ea8-110">The content type you create is stored in the SharePoint content type gallery.</span></span> <span data-ttu-id="d6ea8-111">Vous pouvez également choisir d’utiliser des types de contenu existants pour utiliser leur schéma.</span><span class="sxs-lookup"><span data-stu-id="d6ea8-111">You can also choose to use existing content types to use their schema.</span></span>

<span data-ttu-id="d6ea8-112">Ajoutez des *classifieurs* et des *extracteurs* à vos documents de présentation des modèles pour effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="d6ea8-112">Add *classifiers* and *extractors* to your document understanding models to do the following:</span></span> 

- <span data-ttu-id="d6ea8-113">Les classifieurs sont utilisés pour identifier et classer les documents qui sont chargés dans la bibliothèque de documents.</span><span class="sxs-lookup"><span data-stu-id="d6ea8-113">Classifiers are used to identify and classify documents that are uploaded to the document library.</span></span> <span data-ttu-id="d6ea8-114">Par exemple, un classifieur peut être « formé » pour identifier tous les documents de *renouvellement de contrat* téléchargés dans la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="d6ea8-114">For example, a classifier can be "trained" to identify all *contract renewal* documents that are uploaded to the library.</span></span> <span data-ttu-id="d6ea8-115">Le type de contenu renouvellement de contrat est défini par vous lors de la création de votre classifieur.</span><span class="sxs-lookup"><span data-stu-id="d6ea8-115">The contract renewal content type is defined by you when you create your classifier.</span></span>

- <span data-ttu-id="d6ea8-116">Les extracteurs extraient des informations de ces documents.</span><span class="sxs-lookup"><span data-stu-id="d6ea8-116">Extractors pull information from these documents.</span></span> <span data-ttu-id="d6ea8-117">Par exemple, pour tous les documents de renouvellement de contrat identifiés dans votre bibliothèque de documents, les colonnes s’affichent dans votre vue, qui indiquent également la *Date de début du service* et le  *client* pour chaque document de renouvellement de contrat.</span><span class="sxs-lookup"><span data-stu-id="d6ea8-117">For example, for all contract renewal documents identified in your document library, columns display in your view that also show the *Service Start Date* and  *Client* for each contract renewal document.</span></span> 

<span data-ttu-id="d6ea8-118">Vous pouvez utiliser des fichiers d’exemple pour former et tester vos classifieurs et extracteurs dans votre modèle.</span><span class="sxs-lookup"><span data-stu-id="d6ea8-118">You can use sample files to train and test your classifiers and extractors in your model.</span></span> <span data-ttu-id="d6ea8-119">Les fichiers d’exemple fournissent des exemples de modèles de ce que vous pouvez rechercher lorsque vous essayez d’identifier et d’extraire des données à partir de fichiers.</span><span class="sxs-lookup"><span data-stu-id="d6ea8-119">Sample files provide your model examples of what to look for when trying to identify and extract data from files.</span></span> <span data-ttu-id="d6ea8-120">Par exemple, vous allez former vos classifieurs et extracteurs de renouvellement de contrat avec des exemples de documents de renouvellement de contrat avec lesquels votre société travaille.</span><span class="sxs-lookup"><span data-stu-id="d6ea8-120">For example, you would train your contract renewal classifiers and extractors with samples of contract renewal documents your company works with.</span></span> <span data-ttu-id="d6ea8-121">Vous pouvez également utiliser des fichiers d’exemple pour tester l’efficacité de votre modèle.</span><span class="sxs-lookup"><span data-stu-id="d6ea8-121">You can also use sample files to test the effectiveness of your model.</span></span>

<span data-ttu-id="d6ea8-122">Après avoir publié votre modèle, utilisez le centre de contenu pour l’appliquer à n’importe quelle bibliothèque de documents SharePoint à laquelle vous avez accès.</span><span class="sxs-lookup"><span data-stu-id="d6ea8-122">After publishing your model, use the content center to apply it to any SharePoint document library that you have access to.</span></span>  


## <a name="see-also"></a><span data-ttu-id="d6ea8-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d6ea8-123">See Also</span></span>
[<span data-ttu-id="d6ea8-124">Créer un classifieur</span><span class="sxs-lookup"><span data-stu-id="d6ea8-124">Create a classifier</span></span>](create-a-classifier.md)</br>
[<span data-ttu-id="d6ea8-125">Créer un extracteur</span><span class="sxs-lookup"><span data-stu-id="d6ea8-125">Create an extractor</span></span>](create-an-extractor.md)</br>
<span data-ttu-id="d6ea8-126">[Créer un centre](create-a-content-center.md) 
 de contenu [Créer un modèle de traitement de formulaire](create-a-form-processing-model.md)</span><span class="sxs-lookup"><span data-stu-id="d6ea8-126">[Create a content center](create-a-content-center.md)
[Create a form processing model](create-a-form-processing-model.md)</span></span></br>
<span data-ttu-id="d6ea8-127">[Appliquer un modèle](apply-a-model.md) </span><span class="sxs-lookup"><span data-stu-id="d6ea8-127">[Apply a model](apply-a-model.md) </span></span>  
[<span data-ttu-id="d6ea8-128">Différence entre une présentation de document et un modèle de traitement de formulaire</span><span class="sxs-lookup"><span data-stu-id="d6ea8-128">Difference between a document understanding and a form processing model</span></span>](difference-between-document-understanding-and-form-processing-model.md)  
[<span data-ttu-id="d6ea8-129">Vue d’ensemble du traitement des formulaires</span><span class="sxs-lookup"><span data-stu-id="d6ea8-129">Form processing overview</span></span>](form-processing-overview.md)
