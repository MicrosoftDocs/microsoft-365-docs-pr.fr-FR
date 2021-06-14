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
ms.openlocfilehash: 8c7aeb449da161fe49050631643c63c93268a13f
ms.sourcegitcommit: 33d19853a38dfa4e6ed21b313976643670a14581
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2021
ms.locfileid: "52904209"
---
# <a name="batchdelete"></a><span data-ttu-id="45e88-103">BatchDelete</span><span class="sxs-lookup"><span data-stu-id="45e88-103">BatchDelete</span></span>

<span data-ttu-id="45e88-104">Supprime un modèle appliqué de compréhension de document à partir d’une ou plusieurs bibliothèques.</span><span class="sxs-lookup"><span data-stu-id="45e88-104">Removes an applied document understanding model from one or more libraries.</span></span> <span data-ttu-id="45e88-105">Notez qu’un modèle doit être supprimé de toutes les bibliothèques avant de pouvoir le supprimer (voir [exemple](rest-batchdelete-method.md#examples)).</span><span class="sxs-lookup"><span data-stu-id="45e88-105">Note that a model must be removed from all libraries before it can be deleted (see [example](rest-batchdelete-method.md#examples)).</span></span>

## <a name="http-request"></a><span data-ttu-id="45e88-106">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="45e88-106">HTTP request</span></span>

```HTTP
POST /_api/machinelearning/publications/batchdelete HTTP/1.1
```

## <a name="uri-parameters"></a><span data-ttu-id="45e88-107">Paramètres d’URI</span><span class="sxs-lookup"><span data-stu-id="45e88-107">URI parameters</span></span>

<span data-ttu-id="45e88-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="45e88-108">None</span></span>

## <a name="request-headers"></a><span data-ttu-id="45e88-109">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="45e88-109">Request headers</span></span>

| <span data-ttu-id="45e88-110">En-tête</span><span class="sxs-lookup"><span data-stu-id="45e88-110">Header</span></span> | <span data-ttu-id="45e88-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="45e88-111">Value</span></span> |
|--------|-------|
|<span data-ttu-id="45e88-112">Accepter</span><span class="sxs-lookup"><span data-stu-id="45e88-112">Accept</span></span>|<span data-ttu-id="45e88-113">application/json;odata=verbose</span><span class="sxs-lookup"><span data-stu-id="45e88-113">application/json;odata=verbose</span></span>|
|<span data-ttu-id="45e88-114">Content-Type</span><span class="sxs-lookup"><span data-stu-id="45e88-114">Content-Type</span></span>|<span data-ttu-id="45e88-115">application/json;odata=verbose;charset=utf-8</span><span class="sxs-lookup"><span data-stu-id="45e88-115">application/json;odata=verbose;charset=utf-8</span></span>|
|<span data-ttu-id="45e88-116">x-requestdigest</span><span class="sxs-lookup"><span data-stu-id="45e88-116">x-requestdigest</span></span>|<span data-ttu-id="45e88-117">Résumé approprié pour le site actuel.</span><span class="sxs-lookup"><span data-stu-id="45e88-117">The appropriate digest for current site.</span></span>|

## <a name="request-body"></a><span data-ttu-id="45e88-118">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="45e88-118">Request body</span></span>

| <span data-ttu-id="45e88-119">Nom</span><span class="sxs-lookup"><span data-stu-id="45e88-119">Name</span></span> | <span data-ttu-id="45e88-120">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="45e88-120">Required</span></span> | <span data-ttu-id="45e88-121">Type</span><span class="sxs-lookup"><span data-stu-id="45e88-121">Type</span></span> | <span data-ttu-id="45e88-122">Description</span><span class="sxs-lookup"><span data-stu-id="45e88-122">Description</span></span> |
|--------|-------|--------|------------|
|<span data-ttu-id="45e88-123">ModelUniqueId</span><span class="sxs-lookup"><span data-stu-id="45e88-123">ModelUniqueId</span></span>|<span data-ttu-id="45e88-124">oui</span><span class="sxs-lookup"><span data-stu-id="45e88-124">yes</span></span>|<span data-ttu-id="45e88-125">chaîne</span><span class="sxs-lookup"><span data-stu-id="45e88-125">string</span></span>|<span data-ttu-id="45e88-126">L'ID unique du fichier modèle.</span><span class="sxs-lookup"><span data-stu-id="45e88-126">The unique ID of the model file.</span></span>|
<span data-ttu-id="45e88-127">TargetSiteUrl</span><span class="sxs-lookup"><span data-stu-id="45e88-127">TargetSiteUrl</span></span>|<span data-ttu-id="45e88-128">oui</span><span class="sxs-lookup"><span data-stu-id="45e88-128">yes</span></span>|<span data-ttu-id="45e88-129">chaîne</span><span class="sxs-lookup"><span data-stu-id="45e88-129">string</span></span>|<span data-ttu-id="45e88-130">L’URL complète du site cible de bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="45e88-130">The full URL of the target library site.</span></span>|
<span data-ttu-id="45e88-131">TargetWebServerRelativeUrl</span><span class="sxs-lookup"><span data-stu-id="45e88-131">TargetWebServerRelativeUrl</span></span>|<span data-ttu-id="45e88-132">oui</span><span class="sxs-lookup"><span data-stu-id="45e88-132">yes</span></span>|<span data-ttu-id="45e88-133">chaîne</span><span class="sxs-lookup"><span data-stu-id="45e88-133">string</span></span>|<span data-ttu-id="45e88-134">L’URL du web relative au serveur pour la bibliothèque cible.</span><span class="sxs-lookup"><span data-stu-id="45e88-134">The server relative URL of the web for the target library.</span></span>|
<span data-ttu-id="45e88-135">TargetLibraryServerRelativeUrl</span><span class="sxs-lookup"><span data-stu-id="45e88-135">TargetLibraryServerRelativeUrl</span></span>|<span data-ttu-id="45e88-136">oui</span><span class="sxs-lookup"><span data-stu-id="45e88-136">yes</span></span>|<span data-ttu-id="45e88-137">chaîne</span><span class="sxs-lookup"><span data-stu-id="45e88-137">string</span></span>|<span data-ttu-id="45e88-138">L’URL relative au serveur pour la bibliothèque cible.</span><span class="sxs-lookup"><span data-stu-id="45e88-138">The server relative URL of the target library.</span></span>|
<span data-ttu-id="45e88-139">ViewOption</span><span class="sxs-lookup"><span data-stu-id="45e88-139">ViewOption</span></span>|<span data-ttu-id="45e88-140">Non</span><span class="sxs-lookup"><span data-stu-id="45e88-140">no</span></span>|<span data-ttu-id="45e88-141">string</span><span class="sxs-lookup"><span data-stu-id="45e88-141">string</span></span>|<span data-ttu-id="45e88-142">Spécifie s’il faut définir l’affichage du nouveau modèle comme bibliothèque par défaut.</span><span class="sxs-lookup"><span data-stu-id="45e88-142">Specifies whether to set new model view as the library default.</span></span>|

## <a name="response"></a><span data-ttu-id="45e88-143">Réponse</span><span class="sxs-lookup"><span data-stu-id="45e88-143">Response</span></span>

| <span data-ttu-id="45e88-144">Nom</span><span class="sxs-lookup"><span data-stu-id="45e88-144">Name</span></span>   | <span data-ttu-id="45e88-145">Type</span><span class="sxs-lookup"><span data-stu-id="45e88-145">Type</span></span>  | <span data-ttu-id="45e88-146">Description</span><span class="sxs-lookup"><span data-stu-id="45e88-146">Description</span></span>|
|--------|-------|------------|
|<span data-ttu-id="45e88-147">200 OK</span><span class="sxs-lookup"><span data-stu-id="45e88-147">200 OK</span></span>| |<span data-ttu-id="45e88-148">Opération réussie</span><span class="sxs-lookup"><span data-stu-id="45e88-148">Success</span></span>|


## <a name="examples"></a><span data-ttu-id="45e88-149">Exemples</span><span class="sxs-lookup"><span data-stu-id="45e88-149">Examples</span></span>

### <a name="remove-a-model-from-the-contracts-document-library-in-the-repository-site"></a><span data-ttu-id="45e88-150">Supprimer un modèle de la bibliothèque de documents concernant les contrats dans le site du référentiel</span><span class="sxs-lookup"><span data-stu-id="45e88-150">Remove a model from the contracts document library in the repository site</span></span>

<span data-ttu-id="45e88-151">Dans cet exemple, l’ID du modèle de compréhension de document du Contrat Contoso est `7645e69d-21fb-4a24-a17a-9bdfa7cb63dc`.</span><span class="sxs-lookup"><span data-stu-id="45e88-151">In this sample, the ID of the Contoso Contract document understanding model is `7645e69d-21fb-4a24-a17a-9bdfa7cb63dc`.</span></span>

#### <a name="sample-request"></a><span data-ttu-id="45e88-152">Exemple de demande</span><span class="sxs-lookup"><span data-stu-id="45e88-152">Sample request</span></span>

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


#### <a name="sample-response"></a><span data-ttu-id="45e88-153">Exemple de réponse</span><span class="sxs-lookup"><span data-stu-id="45e88-153">Sample response</span></span>

<span data-ttu-id="45e88-154">Dans la réponse, TotalFailures et TotalSuccesses font référence au nombre d’échecs et de réussite du modèle qui s’applique aux bibliothèques spécifiées.</span><span class="sxs-lookup"><span data-stu-id="45e88-154">In the response, TotalFailures and TotalSuccesses refer to the number of failures and successes of the model being applies to the specified libraries.</span></span>

<span data-ttu-id="45e88-155">**Code d’état :** 200</span><span class="sxs-lookup"><span data-stu-id="45e88-155">**Status code:** 200</span></span>

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

## <a name="see-also"></a><span data-ttu-id="45e88-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="45e88-156">See also</span></span>

[<span data-ttu-id="45e88-157">API REST du modèle de compréhension de document Syntex</span><span class="sxs-lookup"><span data-stu-id="45e88-157">Syntex document understanding model REST API</span></span>](syntex-model-rest-api.md)
