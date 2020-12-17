---
title: Présentation de la compréhension de document
ms.author: efrene
author: efrene
manager: pamgreen
audience: admin
ms.topic: article
ms.prod: microsoft-365-enterprise
search.appverid: ''
ms.collection: enabler-strategic
localization_priority: Priority
description: Obtenez une vue d’ensemble de la compréhension des documents dans Microsoft SharePoint Syntex.
ms.openlocfilehash: 5dd44a119dff6f5d194861c381fa28f76a6f0da7
ms.sourcegitcommit: f231eece2927f0d01072fd092db1eab15525bbc2
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "49701106"
---
# <a name="document-understanding-overview"></a><span data-ttu-id="6aa8e-103">Présentation de la compréhension de document</span><span class="sxs-lookup"><span data-stu-id="6aa8e-103">Document understanding overview</span></span>


</br>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4CSu7] 

</br>

<span data-ttu-id="6aa8e-104">La compréhension de document utilise les modèles de renseignements artificiels pour automatiser la classification des fichiers et l’extraction des informations.</span><span class="sxs-lookup"><span data-stu-id="6aa8e-104">Document understanding uses artificial intelligence (AI) models to automate classification of files and extraction of information.</span></span> <span data-ttu-id="6aa8e-105">Il fonctionne de façon optimale avec les documents non structurés, tels que les lettres ou les contrats.</span><span class="sxs-lookup"><span data-stu-id="6aa8e-105">It works best with unstructured documents, such as letters or contracts.</span></span> <span data-ttu-id="6aa8e-106">Ces documents doivent comporter du texte qui peut être identifié sur la base de phrases ou de modèles.</span><span class="sxs-lookup"><span data-stu-id="6aa8e-106">These documents must have text that can be identified based on phrases or patterns.</span></span> <span data-ttu-id="6aa8e-107">Le texte identifié désigne à la fois le type de fichier (sa classification) et ce que vous voulez extraire (ses extracteurs).</span><span class="sxs-lookup"><span data-stu-id="6aa8e-107">The identified text designates both the type of file it is (its classification) and what you'd like to extract (its extractors).</span></span>

> [!NOTE]
> <span data-ttu-id="6aa8e-108">Pour plus d’informations sur les exemples de scénarios relatifs aux exemples de scénarios, consultez l’article [SharePoint Syntex adoption : Guide de démarrage](https://docs.microsoft.com/microsoft-365/contentunderstanding/adoption-getstarted#document-understanding-scenario-example).</span><span class="sxs-lookup"><span data-stu-id="6aa8e-108">See the [SharePoint Syntex adoption: Get started guide](https://docs.microsoft.com/microsoft-365/contentunderstanding/adoption-getstarted#document-understanding-scenario-example) for more information about document understanding scenario examples.</span></span>

<span data-ttu-id="6aa8e-109">Les modèles de compréhension de document sont créés et gérés dans un site de type SharePoint appelé un *centre de contenu* .</span><span class="sxs-lookup"><span data-stu-id="6aa8e-109">Document understanding models are created and managed in a type of SharePoint site called a *content center*.</span></span> <span data-ttu-id="6aa8e-110">Lorsqu’il est appliqué à une bibliothèque de documents SharePoint, le modèle associé à un type de contenu inclut des colonnes pour stocker les informations extraites.</span><span class="sxs-lookup"><span data-stu-id="6aa8e-110">When applied to a SharePoint document library, the model is associated with a content type has columns to store the information being extracted.</span></span> <span data-ttu-id="6aa8e-111">Le type de contenu que vous créez est stocké dans la Galerie de types de contenu SharePoint.</span><span class="sxs-lookup"><span data-stu-id="6aa8e-111">The content type you create is stored in the SharePoint content type gallery.</span></span> <span data-ttu-id="6aa8e-112">Vous pouvez également choisir d’utiliser des types de contenu existants pour utiliser leur schéma.</span><span class="sxs-lookup"><span data-stu-id="6aa8e-112">You can also choose to use existing content types to use their schema.</span></span>

> [!NOTE]
> <span data-ttu-id="6aa8e-113">Les types de contenus scellés ou en lecture seule ne peuvent pas être mis à jour. Ils ne peuvent donc pas être utilisés dans un modèle.</span><span class="sxs-lookup"><span data-stu-id="6aa8e-113">Read-only or sealed content types cannot be updated, so they cannot be used in a model.</span></span>

<span data-ttu-id="6aa8e-114">Ajoutez des *classificateurs* et des *extracteurs* à votre document présentation des modèles pour effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="6aa8e-114">Add *classifiers* and *extractors* to your document understanding models to do the following:</span></span> 

- <span data-ttu-id="6aa8e-115">Les classificateurs sont utilisés pour identifier et classer les documents téléchargés vers la bibliothèque de documents.</span><span class="sxs-lookup"><span data-stu-id="6aa8e-115">Classifiers are used to identify and classify documents that are uploaded to the document library.</span></span> <span data-ttu-id="6aa8e-116">Par exemple, un classifieur peut être « exercé » pour identifier tous les documents *renouvellement de contrat* qui sont chargés dans la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="6aa8e-116">For example, a classifier can be "trained" to identify all *contract renewal* documents that are uploaded to the library.</span></span> <span data-ttu-id="6aa8e-117">Le type de contenu renouvellement contrat est défini par vous lorsque vous créez votre classifieur.</span><span class="sxs-lookup"><span data-stu-id="6aa8e-117">The contract renewal content type is defined by you when you create your classifier.</span></span>

- <span data-ttu-id="6aa8e-118">Les extracteurs extraient des informations de ces documents.</span><span class="sxs-lookup"><span data-stu-id="6aa8e-118">Extractors pull information from these documents.</span></span> <span data-ttu-id="6aa8e-119">Par exemple, pour tous les documents de renouvellement de contrat identifiés dans votre bibliothèque de documents, les colonnes s’affichent dans votre affichage qui indiquent également la *date de début du service* et *client* pour chaque document de renouvellement de contrat.</span><span class="sxs-lookup"><span data-stu-id="6aa8e-119">For example, for all contract renewal documents identified in your document library, columns display in your view that also show the *Service Start Date* and  *Client* for each contract renewal document.</span></span> 

<span data-ttu-id="6aa8e-120">Vous pouvez utiliser des fichiers d’exemple pour former et tester vos classificateurs et extracteurs de votre modèle.</span><span class="sxs-lookup"><span data-stu-id="6aa8e-120">You can use example files to train and test your classifiers and extractors in your model.</span></span> <span data-ttu-id="6aa8e-121">Les exemples de fichiers fournissent vos exemples de modèles à rechercher lorsque vous essayez d’identifier et d’extraire des données de fichiers.</span><span class="sxs-lookup"><span data-stu-id="6aa8e-121">Example files provide your model examples of what to look for when trying to identify and extract data from files.</span></span> <span data-ttu-id="6aa8e-122">Par exemple, vous devez former vos classificateurs et extracteurs de renouvellement de contrat avec des exemples de documents de renouvellement de contrat que votre entreprise utilise.</span><span class="sxs-lookup"><span data-stu-id="6aa8e-122">For example, you would train your contract renewal classifiers and extractors with examples of contract renewal documents your company works with.</span></span> <span data-ttu-id="6aa8e-123">Vous pouvez également utiliser des exemples de fichiers pour tester l’efficacité de votre modèle.</span><span class="sxs-lookup"><span data-stu-id="6aa8e-123">You can also use example files to test the effectiveness of your model.</span></span>

> [!NOTE]
> <span data-ttu-id="6aa8e-124">Si vous utilisez la technologie de reconnaissance optique des caractères (OCR) pour numériser des documents, Syntex possède une limite de 15 pages pour la formation sur le modèle.</span><span class="sxs-lookup"><span data-stu-id="6aa8e-124">If you use optical character recognition (OCR) technology to scan documents, Syntex has a 15-page limit for model training.</span></span>

<span data-ttu-id="6aa8e-125">Une fois que vous avez publié votre modèle, utilisez le centre de contenu pour l’appliquer à toute bibliothèque de documents SharePoint à laquelle vous avez accès.</span><span class="sxs-lookup"><span data-stu-id="6aa8e-125">After publishing your model, use the content center to apply it to any SharePoint document library that you have access to.</span></span>  

## <a name="see-also"></a><span data-ttu-id="6aa8e-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6aa8e-126">See Also</span></span>
[<span data-ttu-id="6aa8e-127">Créer un classificateur</span><span class="sxs-lookup"><span data-stu-id="6aa8e-127">Create a classifier</span></span>](create-a-classifier.md)

[<span data-ttu-id="6aa8e-128">Créer un extracteur</span><span class="sxs-lookup"><span data-stu-id="6aa8e-128">Create an extractor</span></span>](create-an-extractor.md)

[<span data-ttu-id="6aa8e-129">Créer un centre de contenu</span><span class="sxs-lookup"><span data-stu-id="6aa8e-129">Create a content center</span></span>](create-a-content-center.md)

[<span data-ttu-id="6aa8e-130">Créer un modèle de traitement de formulaire</span><span class="sxs-lookup"><span data-stu-id="6aa8e-130">Create a form processing model</span></span>](create-a-form-processing-model.md)

[<span data-ttu-id="6aa8e-131">Appliquer un modèle</span><span class="sxs-lookup"><span data-stu-id="6aa8e-131">Apply a model</span></span>](apply-a-model.md)   

[<span data-ttu-id="6aa8e-132">Différence entre la compréhension de document et les modèles de traitement de formulaire</span><span class="sxs-lookup"><span data-stu-id="6aa8e-132">Difference between a document understanding and a form processing model</span></span>](difference-between-document-understanding-and-form-processing-model.md)
  
[<span data-ttu-id="6aa8e-133">Vue d’ensemble du traitement des formulaires</span><span class="sxs-lookup"><span data-stu-id="6aa8e-133">Form processing overview</span></span>](form-processing-overview.md)
