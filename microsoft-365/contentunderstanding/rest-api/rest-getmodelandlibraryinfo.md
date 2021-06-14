---
title: Obtenir des informations sur un modèle et une bibliothèque
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
description: Utilisez l’API REST pour obtenir des informations sur une bibliothèque et un modèle dans laquelle elle est appliquée.
ms.openlocfilehash: 6cd61364ed3b360ef235aaba21a2735002fe481e
ms.sourcegitcommit: 33d19853a38dfa4e6ed21b313976643670a14581
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2021
ms.locfileid: "52904226"
---
# <a name="get-model-and-library-information"></a><span data-ttu-id="f7f5b-103">Obtenir des informations sur un modèle et une bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f7f5b-103">Get model and library information</span></span>

<span data-ttu-id="f7f5b-104">Obtient des informations sur une bibliothèque et un modèle dans laquelle elle est appliquée (voir [exemple](rest-getmodelandlibraryinfo.md#examples)).</span><span class="sxs-lookup"><span data-stu-id="f7f5b-104">Gets information about a model and the library where it has been applied (see [example](rest-getmodelandlibraryinfo.md#examples)).</span></span>

## <a name="http-request"></a><span data-ttu-id="f7f5b-105">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="f7f5b-105">HTTP request</span></span>

```HTTP
GET /_api/machinelearning/publications/getbyuniqueid(‘{modelUniqueId}’) HTTP/1.1
```

## <a name="uri-parameters"></a><span data-ttu-id="f7f5b-106">Paramètres d’URI</span><span class="sxs-lookup"><span data-stu-id="f7f5b-106">URI parameters</span></span>

| <span data-ttu-id="f7f5b-107">Nom</span><span class="sxs-lookup"><span data-stu-id="f7f5b-107">Name</span></span> | <span data-ttu-id="f7f5b-108">Dans le paramètre</span><span class="sxs-lookup"><span data-stu-id="f7f5b-108">In</span></span> | <span data-ttu-id="f7f5b-109">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="f7f5b-109">Required</span></span> | <span data-ttu-id="f7f5b-110">Type</span><span class="sxs-lookup"><span data-stu-id="f7f5b-110">Type</span></span> | <span data-ttu-id="f7f5b-111">Description</span><span class="sxs-lookup"><span data-stu-id="f7f5b-111">Description</span></span> |
|--------|-------|--------|------------|
|<span data-ttu-id="f7f5b-112">ModelUniqueId</span><span class="sxs-lookup"><span data-stu-id="f7f5b-112">ModelUniqueId</span></span>|<span data-ttu-id="f7f5b-113">requête</span><span class="sxs-lookup"><span data-stu-id="f7f5b-113">query</span></span>|<span data-ttu-id="f7f5b-114">True</span><span class="sxs-lookup"><span data-stu-id="f7f5b-114">True</span></span>|<span data-ttu-id="f7f5b-115">GUID</span><span class="sxs-lookup"><span data-stu-id="f7f5b-115">GUID</span></span>|<span data-ttu-id="f7f5b-116">L'ID unique du fichier modèle.</span><span class="sxs-lookup"><span data-stu-id="f7f5b-116">The unique id of the model file.</span></span>|

## <a name="request-headers"></a><span data-ttu-id="f7f5b-117">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="f7f5b-117">Request headers</span></span>

| <span data-ttu-id="f7f5b-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="f7f5b-118">Header</span></span> | <span data-ttu-id="f7f5b-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="f7f5b-119">Value</span></span> |
|--------|-------|
|<span data-ttu-id="f7f5b-120">Accepter</span><span class="sxs-lookup"><span data-stu-id="f7f5b-120">Accept</span></span>|<span data-ttu-id="f7f5b-121">application/json;odata=verbose</span><span class="sxs-lookup"><span data-stu-id="f7f5b-121">application/json;odata=verbose</span></span>|


## <a name="request-body"></a><span data-ttu-id="f7f5b-122">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="f7f5b-122">Request body</span></span>

| <span data-ttu-id="f7f5b-123">Nom</span><span class="sxs-lookup"><span data-stu-id="f7f5b-123">Name</span></span> | <span data-ttu-id="f7f5b-124">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="f7f5b-124">Required</span></span> | <span data-ttu-id="f7f5b-125">Type</span><span class="sxs-lookup"><span data-stu-id="f7f5b-125">Type</span></span> | <span data-ttu-id="f7f5b-126">Description</span><span class="sxs-lookup"><span data-stu-id="f7f5b-126">Description</span></span> |
|--------|-------|--------|------------|
|<span data-ttu-id="f7f5b-127">ModelUniqueId</span><span class="sxs-lookup"><span data-stu-id="f7f5b-127">ModelUniqueId</span></span>|<span data-ttu-id="f7f5b-128">oui</span><span class="sxs-lookup"><span data-stu-id="f7f5b-128">yes</span></span>|<span data-ttu-id="f7f5b-129">chaîne</span><span class="sxs-lookup"><span data-stu-id="f7f5b-129">string</span></span>|<span data-ttu-id="f7f5b-130">L'ID unique du fichier modèle.</span><span class="sxs-lookup"><span data-stu-id="f7f5b-130">The unique ID of the model file.</span></span>|
|<span data-ttu-id="f7f5b-131">TargetSiteUrl</span><span class="sxs-lookup"><span data-stu-id="f7f5b-131">TargetSiteUrl</span></span>|<span data-ttu-id="f7f5b-132">oui</span><span class="sxs-lookup"><span data-stu-id="f7f5b-132">yes</span></span>|<span data-ttu-id="f7f5b-133">chaîne</span><span class="sxs-lookup"><span data-stu-id="f7f5b-133">string</span></span>|<span data-ttu-id="f7f5b-134">L’URL complète du site cible de bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="f7f5b-134">The full URL of the target library site.</span></span>|
|<span data-ttu-id="f7f5b-135">TargetWebServerRelativeUrl</span><span class="sxs-lookup"><span data-stu-id="f7f5b-135">TargetWebServerRelativeUrl</span></span>|<span data-ttu-id="f7f5b-136">oui</span><span class="sxs-lookup"><span data-stu-id="f7f5b-136">yes</span></span>|<span data-ttu-id="f7f5b-137">chaîne</span><span class="sxs-lookup"><span data-stu-id="f7f5b-137">string</span></span>|<span data-ttu-id="f7f5b-138">L’URL du web relative au serveur pour la bibliothèque cible.</span><span class="sxs-lookup"><span data-stu-id="f7f5b-138">The server relative URL of the web for the target library.</span></span>|
|<span data-ttu-id="f7f5b-139">TargetLibraryServerRelativeUrl</span><span class="sxs-lookup"><span data-stu-id="f7f5b-139">TargetLibraryServerRelativeUrl</span></span>|<span data-ttu-id="f7f5b-140">oui</span><span class="sxs-lookup"><span data-stu-id="f7f5b-140">yes</span></span>|<span data-ttu-id="f7f5b-141">chaîne</span><span class="sxs-lookup"><span data-stu-id="f7f5b-141">string</span></span>|<span data-ttu-id="f7f5b-142">L’URL relative au serveur pour la bibliothèque cible.</span><span class="sxs-lookup"><span data-stu-id="f7f5b-142">The server relative URL of the target library.</span></span>|
|<span data-ttu-id="f7f5b-143">TargetLibraryRemoved</span><span class="sxs-lookup"><span data-stu-id="f7f5b-143">TargetLibraryRemoved</span></span>|<span data-ttu-id="f7f5b-144">oui</span><span class="sxs-lookup"><span data-stu-id="f7f5b-144">yes</span></span>|<span data-ttu-id="f7f5b-145">int</span><span class="sxs-lookup"><span data-stu-id="f7f5b-145">int</span></span>|<span data-ttu-id="f7f5b-146">Le drapeau indiquant la suppression ou non de la bibliothèque cible.</span><span class="sxs-lookup"><span data-stu-id="f7f5b-146">The flag that indicates if the target library has been removed or not.</span></span>|

## <a name="response"></a><span data-ttu-id="f7f5b-147">Réponse</span><span class="sxs-lookup"><span data-stu-id="f7f5b-147">Response</span></span>

| <span data-ttu-id="f7f5b-148">Nom</span><span class="sxs-lookup"><span data-stu-id="f7f5b-148">Name</span></span>   | <span data-ttu-id="f7f5b-149">Type</span><span class="sxs-lookup"><span data-stu-id="f7f5b-149">Type</span></span>  | <span data-ttu-id="f7f5b-150">Description</span><span class="sxs-lookup"><span data-stu-id="f7f5b-150">Description</span></span>|
|--------|-------|------------|
|<span data-ttu-id="f7f5b-151">200 OK</span><span class="sxs-lookup"><span data-stu-id="f7f5b-151">200 OK</span></span>| |<span data-ttu-id="f7f5b-152">Opération réussie</span><span class="sxs-lookup"><span data-stu-id="f7f5b-152">Success</span></span>|
|<span data-ttu-id="f7f5b-153">201 est créé</span><span class="sxs-lookup"><span data-stu-id="f7f5b-153">201 Created</span></span>| |<span data-ttu-id="f7f5b-154">Notez qu’étant donné que cette API prend en charge l’application du modèle à plusieurs bibliothèques, un code 201 peut être renvoyé, même s’il existe une défaillance dans l’application du modèle à l’une des bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="f7f5b-154">Note that because this API supports applying model to multiple libraries, a 201 could be returned even if there's a failure applying the model to one of the libraries.</span></span> <br><span data-ttu-id="f7f5b-155">Vérifiez que le corps de la réponse pour comprendre si le modèle a été correctement appliqué à toutes les bibliothèques spécifiées.</span><span class="sxs-lookup"><span data-stu-id="f7f5b-155">Check the response body to understand if the model has been successfully applied to all the specified libraries.</span></span> <span data-ttu-id="f7f5b-156">Voir [Corps de réponse](rest-getmodelandlibraryinfo.md#request-body) pour obtenir des détails.</span><span class="sxs-lookup"><span data-stu-id="f7f5b-156">See [Request body](rest-getmodelandlibraryinfo.md#request-body) for details.</span></span>|

## <a name="examples"></a><span data-ttu-id="f7f5b-157">Exemples</span><span class="sxs-lookup"><span data-stu-id="f7f5b-157">Examples</span></span>

### <a name="get-information-about-the-contracts-model-and-primed-document-library-in-the-repository-site"></a><span data-ttu-id="f7f5b-158">Obtenir des informations sur le modèle des contrats et la bibliothèque de document amorcée dans le site du référentiel</span><span class="sxs-lookup"><span data-stu-id="f7f5b-158">Get information about the contracts model and primed document library in the repository site</span></span>

<span data-ttu-id="f7f5b-159">Dans cet exemple, l’ID du modèle de compréhension de document du Contrat Contoso est `7645e69d-21fb-4a24-a17a-9bdfa7cb63dc`.</span><span class="sxs-lookup"><span data-stu-id="f7f5b-159">In this sample, the ID of the Contoso Contract document understanding model is `7645e69d-21fb-4a24-a17a-9bdfa7cb63dc`.</span></span>

#### <a name="sample-request"></a><span data-ttu-id="f7f5b-160">Exemple de demande</span><span class="sxs-lookup"><span data-stu-id="f7f5b-160">Sample request</span></span>

```HTTP
GET /sites/TestCC/_api/machinelearning/publications/getbymodeluniqueid(‘{7645e69d-21fb-4a24-a17a-9bdfa7cb63dc}’) HTTP/1.1
```
#### <a name="sample-response"></a><span data-ttu-id="f7f5b-161">Exemple de réponse</span><span class="sxs-lookup"><span data-stu-id="f7f5b-161">Sample response</span></span>

<span data-ttu-id="f7f5b-162">**Code d’état :** 200</span><span class="sxs-lookup"><span data-stu-id="f7f5b-162">**Status code:** 200</span></span>

```JSON
{
    "@odata.context": "https://contoso.sharepoint.com/sites/TestCC/_api/$metadata#publications",
    "value": [
        {
            "@odata.type": "#Microsoft.Office.Server.ContentCenter.SPMachineLearningPublication",
            "@odata.id": "https://contoso.sharepoint.com/sites/repository /_api/machinelearning/publications/getbyuniqueId('7645e69d-21fb-4a24-a17a-9bdfa7cb63dc')",
            "@odata.etag": "\"7645e69d-21fb-4a24-a17a-9bdfa7cb63dc,94\"",
            "@odata.editLink": " https://contoso.sharepoint.com/sites/TestCC /_api/machinelearning/publications/getbyuniqueId('7645e69d-21fb-4a24-a17a-9bdfa7cb63dc')",
            "Created": "2021-04-27T03:05:25Z",
            "CreatedBy": "i:0#.f|membership|meganb@contoso.com",
            "DriveId": "b!O-aG9qer5UiXx2jEwd8pL0221maIb9lNs9tH5vAMU-gPy9BrxT7GTrtXtdtv1Uzb",
            "ID": 26,
            "ModelId": 16,
            "ModelName": "contosocontract.classifier",
            "ModelType": 0,
            "ModelUniqueId": "7645e69d-21fb-4a24-a17a-9bdfa7cb63dc",
            "ModelVersion": "8.0",
            "Modified": "2021-03-17T17:56:42Z",
            "ModifiedBy": "i:0#.f|membership|joedoe@contoso.com",
            "ObjectId": "01ZBWEM5FZRILGLXTEB5CZ2NNNSCTWBJMQ",
            "PublicationType": 1,
            "TargetLibraryRemoved": false,
            "TargetLibraryServerRelativeUrl": "/sites/repository/contracts",
            "TargetLibraryUrl": " https://contoso.sharepoint.com/sites/repository/contracts",
            "TargetSiteUrl": "https://contoso.sharepoint.com/sites/repository",
            "TargetWebServerRelativeUrl": "/sites/repository",
            "UniqueId": "7645e69d-21fb-4a24-a17a-9bdfa7cb63dc",
            "ViewOption": "NewViewAsDefault"
        },
        {
            "@odata.type": "#Microsoft.Office.Server.ContentCenter.SPMachineLearningPublication",
            "@odata.id": "https://contoso.sharepoint.com /sites/legal/_api/machinelearning/publications/getbyuniqueId('7645e69d-21fb-4a24-a17a-9bdfa7cb63dc')",
            "@odata.etag": "\"7645e69d-21fb-4a24-a17a-9bdfa7cb63dc,101\"",
            "@odata.editLink": "https://contoso.sharepoint.com /sites/legal/_api/machinelearning/publications/getbyuniqueId('7645e69d-21fb-4a24-a17a-9bdfa7cb63dc')",
            "Created": "2021-01-27T03:17:44Z",
            "CreatedBy": "i:0#.f|membership|esherman@contoso.com ",
            "DriveId": "b!O-aG9qer5UiXx2jEwd8pL0221maIb9lNs9tH5vAMU-gPy9BrxT7GTrtXtdtv1Uzb",
            "ID": 27,
            "ModelId": 16,
            "ModelName": "dispositions.classifier",
            "ModelType": 0,
            "ModelUniqueId": "7645e69d-21fb-4a24-a17a-9bdfa7cb63dc",
            "ModelVersion": "8.0",
            "Modified": "2021-03-17T23:17:46Z",
            "ModifiedBy": "i:0#.f|membership|esherman@contoso.com ",
            "ObjectId": "01ZBWEM5B3ERSZK4PAARGLFZ7JP6GMXG2R",
            "PublicationType": 1,
            "TargetLibraryRemoved": false,
            "TargetLibraryServerRelativeUrl": "/sites/legal/dispositions",
            "TargetLibraryUrl": "https://contoso.sharepoint.com/sites/legal/dispositions",
            "TargetSiteUrl": " https://contoso.sharepoint.com/sites/legal",
            "TargetWebServerRelativeUrl": "/sites/legal",
            "UniqueId": "7645e69d-21fb-4a24-a17a-9bdfa7cb63dc",
            "ViewOption": "NewViewAsDefault"
        }
    ]
}```
```

## <a name="see-also"></a><span data-ttu-id="f7f5b-163">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f7f5b-163">See also</span></span>

[<span data-ttu-id="f7f5b-164">API REST du modèle de compréhension de document Syntex</span><span class="sxs-lookup"><span data-stu-id="f7f5b-164">Syntex document understanding model REST API</span></span>](syntex-model-rest-api.md)
