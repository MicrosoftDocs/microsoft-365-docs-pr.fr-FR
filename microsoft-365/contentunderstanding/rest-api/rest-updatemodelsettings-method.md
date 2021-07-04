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
ms.openlocfilehash: c75f669913f16233c6015230a60643cf86f33f5a
ms.sourcegitcommit: 4886457c0d4248407bddec56425dba50bb60d9c4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/03/2021
ms.locfileid: "53288646"
---
# <a name="updatemodelsettings"></a><span data-ttu-id="1ab20-103">UpdateModelSettings</span><span class="sxs-lookup"><span data-stu-id="1ab20-103">UpdateModelSettings</span></span>

<span data-ttu-id="1ab20-104">Met à jour les paramètres des modèles disponibles (description du modèle et étiquette de rétention associés) pour un modèle de compréhension de document SharePoint Syntex (voir [exemple](rest-updatemodelsettings-method.md#examples)).</span><span class="sxs-lookup"><span data-stu-id="1ab20-104">Updates available models settings (associated retention label and model description) for a SharePoint Syntex document understanding model (see [example](rest-updatemodelsettings-method.md#examples)).</span></span>

## <a name="http-request"></a><span data-ttu-id="1ab20-105">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="1ab20-105">HTTP request</span></span>

```HTTP
POST /_api/machinelearning/models/getbytitle('{modelFileName}')/updatemodelsettings HTTP/1.1
```

## <a name="uri-parameters"></a><span data-ttu-id="1ab20-106">Paramètres d’URI</span><span class="sxs-lookup"><span data-stu-id="1ab20-106">URI parameters</span></span>

|<span data-ttu-id="1ab20-107">Nom</span><span class="sxs-lookup"><span data-stu-id="1ab20-107">Name</span></span> |<span data-ttu-id="1ab20-108">Dans le paramètre</span><span class="sxs-lookup"><span data-stu-id="1ab20-108">In</span></span> |<span data-ttu-id="1ab20-109">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="1ab20-109">Required</span></span>|<span data-ttu-id="1ab20-110">Type</span><span class="sxs-lookup"><span data-stu-id="1ab20-110">Type</span></span>|<span data-ttu-id="1ab20-111">Description</span><span class="sxs-lookup"><span data-stu-id="1ab20-111">Description</span></span>|
|-----|---|--------|----|-----------|
|<span data-ttu-id="1ab20-112">modelFileName</span><span class="sxs-lookup"><span data-stu-id="1ab20-112">modelFileName</span></span>|<span data-ttu-id="1ab20-113">requête</span><span class="sxs-lookup"><span data-stu-id="1ab20-113">query</span></span>|<span data-ttu-id="1ab20-114">True</span><span class="sxs-lookup"><span data-stu-id="1ab20-114">True</span></span>|<span data-ttu-id="1ab20-115">string</span><span class="sxs-lookup"><span data-stu-id="1ab20-115">string</span></span>|<span data-ttu-id="1ab20-116">Nom du fichier de modèle Syntex.</span><span class="sxs-lookup"><span data-stu-id="1ab20-116">Name of the Syntex model file.</span></span>|

## <a name="request-headers"></a><span data-ttu-id="1ab20-117">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="1ab20-117">Request headers</span></span>

| <span data-ttu-id="1ab20-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="1ab20-118">Header</span></span> | <span data-ttu-id="1ab20-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="1ab20-119">Value</span></span> |
|--------|-------|
|<span data-ttu-id="1ab20-120">Accepter</span><span class="sxs-lookup"><span data-stu-id="1ab20-120">Accept</span></span>|<span data-ttu-id="1ab20-121">application/json;odata=verbose</span><span class="sxs-lookup"><span data-stu-id="1ab20-121">application/json;odata=verbose</span></span>|
|<span data-ttu-id="1ab20-122">Content-Type</span><span class="sxs-lookup"><span data-stu-id="1ab20-122">Content-Type</span></span>|<span data-ttu-id="1ab20-123">application/json;odata=verbose;charset=utf-8</span><span class="sxs-lookup"><span data-stu-id="1ab20-123">application/json;odata=verbose;charset=utf-8</span></span>|
|<span data-ttu-id="1ab20-124">x-requestdigest</span><span class="sxs-lookup"><span data-stu-id="1ab20-124">x-requestdigest</span></span>|<span data-ttu-id="1ab20-125">Résumé approprié pour le site actuel.</span><span class="sxs-lookup"><span data-stu-id="1ab20-125">The appropriate digest for the current site.</span></span>|

## <a name="request-body"></a><span data-ttu-id="1ab20-126">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="1ab20-126">Request body</span></span>

|<span data-ttu-id="1ab20-127">Nom</span><span class="sxs-lookup"><span data-stu-id="1ab20-127">Name</span></span>    |<span data-ttu-id="1ab20-128">Type</span><span class="sxs-lookup"><span data-stu-id="1ab20-128">Type</span></span>   |<span data-ttu-id="1ab20-129">Description</span><span class="sxs-lookup"><span data-stu-id="1ab20-129">Description</span></span> |
|--------|-------|-------|
|<span data-ttu-id="1ab20-130">ModelSettings</span><span class="sxs-lookup"><span data-stu-id="1ab20-130">ModelSettings</span></span>|<span data-ttu-id="1ab20-131">chaîne</span><span class="sxs-lookup"><span data-stu-id="1ab20-131">string</span></span>|<span data-ttu-id="1ab20-132">JSON des paramètres du modèle.</span><span class="sxs-lookup"><span data-stu-id="1ab20-132">JSON of model settings.</span></span>|
|<span data-ttu-id="1ab20-133">Description</span><span class="sxs-lookup"><span data-stu-id="1ab20-133">Description</span></span>|<span data-ttu-id="1ab20-134">string</span><span class="sxs-lookup"><span data-stu-id="1ab20-134">string</span></span>|<span data-ttu-id="1ab20-135">La description du modèle.</span><span class="sxs-lookup"><span data-stu-id="1ab20-135">The model description.</span></span>|
|<span data-ttu-id="1ab20-136">ÉtiquetteRétention</span><span class="sxs-lookup"><span data-stu-id="1ab20-136">RetentionLabel</span></span>| |<span data-ttu-id="1ab20-137">Informations sur l’étiquette associée (nom et ID d’étiquette).</span><span class="sxs-lookup"><span data-stu-id="1ab20-137">Info for the associated label (label ID and name).</span></span>|

## <a name="responses"></a><span data-ttu-id="1ab20-138">Réponses</span><span class="sxs-lookup"><span data-stu-id="1ab20-138">Responses</span></span>

| <span data-ttu-id="1ab20-139">Nom</span><span class="sxs-lookup"><span data-stu-id="1ab20-139">Name</span></span>   | <span data-ttu-id="1ab20-140">Type</span><span class="sxs-lookup"><span data-stu-id="1ab20-140">Type</span></span>  | <span data-ttu-id="1ab20-141">Description</span><span class="sxs-lookup"><span data-stu-id="1ab20-141">Description</span></span>|
|--------|-------|------------|
|<span data-ttu-id="1ab20-142">200 OK</span><span class="sxs-lookup"><span data-stu-id="1ab20-142">200 OK</span></span>| |<span data-ttu-id="1ab20-143">Opération réussie</span><span class="sxs-lookup"><span data-stu-id="1ab20-143">Success</span></span>|

## <a name="examples"></a><span data-ttu-id="1ab20-144">Exemples</span><span class="sxs-lookup"><span data-stu-id="1ab20-144">Examples</span></span>

### <a name="update-model-settings-for-contoso-contract"></a><span data-ttu-id="1ab20-145">Mettre à jour les paramètres du modèle pour le Contrat Contoso</span><span class="sxs-lookup"><span data-stu-id="1ab20-145">Update model settings for Contoso Contract</span></span>

<span data-ttu-id="1ab20-146">Dans cette exemple, la description du modèle et l’étiquette de rétention « Conservation standard » sont mises à jour.</span><span class="sxs-lookup"><span data-stu-id="1ab20-146">In this example, the model description and "Standard Hold" retention label are updated.</span></span> <span data-ttu-id="1ab20-147">L’ID de l’étiquette de rétention est `27c5fcba-abfd-4c34-823d-0b4a48f7ffe6`.</span><span class="sxs-lookup"><span data-stu-id="1ab20-147">The ID of the retention label is `27c5fcba-abfd-4c34-823d-0b4a48f7ffe6`.</span></span>

#### <a name="sample-request"></a><span data-ttu-id="1ab20-148">Exemple de demande</span><span class="sxs-lookup"><span data-stu-id="1ab20-148">Sample request</span></span>

```HTTP
{
    "ModelSettings": "{\"Description\":\"This model is used to set files classified as Contoso Contracts with a standard hold retention.\", \"RetentionLabel\":{\"Id\":\"27c5fcba-abfd-4c34-823d-0b4a48f7ffe6\",\"Name\":\"Standard Hold\"}}"
}

```

#### <a name="sample-response"></a><span data-ttu-id="1ab20-149">Exemple de réponse</span><span class="sxs-lookup"><span data-stu-id="1ab20-149">Sample response</span></span>

<span data-ttu-id="1ab20-150">**Code d’état :** 200</span><span class="sxs-lookup"><span data-stu-id="1ab20-150">**Status code:** 200</span></span>

## <a name="see-also"></a><span data-ttu-id="1ab20-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1ab20-151">See also</span></span>

[<span data-ttu-id="1ab20-152">API REST du modèle de compréhension de document Syntex</span><span class="sxs-lookup"><span data-stu-id="1ab20-152">Syntex document understanding model REST API</span></span>](syntex-model-rest-api.md)
