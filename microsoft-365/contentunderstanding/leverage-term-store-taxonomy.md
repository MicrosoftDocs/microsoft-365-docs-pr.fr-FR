---
title: Utiliser la taxonomie du magasin de termes lors de la création d’un extracteur
ms.author: efrene
author: efrene
manager: pamgreen
audience: admin
ms.topic: article
ms.prod: microsoft-365-enterprise
search.appverid: ''
ms.collection: enabler-strategic
localization_priority: Priority
description: Utilisez la taxonomie du magasin de termes lors de la création d’un extracteur dans votre modèle de compréhension de document via Microsoft SharePoint Syntex.
ms.openlocfilehash: cf396d14a497981389cc336c5efd121f36392181
ms.sourcegitcommit: c0495e224f12c448bfc162ef2e4b33b82f064ac8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "49709547"
---
# <a name="leverage-term-store-taxonomy-when-creating-an-extractor"></a><span data-ttu-id="b2841-103">Utiliser la taxonomie du magasin de termes lors de la création d’un extracteur</span><span class="sxs-lookup"><span data-stu-id="b2841-103">Leverage term store taxonomy when creating an extractor</span></span>

</br>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4GpJJ]  

</br>

<span data-ttu-id="b2841-104">Lorsque vous créez un extracteur dans votre modèle de compréhension de document via SharePoint Syntex, vous pouvez tirer parti des ensembles de termes globaux [Services de métadonnées gérées](https://docs.microsoft.com/sharepoint/managed-metadata) pour afficher les termes recommandés concernant les données extraites.</span><span class="sxs-lookup"><span data-stu-id="b2841-104">When you create an extractor in your document understanding model using SharePoint Syntex, you can take advantage of global term sets in the [term store](https://docs.microsoft.com/sharepoint/managed-metadata) to display preferred terms for data that you extract.</span></span>  

<span data-ttu-id="b2841-105">Par exemple, votre modèle identifie et classe tous les documents **Contrat** chargés dans la bibliothèque de documents.</span><span class="sxs-lookup"><span data-stu-id="b2841-105">As an example, your model identifies and classifies all **Contract** documents that are uploaded to the document library.</span></span>  <span data-ttu-id="b2841-106">De plus, le modèle extrait également une valeur de **service de contrat** de chaque contrat et l’affiche dans une colonne de la vue de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="b2841-106">Additionally, the model also extracts a **Contract Service** value from each contract, and will display it in a column in your library view.</span></span> <span data-ttu-id="b2841-107">Les diverses valeurs de services des contrats incluent plusieurs éléments plus anciens, à présent inutilisés par votre société et renommés.</span><span class="sxs-lookup"><span data-stu-id="b2841-107">Among the various Contract Services values in the contracts, there are several older values that your company no longer uses and have been renamed.</span></span> <span data-ttu-id="b2841-108">Par exemple, toutes les références aux termes *Conception*, *Graphiques* ou *Topographie* (services de contrat) doivent à présent recevoir l’appellation *Créatif*.</span><span class="sxs-lookup"><span data-stu-id="b2841-108">For example, all references to the terms *Design*, *Graphics*, or *Topography* contract services should now be called *Creative*.</span></span> <span data-ttu-id="b2841-109">Chaque fois que votre modèle extrait l’un des termes obsolètes d’un document contractuel, il doit afficher le terme à jour, à savoir Créatif, dans la vue de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="b2841-109">Whenever your model extracts one of the outdated terms from a contract document, you want it to display the current term - Creative - in your library view.</span></span> <span data-ttu-id="b2841-110">Dans l’exemple ci-après, lors de la formation du modèle, nous constatons qu’un exemple de document contient le terme obsolète *Conception*.</span><span class="sxs-lookup"><span data-stu-id="b2841-110">In the example below, while training the model we see that one sample document contains the outdated term of *Design*.</span></span>

   ![Magasin de termes](../media/content-understanding/design.png)</br>

## <a name="use-a-managed-metadata-column-in-your-extractor"></a><span data-ttu-id="b2841-112">Utiliser une colonne de métadonnées gérées dans l’extracteur</span><span class="sxs-lookup"><span data-stu-id="b2841-112">Use a Managed metadata column in your extractor</span></span>

<span data-ttu-id="b2841-113">Les ensembles de termes sont configurés dans le magasin de termes Services de métadonnées gérées (MMS) dans le Centre d’administration SharePoint.</span><span class="sxs-lookup"><span data-stu-id="b2841-113">Term sets are configured in the Managed Metadata services (MMS) term store in the SharePoint admin center.</span></span> <span data-ttu-id="b2841-114">Dans l’exemple ci-dessous, *l’ensemble de termes* [Services de contrat](https://docs.microsoft.com/sharepoint/managed-metadata#term-set) est configuré pour inclure un certain nombre de termes, y compris *Créatif*.</span><span class="sxs-lookup"><span data-stu-id="b2841-114">In the the example below, the *Contract Services* [term set](https://docs.microsoft.com/sharepoint/managed-metadata#term-set) is configured to include a number of terms, including *Creative*.</span></span>  <span data-ttu-id="b2841-115">Les détails indiquent que le terme a trois synonymes (*Conception*, *Graphiques* et *Topographie*). Il convient de les renommer *Créatif*.</span><span class="sxs-lookup"><span data-stu-id="b2841-115">The details for it show that the term has three synonyms (*Design*, *Graphics*, and *Topography*) and the synonyms should be translated to *Creative*.</span></span> 

   ![Ensemble de termes](../media/content-understanding/term-store.png)</br>

<span data-ttu-id="b2841-117">Plusieurs raisons peuvent expliquer le désir d’utiliser un synonyme de votre ensemble de termes.</span><span class="sxs-lookup"><span data-stu-id="b2841-117">There could be a number of reasons why you might want to use a synonym in your term set.</span></span> <span data-ttu-id="b2841-118">Par exemple, cet ensemble peut inclure des termes obsolètes, des termes renommés ou des termes différents en fonction des services de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="b2841-118">For example, there could be outdated terms, renamed terms, or variations between your organizations departments on naming.</span></span>

<span data-ttu-id="b2841-119">Pour pouvoir sélectionner le champ de métadonnées gérées lorsque vous créez l’extracteur dans votre modèle, vous devez [l’ajouter en tant que colonne de site de métadonnées gérées](https://support.microsoft.com/office/8fad9e35-a618-4400-b3c7-46f02785d27f).</span><span class="sxs-lookup"><span data-stu-id="b2841-119">To make the managed metadata field available for you to select when you create your extractor in your model, you need to [add it as a managed-metadata site column](https://support.microsoft.com/office/8fad9e35-a618-4400-b3c7-46f02785d27f).</span></span> <span data-ttu-id="b2841-120">Après avoir ajouté la colonne de site, vous pouvez la sélectionner lorsque vous créez l’extracteur de votre modèle.</span><span class="sxs-lookup"><span data-stu-id="b2841-120">After you add the site column, it will be available for you to select when you create the extractor for your model.</span></span>

   ![Service de contrat](../media/content-understanding/contract-services.png)</br>


<span data-ttu-id="b2841-122">Une fois votre modèle appliqué à la bibliothèque de documents, lors du chargement des documents dans la bibliothèque, la colonne *Services de création* affiche le terme recommandé (*Créatif*) quand l’extracteur trouve l’une des valeurs synonymes (*Conception*, *Graphiques* et *Topographie*).</span><span class="sxs-lookup"><span data-stu-id="b2841-122">After applying your model to the document library, when documents are uploaded to library, the *Creative Services* column will display the preferred term (*Creative*) when the extractor finds any of the synonym values (*Design*, *Graphics*, and *Topography*).</span></span>

   ![Colonne Service de contrat](../media/content-understanding/creative.png)</br>


## <a name="see-also"></a><span data-ttu-id="b2841-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b2841-124">See Also</span></span>
[<span data-ttu-id="b2841-125">Présentation des métadonnées gérées</span><span class="sxs-lookup"><span data-stu-id="b2841-125">Introduction to Managed Metadata</span></span>](https://docs.microsoft.com/sharepoint/managed-metadata#terms)

[<span data-ttu-id="b2841-126">Créer un extracteur</span><span class="sxs-lookup"><span data-stu-id="b2841-126">Create an extractor</span></span>](create-an-extractor.md)

[<span data-ttu-id="b2841-127">Créer une colonne de métadonnées gérées</span><span class="sxs-lookup"><span data-stu-id="b2841-127">Create a managed metadata column</span></span>](https://support.microsoft.com/office/create-a-managed-metadata-column-8fad9e35-a618-4400-b3c7-46f02785d27f?redirectSourcePath=%252farticle%252fc2a06717-8105-4aea-890d-3082853ab7b7&ui=en-US&rs=en-US&ad=US)





