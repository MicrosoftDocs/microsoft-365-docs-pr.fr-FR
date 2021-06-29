---
title: Créer un modèle
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
description: Utilisez l’API REST pour créer un modèle et son type de contenu associé.
ms.openlocfilehash: 0a1b6ef9b7e38f2c4f52082103530da432e3e855
ms.sourcegitcommit: cfd7644570831ceb7f57c61401df6a0001ef0a6a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/29/2021
ms.locfileid: "53177152"
---
# <a name="create-model"></a><span data-ttu-id="47627-103">Créer un modèle</span><span class="sxs-lookup"><span data-stu-id="47627-103">Create model</span></span>

<span data-ttu-id="47627-104">Crée un modèle et son type de contenu associé.</span><span class="sxs-lookup"><span data-stu-id="47627-104">Creates a model and its associated content type.</span></span> <span data-ttu-id="47627-105">Notez que cette opération crée le modèle uniquement.</span><span class="sxs-lookup"><span data-stu-id="47627-105">Note that this only creates the model.</span></span> <span data-ttu-id="47627-106">Il devra être formé dans le centre de contenu (voir [exemple](rest-createmodel-method.md#examples)).</span><span class="sxs-lookup"><span data-stu-id="47627-106">It will still need to be trained in the content center (see [example](rest-createmodel-method.md#examples)).</span></span>

## <a name="http-request"></a><span data-ttu-id="47627-107">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="47627-107">HTTP request</span></span>

```
POST /_api/machinelearning/models HTTP/1.1
```
## <a name="uri-parameters"></a><span data-ttu-id="47627-108">Paramètres d’URI</span><span class="sxs-lookup"><span data-stu-id="47627-108">URI Parameters</span></span>

<span data-ttu-id="47627-109">Aucun</span><span class="sxs-lookup"><span data-stu-id="47627-109">None</span></span>

## <a name="request-headers"></a><span data-ttu-id="47627-110">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="47627-110">Request headers</span></span>

| <span data-ttu-id="47627-111">En-tête</span><span class="sxs-lookup"><span data-stu-id="47627-111">Header</span></span> | <span data-ttu-id="47627-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="47627-112">Value</span></span> |
|--------|-------|
|<span data-ttu-id="47627-113">Accepter</span><span class="sxs-lookup"><span data-stu-id="47627-113">Accept</span></span>|<span data-ttu-id="47627-114">application/json;odata=verbose</span><span class="sxs-lookup"><span data-stu-id="47627-114">application/json;odata=verbose</span></span>|
|<span data-ttu-id="47627-115">Content-Type</span><span class="sxs-lookup"><span data-stu-id="47627-115">Content-Type</span></span>|<span data-ttu-id="47627-116">application/json;odata=verbose;charset=utf-8</span><span class="sxs-lookup"><span data-stu-id="47627-116">application/json;odata=verbose;charset=utf-8</span></span>|
|<span data-ttu-id="47627-117">x-requestdigest</span><span class="sxs-lookup"><span data-stu-id="47627-117">x-requestdigest</span></span>|<span data-ttu-id="47627-118">Résumé approprié pour le site actuel</span><span class="sxs-lookup"><span data-stu-id="47627-118">The appropriate digest for current site</span></span>|

## <a name="request-body"></a><span data-ttu-id="47627-119">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="47627-119">Request body</span></span>

|<span data-ttu-id="47627-120">Nom</span><span class="sxs-lookup"><span data-stu-id="47627-120">Name</span></span>    |<span data-ttu-id="47627-121">Type</span><span class="sxs-lookup"><span data-stu-id="47627-121">Type</span></span>   |<span data-ttu-id="47627-122">Description</span><span class="sxs-lookup"><span data-stu-id="47627-122">Description</span></span> |
|--------|-------|------------|
|<span data-ttu-id="47627-123">_métadonnées</span><span class="sxs-lookup"><span data-stu-id="47627-123">_metadata</span></span>|  |<span data-ttu-id="47627-124">Définissez l’objet méta sur le SPO.</span><span class="sxs-lookup"><span data-stu-id="47627-124">Set the object meta on the SPO.</span></span> <span data-ttu-id="47627-125">Utilisez toujours la valeur : {"type": "Microsoft.Office.Server.ContentCenter.SPMachineLearningModelEntityData"}.</span><span class="sxs-lookup"><span data-stu-id="47627-125">Always use the value: {"type": "Microsoft.Office.Server.ContentCenter.SPMachineLearningModelEntityData"}.</span></span> |
|<span data-ttu-id="47627-126">ContentTypeGroup</span><span class="sxs-lookup"><span data-stu-id="47627-126">ContentTypeGroup</span></span>|<span data-ttu-id="47627-127">chaîne</span><span class="sxs-lookup"><span data-stu-id="47627-127">string</span></span>|<span data-ttu-id="47627-128">Le groupe de types associés de contenu associé au modèle.</span><span class="sxs-lookup"><span data-stu-id="47627-128">The associated content type group associated with the model.</span></span> <span data-ttu-id="47627-129">« Types de contenu de document intelligent » par défaut.</span><span class="sxs-lookup"><span data-stu-id="47627-129">Defaulted to "Intelligent Document Content Types".</span></span>|
|<span data-ttu-id="47627-130">ContentTypeName</span><span class="sxs-lookup"><span data-stu-id="47627-130">ContentTypeName</span></span>|<span data-ttu-id="47627-131">chaîne</span><span class="sxs-lookup"><span data-stu-id="47627-131">string</span></span>|<span data-ttu-id="47627-132">Le nom du type de contenu associé.</span><span class="sxs-lookup"><span data-stu-id="47627-132">The associated content type name.</span></span> <span data-ttu-id="47627-133">Le fichier de modèle créé portera le même nom.</span><span class="sxs-lookup"><span data-stu-id="47627-133">The created model file will have the same name.</span></span>|

## <a name="responses"></a><span data-ttu-id="47627-134">Réponses</span><span class="sxs-lookup"><span data-stu-id="47627-134">Responses</span></span>

| <span data-ttu-id="47627-135">Nom</span><span class="sxs-lookup"><span data-stu-id="47627-135">Name</span></span>   | <span data-ttu-id="47627-136">Type</span><span class="sxs-lookup"><span data-stu-id="47627-136">Type</span></span>  | <span data-ttu-id="47627-137">Description</span><span class="sxs-lookup"><span data-stu-id="47627-137">Description</span></span>|
|--------|-------|------------|
|<span data-ttu-id="47627-138">201 est créé</span><span class="sxs-lookup"><span data-stu-id="47627-138">201 Created</span></span>| |<span data-ttu-id="47627-139">Opération réussie</span><span class="sxs-lookup"><span data-stu-id="47627-139">Success</span></span>|

## <a name="examples"></a><span data-ttu-id="47627-140">Exemples</span><span class="sxs-lookup"><span data-stu-id="47627-140">Examples</span></span>

### <a name="create-a-new-document-understanding-model-called-contoso-contract"></a><span data-ttu-id="47627-141">Crée un modèle de compréhension de document appelé « Contrat Contoso »</span><span class="sxs-lookup"><span data-stu-id="47627-141">Create a new document understanding model called "Contoso Contract"</span></span>

#### <a name="sample-request"></a><span data-ttu-id="47627-142">Exemple de demande</span><span class="sxs-lookup"><span data-stu-id="47627-142">Sample request</span></span>

```
{
    "__metadata": {
        "type": "Microsoft.Office.Server.ContentCenter.SPMachineLearningModelEntityData"
    },
    "ContentTypeGroup": "Intelligent Document Content Types",
    "ContentTypeName": "Contoso Contract"
}
```

#### <a name="sample-response"></a><span data-ttu-id="47627-143">Exemple de réponse</span><span class="sxs-lookup"><span data-stu-id="47627-143">Sample response</span></span>

<span data-ttu-id="47627-144">**Code d'état :** 201</span><span class="sxs-lookup"><span data-stu-id="47627-144">**Status code:** 201</span></span>

## <a name="see-also"></a><span data-ttu-id="47627-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="47627-145">See also</span></span>

[<span data-ttu-id="47627-146">API REST du modèle de compréhension de document Syntex</span><span class="sxs-lookup"><span data-stu-id="47627-146">Syntex document understanding model REST API</span></span>](syntex-model-rest-api.md)
