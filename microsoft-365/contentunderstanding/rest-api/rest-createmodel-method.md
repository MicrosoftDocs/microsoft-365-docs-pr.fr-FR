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
ms.openlocfilehash: 4af980d0733fce63767c6570003342eadb079f26
ms.sourcegitcommit: 33d19853a38dfa4e6ed21b313976643670a14581
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2021
ms.locfileid: "52904221"
---
# <a name="create-model"></a><span data-ttu-id="03b12-103">Créer un modèle</span><span class="sxs-lookup"><span data-stu-id="03b12-103">Create model</span></span>

<span data-ttu-id="03b12-104">Crée un modèle et son type de contenu associé.</span><span class="sxs-lookup"><span data-stu-id="03b12-104">Creates a model and its associated content type.</span></span> <span data-ttu-id="03b12-105">Notez que cette opération crée le modèle uniquement.</span><span class="sxs-lookup"><span data-stu-id="03b12-105">Note that this only creates the model.</span></span> <span data-ttu-id="03b12-106">Il devra être formé dans le centre de contenu (voir [exemple](rest-createmodel-method.md#examples)).</span><span class="sxs-lookup"><span data-stu-id="03b12-106">It will still need to be trained in the content center (see [example](rest-createmodel-method.md#examples)).</span></span>

## <a name="http-request"></a><span data-ttu-id="03b12-107">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="03b12-107">HTTP request</span></span>

```
POST /_api/machinelearning/models HTTP/1.1
```
## <a name="uri-parameters"></a><span data-ttu-id="03b12-108">Paramètres d’URI</span><span class="sxs-lookup"><span data-stu-id="03b12-108">URI Parameters</span></span>

<span data-ttu-id="03b12-109">Aucun</span><span class="sxs-lookup"><span data-stu-id="03b12-109">None</span></span>

## <a name="request-headers"></a><span data-ttu-id="03b12-110">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="03b12-110">Request headers</span></span>

| <span data-ttu-id="03b12-111">En-tête</span><span class="sxs-lookup"><span data-stu-id="03b12-111">Header</span></span> | <span data-ttu-id="03b12-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="03b12-112">Value</span></span> |
|--------|-------|
|<span data-ttu-id="03b12-113">Accepter</span><span class="sxs-lookup"><span data-stu-id="03b12-113">Accept</span></span>|<span data-ttu-id="03b12-114">application/json;odata=verbose</span><span class="sxs-lookup"><span data-stu-id="03b12-114">application/json;odata=verbose</span></span>|
|<span data-ttu-id="03b12-115">Content-Type</span><span class="sxs-lookup"><span data-stu-id="03b12-115">Content-Type</span></span>|<span data-ttu-id="03b12-116">application/json;odata=verbose;charset=utf-8</span><span class="sxs-lookup"><span data-stu-id="03b12-116">application/json;odata=verbose;charset=utf-8</span></span>|
|<span data-ttu-id="03b12-117">x-requestdigest</span><span class="sxs-lookup"><span data-stu-id="03b12-117">x-requestdigest</span></span>|<span data-ttu-id="03b12-118">Résumé approprié pour le site actuel</span><span class="sxs-lookup"><span data-stu-id="03b12-118">The appropriate digest for current site</span></span>|

## <a name="request-body"></a><span data-ttu-id="03b12-119">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="03b12-119">Request body</span></span>

|<span data-ttu-id="03b12-120">Nom</span><span class="sxs-lookup"><span data-stu-id="03b12-120">Name</span></span>    |<span data-ttu-id="03b12-121">Type</span><span class="sxs-lookup"><span data-stu-id="03b12-121">Type</span></span>   |<span data-ttu-id="03b12-122">Description</span><span class="sxs-lookup"><span data-stu-id="03b12-122">Description</span></span> |
|--------|-------|------------|
|<span data-ttu-id="03b12-123">_métadonnées</span><span class="sxs-lookup"><span data-stu-id="03b12-123">_metadata</span></span>|  |<span data-ttu-id="03b12-124">Définissez l’objet méta sur le SPO.</span><span class="sxs-lookup"><span data-stu-id="03b12-124">Set the object meta on the SPO.</span></span> <span data-ttu-id="03b12-125">Utilisez toujours la valeur : {"type": "Microsoft.Office.Server.ContentCenter.SPMachineLearningModelEntityData"}.</span><span class="sxs-lookup"><span data-stu-id="03b12-125">Always use the value: {"type": "Microsoft.Office.Server.ContentCenter.SPMachineLearningModelEntityData"}.</span></span> |
|<span data-ttu-id="03b12-126">ContentTypeGroup</span><span class="sxs-lookup"><span data-stu-id="03b12-126">ContentTypeGroup</span></span>|<span data-ttu-id="03b12-127">chaîne</span><span class="sxs-lookup"><span data-stu-id="03b12-127">string</span></span>|<span data-ttu-id="03b12-128">Le groupe de types associés de contenu associé au modèle.</span><span class="sxs-lookup"><span data-stu-id="03b12-128">The associated content type group associated with the model.</span></span> <span data-ttu-id="03b12-129">« Types de contenu de document intelligent » par défaut.</span><span class="sxs-lookup"><span data-stu-id="03b12-129">Defaulted to "Intelligent Document Content Types".</span></span>|
|<span data-ttu-id="03b12-130">ContentTypeName</span><span class="sxs-lookup"><span data-stu-id="03b12-130">ContentTypeName</span></span>|<span data-ttu-id="03b12-131">chaîne</span><span class="sxs-lookup"><span data-stu-id="03b12-131">string</span></span>|<span data-ttu-id="03b12-132">Le nom du type de contenu associé.</span><span class="sxs-lookup"><span data-stu-id="03b12-132">The associated content type name.</span></span> <span data-ttu-id="03b12-133">Le fichier de modèle créé portera le même nom.</span><span class="sxs-lookup"><span data-stu-id="03b12-133">The created model file will have the same name.</span></span>|

## <a name="responses"></a><span data-ttu-id="03b12-134">Réponses</span><span class="sxs-lookup"><span data-stu-id="03b12-134">Responses</span></span>

| <span data-ttu-id="03b12-135">Nom</span><span class="sxs-lookup"><span data-stu-id="03b12-135">Name</span></span>   | <span data-ttu-id="03b12-136">Type</span><span class="sxs-lookup"><span data-stu-id="03b12-136">Type</span></span>  | <span data-ttu-id="03b12-137">Description</span><span class="sxs-lookup"><span data-stu-id="03b12-137">Description</span></span>|
|--------|-------|------------|
|<span data-ttu-id="03b12-138">201 est créé</span><span class="sxs-lookup"><span data-stu-id="03b12-138">201 Created</span></span>| |<span data-ttu-id="03b12-139">Opération réussie</span><span class="sxs-lookup"><span data-stu-id="03b12-139">Success</span></span>|

## <a name="examples"></a><span data-ttu-id="03b12-140">Exemples</span><span class="sxs-lookup"><span data-stu-id="03b12-140">Examples</span></span>

### <a name="create-a-new-document-understanding-model-called-contoso-contract"></a><span data-ttu-id="03b12-141">Crée un modèle de compréhension de document appelé « Contrat Contoso »</span><span class="sxs-lookup"><span data-stu-id="03b12-141">Create a new document understanding model called "Contoso Contract"</span></span>

#### <a name="sample-request"></a><span data-ttu-id="03b12-142">Exemple de demande</span><span class="sxs-lookup"><span data-stu-id="03b12-142">Sample request</span></span>

```
{
    "__metadata": {
        "type": "Microsoft.Office.Server.ContentCenter.SPMachineLearningModelEntityData"
    },
    "ContentTypeGroup": "Intelligent Document Content Types",
    "ContentTypeName": "Contoso Contract",
}
```

#### <a name="sample-response"></a><span data-ttu-id="03b12-143">Exemple de réponse</span><span class="sxs-lookup"><span data-stu-id="03b12-143">Sample response</span></span>

<span data-ttu-id="03b12-144">**Code d'état :** 201</span><span class="sxs-lookup"><span data-stu-id="03b12-144">**Status code:** 201</span></span>

## <a name="see-also"></a><span data-ttu-id="03b12-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="03b12-145">See also</span></span>

[<span data-ttu-id="03b12-146">API REST du modèle de compréhension de document Syntex</span><span class="sxs-lookup"><span data-stu-id="03b12-146">Syntex document understanding model REST API</span></span>](syntex-model-rest-api.md)
