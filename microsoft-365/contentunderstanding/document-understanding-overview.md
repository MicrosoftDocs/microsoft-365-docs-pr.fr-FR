---
title: Présentation de la compréhension de document
ms.author: efrene
author: efrene
manager: pamgreen
audience: admin
ms.topic: article
ms.prod: microsoft-365-enterprise
search.appverid: ''
localization_priority: Priority
description: Obtenez une vue d’ensemble de la compréhension des documents dans Microsoft SharePoint Syntex.
ms.openlocfilehash: 3f2c463d3713048ffff7c20f2fcf6220d55d6a32
ms.sourcegitcommit: f7ca339bdcad38796c550064fb152ea09687d0f3
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/30/2020
ms.locfileid: "48321772"
---
# <a name="document-understanding-overview"></a><span data-ttu-id="f7fd5-103">Présentation de la compréhension de document</span><span class="sxs-lookup"><span data-stu-id="f7fd5-103">Document understanding overview</span></span>


</br>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4CSu7] 

</br>

<span data-ttu-id="f7fd5-104">La compréhension de document utilise les modèles de renseignements artificiels pour automatiser la classification des fichiers et l’extraction des informations.</span><span class="sxs-lookup"><span data-stu-id="f7fd5-104">Document understanding uses artificial intelligence (AI) models to automate classification of files and extraction of information.</span></span> <span data-ttu-id="f7fd5-105">Il fonctionne de façon optimale avec les documents non structurés, tels que les lettres ou les contrats.</span><span class="sxs-lookup"><span data-stu-id="f7fd5-105">It works best with unstructured documents, such as letters or contracts.</span></span> <span data-ttu-id="f7fd5-106">Ces documents doivent comporter du texte qui peut être identifié sur la base de phrases ou de modèles.</span><span class="sxs-lookup"><span data-stu-id="f7fd5-106">These documents must have text that can be identified based on phrases or patterns.</span></span> <span data-ttu-id="f7fd5-107">Le texte identifié désigne à la fois le type de fichier (sa classification) et ce que vous voulez extraire (ses extracteurs).</span><span class="sxs-lookup"><span data-stu-id="f7fd5-107">The identified text designates both the type of file it is (its classification) and what you'd like to extract (its extractors).</span></span>

<span data-ttu-id="f7fd5-108">Les modèles de compréhension de document sont créés et gérés dans un site de type SharePoint appelé un *centre de contenu* .</span><span class="sxs-lookup"><span data-stu-id="f7fd5-108">Document understanding models are created and managed in a type of SharePoint site called a *content center*.</span></span> <span data-ttu-id="f7fd5-109">Lorsqu’il est appliqué à une bibliothèque de documents SharePoint, le modèle associé à un type de contenu inclut des colonnes pour stocker les informations extraites.</span><span class="sxs-lookup"><span data-stu-id="f7fd5-109">When applied to a SharePoint document library, the model is associated with a content type has columns to store the information being extracted.</span></span> <span data-ttu-id="f7fd5-110">Le type de contenu que vous créez est stocké dans la Galerie de types de contenu SharePoint.</span><span class="sxs-lookup"><span data-stu-id="f7fd5-110">The content type you create is stored in the SharePoint content type gallery.</span></span> <span data-ttu-id="f7fd5-111">Vous pouvez également choisir d’utiliser des types de contenu existants pour utiliser leur schéma.</span><span class="sxs-lookup"><span data-stu-id="f7fd5-111">You can also choose to use existing content types to use their schema.</span></span>

<span data-ttu-id="f7fd5-112">Ajoutez des *classificateurs* et des *extracteurs* à votre document présentation des modèles pour effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="f7fd5-112">Add *classifiers* and *extractors* to your document understanding models to do the following:</span></span> 

- <span data-ttu-id="f7fd5-113">Les classificateurs sont utilisés pour identifier et classer les documents téléchargés vers la bibliothèque de documents.</span><span class="sxs-lookup"><span data-stu-id="f7fd5-113">Classifiers are used to identify and classify documents that are uploaded to the document library.</span></span> <span data-ttu-id="f7fd5-114">Par exemple, un classifieur peut être « exercé » pour identifier tous les documents*renouvellement de contrat* qui sont chargés dans la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="f7fd5-114">For example, a classifier can be "trained" to identify all *contract renewal* documents that are uploaded to the library.</span></span> <span data-ttu-id="f7fd5-115">Le type de contenu renouvellement contrat est défini par vous lorsque vous créez votre classifieur.</span><span class="sxs-lookup"><span data-stu-id="f7fd5-115">The contract renewal content type is defined by you when you create your classifier.</span></span>

- <span data-ttu-id="f7fd5-116">Les extracteurs extraient des informations de ces documents.</span><span class="sxs-lookup"><span data-stu-id="f7fd5-116">Extractors pull information from these documents.</span></span> <span data-ttu-id="f7fd5-117">Par exemple, pour tous les documents de renouvellement de contrat identifiés dans votre bibliothèque de documents, les colonnes s’affichent dans votre affichage qui indiquent également la *date de début du service* et *client* pour chaque document de renouvellement de contrat.</span><span class="sxs-lookup"><span data-stu-id="f7fd5-117">For example, for all contract renewal documents identified in your document library, columns display in your view that also show the *Service Start Date* and  *Client* for each contract renewal document.</span></span> 

<span data-ttu-id="f7fd5-118">Vous pouvez utiliser des fichiers d’exemple pour former et tester vos classificateurs et extracteurs de votre modèle.</span><span class="sxs-lookup"><span data-stu-id="f7fd5-118">You can use example files to train and test your classifiers and extractors in your model.</span></span> <span data-ttu-id="f7fd5-119">Les exemples de fichiers fournissent vos exemples de modèles à rechercher lorsque vous essayez d’identifier et d’extraire des données de fichiers.</span><span class="sxs-lookup"><span data-stu-id="f7fd5-119">Example files provide your model examples of what to look for when trying to identify and extract data from files.</span></span> <span data-ttu-id="f7fd5-120">Par exemple, vous devez former vos classificateurs et extracteurs de renouvellement de contrat avec des exemples de documents de renouvellement de contrat que votre entreprise utilise.</span><span class="sxs-lookup"><span data-stu-id="f7fd5-120">For example, you would train your contract renewal classifiers and extractors with examples of contract renewal documents your company works with.</span></span> <span data-ttu-id="f7fd5-121">Vous pouvez également utiliser des exemples de fichiers pour tester l’efficacité de votre modèle.</span><span class="sxs-lookup"><span data-stu-id="f7fd5-121">You can also use example files to test the effectiveness of your model.</span></span>

<span data-ttu-id="f7fd5-122">Une fois que vous avez publié votre modèle, utilisez le centre de contenu pour l’appliquer à toute bibliothèque de documents SharePoint à laquelle vous avez accès.</span><span class="sxs-lookup"><span data-stu-id="f7fd5-122">After publishing your model, use the content center to apply it to any SharePoint document library that you have access to.</span></span>  



## <a name="see-also"></a><span data-ttu-id="f7fd5-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f7fd5-123">See Also</span></span>
[<span data-ttu-id="f7fd5-124">Créer un classificateur</span><span class="sxs-lookup"><span data-stu-id="f7fd5-124">Create a classifier</span></span>](create-a-classifier.md)

[<span data-ttu-id="f7fd5-125">Créer un extracteur</span><span class="sxs-lookup"><span data-stu-id="f7fd5-125">Create an extractor</span></span>](create-an-extractor.md)

[<span data-ttu-id="f7fd5-126">Créer un centre de contenu</span><span class="sxs-lookup"><span data-stu-id="f7fd5-126">Create a content center</span></span>](create-a-content-center.md)

[<span data-ttu-id="f7fd5-127">Créer un modèle de traitement de formulaire</span><span class="sxs-lookup"><span data-stu-id="f7fd5-127">Create a form processing model</span></span>](create-a-form-processing-model.md)

[<span data-ttu-id="f7fd5-128">Appliquer un modèle</span><span class="sxs-lookup"><span data-stu-id="f7fd5-128">Apply a model</span></span>](apply-a-model.md)   

[<span data-ttu-id="f7fd5-129">Différence entre la compréhension de document et les modèles de traitement de formulaire</span><span class="sxs-lookup"><span data-stu-id="f7fd5-129">Difference between a document understanding and a form processing model</span></span>](difference-between-document-understanding-and-form-processing-model.md)
  
[<span data-ttu-id="f7fd5-130">Vue d’ensemble du traitement des formulaires</span><span class="sxs-lookup"><span data-stu-id="f7fd5-130">Form processing overview</span></span>](form-processing-overview.md)
