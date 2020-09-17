---
title: Vue d’ensemble du traitement des formulaires (aperçu)
ms.author: efrene
author: efrene
manager: pamgreen
ms.date: 8/1/2020
audience: admin
ms.topic: article
ms.service: o365-administration
search.appverid: ''
localization_priority: None
ROBOTS: NOINDEX, NOFOLLOW
description: En savoir plus sur le traitement de formulaire dans le projet cortex.
ms.openlocfilehash: de8e0ed546380059cc1b7b209eeec71f1eb779f9
ms.sourcegitcommit: dffb9b72acd2e0bd286ff7e79c251e7ec6e8ecae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/17/2020
ms.locfileid: "47950023"
---
# <a name="form-processing-overview-preview"></a><span data-ttu-id="76951-103">Vue d’ensemble du traitement des formulaires (aperçu)</span><span class="sxs-lookup"><span data-stu-id="76951-103">Form Processing overview (Preview)</span></span>
> [!Note]
> <span data-ttu-id="76951-104">Le contenu de cet article est destiné à Project cortex privé preview.</span><span class="sxs-lookup"><span data-stu-id="76951-104">The content in this article is for Project Cortex Private Preview.</span></span> <span data-ttu-id="76951-105">Pour [plus d’informations sur le projet cortex](https://aka.ms/projectcortex).</span><span class="sxs-lookup"><span data-stu-id="76951-105">[Find out more about Project Cortex](https://aka.ms/projectcortex).</span></span>

<span data-ttu-id="76951-106">Le projet cortex utilise le traitement des formulaires Microsoft PowerApp. [ai Builder](https://docs.microsoft.com/ai-builder/overview) pour créer des modèles dans les bibliothèques de documents SharePoint.</span><span class="sxs-lookup"><span data-stu-id="76951-106">Project Cortex uses Microsoft PowerApps [AI Builder](https://docs.microsoft.com/ai-builder/overview) form processing to create models within SharePoint document libraries.</span></span>
<span data-ttu-id="76951-107">Vous pouvez utiliser le traitement des formulaires du générateur AI pour créer des modèles AI qui utilisent la technologie machine learning pour identifier et extraire des paires clé-valeur et des données de tableau à partir de documents structurés ou semi-structurés, tels que les formulaires et les factures.</span><span class="sxs-lookup"><span data-stu-id="76951-107">You can use AI Builder form processing to create AI models that use machine learning technology to identify and extract key-value pairs and table data from structured or semi-structured  documents, like forms and invoices.</span></span>

<span data-ttu-id="76951-108">Les entreprises reçoivent souvent des factures en grandes quantités et provenant de diverses sources, telles que des courriers électroniques, des télécopies, des messages électroniques ou en personne.</span><span class="sxs-lookup"><span data-stu-id="76951-108">Companies often receive invoices in large quantities and from a variety of sources, such as mail, fax, email, or in person.</span></span> <span data-ttu-id="76951-109">Le traitement de ces documents et leur saisie manuelle dans votre base de données peuvent prendre beaucoup de temps.</span><span class="sxs-lookup"><span data-stu-id="76951-109">Processing these documents and manually entering them into your database can take a considerable amount of time.</span></span> <span data-ttu-id="76951-110">En utilisant l’IA pour extraire le texte, les paires clé/valeur et les tables de vos documents, le traitement de formulaire automatisera ce processus.</span><span class="sxs-lookup"><span data-stu-id="76951-110">By using AI to extract the text, key/value pairs, and tables from your documents, form processing will automate this process.</span></span> 

<span data-ttu-id="76951-111">Par exemple, vous pouvez créer un modèle de traitement de formulaire qui identifie tous les documents de bons de commande chargés dans la bibliothèque de documents.</span><span class="sxs-lookup"><span data-stu-id="76951-111">For example, you can create a form processing model that will identify all purchase order documents that are uploaded to the document library.</span></span> <span data-ttu-id="76951-112">Et à partir de chaque bon de commande, vous pouvez extraire et afficher des données spécifiques importantes pour vous, telles que le *numéro de bon de commande*, la *Date*ou le *coût total*.</span><span class="sxs-lookup"><span data-stu-id="76951-112">And from each purchase order you can extract and display specific data that is important to you, such as *PO Number*, *Date*, or *Total Cost*.</span></span>

<span data-ttu-id="76951-113">Vous utilisez des exemples de fichiers pour former votre modèle et définir les informations à extraire de votre formulaire.</span><span class="sxs-lookup"><span data-stu-id="76951-113">You use example files to train your model and define the information to be extracted from your form.</span></span> <span data-ttu-id="76951-114">La mise en page de votre document est une formation sur votre modèle.</span><span class="sxs-lookup"><span data-stu-id="76951-114">The layout of your document is learned by training your model.</span></span> <span data-ttu-id="76951-115">Vous n’avez besoin que de cinq documents de formulaires pour commencer.</span><span class="sxs-lookup"><span data-stu-id="76951-115">You only need five form documents to get started.</span></span> <span data-ttu-id="76951-116">Le générateur AI analyse vos exemples de fichiers pour les paires clé-valeur et vous pouvez également identifier manuellement ceux qui n’ont peut-être pas été détectés.</span><span class="sxs-lookup"><span data-stu-id="76951-116">AI Builder will analyze your example files for key-value pairs, and you can also manually identify ones that may not have been detected.</span></span>  <span data-ttu-id="76951-117">Le générateur AI vous permet de tester la précision de votre modèle sur vos fichiers d’exemple.</span><span class="sxs-lookup"><span data-stu-id="76951-117">AI builder lets you test the accuracy of your model on your sample files.</span></span>

<span data-ttu-id="76951-118">Une fois que vous avez formé et publié votre modèle, vous pouvez l’utiliser pour créer un [flux Automated Power](https://docs.microsoft.com/power-automate/getting-started).</span><span class="sxs-lookup"><span data-stu-id="76951-118">After you train and publish your model, to use it you create a [Power Automate Flow](https://docs.microsoft.com/power-automate/getting-started).</span></span> <span data-ttu-id="76951-119">Le flux s’exécute lorsqu’un fichier est téléchargé vers la bibliothèque de documents SharePoint et extrait les données qui ont été identifiées dans le modèle.</span><span class="sxs-lookup"><span data-stu-id="76951-119">The flow runs when a file is uploaded to the SharePoint document library and will extract data that has been identified in the model.</span></span> <span data-ttu-id="76951-120">Les données extraites s’afficheront dans les colonnes de la vue bibliothèque de documents de votre modèle.</span><span class="sxs-lookup"><span data-stu-id="76951-120">The extracted data will display in columns in your model's document library view.</span></span>

<span data-ttu-id="76951-121">Un administrateur Office 365 doit [activer le traitement de formulaire](https://docs.microsoft.com/microsoft-365/contentunderstanding/set-up-content-understanding?view=o365-worldwide#to-set-up-content-understanding) pour la bibliothèque de documents SharePoint afin que les utilisateurs puissent [créer un modèle de traitement de formulaire](create-a-form-processing-model.md) dans celui-ci.</span><span class="sxs-lookup"><span data-stu-id="76951-121">An Office 365 admin needs to [enable Form processing](https://docs.microsoft.com/microsoft-365/contentunderstanding/set-up-content-understanding?view=o365-worldwide#to-set-up-content-understanding) for the SharePoint document library for users to be able to [create a form processing model](create-a-form-processing-model.md) in it.</span></span>



## <a name="see-also"></a><span data-ttu-id="76951-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="76951-122">See Also</span></span>
  
[<span data-ttu-id="76951-123">Mise à l’arrêt de la documentation</span><span class="sxs-lookup"><span data-stu-id="76951-123">Power Automate documentation</span></span>](https://docs.microsoft.com/power-automate/)</br>
[<span data-ttu-id="76951-124">Créer un modèle de traitement de formulaire</span><span class="sxs-lookup"><span data-stu-id="76951-124">Create a form processing model</span></span>](create-a-form-processing-model.md)</br>
[<span data-ttu-id="76951-125">Présentation de l’explication des documents</span><span class="sxs-lookup"><span data-stu-id="76951-125">Document understanding overview</span></span>](document-understanding-overview.md)</br>
[<span data-ttu-id="76951-126">Formation : améliorer les performances d’entreprise avec le générateur AI</span><span class="sxs-lookup"><span data-stu-id="76951-126">Training: Improve business performance with AI Builder</span></span>](https://docs.microsoft.com/learn/paths/improve-business-performance-ai-builder/?source=learn)</br>




