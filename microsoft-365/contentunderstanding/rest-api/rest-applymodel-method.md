---
title: Appliquer un modèle
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
description: Utilisez l’API REST pour appliquer un modèle de compréhension de document à une ou plusieurs bibliothèques.
ms.openlocfilehash: d4cadad3c45dd7af0cdaeb4e1b367426289db870
ms.sourcegitcommit: 33d19853a38dfa4e6ed21b313976643670a14581
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2021
ms.locfileid: "52904265"
---
# <a name="apply-model"></a><span data-ttu-id="e1fd8-103">Appliquer un modèle</span><span class="sxs-lookup"><span data-stu-id="e1fd8-103">Apply model</span></span>

<span data-ttu-id="e1fd8-104">Applique (ou synchronise) un modèle de compréhension de document formé à une ou plusieurs bibliothèques (voir [exemple](rest-applymodel-method.md#examples)).</span><span class="sxs-lookup"><span data-stu-id="e1fd8-104">Applies (or syncs) a trained document understanding model to one or more libraries (see [example](rest-applymodel-method.md#examples)).</span></span>

## <a name="http-request"></a><span data-ttu-id="e1fd8-105">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="e1fd8-105">HTTP request</span></span>

```HTTP
POST /_api/machinelearning/publications HTTP/1.1
```

## <a name="uri-parameters"></a><span data-ttu-id="e1fd8-106">Paramètres d’URI</span><span class="sxs-lookup"><span data-stu-id="e1fd8-106">URI parameters</span></span>

<span data-ttu-id="e1fd8-107">Aucun</span><span class="sxs-lookup"><span data-stu-id="e1fd8-107">None</span></span>

## <a name="request-headers"></a><span data-ttu-id="e1fd8-108">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="e1fd8-108">Request headers</span></span>

| <span data-ttu-id="e1fd8-109">En-tête</span><span class="sxs-lookup"><span data-stu-id="e1fd8-109">Header</span></span> | <span data-ttu-id="e1fd8-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1fd8-110">Value</span></span> |
|--------|-------|
|<span data-ttu-id="e1fd8-111">Accepter</span><span class="sxs-lookup"><span data-stu-id="e1fd8-111">Accept</span></span>|<span data-ttu-id="e1fd8-112">application/json;odata=verbose</span><span class="sxs-lookup"><span data-stu-id="e1fd8-112">application/json;odata=verbose</span></span>|
|<span data-ttu-id="e1fd8-113">Content-Type</span><span class="sxs-lookup"><span data-stu-id="e1fd8-113">Content-Type</span></span>|<span data-ttu-id="e1fd8-114">application/json;odata=verbose;charset=utf-8</span><span class="sxs-lookup"><span data-stu-id="e1fd8-114">application/json;odata=verbose;charset=utf-8</span></span>|
|<span data-ttu-id="e1fd8-115">x-requestdigest</span><span class="sxs-lookup"><span data-stu-id="e1fd8-115">x-requestdigest</span></span>|<span data-ttu-id="e1fd8-116">Résumé approprié pour le site actuel.</span><span class="sxs-lookup"><span data-stu-id="e1fd8-116">The appropriate digest for current site.</span></span>|

## <a name="request-body"></a><span data-ttu-id="e1fd8-117">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="e1fd8-117">Request body</span></span>

| <span data-ttu-id="e1fd8-118">Nom</span><span class="sxs-lookup"><span data-stu-id="e1fd8-118">Name</span></span> | <span data-ttu-id="e1fd8-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="e1fd8-119">Required</span></span> | <span data-ttu-id="e1fd8-120">Type</span><span class="sxs-lookup"><span data-stu-id="e1fd8-120">Type</span></span> | <span data-ttu-id="e1fd8-121">Description</span><span class="sxs-lookup"><span data-stu-id="e1fd8-121">Description</span></span> |
|--------|-------|--------|------------|
|<span data-ttu-id="e1fd8-122">ModelUniqueId</span><span class="sxs-lookup"><span data-stu-id="e1fd8-122">ModelUniqueId</span></span>|<span data-ttu-id="e1fd8-123">oui</span><span class="sxs-lookup"><span data-stu-id="e1fd8-123">yes</span></span>|<span data-ttu-id="e1fd8-124">chaîne</span><span class="sxs-lookup"><span data-stu-id="e1fd8-124">string</span></span>|<span data-ttu-id="e1fd8-125">L'ID unique du fichier modèle.</span><span class="sxs-lookup"><span data-stu-id="e1fd8-125">The unique ID of the model file.</span></span>|
<span data-ttu-id="e1fd8-126">TargetSiteUrl</span><span class="sxs-lookup"><span data-stu-id="e1fd8-126">TargetSiteUrl</span></span>|<span data-ttu-id="e1fd8-127">oui</span><span class="sxs-lookup"><span data-stu-id="e1fd8-127">yes</span></span>|<span data-ttu-id="e1fd8-128">chaîne</span><span class="sxs-lookup"><span data-stu-id="e1fd8-128">string</span></span>|<span data-ttu-id="e1fd8-129">L’URL complète du site cible de bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="e1fd8-129">The full URL of the target library site.</span></span>|
<span data-ttu-id="e1fd8-130">TargetWebServerRelativeUrl</span><span class="sxs-lookup"><span data-stu-id="e1fd8-130">TargetWebServerRelativeUrl</span></span>|<span data-ttu-id="e1fd8-131">oui</span><span class="sxs-lookup"><span data-stu-id="e1fd8-131">yes</span></span>|<span data-ttu-id="e1fd8-132">chaîne</span><span class="sxs-lookup"><span data-stu-id="e1fd8-132">string</span></span>|<span data-ttu-id="e1fd8-133">L’URL du web relative au serveur pour la bibliothèque cible.</span><span class="sxs-lookup"><span data-stu-id="e1fd8-133">The server relative URL of the web for the target library.</span></span>|
<span data-ttu-id="e1fd8-134">TargetLibraryServerRelativeUrl</span><span class="sxs-lookup"><span data-stu-id="e1fd8-134">TargetLibraryServerRelativeUrl</span></span>|<span data-ttu-id="e1fd8-135">oui</span><span class="sxs-lookup"><span data-stu-id="e1fd8-135">yes</span></span>|<span data-ttu-id="e1fd8-136">chaîne</span><span class="sxs-lookup"><span data-stu-id="e1fd8-136">string</span></span>|<span data-ttu-id="e1fd8-137">L’URL relative au serveur pour la bibliothèque cible.</span><span class="sxs-lookup"><span data-stu-id="e1fd8-137">The server relative URL of the target library.</span></span>|
<span data-ttu-id="e1fd8-138">ViewOption</span><span class="sxs-lookup"><span data-stu-id="e1fd8-138">ViewOption</span></span>|<span data-ttu-id="e1fd8-139">Non</span><span class="sxs-lookup"><span data-stu-id="e1fd8-139">no</span></span>|<span data-ttu-id="e1fd8-140">string</span><span class="sxs-lookup"><span data-stu-id="e1fd8-140">string</span></span>|<span data-ttu-id="e1fd8-141">Spécifie s’il faut définir l’affichage du nouveau modèle comme bibliothèque par défaut.</span><span class="sxs-lookup"><span data-stu-id="e1fd8-141">Specifies whether to set new model view as the library default.</span></span>|

## <a name="response"></a><span data-ttu-id="e1fd8-142">Réponse</span><span class="sxs-lookup"><span data-stu-id="e1fd8-142">Response</span></span>

| <span data-ttu-id="e1fd8-143">Nom</span><span class="sxs-lookup"><span data-stu-id="e1fd8-143">Name</span></span>   | <span data-ttu-id="e1fd8-144">Type</span><span class="sxs-lookup"><span data-stu-id="e1fd8-144">Type</span></span>  | <span data-ttu-id="e1fd8-145">Description</span><span class="sxs-lookup"><span data-stu-id="e1fd8-145">Description</span></span>|
|--------|-------|------------|
|<span data-ttu-id="e1fd8-146">200 OK</span><span class="sxs-lookup"><span data-stu-id="e1fd8-146">200 OK</span></span>| |<span data-ttu-id="e1fd8-147">Opération réussie</span><span class="sxs-lookup"><span data-stu-id="e1fd8-147">Success</span></span>|
|<span data-ttu-id="e1fd8-148">201 est créé</span><span class="sxs-lookup"><span data-stu-id="e1fd8-148">201 Created</span></span>| |<span data-ttu-id="e1fd8-149">Notez qu’étant donné que cette API prend en charge l’application du modèle à plusieurs bibliothèques, un code 201 peut être renvoyé, même s’il existe une défaillance dans l’application du modèle à l’une des bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="e1fd8-149">Note that because this API supports applying model to multiple libraries, a 201 could be returned even if there's a failure applying the model to one of the libraries.</span></span> <br><span data-ttu-id="e1fd8-150">Vérifiez que le corps de la réponse pour comprendre si le modèle a été correctement appliqué à toutes les bibliothèques spécifiées.</span><span class="sxs-lookup"><span data-stu-id="e1fd8-150">Check the response body to understand if the model has been successfully applied to all the specified libraries.</span></span> <span data-ttu-id="e1fd8-151">Voir [Corps de réponse](rest-applymodel-method.md#request-body) pour obtenir des détails.</span><span class="sxs-lookup"><span data-stu-id="e1fd8-151">See [Request body](rest-applymodel-method.md#request-body) for details.</span></span>|

## <a name="examples"></a><span data-ttu-id="e1fd8-152">Exemples</span><span class="sxs-lookup"><span data-stu-id="e1fd8-152">Examples</span></span>

### <a name="apply-a-model-to-the-contracts-document-library-in-the-repository-site"></a><span data-ttu-id="e1fd8-153">Appliquer un modèle à la bibliothèque de documents concernant les contrats dans le site du référentiel</span><span class="sxs-lookup"><span data-stu-id="e1fd8-153">Apply a model to the contracts document library in the repository site</span></span>

<span data-ttu-id="e1fd8-154">Dans cet exemple, l’ID du modèle de compréhension de document du Contrat Contoso est `7645e69d-21fb-4a24-a17a-9bdfa7cb63dc`.</span><span class="sxs-lookup"><span data-stu-id="e1fd8-154">In this sample, the ID of the Contoso Contract document understanding model is `7645e69d-21fb-4a24-a17a-9bdfa7cb63dc`.</span></span>

#### <a name="sample-request"></a><span data-ttu-id="e1fd8-155">Exemple de demande</span><span class="sxs-lookup"><span data-stu-id="e1fd8-155">Sample request</span></span>

```HTTP
{
    "__metadata": {
        "type": "Microsoft.Office.Server.ContentCenter.SPMachineLearningPublicationsEntityData"
    },
    "Publications": {
        "results": [
            {
                "ModelUniqueId": "7645e69d-21fb-4a24-a17a-9bdfa7cb63dc",
                "TargetSiteUrl": "https://contoso.sharepoint.com/sites/repository/",
                "TargetWebServerRelativeUrl": "/sites/repository",
                "TargetLibraryServerRelativeUrl": "/sites/repository/contracts",
                "ViewOption": "NewViewAsDefault"
            }
        ]
    }
}
```


#### <a name="sample-response"></a><span data-ttu-id="e1fd8-156">Exemple de réponse</span><span class="sxs-lookup"><span data-stu-id="e1fd8-156">Sample response</span></span>

<span data-ttu-id="e1fd8-157">Dans la réponse, TotalFailures et TotalSuccesses font référence au nombre d’échecs et de réussite du modèle qui s’applique aux bibliothèques spécifiées.</span><span class="sxs-lookup"><span data-stu-id="e1fd8-157">In the response, TotalFailures and TotalSuccesses refers to the number of failures and successes of the model being applies to the specified libraries.</span></span>

<span data-ttu-id="e1fd8-158">**Code d’état :** 200</span><span class="sxs-lookup"><span data-stu-id="e1fd8-158">**Status code:** 200</span></span>

```JSON
{
    "Details": [
        {
            "ErrorMessage": null,
            "Publication": {
                "ModelUniqueId": "7645e69d-21fb-4a24-a17a-9bdfa7cb63dc",
                "TargetSiteUrl": "https://contoso.sharepoint.com/sites/repository/",
                "TargetWebServerRelativeUrl": "/sites/repository",
                "TargetLibraryServerRelativeUrl": "/sites/repository/contracts",
                "ViewOption": "NewViewAsDefault"
            },
            "StatusCode": 200
        }
    ],
    "TotalFailures": 0,
    "TotalSuccesses": 1
}
```

## <a name="see-also"></a><span data-ttu-id="e1fd8-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e1fd8-159">See also</span></span>

[<span data-ttu-id="e1fd8-160">API REST du modèle de compréhension de document Syntex</span><span class="sxs-lookup"><span data-stu-id="e1fd8-160">Syntex document understanding model REST API</span></span>](syntex-model-rest-api.md)
