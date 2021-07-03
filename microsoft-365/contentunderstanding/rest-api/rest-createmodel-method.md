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
ms.openlocfilehash: 1c5bd84c777774edc1aa0c2419181f7b84aa4707
ms.sourcegitcommit: 4886457c0d4248407bddec56425dba50bb60d9c4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/03/2021
ms.locfileid: "53287244"
---
# <a name="create-model"></a><span data-ttu-id="18061-103">Créer un modèle</span><span class="sxs-lookup"><span data-stu-id="18061-103">Create model</span></span>

<span data-ttu-id="18061-104">Crée un modèle et son type de contenu associé.</span><span class="sxs-lookup"><span data-stu-id="18061-104">Creates a model and its associated content type.</span></span> <span data-ttu-id="18061-105">Notez que cette opération crée le modèle uniquement.</span><span class="sxs-lookup"><span data-stu-id="18061-105">Note that this only creates the model.</span></span> <span data-ttu-id="18061-106">Il devra être formé dans le centre de contenu (voir [exemple](rest-createmodel-method.md#examples)).</span><span class="sxs-lookup"><span data-stu-id="18061-106">It will still need to be trained in the content center (see [example](rest-createmodel-method.md#examples)).</span></span>

## <a name="http-request"></a><span data-ttu-id="18061-107">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="18061-107">HTTP request</span></span>

```http
POST /_api/machinelearning/models HTTP/1.1
```
## <a name="uri-parameters"></a><span data-ttu-id="18061-108">Paramètres d’URI</span><span class="sxs-lookup"><span data-stu-id="18061-108">URI Parameters</span></span>

<span data-ttu-id="18061-109">Aucun</span><span class="sxs-lookup"><span data-stu-id="18061-109">None</span></span>

## <a name="request-headers"></a><span data-ttu-id="18061-110">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="18061-110">Request headers</span></span>

| <span data-ttu-id="18061-111">En-tête</span><span class="sxs-lookup"><span data-stu-id="18061-111">Header</span></span> | <span data-ttu-id="18061-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="18061-112">Value</span></span> |
|--------|-------|
|<span data-ttu-id="18061-113">Accepter</span><span class="sxs-lookup"><span data-stu-id="18061-113">Accept</span></span>|<span data-ttu-id="18061-114">application/json;odata=verbose</span><span class="sxs-lookup"><span data-stu-id="18061-114">application/json;odata=verbose</span></span>|
|<span data-ttu-id="18061-115">Content-Type</span><span class="sxs-lookup"><span data-stu-id="18061-115">Content-Type</span></span>|<span data-ttu-id="18061-116">application/json;odata=verbose;charset=utf-8</span><span class="sxs-lookup"><span data-stu-id="18061-116">application/json;odata=verbose;charset=utf-8</span></span>|
|<span data-ttu-id="18061-117">x-requestdigest</span><span class="sxs-lookup"><span data-stu-id="18061-117">x-requestdigest</span></span>|<span data-ttu-id="18061-118">Résumé approprié pour le site actuel</span><span class="sxs-lookup"><span data-stu-id="18061-118">The appropriate digest for current site</span></span>|

## <a name="request-body"></a><span data-ttu-id="18061-119">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="18061-119">Request body</span></span>

|<span data-ttu-id="18061-120">Nom</span><span class="sxs-lookup"><span data-stu-id="18061-120">Name</span></span>    |<span data-ttu-id="18061-121">Type</span><span class="sxs-lookup"><span data-stu-id="18061-121">Type</span></span>   |<span data-ttu-id="18061-122">Description</span><span class="sxs-lookup"><span data-stu-id="18061-122">Description</span></span> |
|--------|-------|------------|
|<span data-ttu-id="18061-123">_métadonnées</span><span class="sxs-lookup"><span data-stu-id="18061-123">_metadata</span></span>|  |<span data-ttu-id="18061-124">Définissez l’objet méta sur le SPO.</span><span class="sxs-lookup"><span data-stu-id="18061-124">Set the object meta on the SPO.</span></span> <span data-ttu-id="18061-125">Utilisez toujours la valeur : {"type": "Microsoft.Office.Server.ContentCenter.SPMachineLearningModelEntityData"}.</span><span class="sxs-lookup"><span data-stu-id="18061-125">Always use the value: {"type": "Microsoft.Office.Server.ContentCenter.SPMachineLearningModelEntityData"}.</span></span> |
|<span data-ttu-id="18061-126">ContentTypeGroup</span><span class="sxs-lookup"><span data-stu-id="18061-126">ContentTypeGroup</span></span>|<span data-ttu-id="18061-127">chaîne</span><span class="sxs-lookup"><span data-stu-id="18061-127">string</span></span>|<span data-ttu-id="18061-128">Le groupe de types associés de contenu associé au modèle.</span><span class="sxs-lookup"><span data-stu-id="18061-128">The associated content type group associated with the model.</span></span> <span data-ttu-id="18061-129">« Types de contenu de document intelligent » par défaut.</span><span class="sxs-lookup"><span data-stu-id="18061-129">Defaulted to "Intelligent Document Content Types".</span></span>|
|<span data-ttu-id="18061-130">ContentTypeName</span><span class="sxs-lookup"><span data-stu-id="18061-130">ContentTypeName</span></span>|<span data-ttu-id="18061-131">chaîne</span><span class="sxs-lookup"><span data-stu-id="18061-131">string</span></span>|<span data-ttu-id="18061-132">Le nom du type de contenu associé.</span><span class="sxs-lookup"><span data-stu-id="18061-132">The associated content type name.</span></span> <span data-ttu-id="18061-133">Le fichier de modèle créé portera le même nom.</span><span class="sxs-lookup"><span data-stu-id="18061-133">The created model file will have the same name.</span></span>|

## <a name="responses"></a><span data-ttu-id="18061-134">Réponses</span><span class="sxs-lookup"><span data-stu-id="18061-134">Responses</span></span>

| <span data-ttu-id="18061-135">Nom</span><span class="sxs-lookup"><span data-stu-id="18061-135">Name</span></span>   | <span data-ttu-id="18061-136">Type</span><span class="sxs-lookup"><span data-stu-id="18061-136">Type</span></span>  | <span data-ttu-id="18061-137">Description</span><span class="sxs-lookup"><span data-stu-id="18061-137">Description</span></span>|
|--------|-------|------------|
|<span data-ttu-id="18061-138">201 est créé</span><span class="sxs-lookup"><span data-stu-id="18061-138">201 Created</span></span>| |<span data-ttu-id="18061-139">Opération réussie</span><span class="sxs-lookup"><span data-stu-id="18061-139">Success</span></span>|

## <a name="examples"></a><span data-ttu-id="18061-140">Exemples</span><span class="sxs-lookup"><span data-stu-id="18061-140">Examples</span></span>

### <a name="create-a-new-document-understanding-model-called-contoso-contract"></a><span data-ttu-id="18061-141">Crée un modèle de compréhension de document appelé « Contrat Contoso »</span><span class="sxs-lookup"><span data-stu-id="18061-141">Create a new document understanding model called "Contoso Contract"</span></span>

#### <a name="sample-request"></a><span data-ttu-id="18061-142">Exemple de demande</span><span class="sxs-lookup"><span data-stu-id="18061-142">Sample request</span></span>

```json
{
    "__metadata": {
        "type": "Microsoft.Office.Server.ContentCenter.SPMachineLearningModelEntityData"
    },
    "ContentTypeGroup": "Intelligent Document Content Types",
    "ContentTypeName": "Contoso Contract"
}
```

#### <a name="sample-response"></a><span data-ttu-id="18061-143">Exemple de réponse</span><span class="sxs-lookup"><span data-stu-id="18061-143">Sample response</span></span>

<span data-ttu-id="18061-144">**Code d'état :** 201</span><span class="sxs-lookup"><span data-stu-id="18061-144">**Status code:** 201</span></span>

## <a name="see-also"></a><span data-ttu-id="18061-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="18061-145">See also</span></span>

[<span data-ttu-id="18061-146">API REST du modèle de compréhension de document Syntex</span><span class="sxs-lookup"><span data-stu-id="18061-146">Syntex document understanding model REST API</span></span>](syntex-model-rest-api.md)
