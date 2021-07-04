---
title: BatchDelete
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
description: Utilisez l’API REST pour supprimer un modèle appliqué de compréhension de document à partir d’une ou plusieurs bibliothèques.
ms.openlocfilehash: bbd3e496b50d3fddb31342fbc07d30984544e744
ms.sourcegitcommit: 4886457c0d4248407bddec56425dba50bb60d9c4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/03/2021
ms.locfileid: "53287452"
---
# <a name="batchdelete"></a><span data-ttu-id="3d832-103">BatchDelete</span><span class="sxs-lookup"><span data-stu-id="3d832-103">BatchDelete</span></span>

<span data-ttu-id="3d832-104">Supprime un modèle appliqué de compréhension de document à partir d’une ou plusieurs bibliothèques.</span><span class="sxs-lookup"><span data-stu-id="3d832-104">Removes an applied document understanding model from one or more libraries.</span></span> <span data-ttu-id="3d832-105">Notez qu’un modèle doit être supprimé de toutes les bibliothèques avant de pouvoir le supprimer (voir [exemple](rest-batchdelete-method.md#examples)).</span><span class="sxs-lookup"><span data-stu-id="3d832-105">Note that a model must be removed from all libraries before it can be deleted (see [example](rest-batchdelete-method.md#examples)).</span></span>

## <a name="http-request"></a><span data-ttu-id="3d832-106">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="3d832-106">HTTP request</span></span>

```HTTP
POST /_api/machinelearning/publications/batchdelete HTTP/1.1
```

## <a name="uri-parameters"></a><span data-ttu-id="3d832-107">Paramètres d’URI</span><span class="sxs-lookup"><span data-stu-id="3d832-107">URI parameters</span></span>

<span data-ttu-id="3d832-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="3d832-108">None</span></span>

## <a name="request-headers"></a><span data-ttu-id="3d832-109">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="3d832-109">Request headers</span></span>

| <span data-ttu-id="3d832-110">En-tête</span><span class="sxs-lookup"><span data-stu-id="3d832-110">Header</span></span> | <span data-ttu-id="3d832-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="3d832-111">Value</span></span> |
|--------|-------|
|<span data-ttu-id="3d832-112">Accepter</span><span class="sxs-lookup"><span data-stu-id="3d832-112">Accept</span></span>|<span data-ttu-id="3d832-113">application/json;odata=verbose</span><span class="sxs-lookup"><span data-stu-id="3d832-113">application/json;odata=verbose</span></span>|
|<span data-ttu-id="3d832-114">Content-Type</span><span class="sxs-lookup"><span data-stu-id="3d832-114">Content-Type</span></span>|<span data-ttu-id="3d832-115">application/json;odata=verbose;charset=utf-8</span><span class="sxs-lookup"><span data-stu-id="3d832-115">application/json;odata=verbose;charset=utf-8</span></span>|
|<span data-ttu-id="3d832-116">x-requestdigest</span><span class="sxs-lookup"><span data-stu-id="3d832-116">x-requestdigest</span></span>|<span data-ttu-id="3d832-117">Résumé approprié pour le site actuel.</span><span class="sxs-lookup"><span data-stu-id="3d832-117">The appropriate digest for current site.</span></span>|

## <a name="request-body"></a><span data-ttu-id="3d832-118">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="3d832-118">Request body</span></span>

| <span data-ttu-id="3d832-119">Nom</span><span class="sxs-lookup"><span data-stu-id="3d832-119">Name</span></span> | <span data-ttu-id="3d832-120">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="3d832-120">Required</span></span> | <span data-ttu-id="3d832-121">Type</span><span class="sxs-lookup"><span data-stu-id="3d832-121">Type</span></span> | <span data-ttu-id="3d832-122">Description</span><span class="sxs-lookup"><span data-stu-id="3d832-122">Description</span></span> |
|--------|-------|--------|------------|
|<span data-ttu-id="3d832-123">Publications</span><span class="sxs-lookup"><span data-stu-id="3d832-123">Publications</span></span>|<span data-ttu-id="3d832-124">oui</span><span class="sxs-lookup"><span data-stu-id="3d832-124">yes</span></span>|<span data-ttu-id="3d832-125">MachineLearningPublicationEntityData[]</span><span class="sxs-lookup"><span data-stu-id="3d832-125">MachineLearningPublicationEntityData[]</span></span>|<span data-ttu-id="3d832-126">La collection de chaque MachineLearningPublicationEntityData qui spécifie le modèle et la bibliothèque de documents cible.</span><span class="sxs-lookup"><span data-stu-id="3d832-126">The collection of MachineLearningPublicationEntityData each of which specifies the model and target document library.</span></span>|

### <a name="machinelearningpublicationentitydata"></a><span data-ttu-id="3d832-127">MachineLearningPublicationEntityData</span><span class="sxs-lookup"><span data-stu-id="3d832-127">MachineLearningPublicationEntityData</span></span>

| <span data-ttu-id="3d832-128">Nom</span><span class="sxs-lookup"><span data-stu-id="3d832-128">Name</span></span> | <span data-ttu-id="3d832-129">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="3d832-129">Required</span></span> | <span data-ttu-id="3d832-130">Type</span><span class="sxs-lookup"><span data-stu-id="3d832-130">Type</span></span> | <span data-ttu-id="3d832-131">Description</span><span class="sxs-lookup"><span data-stu-id="3d832-131">Description</span></span> |
|--------|-------|--------|------------|
|<span data-ttu-id="3d832-132">ModelUniqueId</span><span class="sxs-lookup"><span data-stu-id="3d832-132">ModelUniqueId</span></span>|<span data-ttu-id="3d832-133">oui</span><span class="sxs-lookup"><span data-stu-id="3d832-133">yes</span></span>|<span data-ttu-id="3d832-134">chaîne</span><span class="sxs-lookup"><span data-stu-id="3d832-134">string</span></span>|<span data-ttu-id="3d832-135">L'ID unique du fichier modèle.</span><span class="sxs-lookup"><span data-stu-id="3d832-135">The unique ID of the model file.</span></span>|
|<span data-ttu-id="3d832-136">TargetSiteUrl</span><span class="sxs-lookup"><span data-stu-id="3d832-136">TargetSiteUrl</span></span>|<span data-ttu-id="3d832-137">oui</span><span class="sxs-lookup"><span data-stu-id="3d832-137">yes</span></span>|<span data-ttu-id="3d832-138">chaîne</span><span class="sxs-lookup"><span data-stu-id="3d832-138">string</span></span>|<span data-ttu-id="3d832-139">L’URL complète du site cible de bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="3d832-139">The full URL of the target library site.</span></span>|
|<span data-ttu-id="3d832-140">TargetWebServerRelativeUrl</span><span class="sxs-lookup"><span data-stu-id="3d832-140">TargetWebServerRelativeUrl</span></span>|<span data-ttu-id="3d832-141">oui</span><span class="sxs-lookup"><span data-stu-id="3d832-141">yes</span></span>|<span data-ttu-id="3d832-142">chaîne</span><span class="sxs-lookup"><span data-stu-id="3d832-142">string</span></span>|<span data-ttu-id="3d832-143">L’URL du web relative au serveur pour la bibliothèque cible.</span><span class="sxs-lookup"><span data-stu-id="3d832-143">The server relative URL of the web for the target library.</span></span>|
|<span data-ttu-id="3d832-144">TargetLibraryServerRelativeUrl</span><span class="sxs-lookup"><span data-stu-id="3d832-144">TargetLibraryServerRelativeUrl</span></span>|<span data-ttu-id="3d832-145">oui</span><span class="sxs-lookup"><span data-stu-id="3d832-145">yes</span></span>|<span data-ttu-id="3d832-146">chaîne</span><span class="sxs-lookup"><span data-stu-id="3d832-146">string</span></span>|<span data-ttu-id="3d832-147">L’URL relative au serveur pour la bibliothèque cible.</span><span class="sxs-lookup"><span data-stu-id="3d832-147">The server relative URL of the target library.</span></span>|

## <a name="response"></a><span data-ttu-id="3d832-148">Réponse</span><span class="sxs-lookup"><span data-stu-id="3d832-148">Response</span></span>

| <span data-ttu-id="3d832-149">Nom</span><span class="sxs-lookup"><span data-stu-id="3d832-149">Name</span></span>   | <span data-ttu-id="3d832-150">Type</span><span class="sxs-lookup"><span data-stu-id="3d832-150">Type</span></span>  | <span data-ttu-id="3d832-151">Description</span><span class="sxs-lookup"><span data-stu-id="3d832-151">Description</span></span>|
|--------|-------|------------|
|<span data-ttu-id="3d832-152">200 OK</span><span class="sxs-lookup"><span data-stu-id="3d832-152">200 OK</span></span>||<span data-ttu-id="3d832-p102">Il s’agit d’une API personnalisée pour prendre en charge la suppression d’un modèle de plusieurs bibliothèques de documents. Dans le cas d’une réussite partielle, 200 OK créé peut encore être renvoyé et l’appelant doit inspecter le corps de la réponse pour savoir si le modèle a été correctement supprimé d’une bibliothèque de documents.</span><span class="sxs-lookup"><span data-stu-id="3d832-p102">This is a customized API to support removing a model from multi document libraries. In the case of partial success, 200 OK could still be returned and the caller needs to inspect the response body to understand if the model has been successfully removed from a document library.</span></span>|

## <a name="response-body"></a><span data-ttu-id="3d832-155">Corps de la réponse</span><span class="sxs-lookup"><span data-stu-id="3d832-155">Response Body</span></span>

| <span data-ttu-id="3d832-156">Nom</span><span class="sxs-lookup"><span data-stu-id="3d832-156">Name</span></span>   | <span data-ttu-id="3d832-157">Type</span><span class="sxs-lookup"><span data-stu-id="3d832-157">Type</span></span>  | <span data-ttu-id="3d832-158">Description</span><span class="sxs-lookup"><span data-stu-id="3d832-158">Description</span></span>|
|--------|-------|------------|
|<span data-ttu-id="3d832-159">TotalSuccesses</span><span class="sxs-lookup"><span data-stu-id="3d832-159">TotalSuccesses</span></span>|<span data-ttu-id="3d832-160">int</span><span class="sxs-lookup"><span data-stu-id="3d832-160">int</span></span>|<span data-ttu-id="3d832-161">Le nombre total de suppressions réussies d’un modèle dans une bibliothèque de documents.</span><span class="sxs-lookup"><span data-stu-id="3d832-161">The total number of a model being successfully removed from a document library.</span></span>|
|<span data-ttu-id="3d832-162">TotalFailures</span><span class="sxs-lookup"><span data-stu-id="3d832-162">TotalFailures</span></span>|<span data-ttu-id="3d832-163">int</span><span class="sxs-lookup"><span data-stu-id="3d832-163">int</span></span>|<span data-ttu-id="3d832-164">Le nombre total de suppressions défaillantes d’un modèle dans une bibliothèque de documents.</span><span class="sxs-lookup"><span data-stu-id="3d832-164">The total number of a model failing to be removed from a document library.</span></span>|
|<span data-ttu-id="3d832-165">Détails</span><span class="sxs-lookup"><span data-stu-id="3d832-165">Details</span></span>|<span data-ttu-id="3d832-166">MachineLearningPublicationResult[]</span><span class="sxs-lookup"><span data-stu-id="3d832-166">MachineLearningPublicationResult[]</span></span>|<span data-ttu-id="3d832-167">La collection de chaque MachineLearningPublicationResult qui spécifie le résultat détaillé de la suppression du modèle dans une bibliothèque de documents.</span><span class="sxs-lookup"><span data-stu-id="3d832-167">The collection of MachineLearningPublicationResult each of which specifies the detailed result of removing the model from a document library.</span></span>|

### <a name="machinelearningpublicationresult"></a><span data-ttu-id="3d832-168">MachineLearningPublicationResult</span><span class="sxs-lookup"><span data-stu-id="3d832-168">MachineLearningPublicationResult</span></span>

| <span data-ttu-id="3d832-169">Nom</span><span class="sxs-lookup"><span data-stu-id="3d832-169">Name</span></span>   | <span data-ttu-id="3d832-170">Type</span><span class="sxs-lookup"><span data-stu-id="3d832-170">Type</span></span>  | <span data-ttu-id="3d832-171">Description</span><span class="sxs-lookup"><span data-stu-id="3d832-171">Description</span></span>|
|--------|-------|------------|
|<span data-ttu-id="3d832-172">StatusCode</span><span class="sxs-lookup"><span data-stu-id="3d832-172">StatusCode</span></span>|<span data-ttu-id="3d832-173">int</span><span class="sxs-lookup"><span data-stu-id="3d832-173">int</span></span>|<span data-ttu-id="3d832-174">Le code d’état HTTP.</span><span class="sxs-lookup"><span data-stu-id="3d832-174">The HTTP status code.</span></span>|
|<span data-ttu-id="3d832-175">ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="3d832-175">ErrorMessage</span></span>|<span data-ttu-id="3d832-176">chaîne</span><span class="sxs-lookup"><span data-stu-id="3d832-176">string</span></span>|<span data-ttu-id="3d832-177">Le message d’erreur indiquant le problème lors de l’application du modèle à la bibliothèque de documents.</span><span class="sxs-lookup"><span data-stu-id="3d832-177">The error message which tells what's wrong when apply the model to the document library.</span></span>|
|<span data-ttu-id="3d832-178">Publication</span><span class="sxs-lookup"><span data-stu-id="3d832-178">Publication</span></span>|<span data-ttu-id="3d832-179">MachineLearningPublicationEntityData</span><span class="sxs-lookup"><span data-stu-id="3d832-179">MachineLearningPublicationEntityData</span></span>|<span data-ttu-id="3d832-180">Il s’agit des informations sur le modèle et la bibliothèque de documents cible.</span><span class="sxs-lookup"><span data-stu-id="3d832-180">It specifies the model info and the target document library.</span></span>| 

### <a name="machinelearningpublicationentitydata"></a><span data-ttu-id="3d832-181">MachineLearningPublicationEntityData</span><span class="sxs-lookup"><span data-stu-id="3d832-181">MachineLearningPublicationEntityData</span></span>

| <span data-ttu-id="3d832-182">Nom</span><span class="sxs-lookup"><span data-stu-id="3d832-182">Name</span></span> | <span data-ttu-id="3d832-183">Type</span><span class="sxs-lookup"><span data-stu-id="3d832-183">Type</span></span> | <span data-ttu-id="3d832-184">Description</span><span class="sxs-lookup"><span data-stu-id="3d832-184">Description</span></span> |
|--------|--------|------------|
|<span data-ttu-id="3d832-185">ModelUniqueId</span><span class="sxs-lookup"><span data-stu-id="3d832-185">ModelUniqueId</span></span>|<span data-ttu-id="3d832-186">chaîne</span><span class="sxs-lookup"><span data-stu-id="3d832-186">string</span></span>|<span data-ttu-id="3d832-187">L'ID unique du fichier modèle.</span><span class="sxs-lookup"><span data-stu-id="3d832-187">The unique ID of the model file.</span></span>|
|<span data-ttu-id="3d832-188">TargetSiteUrl</span><span class="sxs-lookup"><span data-stu-id="3d832-188">TargetSiteUrl</span></span>|<span data-ttu-id="3d832-189">chaîne</span><span class="sxs-lookup"><span data-stu-id="3d832-189">string</span></span>|<span data-ttu-id="3d832-190">L’URL complète du site cible de bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="3d832-190">The full URL of the target library site.</span></span>|
|<span data-ttu-id="3d832-191">TargetWebServerRelativeUrl</span><span class="sxs-lookup"><span data-stu-id="3d832-191">TargetWebServerRelativeUrl</span></span>|<span data-ttu-id="3d832-192">chaîne</span><span class="sxs-lookup"><span data-stu-id="3d832-192">string</span></span>|<span data-ttu-id="3d832-193">L’URL du web relative au serveur pour la bibliothèque cible.</span><span class="sxs-lookup"><span data-stu-id="3d832-193">The server relative URL of the web for the target library.</span></span>|
|<span data-ttu-id="3d832-194">TargetLibraryServerRelativeUrl</span><span class="sxs-lookup"><span data-stu-id="3d832-194">TargetLibraryServerRelativeUrl</span></span>|<span data-ttu-id="3d832-195">chaîne</span><span class="sxs-lookup"><span data-stu-id="3d832-195">string</span></span>|<span data-ttu-id="3d832-196">L’URL relative au serveur pour la bibliothèque cible.</span><span class="sxs-lookup"><span data-stu-id="3d832-196">The server relative URL of the target library.</span></span>|

## <a name="examples"></a><span data-ttu-id="3d832-197">Exemples</span><span class="sxs-lookup"><span data-stu-id="3d832-197">Examples</span></span>

### <a name="remove-a-model-from-the-contracts-document-library-in-the-repository-site"></a><span data-ttu-id="3d832-198">Supprimer un modèle de la bibliothèque de documents concernant les contrats dans le site du référentiel</span><span class="sxs-lookup"><span data-stu-id="3d832-198">Remove a model from the contracts document library in the repository site</span></span>

<span data-ttu-id="3d832-199">Dans cet exemple, l’ID du modèle de compréhension de document du Contrat Contoso est `7645e69d-21fb-4a24-a17a-9bdfa7cb63dc`.</span><span class="sxs-lookup"><span data-stu-id="3d832-199">In this sample, the ID of the Contoso Contract document understanding model is `7645e69d-21fb-4a24-a17a-9bdfa7cb63dc`.</span></span>

#### <a name="sample-request"></a><span data-ttu-id="3d832-200">Exemple de demande</span><span class="sxs-lookup"><span data-stu-id="3d832-200">Sample request</span></span>

```HTTP
{ 
    "publications": [ 
        { 
            "ModelUniqueId": "7645e69d-21fb-4a24-a17a-9bdfa7cb63dc", 
            "TargetSiteUrl": "https://constco.sharepoint-df.com/sites/docsite", 
            "TargetWebServerRelativeUrl": "/sites/docsite ", 
            "TargetLibraryServerRelativeUrl": "/sites/dcocsite/joedcos" 
        } 
    ] 
} 
```

#### <a name="sample-response"></a><span data-ttu-id="3d832-201">Exemple de réponse</span><span class="sxs-lookup"><span data-stu-id="3d832-201">Sample response</span></span>

<span data-ttu-id="3d832-202">Dans la réponse, TotalFailures et TotalSuccesses font référence au nombre d’échecs et de réussites de la suppression du modèle dans les bibliothèques spécifiées.</span><span class="sxs-lookup"><span data-stu-id="3d832-202">In the response, TotalFailures and TotalSuccesses refer to the number of failures and successes of the model being removed from the specified libraries.</span></span>

<span data-ttu-id="3d832-203">**Code d’état :** 200</span><span class="sxs-lookup"><span data-stu-id="3d832-203">**Status code:** 200</span></span>

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

## <a name="see-also"></a><span data-ttu-id="3d832-204">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3d832-204">See also</span></span>

[<span data-ttu-id="3d832-205">API REST du modèle de compréhension de document Syntex</span><span class="sxs-lookup"><span data-stu-id="3d832-205">Syntex document understanding model REST API</span></span>](syntex-model-rest-api.md)
