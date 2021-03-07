---
title: Vue d’ensemble du traitement des formulaires
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
description: En savoir plus sur le traitement de formulaires dans Microsoft SharePoint Syntex
ms.openlocfilehash: 1dba8828a158a5163017ee5f37735f44e974274c
ms.sourcegitcommit: babbba2b5bf69fd3facde2905ec024b753dcd1b3
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "50515159"
---
# <a name="form-processing-overview"></a><span data-ttu-id="4ef7b-103">Vue d’ensemble du traitement des formulaires</span><span class="sxs-lookup"><span data-stu-id="4ef7b-103">Form processing overview</span></span>

 ![Générateur d’intelligence artificielle](../media/content-understanding/ai-builder.png)</br>

<span data-ttu-id="4ef7b-105">Microsoft SharePoint Syntex utilise le traitement de formulaire Microsoft PowerApps [AI Builder](https://docs.microsoft.com/ai-builder/overview) pour créer des modèles au sein de bibliothèques de documents SharePoint.</span><span class="sxs-lookup"><span data-stu-id="4ef7b-105">Microsoft SharePoint Syntex uses Microsoft PowerApps [AI Builder](https://docs.microsoft.com/ai-builder/overview) form processing to create models within SharePoint document libraries.</span></span>

<span data-ttu-id="4ef7b-106">Vous pouvez utiliser le traitement de formulaire du générateur AI pour créer des modèles AI qui utilisent la technologie d’apprentissage automatique pour identifier et extraire des paires clés et des données de tableau à partir de documents structurés ou semi-structurés, tels que les formulaires et les factures.</span><span class="sxs-lookup"><span data-stu-id="4ef7b-106">You can use AI Builder form processing to create AI models that use machine learning technology to identify and extract key-value pairs and table data from structured or semi-structured  documents, like forms and invoices.</span></span>

<span data-ttu-id="4ef7b-107">Les organisations reçoivent souvent des factures en grande quantité provenant de sources variées, telles que le courrier, les télécopies, la messagerie, etc. Le traitement de ces documents et leur saisie manuelle dans une base de données peut prendre beaucoup de temps.</span><span class="sxs-lookup"><span data-stu-id="4ef7b-107">Organizations often receive invoices in large quantities from a variety of sources, such as mail, fax, email, etc. Processing these documents and manually entering them into a database can take a considerable amount of time.</span></span> <span data-ttu-id="4ef7b-108">L’utilisation de l’AI pour extraire le texte, les paires clé/valeur et les tables de vos documents, le traitement de formulaire automatise ce processus.</span><span class="sxs-lookup"><span data-stu-id="4ef7b-108">By using AI to extract the text, key/value pairs, and tables from your documents, form processing automates this process.</span></span> 

> [!NOTE]
> <span data-ttu-id="4ef7b-109">Pour plus d’informations sur les exemples de scénarios de traitement de formulaires, consultez l’article [SharePoint Syntex adoption : Guide de démarrage](https://docs.microsoft.com/microsoft-365/contentunderstanding/adoption-getstarted#form-processing-scenario-example).</span><span class="sxs-lookup"><span data-stu-id="4ef7b-109">See the [SharePoint Syntex adoption: Get started guide](https://docs.microsoft.com/microsoft-365/contentunderstanding/adoption-getstarted#form-processing-scenario-example) for more information about form processing scenario examples.</span></span>

<span data-ttu-id="4ef7b-110">Par exemple, vous pouvez créer un modèle de traitement de formulaire qui identifie tous les documents de bon de commande téléchargés dans la bibliothèque de documents.</span><span class="sxs-lookup"><span data-stu-id="4ef7b-110">For example, you can create a form processing model that identifies all purchase order documents that are uploaded to the document library.</span></span> <span data-ttu-id="4ef7b-111">À partir de chaque bon de commande, vous pouvez extraire et afficher des données spécifiques qui vous sont importantes, telles que *numéro de bon de commande*, *date* ou *coût total*.</span><span class="sxs-lookup"><span data-stu-id="4ef7b-111">From each purchase order you can then extract and display specific data that is important to you, such as *PO Number*, *Date*, or *Total Cost*.</span></span>

![Vue de la bibliothèque de documents](../media/content-understanding/doc-lib-done.png)</br>  

<span data-ttu-id="4ef7b-113">Vous pouvez également utiliser des exemples de fichiers pour former votre modèle et définir les informations à extraire de votre formulaire.</span><span class="sxs-lookup"><span data-stu-id="4ef7b-113">You use example files to train your model and define the information to be extracted from your form.</span></span> <span data-ttu-id="4ef7b-114">La mise en page de votre document est acquise en formant votre modèle.</span><span class="sxs-lookup"><span data-stu-id="4ef7b-114">The layout of your document is learned by training your model.</span></span> <span data-ttu-id="4ef7b-115">Vous n’avez besoin que de cinq documents de formulaires pour commencer.</span><span class="sxs-lookup"><span data-stu-id="4ef7b-115">You only need five form documents to get started.</span></span> <span data-ttu-id="4ef7b-116">AI analyse vos exemples de fichiers pour les paires clé-valeur, puis identifie manuellement celles qui n’ont pas été détectées.</span><span class="sxs-lookup"><span data-stu-id="4ef7b-116">AI Builder will analyze your example files for key-value pairs, and you can also manually identify ones that may not have been detected.</span></span>  <span data-ttu-id="4ef7b-117">Le générateur AI vous permet de tester la précision de votre modèle dans vos exemples de fichiers.</span><span class="sxs-lookup"><span data-stu-id="4ef7b-117">AI builder lets you test the accuracy of your model on your example files.</span></span>

<span data-ttu-id="4ef7b-118">Une fois que vous avez créé votre modèle et que vous l’avez publié, celui-ci crée un [Power Automate Flow](https://docs.microsoft.com/power-automate/getting-started).</span><span class="sxs-lookup"><span data-stu-id="4ef7b-118">After you train and publish your model, your model creates a [Power Automate Flow](https://docs.microsoft.com/power-automate/getting-started).</span></span> <span data-ttu-id="4ef7b-119">Le flux s’exécute lorsqu’un fichier est téléchargé dans la bibliothèque de documents SharePoint et extrait les données qui ont été identifiées dans le modèle.</span><span class="sxs-lookup"><span data-stu-id="4ef7b-119">The flow runs when a file is uploaded to the SharePoint document library and will extract data that has been identified in the model.</span></span> <span data-ttu-id="4ef7b-120">Les données extraites s’affichent dans les colonnes de la vue bibliothèque de documents de votre modèle.</span><span class="sxs-lookup"><span data-stu-id="4ef7b-120">The extracted data will display in columns in your model's document library view.</span></span>

<span data-ttu-id="4ef7b-121">Un administrateur Office 365 doit [activer le traitement de formulaires](https://docs.microsoft.com/microsoft-365/contentunderstanding/set-up-content-understanding#to-set-up-content-understanding)pour la bibliothèque de documents SharePoint pour permettre aux utilisateurs de [créer un modèle de traitement de formulaire](create-a-form-processing-model.md) dans celui-ci.</span><span class="sxs-lookup"><span data-stu-id="4ef7b-121">An Office 365 admin needs to [enable Form processing](https://docs.microsoft.com/microsoft-365/contentunderstanding/set-up-content-understanding#to-set-up-content-understanding) for the SharePoint document library for users to be able to [create a form processing model](create-a-form-processing-model.md) in it.</span></span> <span data-ttu-id="4ef7b-122">Vous pouvez sélectionner les sites pendant ou après la configuration dans vos paramètres de gestion.</span><span class="sxs-lookup"><span data-stu-id="4ef7b-122">You can select the sites during setup, or after setup in your management settings.</span></span>

### <a name="file-limitations"></a><span data-ttu-id="4ef7b-123">Limitations de fichier</span><span class="sxs-lookup"><span data-stu-id="4ef7b-123">File limitations</span></span>

<span data-ttu-id="4ef7b-124">Lorsque vous utilisez des modèles de traitement de formulaires, veillez à noter les [exigences et les limites d'utilisation des fichiers](https://docs.microsoft.com/ai-builder/form-processing-model-requirements).</span><span class="sxs-lookup"><span data-stu-id="4ef7b-124">When using form processing models, make sure to note the [requirements and limitations for file usage](https://docs.microsoft.com/ai-builder/form-processing-model-requirements).</span></span>

### <a name="multi-geo-environments"></a><span data-ttu-id="4ef7b-125">Microsoft 365 Multigéographie</span><span class="sxs-lookup"><span data-stu-id="4ef7b-125">Multi-Geo environments</span></span>

<span data-ttu-id="4ef7b-126">Lors de la configuration de SharePoint Syntex dans un[environnement Microsoft 365 Multigéographie](https://docs.microsoft.com/microsoft-365/enterprise/microsoft-365-multi-geo), vous pouvez seulement le configurer pour utiliser le traitement des formulaires à l’emplacement central.</span><span class="sxs-lookup"><span data-stu-id="4ef7b-126">When setting up SharePoint Syntex in a [Microsoft 365 Multi-Geo environment](https://docs.microsoft.com/microsoft-365/enterprise/microsoft-365-multi-geo), you can only configure it to use form processing in the central location.</span></span> <span data-ttu-id="4ef7b-127">Si vous souhaitez utiliser le traitement de formulaires dans un emplacement satellite, contactez le support Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4ef7b-127">If you want to use form processing in a satellite location, contact Microsoft support.</span></span>






## <a name="see-also"></a><span data-ttu-id="4ef7b-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4ef7b-128">See Also</span></span>
  
[<span data-ttu-id="4ef7b-129">Documentation Power Automate</span><span class="sxs-lookup"><span data-stu-id="4ef7b-129">Power Automate documentation</span></span>](https://docs.microsoft.com/power-automate/)

[<span data-ttu-id="4ef7b-130">Créer un modèle de traitement de formulaire</span><span class="sxs-lookup"><span data-stu-id="4ef7b-130">Create a form processing model</span></span>](create-a-form-processing-model.md)

[<span data-ttu-id="4ef7b-131">Présentation de la présentation des documents</span><span class="sxs-lookup"><span data-stu-id="4ef7b-131">Document understanding overview</span></span>](document-understanding-overview.md)

[<span data-ttu-id="4ef7b-132">Formation : Améliorer les performances de votre entreprise avec AI Builder</span><span class="sxs-lookup"><span data-stu-id="4ef7b-132">Training: Improve business performance with AI Builder</span></span>](https://docs.microsoft.com/learn/paths/improve-business-performance-ai-builder/?source=learn)
