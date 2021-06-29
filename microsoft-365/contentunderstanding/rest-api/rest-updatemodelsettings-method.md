---
title: UpdateModelSettings
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
description: Utilisez l’API REST pour mettre à jour les paramètres des modèles disponibles pour un modèle de compréhension de document SharePoint Syntex.
ms.openlocfilehash: cd288812044f3b02839c3c11c321947bd02cccaa
ms.sourcegitcommit: cfd7644570831ceb7f57c61401df6a0001ef0a6a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/29/2021
ms.locfileid: "53177164"
---
# <a name="updatemodelsettings"></a><span data-ttu-id="f7fd0-103">UpdateModelSettings</span><span class="sxs-lookup"><span data-stu-id="f7fd0-103">UpdateModelSettings</span></span>

<span data-ttu-id="f7fd0-104">Met à jour les paramètres des modèles disponibles (description du modèle et étiquette de rétention associés) pour un modèle de compréhension de document SharePoint Syntex (voir [exemple](rest-updatemodelsettings-method.md#examples)).</span><span class="sxs-lookup"><span data-stu-id="f7fd0-104">Updates available models settings (associated retention label and model description) for a SharePoint Syntex document understanding model (see [example](rest-updatemodelsettings-method.md#examples)).</span></span>

## <a name="http-request"></a><span data-ttu-id="f7fd0-105">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="f7fd0-105">HTTP request</span></span>

```HTTP
POST /_api/machinelearning/models/getbytitle('{modelFileName}')/updatemodelsettings HTTP/1.1
```

## <a name="uri-parameters"></a><span data-ttu-id="f7fd0-106">Paramètres d’URI</span><span class="sxs-lookup"><span data-stu-id="f7fd0-106">URI parameters</span></span>

|<span data-ttu-id="f7fd0-107">Nom</span><span class="sxs-lookup"><span data-stu-id="f7fd0-107">Name</span></span> |<span data-ttu-id="f7fd0-108">Dans le paramètre</span><span class="sxs-lookup"><span data-stu-id="f7fd0-108">In</span></span> |<span data-ttu-id="f7fd0-109">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="f7fd0-109">Required</span></span>|<span data-ttu-id="f7fd0-110">Type</span><span class="sxs-lookup"><span data-stu-id="f7fd0-110">Type</span></span>|<span data-ttu-id="f7fd0-111">Description</span><span class="sxs-lookup"><span data-stu-id="f7fd0-111">Description</span></span>|
|-----|---|--------|----|-----------|
|<span data-ttu-id="f7fd0-112">modelFileName</span><span class="sxs-lookup"><span data-stu-id="f7fd0-112">modelFileName</span></span>|<span data-ttu-id="f7fd0-113">requête</span><span class="sxs-lookup"><span data-stu-id="f7fd0-113">query</span></span>|<span data-ttu-id="f7fd0-114">True</span><span class="sxs-lookup"><span data-stu-id="f7fd0-114">True</span></span>|<span data-ttu-id="f7fd0-115">string</span><span class="sxs-lookup"><span data-stu-id="f7fd0-115">string</span></span>|<span data-ttu-id="f7fd0-116">Nom du fichier de modèle Syntex.</span><span class="sxs-lookup"><span data-stu-id="f7fd0-116">Name of the Syntex model file.</span></span>|

## <a name="request-headers"></a><span data-ttu-id="f7fd0-117">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="f7fd0-117">Request headers</span></span>

| <span data-ttu-id="f7fd0-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="f7fd0-118">Header</span></span> | <span data-ttu-id="f7fd0-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="f7fd0-119">Value</span></span> |
|--------|-------|
|<span data-ttu-id="f7fd0-120">Accepter</span><span class="sxs-lookup"><span data-stu-id="f7fd0-120">Accept</span></span>|<span data-ttu-id="f7fd0-121">application/json;odata=verbose</span><span class="sxs-lookup"><span data-stu-id="f7fd0-121">application/json;odata=verbose</span></span>|
|<span data-ttu-id="f7fd0-122">Content-Type</span><span class="sxs-lookup"><span data-stu-id="f7fd0-122">Content-Type</span></span>|<span data-ttu-id="f7fd0-123">application/json;odata=verbose;charset=utf-8</span><span class="sxs-lookup"><span data-stu-id="f7fd0-123">application/json;odata=verbose;charset=utf-8</span></span>|
|<span data-ttu-id="f7fd0-124">x-requestdigest</span><span class="sxs-lookup"><span data-stu-id="f7fd0-124">x-requestdigest</span></span>|<span data-ttu-id="f7fd0-125">Résumé approprié pour le site actuel.</span><span class="sxs-lookup"><span data-stu-id="f7fd0-125">The appropriate digest for the current site.</span></span>|

## <a name="request-body"></a><span data-ttu-id="f7fd0-126">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="f7fd0-126">Request body</span></span>

|<span data-ttu-id="f7fd0-127">Nom</span><span class="sxs-lookup"><span data-stu-id="f7fd0-127">Name</span></span>    |<span data-ttu-id="f7fd0-128">Type</span><span class="sxs-lookup"><span data-stu-id="f7fd0-128">Type</span></span>   |<span data-ttu-id="f7fd0-129">Description</span><span class="sxs-lookup"><span data-stu-id="f7fd0-129">Description</span></span> |
|--------|-------|-------|
|<span data-ttu-id="f7fd0-130">ModelSettings</span><span class="sxs-lookup"><span data-stu-id="f7fd0-130">ModelSettings</span></span>|<span data-ttu-id="f7fd0-131">chaîne</span><span class="sxs-lookup"><span data-stu-id="f7fd0-131">string</span></span>|<span data-ttu-id="f7fd0-132">JSON des paramètres du modèle.</span><span class="sxs-lookup"><span data-stu-id="f7fd0-132">JSON of model settings.</span></span>|
|<span data-ttu-id="f7fd0-133">Description</span><span class="sxs-lookup"><span data-stu-id="f7fd0-133">Description</span></span>|<span data-ttu-id="f7fd0-134">string</span><span class="sxs-lookup"><span data-stu-id="f7fd0-134">string</span></span>|<span data-ttu-id="f7fd0-135">La description du modèle.</span><span class="sxs-lookup"><span data-stu-id="f7fd0-135">The model description.</span></span>|
|<span data-ttu-id="f7fd0-136">ÉtiquetteRétention</span><span class="sxs-lookup"><span data-stu-id="f7fd0-136">RetentionLabel</span></span>| |<span data-ttu-id="f7fd0-137">Informations sur l’étiquette associée (nom et ID d’étiquette).</span><span class="sxs-lookup"><span data-stu-id="f7fd0-137">Info for the associated label (label ID and name).</span></span>|

## <a name="responses"></a><span data-ttu-id="f7fd0-138">Réponses</span><span class="sxs-lookup"><span data-stu-id="f7fd0-138">Responses</span></span>

| <span data-ttu-id="f7fd0-139">Nom</span><span class="sxs-lookup"><span data-stu-id="f7fd0-139">Name</span></span>   | <span data-ttu-id="f7fd0-140">Type</span><span class="sxs-lookup"><span data-stu-id="f7fd0-140">Type</span></span>  | <span data-ttu-id="f7fd0-141">Description</span><span class="sxs-lookup"><span data-stu-id="f7fd0-141">Description</span></span>|
|--------|-------|------------|
|<span data-ttu-id="f7fd0-142">200 OK</span><span class="sxs-lookup"><span data-stu-id="f7fd0-142">200 OK</span></span>| |<span data-ttu-id="f7fd0-143">Opération réussie</span><span class="sxs-lookup"><span data-stu-id="f7fd0-143">Success</span></span>|

## <a name="examples"></a><span data-ttu-id="f7fd0-144">Exemples</span><span class="sxs-lookup"><span data-stu-id="f7fd0-144">Examples</span></span>

### <a name="update-model-settings-for-contoso-contract"></a><span data-ttu-id="f7fd0-145">Mettre à jour les paramètres du modèle pour le Contrat Contoso</span><span class="sxs-lookup"><span data-stu-id="f7fd0-145">Update model settings for Contoso Contract</span></span>

<span data-ttu-id="f7fd0-146">Dans cette exemple, la description du modèle et l’étiquette de rétention « Conservation standard » sont mises à jour.</span><span class="sxs-lookup"><span data-stu-id="f7fd0-146">In this example, the model description and "Standard Hold" retention label are updated.</span></span> <span data-ttu-id="f7fd0-147">L’ID de l’étiquette de rétention est `27c5fcba-abfd-4c34-823d-0b4a48f7ffe6`.</span><span class="sxs-lookup"><span data-stu-id="f7fd0-147">The ID of the retention label is `27c5fcba-abfd-4c34-823d-0b4a48f7ffe6`.</span></span>

#### <a name="sample-request"></a><span data-ttu-id="f7fd0-148">Exemple de demande</span><span class="sxs-lookup"><span data-stu-id="f7fd0-148">Sample request</span></span>

```HTTP
{
    "ModelSettings": "{\"Description\":\"This model is used to set files classified as Contoso Contracts with a standard hold retention.\", \"RetentionLabel\":{\"Id\":\"27c5fcba-abfd-4c34-823d-0b4a48f7ffe6\",\"Name\":\"Standard Hold\"}}"
}

```

#### <a name="sample-response"></a><span data-ttu-id="f7fd0-149">Exemple de réponse</span><span class="sxs-lookup"><span data-stu-id="f7fd0-149">Sample response</span></span>

<span data-ttu-id="f7fd0-150">**Code d’état :** 200</span><span class="sxs-lookup"><span data-stu-id="f7fd0-150">**Status code:** 200</span></span>

## <a name="see-also"></a><span data-ttu-id="f7fd0-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f7fd0-151">See also</span></span>

[<span data-ttu-id="f7fd0-152">API REST du modèle de compréhension de document Syntex</span><span class="sxs-lookup"><span data-stu-id="f7fd0-152">Syntex document understanding model REST API</span></span>](syntex-model-rest-api.md)
