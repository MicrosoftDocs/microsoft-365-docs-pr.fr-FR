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
ms.openlocfilehash: f24fc8428adbf22ded2ca6d7a49cabc84b385770
ms.sourcegitcommit: 33d19853a38dfa4e6ed21b313976643670a14581
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2021
ms.locfileid: "52904227"
---
# <a name="updatemodelsettings"></a><span data-ttu-id="fd885-103">UpdateModelSettings</span><span class="sxs-lookup"><span data-stu-id="fd885-103">UpdateModelSettings</span></span>

<span data-ttu-id="fd885-104">Met à jour les paramètres des modèles disponibles (description du modèle et étiquette de rétention associés) pour un modèle de compréhension de document SharePoint Syntex (voir [exemple](rest-updatemodelsettings-method.md#examples)).</span><span class="sxs-lookup"><span data-stu-id="fd885-104">Updates available models settings (associated retention label and model description) for a SharePoint Syntex document understanding model (see [example](rest-updatemodelsettings-method.md#examples)).</span></span>

## <a name="http-request"></a><span data-ttu-id="fd885-105">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="fd885-105">HTTP request</span></span>

```HTTP
POST /_api/machinelearning/models/updatemodelsettings HTTP/1.1
```

## <a name="uri-parameters"></a><span data-ttu-id="fd885-106">Paramètres d’URI</span><span class="sxs-lookup"><span data-stu-id="fd885-106">URI parameters</span></span>

<span data-ttu-id="fd885-107">Aucun</span><span class="sxs-lookup"><span data-stu-id="fd885-107">None</span></span>

## <a name="request-headers"></a><span data-ttu-id="fd885-108">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="fd885-108">Request headers</span></span>

| <span data-ttu-id="fd885-109">En-tête</span><span class="sxs-lookup"><span data-stu-id="fd885-109">Header</span></span> | <span data-ttu-id="fd885-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="fd885-110">Value</span></span> |
|--------|-------|
|<span data-ttu-id="fd885-111">Accepter</span><span class="sxs-lookup"><span data-stu-id="fd885-111">Accept</span></span>|<span data-ttu-id="fd885-112">application/json;odata=verbose</span><span class="sxs-lookup"><span data-stu-id="fd885-112">application/json;odata=verbose</span></span>|
|<span data-ttu-id="fd885-113">Content-Type</span><span class="sxs-lookup"><span data-stu-id="fd885-113">Content-Type</span></span>|<span data-ttu-id="fd885-114">application/json;odata=verbose;charset=utf-8</span><span class="sxs-lookup"><span data-stu-id="fd885-114">application/json;odata=verbose;charset=utf-8</span></span>|
|<span data-ttu-id="fd885-115">x-requestdigest</span><span class="sxs-lookup"><span data-stu-id="fd885-115">x-requestdigest</span></span>|<span data-ttu-id="fd885-116">Résumé approprié pour le site actuel.</span><span class="sxs-lookup"><span data-stu-id="fd885-116">The appropriate digest for the current site.</span></span>|

## <a name="request-body"></a><span data-ttu-id="fd885-117">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="fd885-117">Request body</span></span>

|<span data-ttu-id="fd885-118">Nom</span><span class="sxs-lookup"><span data-stu-id="fd885-118">Name</span></span>    |<span data-ttu-id="fd885-119">Type</span><span class="sxs-lookup"><span data-stu-id="fd885-119">Type</span></span>   |<span data-ttu-id="fd885-120">Description</span><span class="sxs-lookup"><span data-stu-id="fd885-120">Description</span></span> |
|--------|-------|-------|
|<span data-ttu-id="fd885-121">ModelSettings</span><span class="sxs-lookup"><span data-stu-id="fd885-121">ModelSettings</span></span>|<span data-ttu-id="fd885-122">chaîne</span><span class="sxs-lookup"><span data-stu-id="fd885-122">string</span></span>|<span data-ttu-id="fd885-123">JSON des paramètres du modèle.</span><span class="sxs-lookup"><span data-stu-id="fd885-123">JSON of model settings.</span></span>|
|<span data-ttu-id="fd885-124">Description</span><span class="sxs-lookup"><span data-stu-id="fd885-124">Description</span></span>|<span data-ttu-id="fd885-125">string</span><span class="sxs-lookup"><span data-stu-id="fd885-125">string</span></span>|<span data-ttu-id="fd885-126">La description du modèle.</span><span class="sxs-lookup"><span data-stu-id="fd885-126">The model description.</span></span>|
|<span data-ttu-id="fd885-127">ÉtiquetteRétention</span><span class="sxs-lookup"><span data-stu-id="fd885-127">RetentionLabel</span></span>| |<span data-ttu-id="fd885-128">Informations sur l’étiquette associée (nom et ID d’étiquette).</span><span class="sxs-lookup"><span data-stu-id="fd885-128">Info for the associated label (label ID and name).</span></span>|

## <a name="responses"></a><span data-ttu-id="fd885-129">Réponses</span><span class="sxs-lookup"><span data-stu-id="fd885-129">Responses</span></span>

| <span data-ttu-id="fd885-130">Nom</span><span class="sxs-lookup"><span data-stu-id="fd885-130">Name</span></span>   | <span data-ttu-id="fd885-131">Type</span><span class="sxs-lookup"><span data-stu-id="fd885-131">Type</span></span>  | <span data-ttu-id="fd885-132">Description</span><span class="sxs-lookup"><span data-stu-id="fd885-132">Description</span></span>|
|--------|-------|------------|
|<span data-ttu-id="fd885-133">200 OK</span><span class="sxs-lookup"><span data-stu-id="fd885-133">200 OK</span></span>| |<span data-ttu-id="fd885-134">Opération réussie</span><span class="sxs-lookup"><span data-stu-id="fd885-134">Success</span></span>|

## <a name="examples"></a><span data-ttu-id="fd885-135">Exemples</span><span class="sxs-lookup"><span data-stu-id="fd885-135">Examples</span></span>

### <a name="update-model-settings-for-contoso-contract"></a><span data-ttu-id="fd885-136">Mettre à jour les paramètres du modèle pour le Contrat Contoso</span><span class="sxs-lookup"><span data-stu-id="fd885-136">Update model settings for Contoso Contract</span></span>

<span data-ttu-id="fd885-137">Dans cette exemple, la description du modèle et l’étiquette de rétention « Conservation standard » sont mises à jour.</span><span class="sxs-lookup"><span data-stu-id="fd885-137">In this example, the model description and "Standard Hold" retention label are updated.</span></span> <span data-ttu-id="fd885-138">L’ID de l’étiquette de rétention est `27c5fcba-abfd-4c34-823d-0b4a48f7ffe6`.</span><span class="sxs-lookup"><span data-stu-id="fd885-138">The ID of the retention label is `27c5fcba-abfd-4c34-823d-0b4a48f7ffe6`.</span></span>

#### <a name="sample-request"></a><span data-ttu-id="fd885-139">Exemple de demande</span><span class="sxs-lookup"><span data-stu-id="fd885-139">Sample request</span></span>

```HTTP
{
    "ModelSettings": "{\"Description\":\"This model is used to set files classified as Contoso Contracts with a standard hold retention.\", \"RetentionLabel\":{\"Id\":\"27c5fcba-abfd-4c34-823d-0b4a48f7ffe6\",\"Name\":\"Standard Hold\"}}"
}

```

#### <a name="sample-response"></a><span data-ttu-id="fd885-140">Exemple de réponse</span><span class="sxs-lookup"><span data-stu-id="fd885-140">Sample response</span></span>

<span data-ttu-id="fd885-141">**Code d’état :** 200</span><span class="sxs-lookup"><span data-stu-id="fd885-141">**Status code:** 200</span></span>

## <a name="see-also"></a><span data-ttu-id="fd885-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fd885-142">See also</span></span>

[<span data-ttu-id="fd885-143">API REST du modèle de compréhension de document Syntex</span><span class="sxs-lookup"><span data-stu-id="fd885-143">Syntex document understanding model REST API</span></span>](syntex-model-rest-api.md)
