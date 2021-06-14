---
title: API REST du modèle de compréhension de document SharePoint Syntex
ms.author: chucked
author: chuckedmonson
manager: pamgreen
ms.reviewer: ssquires
audience: admin
ms.topic: reference
ms.prod: microsoft-365-enterprise
search.appverid: ''
ms.collection: m365initiative-syntex
localization_priority: Priority
description: Vue d’ensemble de l’API REST du modèle de compréhension de document SharePoint Syntex.
ms.openlocfilehash: e661df76828db0d05f7c3492880259117b9f8bf1
ms.sourcegitcommit: 3e197d1ff7d8100faeaf1f5a33f1ad4ed2f72e99
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2021
ms.locfileid: "52908088"
---
# <a name="sharepoint-syntex-document-understanding-model-rest-api"></a><span data-ttu-id="27cf3-103">API REST du modèle de compréhension de document SharePoint Syntex</span><span class="sxs-lookup"><span data-stu-id="27cf3-103">SharePoint Syntex document understanding model REST API</span></span>

<span data-ttu-id="27cf3-104">Vous pouvez utiliser l’interface SharePoint REST pour créer un modèle de compréhension de document, appliquer ou supprimer le modèle dans une ou plusieurs bibliothèques, ainsi qu’obtenir ou mettre à jour les informations concernant le modèle.</span><span class="sxs-lookup"><span data-stu-id="27cf3-104">You can use the SharePoint REST interface to create a document understanding model, apply or remove the model to one or more libraries, and obtain or update information about the model.</span></span> 

<span data-ttu-id="27cf3-105">Le service REST SharePoint Online (et SharePoint sur site 2016 et ultérieur) prend en charge la combinaison de plusieurs requêtes en un seul appel au service à l’aide de l’option de requête $batch OData.</span><span class="sxs-lookup"><span data-stu-id="27cf3-105">The SharePoint Online (and SharePoint 2016 and later on-premises) REST service supports combining multiple requests into a single call to the service by using the OData $batch query option.</span></span> 

<span data-ttu-id="27cf3-106">Pour plus d’informations et des liens vers des exemples de code, consultez la rubrique [Créer des requêtes de lots avec l’API REST](/sharepoint/dev/sp-add-ins/make-batch-requests-with-the-rest-apis).</span><span class="sxs-lookup"><span data-stu-id="27cf3-106">For details and links to code samples, see [Make batch requests with the REST APIs](/sharepoint/dev/sp-add-ins/make-batch-requests-with-the-rest-apis).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="27cf3-107">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="27cf3-107">Prerequisites</span></span>

<span data-ttu-id="27cf3-108">Avant de commencer, assurez-vous que vous connaissez les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="27cf3-108">Before you get started, make sure that you're familiar with the following:</span></span>

- [<span data-ttu-id="27cf3-109">Découverte du service REST SharePoint</span><span class="sxs-lookup"><span data-stu-id="27cf3-109">Get to know the SharePoint REST service</span></span>](/sharepoint/dev/sp-add-ins/get-to-know-the-sharepoint-rest-service) 
- [<span data-ttu-id="27cf3-110">Effectuer des opérations de base à l’aide de terminaux REST SharePoint</span><span class="sxs-lookup"><span data-stu-id="27cf3-110">Complete basic operations using SharePoint REST endpoints</span></span>](/sharepoint/dev/sp-add-ins/complete-basic-operations-using-sharepoint-rest-endpoints)

## <a name="rest-commands"></a><span data-ttu-id="27cf3-111">Commandes REST</span><span class="sxs-lookup"><span data-stu-id="27cf3-111">REST commands</span></span>

<span data-ttu-id="27cf3-112">Les commandes REST suivantes peuvent être utilisées avec les modèles de compréhension de document :</span><span class="sxs-lookup"><span data-stu-id="27cf3-112">The following REST commands are available for working with Syntex document understanding models:</span></span>

- <span data-ttu-id="27cf3-113">[Créer un modèle](rest-createmodel-method.md) : Crée un modèle et son type de contenu associé.</span><span class="sxs-lookup"><span data-stu-id="27cf3-113">[Create model](rest-createmodel-method.md) – Creates a model and its associated content type.</span></span>
- <span data-ttu-id="27cf3-114">[GetByUniqueId](rest-getbyuniqueid-method.md) : reçoit ou met à jour les informations sur un modèle de compréhension de document SharePoint Syntex.</span><span class="sxs-lookup"><span data-stu-id="27cf3-114">[GetByUniqueId](rest-getbyuniqueid-method.md) – Gets or updates information about a SharePoint Syntex document understanding model.</span></span>
- <span data-ttu-id="27cf3-115">[GetByTitle](rest-getbytitle-method.md) : reçoit ou met à jour les informations sur un modèle de compréhension de document utilisant le titre du modèle.</span><span class="sxs-lookup"><span data-stu-id="27cf3-115">[GetByTitle](rest-getbytitle-method.md) – Gets or updates information about a SharePoint Syntex document understanding model using the model title.</span></span>
- <span data-ttu-id="27cf3-116">[Appliquer un modèle](rest-applymodel-method.md) : applique (ou synchronise) un modèle de compréhension de document formé à une ou plusieurs bibliothèques.</span><span class="sxs-lookup"><span data-stu-id="27cf3-116">[Apply model](rest-applymodel-method.md) – Applies (or syncs) a trained document understanding model to one or more libraries.</span></span>
- <span data-ttu-id="27cf3-117">[Obtenir des informations sur des bibliothèques et des modèles](rest-getmodelandlibraryinfo.md) : reçoit des informations sur un modèle et la bibliothèque dans laquelle il est appliqué.</span><span class="sxs-lookup"><span data-stu-id="27cf3-117">[Get model and library information](rest-getmodelandlibraryinfo.md) – Gets information about a model and the library where it has been applied.</span></span>
- <span data-ttu-id="27cf3-118">[UpdateModelSettings](rest-updatemodelsettings-method.md) : met à jour les paramètres des modèles disponibles (description du modèle et étiquette de rétention associés) pour un modèle de compréhension de document SharePoint Syntex.</span><span class="sxs-lookup"><span data-stu-id="27cf3-118">[UpdateModelSettings](rest-updatemodelsettings-method.md) – Updates available models settings (associated retention label and model description) for a SharePoint Syntex document understanding model.</span></span>
- <span data-ttu-id="27cf3-119">[BatchDelete](rest-batchdelete-method.md) : Supprime un modèle appliqué de compréhension de document à partir d’une ou plusieurs bibliothèques.</span><span class="sxs-lookup"><span data-stu-id="27cf3-119">[BatchDelete](rest-batchdelete-method.md) – Removes an applied document understanding model from one or more libraries.</span></span>
- <span data-ttu-id="27cf3-120">[Créer une demande de classification](rest-createclassificationrequest.md) : crée une demande pour classifier un ou plusieurs fichiers spécifiés en utilisant le modèle appliqué.</span><span class="sxs-lookup"><span data-stu-id="27cf3-120">[Create classification request](rest-createclassificationrequest.md) – Creates a request to classify a specified file or files using the applied model.</span></span>

## <a name="scenarios"></a><span data-ttu-id="27cf3-121">Scénarios</span><span class="sxs-lookup"><span data-stu-id="27cf3-121">Scenarios</span></span>

<span data-ttu-id="27cf3-122">Notez que les exemples de scénarios suivants ne sont pas intuitifs par rapport au nom de la méthode.</span><span class="sxs-lookup"><span data-stu-id="27cf3-122">Note the following scenario examples that aren't intuitive from the method name.</span></span> <span data-ttu-id="27cf3-123">Pour plus d'informations, voir chaque article.</span><span class="sxs-lookup"><span data-stu-id="27cf3-123">For more information, see each article.</span></span>

<span data-ttu-id="27cf3-124">La méthode Créer un modèle crée uniquement l’objet du modèle et son type de contenu associé.</span><span class="sxs-lookup"><span data-stu-id="27cf3-124">The create model method only creates the model object and its associated content type.</span></span> <span data-ttu-id="27cf3-125">Vous devrez d’abord former le modèle dans le centre de contenu avant de pouvoir l’appliquer à une bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="27cf3-125">You'll need to first train the model in the content center before it can be applied to a library.</span></span>

<span data-ttu-id="27cf3-126">La méthode Appliquer un modèle est utilisée pour configurer le modèle sur la bibliothèque cible pour classifier des documents et extraire éventuellement des informations supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="27cf3-126">The apply model method is used to configure the model on the target library to classify documents and optionally extract additional information.</span></span> <span data-ttu-id="27cf3-127">Cette API prend également en charge le lot appliquant le modèle à plusieurs bibliothèques.</span><span class="sxs-lookup"><span data-stu-id="27cf3-127">This API also supports batch applying the model to multiple libraries.</span></span>

<span data-ttu-id="27cf3-128">La méthode Supprimer un modèle supprime simplement le modèle d’une ou plusieurs bibliothèques dans lesquelles il a été précédemment appliqué.</span><span class="sxs-lookup"><span data-stu-id="27cf3-128">The remove model method just removes the model from one or more libraries where it was previously applied.</span></span> <span data-ttu-id="27cf3-129">Si vous souhaitez supprimer le modèle, vous devez d’abord le supprimer de toutes les bibliothèques dans lesquelles il a été appliqué.</span><span class="sxs-lookup"><span data-stu-id="27cf3-129">If you want to delete the model, it must first be removed from all the libraries where it was applied.</span></span>


## <a name="see-also"></a><span data-ttu-id="27cf3-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="27cf3-130">See also</span></span>

[<span data-ttu-id="27cf3-131">Vue d’ensemble de la compréhension de document</span><span class="sxs-lookup"><span data-stu-id="27cf3-131">Document understanding overview</span></span>](../document-understanding-overview.md)

