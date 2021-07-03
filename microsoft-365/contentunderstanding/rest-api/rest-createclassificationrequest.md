---
title: Créer une demande de classification
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
description: Utiliser l’API REST pour créer une demande pour classifier un ou plusieurs fichiers à l’aide d’un modèle formé de compréhension de document.
ms.openlocfilehash: b1022787d6e11ebe36c88ecd29936a777289dd74
ms.sourcegitcommit: 4886457c0d4248407bddec56425dba50bb60d9c4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/03/2021
ms.locfileid: "53287232"
---
# <a name="create-classification-request"></a><span data-ttu-id="6482d-103">Créer une demande de classification</span><span class="sxs-lookup"><span data-stu-id="6482d-103">Create classification request</span></span>

<span data-ttu-id="6482d-104">Crée une demande pour classifier un ou plusieurs fichiers à l’aide d’un modèle formé de compréhension de document (voir [exemple](rest-createclassificationrequest.md#examples)).</span><span class="sxs-lookup"><span data-stu-id="6482d-104">Creates a request to classify one or more files using the applied document understanding model (see [example](rest-createclassificationrequest.md#examples)).</span></span>

<span data-ttu-id="6482d-105">Le service REST SharePoint Online (et SharePoint 2016 et version ultérieure sur site) prend en charge la combinaison de plusieurs requêtes.</span><span class="sxs-lookup"><span data-stu-id="6482d-105">The SharePoint Online (and SharePoint 2016 and later on-premises) REST service supports combining multiple requests.</span></span> <span data-ttu-id="6482d-106">Les demandes sont regroupées en un seul appel vers le service en utilisant l’option de requête OData $batch.</span><span class="sxs-lookup"><span data-stu-id="6482d-106">Requests are combined into a single call to the service by using the OData $batch query option.</span></span> <span data-ttu-id="6482d-107">Vous pouvez utiliser cette méthode pour placer en file d’attente des éléments de travail de classification pour des centaines de documents à la fois.</span><span class="sxs-lookup"><span data-stu-id="6482d-107">This method can be used to enqueue classification work items for hundreds of documents at one time.</span></span>

## <a name="http-request"></a><span data-ttu-id="6482d-108">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="6482d-108">HTTP request</span></span>

```http
POST /_api/machinelearning/workItems HTTP/1.1
```
## <a name="uri-parameters"></a><span data-ttu-id="6482d-109">Paramètres d’URI</span><span class="sxs-lookup"><span data-stu-id="6482d-109">URI Parameters</span></span>

<span data-ttu-id="6482d-110">Aucun</span><span class="sxs-lookup"><span data-stu-id="6482d-110">None</span></span>

## <a name="request-headers"></a><span data-ttu-id="6482d-111">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="6482d-111">Request headers</span></span>

| <span data-ttu-id="6482d-112">En-tête</span><span class="sxs-lookup"><span data-stu-id="6482d-112">Header</span></span> | <span data-ttu-id="6482d-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="6482d-113">Value</span></span> |
|--------|-------|
|<span data-ttu-id="6482d-114">Accepter</span><span class="sxs-lookup"><span data-stu-id="6482d-114">Accept</span></span>|<span data-ttu-id="6482d-115">application/json;odata=verbose</span><span class="sxs-lookup"><span data-stu-id="6482d-115">application/json;odata=verbose</span></span>|
|<span data-ttu-id="6482d-116">Content-Type</span><span class="sxs-lookup"><span data-stu-id="6482d-116">Content-Type</span></span>|<span data-ttu-id="6482d-117">application/json;odata=verbose;charset=utf-8</span><span class="sxs-lookup"><span data-stu-id="6482d-117">application/json;odata=verbose;charset=utf-8</span></span>|
|<span data-ttu-id="6482d-118">x-requestdigest</span><span class="sxs-lookup"><span data-stu-id="6482d-118">x-requestdigest</span></span>|<span data-ttu-id="6482d-119">Résumé approprié pour le site actuel</span><span class="sxs-lookup"><span data-stu-id="6482d-119">The appropriate digest for current site</span></span>|

## <a name="request-body"></a><span data-ttu-id="6482d-120">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="6482d-120">Request body</span></span>

|<span data-ttu-id="6482d-121">Nom</span><span class="sxs-lookup"><span data-stu-id="6482d-121">Name</span></span>    |<span data-ttu-id="6482d-122">Type</span><span class="sxs-lookup"><span data-stu-id="6482d-122">Type</span></span>   |<span data-ttu-id="6482d-123">Description</span><span class="sxs-lookup"><span data-stu-id="6482d-123">Description</span></span> |
|--------|-------|------------|
|<span data-ttu-id="6482d-124">_métadonnées</span><span class="sxs-lookup"><span data-stu-id="6482d-124">_metadata</span></span>|<span data-ttu-id="6482d-125">chaîne</span><span class="sxs-lookup"><span data-stu-id="6482d-125">string</span></span> |<span data-ttu-id="6482d-126">Définissez l’objet méta sur le SPO.</span><span class="sxs-lookup"><span data-stu-id="6482d-126">Set the object meta on the SPO.</span></span> <span data-ttu-id="6482d-127">Utilisez toujours la valeur : {"type": "Microsoft.Office.Server.ContentCenter.SPMachineLearningWorkItemEntityData"}.</span><span class="sxs-lookup"><span data-stu-id="6482d-127">Always use the value: {"type": "Microsoft.Office.Server.ContentCenter.SPMachineLearningWorkItemEntityData"}.</span></span> |
|<span data-ttu-id="6482d-128">TargetSiteId</span><span class="sxs-lookup"><span data-stu-id="6482d-128">TargetSiteId</span></span>|<span data-ttu-id="6482d-129">guid</span><span class="sxs-lookup"><span data-stu-id="6482d-129">guid</span></span>|<span data-ttu-id="6482d-130">L’ID du site dans lequel se trouve le fichier à classifier.</span><span class="sxs-lookup"><span data-stu-id="6482d-130">The id of the site where the file to classify is located.</span></span>|
|<span data-ttu-id="6482d-131">TargetWebId</span><span class="sxs-lookup"><span data-stu-id="6482d-131">TargetWebId</span></span>|<span data-ttu-id="6482d-132">guid</span><span class="sxs-lookup"><span data-stu-id="6482d-132">guid</span></span>|<span data-ttu-id="6482d-133">L’ID du web dans lequel se trouve le fichier à classifier.</span><span class="sxs-lookup"><span data-stu-id="6482d-133">The id of the web where the file to classify is located.</span></span>|
|<span data-ttu-id="6482d-134">TargetUniqueId</span><span class="sxs-lookup"><span data-stu-id="6482d-134">TargetUniqueId</span></span>|<span data-ttu-id="6482d-135">guid</span><span class="sxs-lookup"><span data-stu-id="6482d-135">guid</span></span>|<span data-ttu-id="6482d-136">L’ID du fichier à classifier.</span><span class="sxs-lookup"><span data-stu-id="6482d-136">The id of the file to classify.</span></span>|

## <a name="responses"></a><span data-ttu-id="6482d-137">Réponses</span><span class="sxs-lookup"><span data-stu-id="6482d-137">Responses</span></span>

| <span data-ttu-id="6482d-138">Nom</span><span class="sxs-lookup"><span data-stu-id="6482d-138">Name</span></span>   | <span data-ttu-id="6482d-139">Type</span><span class="sxs-lookup"><span data-stu-id="6482d-139">Type</span></span>  | <span data-ttu-id="6482d-140">Description</span><span class="sxs-lookup"><span data-stu-id="6482d-140">Description</span></span>|
|--------|-------|------------|
|<span data-ttu-id="6482d-141">201 est créé</span><span class="sxs-lookup"><span data-stu-id="6482d-141">201 Created</span></span>| |<span data-ttu-id="6482d-142">Opération réussie</span><span class="sxs-lookup"><span data-stu-id="6482d-142">Success</span></span>|

## <a name="examples"></a><span data-ttu-id="6482d-143">Exemples</span><span class="sxs-lookup"><span data-stu-id="6482d-143">Examples</span></span>

### <a name="enqueue-a-request-to-classify-a-file-of-id-e6cff8b7-c90c-4564-b5b8-033449090932"></a><span data-ttu-id="6482d-144">Placer en file d’attente une demande pour classifier un fichier avec l’ID « e6cff8b7-c90c-4564-b5b8-033449090932 »</span><span class="sxs-lookup"><span data-stu-id="6482d-144">Enqueue a request to classify a file of id "e6cff8b7-c90c-4564-b5b8-033449090932"</span></span>

#### <a name="sample-request"></a><span data-ttu-id="6482d-145">Exemple de demande</span><span class="sxs-lookup"><span data-stu-id="6482d-145">Sample request</span></span>

```JSON
{
    "__metadata": {
        "type": "Microsoft.Office.Server.ContentCenter.SPMachineLearningWorkItemEntityData"
    },
    "TargetSiteId": "f686e63b-aba7-48e5-97c7-68c4c1df292f",
    "TargetWebId": "66d6b64d-6f88-4dd9-b3db-47e6f00c53e8",
    "TargetUniqueId": "e6cff8b7-c90c-4564-b5b8-033449090932"
}
```

#### <a name="sample-response"></a><span data-ttu-id="6482d-146">Exemple de réponse</span><span class="sxs-lookup"><span data-stu-id="6482d-146">Sample response</span></span>

<span data-ttu-id="6482d-147">**Code d'état :** 201</span><span class="sxs-lookup"><span data-stu-id="6482d-147">**Status code:** 201</span></span>

## <a name="see-also"></a><span data-ttu-id="6482d-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6482d-148">See also</span></span>

[<span data-ttu-id="6482d-149">API REST du modèle de compréhension de document Syntex</span><span class="sxs-lookup"><span data-stu-id="6482d-149">Syntex document understanding model REST API</span></span>](syntex-model-rest-api.md)
