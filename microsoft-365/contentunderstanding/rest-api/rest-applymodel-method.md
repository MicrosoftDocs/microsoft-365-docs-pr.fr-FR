---
title: Appliquer un modèle par lots
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
ms.openlocfilehash: 04f1dfdb0c16110c9ba7de12f5f0735d498d50cf
ms.sourcegitcommit: 4886457c0d4248407bddec56425dba50bb60d9c4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/03/2021
ms.locfileid: "53286536"
---
# <a name="batch-apply-model"></a><span data-ttu-id="d395a-103">Appliquer un modèle par lots</span><span class="sxs-lookup"><span data-stu-id="d395a-103">Batch Apply model</span></span>

<span data-ttu-id="d395a-104">Applique (ou synchronise) un modèle de compréhension de document formé à une ou plusieurs bibliothèques (voir [exemple](rest-applymodel-method.md#examples)).</span><span class="sxs-lookup"><span data-stu-id="d395a-104">Applies (or syncs) a trained document understanding model to one or more libraries (see [example](rest-applymodel-method.md#examples)).</span></span>

## <a name="http-request"></a><span data-ttu-id="d395a-105">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="d395a-105">HTTP request</span></span>

```HTTP
POST /_api/machinelearning/publications HTTP/1.1
```

## <a name="uri-parameters"></a><span data-ttu-id="d395a-106">Paramètres d’URI</span><span class="sxs-lookup"><span data-stu-id="d395a-106">URI parameters</span></span>

<span data-ttu-id="d395a-107">Aucun</span><span class="sxs-lookup"><span data-stu-id="d395a-107">None</span></span>

## <a name="request-headers"></a><span data-ttu-id="d395a-108">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="d395a-108">Request headers</span></span>

| <span data-ttu-id="d395a-109">En-tête</span><span class="sxs-lookup"><span data-stu-id="d395a-109">Header</span></span> | <span data-ttu-id="d395a-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="d395a-110">Value</span></span> |
|--------|-------|
|<span data-ttu-id="d395a-111">Accepter</span><span class="sxs-lookup"><span data-stu-id="d395a-111">Accept</span></span>|<span data-ttu-id="d395a-112">application/json;odata=verbose</span><span class="sxs-lookup"><span data-stu-id="d395a-112">application/json;odata=verbose</span></span>|
|<span data-ttu-id="d395a-113">Content-Type</span><span class="sxs-lookup"><span data-stu-id="d395a-113">Content-Type</span></span>|<span data-ttu-id="d395a-114">application/json;odata=verbose;charset=utf-8</span><span class="sxs-lookup"><span data-stu-id="d395a-114">application/json;odata=verbose;charset=utf-8</span></span>|
|<span data-ttu-id="d395a-115">x-requestdigest</span><span class="sxs-lookup"><span data-stu-id="d395a-115">x-requestdigest</span></span>|<span data-ttu-id="d395a-116">Résumé approprié pour le site actuel.</span><span class="sxs-lookup"><span data-stu-id="d395a-116">The appropriate digest for current site.</span></span>|

## <a name="request-body"></a><span data-ttu-id="d395a-117">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="d395a-117">Request body</span></span>

| <span data-ttu-id="d395a-118">Nom</span><span class="sxs-lookup"><span data-stu-id="d395a-118">Name</span></span> | <span data-ttu-id="d395a-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="d395a-119">Required</span></span> | <span data-ttu-id="d395a-120">Type</span><span class="sxs-lookup"><span data-stu-id="d395a-120">Type</span></span> | <span data-ttu-id="d395a-121">Description</span><span class="sxs-lookup"><span data-stu-id="d395a-121">Description</span></span> |
|--------|-------|--------|------------|
|<span data-ttu-id="d395a-122">_métadonnées</span><span class="sxs-lookup"><span data-stu-id="d395a-122">__metadata</span></span>|<span data-ttu-id="d395a-123">oui</span><span class="sxs-lookup"><span data-stu-id="d395a-123">yes</span></span>|<span data-ttu-id="d395a-124">chaîne</span><span class="sxs-lookup"><span data-stu-id="d395a-124">string</span></span>|<span data-ttu-id="d395a-125">Définissez l’objet méta sur le SPO.</span><span class="sxs-lookup"><span data-stu-id="d395a-125">Set the object meta on the SPO.</span></span> <span data-ttu-id="d395a-126">Utilisez toujours la valeur : {"type": "Microsoft.Office.Server.ContentCenter.SPMachineLearningPublicationsEntityData"}.</span><span class="sxs-lookup"><span data-stu-id="d395a-126">Always use the value: {"type": "Microsoft.Office.Server.ContentCenter.SPMachineLearningPublicationsEntityData"}.</span></span>|
|<span data-ttu-id="d395a-127">Publications</span><span class="sxs-lookup"><span data-stu-id="d395a-127">Publications</span></span>|<span data-ttu-id="d395a-128">oui</span><span class="sxs-lookup"><span data-stu-id="d395a-128">yes</span></span>|<span data-ttu-id="d395a-129">MachineLearningPublicationEntityData[]</span><span class="sxs-lookup"><span data-stu-id="d395a-129">MachineLearningPublicationEntityData[]</span></span>|<span data-ttu-id="d395a-130">La collection de chaque MachineLearningPublicationEntityData qui spécifie le modèle et la bibliothèque de documents cible.</span><span class="sxs-lookup"><span data-stu-id="d395a-130">The collection of MachineLearningPublicationEntityData each of which specifies the model and target document library.</span></span>|

### <a name="machinelearningpublicationentitydata"></a><span data-ttu-id="d395a-131">MachineLearningPublicationEntityData</span><span class="sxs-lookup"><span data-stu-id="d395a-131">MachineLearningPublicationEntityData</span></span>

| <span data-ttu-id="d395a-132">Nom</span><span class="sxs-lookup"><span data-stu-id="d395a-132">Name</span></span> | <span data-ttu-id="d395a-133">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="d395a-133">Required</span></span> | <span data-ttu-id="d395a-134">Type</span><span class="sxs-lookup"><span data-stu-id="d395a-134">Type</span></span> | <span data-ttu-id="d395a-135">Description</span><span class="sxs-lookup"><span data-stu-id="d395a-135">Description</span></span> |
|--------|-------|--------|------------|
|<span data-ttu-id="d395a-136">ModelUniqueId</span><span class="sxs-lookup"><span data-stu-id="d395a-136">ModelUniqueId</span></span>|<span data-ttu-id="d395a-137">oui</span><span class="sxs-lookup"><span data-stu-id="d395a-137">yes</span></span>|<span data-ttu-id="d395a-138">chaîne</span><span class="sxs-lookup"><span data-stu-id="d395a-138">string</span></span>|<span data-ttu-id="d395a-139">L'ID unique du fichier modèle.</span><span class="sxs-lookup"><span data-stu-id="d395a-139">The unique ID of the model file.</span></span>|
|<span data-ttu-id="d395a-140">TargetSiteUrl</span><span class="sxs-lookup"><span data-stu-id="d395a-140">TargetSiteUrl</span></span>|<span data-ttu-id="d395a-141">oui</span><span class="sxs-lookup"><span data-stu-id="d395a-141">yes</span></span>|<span data-ttu-id="d395a-142">chaîne</span><span class="sxs-lookup"><span data-stu-id="d395a-142">string</span></span>|<span data-ttu-id="d395a-143">L’URL complète du site cible de bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="d395a-143">The full URL of the target library site.</span></span>|
|<span data-ttu-id="d395a-144">TargetWebServerRelativeUrl</span><span class="sxs-lookup"><span data-stu-id="d395a-144">TargetWebServerRelativeUrl</span></span>|<span data-ttu-id="d395a-145">oui</span><span class="sxs-lookup"><span data-stu-id="d395a-145">yes</span></span>|<span data-ttu-id="d395a-146">chaîne</span><span class="sxs-lookup"><span data-stu-id="d395a-146">string</span></span>|<span data-ttu-id="d395a-147">L’URL du web relative au serveur pour la bibliothèque cible.</span><span class="sxs-lookup"><span data-stu-id="d395a-147">The server relative URL of the web for the target library.</span></span>|
|<span data-ttu-id="d395a-148">TargetLibraryServerRelativeUrl</span><span class="sxs-lookup"><span data-stu-id="d395a-148">TargetLibraryServerRelativeUrl</span></span>|<span data-ttu-id="d395a-149">oui</span><span class="sxs-lookup"><span data-stu-id="d395a-149">yes</span></span>|<span data-ttu-id="d395a-150">chaîne</span><span class="sxs-lookup"><span data-stu-id="d395a-150">string</span></span>|<span data-ttu-id="d395a-151">L’URL relative au serveur pour la bibliothèque cible.</span><span class="sxs-lookup"><span data-stu-id="d395a-151">The server relative URL of the target library.</span></span>|
|<span data-ttu-id="d395a-152">ViewOption</span><span class="sxs-lookup"><span data-stu-id="d395a-152">ViewOption</span></span>|<span data-ttu-id="d395a-153">Non</span><span class="sxs-lookup"><span data-stu-id="d395a-153">no</span></span>|<span data-ttu-id="d395a-154">string</span><span class="sxs-lookup"><span data-stu-id="d395a-154">string</span></span>|<span data-ttu-id="d395a-155">Spécifie s’il faut définir l’affichage du nouveau modèle comme bibliothèque par défaut.</span><span class="sxs-lookup"><span data-stu-id="d395a-155">Specifies whether to set new model view as the library default.</span></span>|

## <a name="response"></a><span data-ttu-id="d395a-156">Réponse</span><span class="sxs-lookup"><span data-stu-id="d395a-156">Response</span></span>

| <span data-ttu-id="d395a-157">Nom</span><span class="sxs-lookup"><span data-stu-id="d395a-157">Name</span></span>   | <span data-ttu-id="d395a-158">Type</span><span class="sxs-lookup"><span data-stu-id="d395a-158">Type</span></span>  | <span data-ttu-id="d395a-159">Description</span><span class="sxs-lookup"><span data-stu-id="d395a-159">Description</span></span>|
|--------|-------|------------|
|<span data-ttu-id="d395a-160">201 est créé</span><span class="sxs-lookup"><span data-stu-id="d395a-160">201 Created</span></span>||<span data-ttu-id="d395a-p102">Il s’agit d’une API personnalisée pour prendre en charge l’application d’un modèle à plusieurs bibliothèques de documents. En cas de réussite partielle, 201 créé peut toujours être retourné et l’appelant doit inspecter le corps de la réponse pour déterminer si le modèle a été correctement appliqué à une bibliothèque de documents.</span><span class="sxs-lookup"><span data-stu-id="d395a-p102">This is a customized API to support applying a model to multi document libraries. In the case of partial success, 201 created could still be returned and the caller needs to inspect the response body to understand if the model has been successfully applied to a document library.</span></span>|

## <a name="response-body"></a><span data-ttu-id="d395a-163">Corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="d395a-163">Response Body</span></span>

| <span data-ttu-id="d395a-164">Nom</span><span class="sxs-lookup"><span data-stu-id="d395a-164">Name</span></span>   | <span data-ttu-id="d395a-165">Type</span><span class="sxs-lookup"><span data-stu-id="d395a-165">Type</span></span>  | <span data-ttu-id="d395a-166">Description</span><span class="sxs-lookup"><span data-stu-id="d395a-166">Description</span></span>|
|--------|-------|------------|
|<span data-ttu-id="d395a-167">TotalSuccesses</span><span class="sxs-lookup"><span data-stu-id="d395a-167">TotalSuccesses</span></span>|<span data-ttu-id="d395a-168">int</span><span class="sxs-lookup"><span data-stu-id="d395a-168">int</span></span>|<span data-ttu-id="d395a-169">Le nombre total d’applications réussies d’un modèle à une bibliothèque de documents.</span><span class="sxs-lookup"><span data-stu-id="d395a-169">The total number of a model being successfully applied to a document library.</span></span>|
|<span data-ttu-id="d395a-170">TotalFailures</span><span class="sxs-lookup"><span data-stu-id="d395a-170">TotalFailures</span></span>|<span data-ttu-id="d395a-171">int</span><span class="sxs-lookup"><span data-stu-id="d395a-171">int</span></span>|<span data-ttu-id="d395a-172">Le nombre total d’applications défaillantes d’un modèle à une bibliothèque de documents.</span><span class="sxs-lookup"><span data-stu-id="d395a-172">The total number of a model failing to be applied to a document library.</span></span>|
|<span data-ttu-id="d395a-173">Détails</span><span class="sxs-lookup"><span data-stu-id="d395a-173">Details</span></span>|<span data-ttu-id="d395a-174">MachineLearningPublicationResult[]</span><span class="sxs-lookup"><span data-stu-id="d395a-174">MachineLearningPublicationResult[]</span></span>|<span data-ttu-id="d395a-175">La collection de chaque MachineLearningPublicationResult qui spécifie le résultat détaillé de l’application du modèle à la bibliothèque de documents.</span><span class="sxs-lookup"><span data-stu-id="d395a-175">The collection of MachineLearningPublicationResult each of which specifies the detailed result of applying the model to the document library.</span></span>|

### <a name="machinelearningpublicationresult"></a><span data-ttu-id="d395a-176">MachineLearningPublicationResult</span><span class="sxs-lookup"><span data-stu-id="d395a-176">MachineLearningPublicationResult</span></span>

| <span data-ttu-id="d395a-177">Nom</span><span class="sxs-lookup"><span data-stu-id="d395a-177">Name</span></span>   | <span data-ttu-id="d395a-178">Type</span><span class="sxs-lookup"><span data-stu-id="d395a-178">Type</span></span>  | <span data-ttu-id="d395a-179">Description</span><span class="sxs-lookup"><span data-stu-id="d395a-179">Description</span></span>|
|--------|-------|------------|
|<span data-ttu-id="d395a-180">StatusCode</span><span class="sxs-lookup"><span data-stu-id="d395a-180">StatusCode</span></span>|<span data-ttu-id="d395a-181">int</span><span class="sxs-lookup"><span data-stu-id="d395a-181">int</span></span>|<span data-ttu-id="d395a-182">Le code d’état HTTP.</span><span class="sxs-lookup"><span data-stu-id="d395a-182">The HTTP status code.</span></span>|
|<span data-ttu-id="d395a-183">ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="d395a-183">ErrorMessage</span></span>|<span data-ttu-id="d395a-184">chaîne</span><span class="sxs-lookup"><span data-stu-id="d395a-184">string</span></span>|<span data-ttu-id="d395a-185">Le message d’erreur indiquant le problème lors de l’application du modèle à la bibliothèque de documents.</span><span class="sxs-lookup"><span data-stu-id="d395a-185">The error message which tells what's wrong when apply the model to the document library.</span></span>|
|<span data-ttu-id="d395a-186">Publication</span><span class="sxs-lookup"><span data-stu-id="d395a-186">Publication</span></span>|<span data-ttu-id="d395a-187">MachineLearningPublicationEntityData</span><span class="sxs-lookup"><span data-stu-id="d395a-187">MachineLearningPublicationEntityData</span></span>|<span data-ttu-id="d395a-188">Il s’agit des informations sur le modèle et la bibliothèque de documents cible.</span><span class="sxs-lookup"><span data-stu-id="d395a-188">It specifies the model info and the target document library.</span></span>| 

### <a name="machinelearningpublicationentitydata"></a><span data-ttu-id="d395a-189">MachineLearningPublicationEntityData</span><span class="sxs-lookup"><span data-stu-id="d395a-189">MachineLearningPublicationEntityData</span></span>

| <span data-ttu-id="d395a-190">Nom</span><span class="sxs-lookup"><span data-stu-id="d395a-190">Name</span></span> | <span data-ttu-id="d395a-191">Type</span><span class="sxs-lookup"><span data-stu-id="d395a-191">Type</span></span> | <span data-ttu-id="d395a-192">Description</span><span class="sxs-lookup"><span data-stu-id="d395a-192">Description</span></span> |
|--------|--------|------------|
|<span data-ttu-id="d395a-193">ModelUniqueId</span><span class="sxs-lookup"><span data-stu-id="d395a-193">ModelUniqueId</span></span>|<span data-ttu-id="d395a-194">chaîne</span><span class="sxs-lookup"><span data-stu-id="d395a-194">string</span></span>|<span data-ttu-id="d395a-195">L'ID unique du fichier modèle.</span><span class="sxs-lookup"><span data-stu-id="d395a-195">The unique ID of the model file.</span></span>|
|<span data-ttu-id="d395a-196">TargetSiteUrl</span><span class="sxs-lookup"><span data-stu-id="d395a-196">TargetSiteUrl</span></span>|<span data-ttu-id="d395a-197">chaîne</span><span class="sxs-lookup"><span data-stu-id="d395a-197">string</span></span>|<span data-ttu-id="d395a-198">L’URL complète du site cible de bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="d395a-198">The full URL of the target library site.</span></span>|
|<span data-ttu-id="d395a-199">TargetWebServerRelativeUrl</span><span class="sxs-lookup"><span data-stu-id="d395a-199">TargetWebServerRelativeUrl</span></span>|<span data-ttu-id="d395a-200">chaîne</span><span class="sxs-lookup"><span data-stu-id="d395a-200">string</span></span>|<span data-ttu-id="d395a-201">L’URL du web relative au serveur pour la bibliothèque cible.</span><span class="sxs-lookup"><span data-stu-id="d395a-201">The server relative URL of the web for the target library.</span></span>|
|<span data-ttu-id="d395a-202">TargetLibraryServerRelativeUrl</span><span class="sxs-lookup"><span data-stu-id="d395a-202">TargetLibraryServerRelativeUrl</span></span>|<span data-ttu-id="d395a-203">chaîne</span><span class="sxs-lookup"><span data-stu-id="d395a-203">string</span></span>|<span data-ttu-id="d395a-204">L’URL relative au serveur pour la bibliothèque cible.</span><span class="sxs-lookup"><span data-stu-id="d395a-204">The server relative URL of the target library.</span></span>|

## <a name="examples"></a><span data-ttu-id="d395a-205">Exemples</span><span class="sxs-lookup"><span data-stu-id="d395a-205">Examples</span></span>

### <a name="apply-a-model-to-the-contracts-document-library-in-the-repository-site"></a><span data-ttu-id="d395a-206">Appliquer un modèle à la bibliothèque de documents concernant les contrats dans le site du référentiel</span><span class="sxs-lookup"><span data-stu-id="d395a-206">Apply a model to the contracts document library in the repository site</span></span>

<span data-ttu-id="d395a-207">Dans cet exemple, l’ID du modèle de compréhension de document du Contrat Contoso est `7645e69d-21fb-4a24-a17a-9bdfa7cb63dc`.</span><span class="sxs-lookup"><span data-stu-id="d395a-207">In this sample, the ID of the Contoso Contract document understanding model is `7645e69d-21fb-4a24-a17a-9bdfa7cb63dc`.</span></span>

#### <a name="sample-request"></a><span data-ttu-id="d395a-208">Exemple de demande</span><span class="sxs-lookup"><span data-stu-id="d395a-208">Sample request</span></span>

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


#### <a name="sample-response"></a><span data-ttu-id="d395a-209">Exemple de réponse</span><span class="sxs-lookup"><span data-stu-id="d395a-209">Sample response</span></span>

<span data-ttu-id="d395a-210">Dans la réponse, TotalFailures et TotalSuccesses font référence au nombre d’échecs et de réussite du modèle qui s’applique aux bibliothèques spécifiées.</span><span class="sxs-lookup"><span data-stu-id="d395a-210">In the response, TotalFailures and TotalSuccesses refers to the number of failures and successes of the model being applies to the specified libraries.</span></span>

<span data-ttu-id="d395a-211">**Code d'état :** 201</span><span class="sxs-lookup"><span data-stu-id="d395a-211">**Status code:** 201</span></span>

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
            "StatusCode": 201
        }
    ],
    "TotalFailures": 0,
    "TotalSuccesses": 1
}
```

## <a name="see-also"></a><span data-ttu-id="d395a-212">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d395a-212">See also</span></span>

[<span data-ttu-id="d395a-213">API REST du modèle de compréhension de document Syntex</span><span class="sxs-lookup"><span data-stu-id="d395a-213">Syntex document understanding model REST API</span></span>](syntex-model-rest-api.md)
