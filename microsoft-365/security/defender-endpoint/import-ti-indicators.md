---
title: API Importer des indicateurs
description: Découvrez comment utiliser le lot d’importation de l’API d’indicateur dans Microsoft Defender pour le point de terminaison.
keywords: api, api pris en charge, envoyer, ti, indicateur, mettre à jour
search.product: eADQiWindows 10XVcnh
ms.prod: w10
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: macapara
author: mjcaparas
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.openlocfilehash: b1777adf7b97083fae2daf4213a4bda742ba097d
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51198244"
---
# <a name="import-indicators-api"></a><span data-ttu-id="b26e8-104">API Importer des indicateurs</span><span class="sxs-lookup"><span data-stu-id="b26e8-104">Import Indicators API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="b26e8-105">**S’applique à :** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span><span class="sxs-lookup"><span data-stu-id="b26e8-105">**Applies to:** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span></span>

- <span data-ttu-id="b26e8-106">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="b26e8-106">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="b26e8-107">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="b26e8-107">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]


## <a name="api-description"></a><span data-ttu-id="b26e8-108">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="b26e8-108">API description</span></span>
<span data-ttu-id="b26e8-109">Envoie ou met à jour le lot [d’entités](ti-indicator.md) d’indicateur.</span><span class="sxs-lookup"><span data-stu-id="b26e8-109">Submits or Updates batch of [Indicator](ti-indicator.md) entities.</span></span>
<br><span data-ttu-id="b26e8-110">La notation CIDR pour les IPs n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="b26e8-110">CIDR notation for IPs is not supported.</span></span>

## <a name="limitations"></a><span data-ttu-id="b26e8-111">Limites</span><span class="sxs-lookup"><span data-stu-id="b26e8-111">Limitations</span></span>
1. <span data-ttu-id="b26e8-112">Les limites de taux pour cette API sont de 30 appels par minute.</span><span class="sxs-lookup"><span data-stu-id="b26e8-112">Rate limitations for this API are 30 calls per minute.</span></span>
2. <span data-ttu-id="b26e8-113">Il existe une limite de 15 000 indicateurs [actifs](ti-indicator.md) par client.</span><span class="sxs-lookup"><span data-stu-id="b26e8-113">There is a limit of 15,000 active [Indicators](ti-indicator.md) per tenant.</span></span> 
3. <span data-ttu-id="b26e8-114">La taille de lot maximale pour un appel d’API est de 500.</span><span class="sxs-lookup"><span data-stu-id="b26e8-114">Maximum batch size for one API call is 500.</span></span>

## <a name="permissions"></a><span data-ttu-id="b26e8-115">Autorisations</span><span class="sxs-lookup"><span data-stu-id="b26e8-115">Permissions</span></span>
<span data-ttu-id="b26e8-116">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="b26e8-116">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="b26e8-117">Pour en savoir plus, notamment sur le choix des autorisations, [consultez La](apis-intro.md) mise en place</span><span class="sxs-lookup"><span data-stu-id="b26e8-117">To learn more, including how to choose permissions, see [Get started](apis-intro.md)</span></span>

<span data-ttu-id="b26e8-118">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="b26e8-118">Permission type</span></span> |   <span data-ttu-id="b26e8-119">Autorisation</span><span class="sxs-lookup"><span data-stu-id="b26e8-119">Permission</span></span>  |   <span data-ttu-id="b26e8-120">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="b26e8-120">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="b26e8-121">Application</span><span class="sxs-lookup"><span data-stu-id="b26e8-121">Application</span></span> |   <span data-ttu-id="b26e8-122">Ti.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b26e8-122">Ti.ReadWrite</span></span> |  <span data-ttu-id="b26e8-123">« Lire et écrire des indicateurs »</span><span class="sxs-lookup"><span data-stu-id="b26e8-123">'Read and write Indicators'</span></span>
<span data-ttu-id="b26e8-124">Application</span><span class="sxs-lookup"><span data-stu-id="b26e8-124">Application</span></span> |   <span data-ttu-id="b26e8-125">Ti.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b26e8-125">Ti.ReadWrite.All</span></span> |  <span data-ttu-id="b26e8-126">« Lire et écrire tous les indicateurs »</span><span class="sxs-lookup"><span data-stu-id="b26e8-126">'Read and write All Indicators'</span></span>
<span data-ttu-id="b26e8-127">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="b26e8-127">Delegated (work or school account)</span></span> |    <span data-ttu-id="b26e8-128">Ti.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b26e8-128">Ti.ReadWrite</span></span> |  <span data-ttu-id="b26e8-129">« Lire et écrire des indicateurs »</span><span class="sxs-lookup"><span data-stu-id="b26e8-129">'Read and write Indicators'</span></span>


## <a name="http-request"></a><span data-ttu-id="b26e8-130">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="b26e8-130">HTTP request</span></span>
```
POST https://api.securitycenter.microsoft.com/api/indicators/import
```

## <a name="request-headers"></a><span data-ttu-id="b26e8-131">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="b26e8-131">Request headers</span></span>

<span data-ttu-id="b26e8-132">Nom</span><span class="sxs-lookup"><span data-stu-id="b26e8-132">Name</span></span> | <span data-ttu-id="b26e8-133">Type</span><span class="sxs-lookup"><span data-stu-id="b26e8-133">Type</span></span> | <span data-ttu-id="b26e8-134">Description</span><span class="sxs-lookup"><span data-stu-id="b26e8-134">Description</span></span>
:---|:---|:---
<span data-ttu-id="b26e8-135">Autorisation</span><span class="sxs-lookup"><span data-stu-id="b26e8-135">Authorization</span></span> | <span data-ttu-id="b26e8-136">Chaîne</span><span class="sxs-lookup"><span data-stu-id="b26e8-136">String</span></span> | <span data-ttu-id="b26e8-137">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="b26e8-137">Bearer {token}.</span></span> <span data-ttu-id="b26e8-138">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="b26e8-138">**Required**.</span></span>
<span data-ttu-id="b26e8-139">Content-Type</span><span class="sxs-lookup"><span data-stu-id="b26e8-139">Content-Type</span></span> | <span data-ttu-id="b26e8-140">string</span><span class="sxs-lookup"><span data-stu-id="b26e8-140">string</span></span> | <span data-ttu-id="b26e8-141">application/json.</span><span class="sxs-lookup"><span data-stu-id="b26e8-141">application/json.</span></span> <span data-ttu-id="b26e8-142">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="b26e8-142">**Required**.</span></span>

## <a name="request-body"></a><span data-ttu-id="b26e8-143">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="b26e8-143">Request body</span></span>
<span data-ttu-id="b26e8-144">Dans le corps de la demande, fournissons un objet JSON avec les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="b26e8-144">In the request body, supply a JSON object with the following parameters:</span></span>

<span data-ttu-id="b26e8-145">Paramètre</span><span class="sxs-lookup"><span data-stu-id="b26e8-145">Parameter</span></span> | <span data-ttu-id="b26e8-146">Type</span><span class="sxs-lookup"><span data-stu-id="b26e8-146">Type</span></span>    | <span data-ttu-id="b26e8-147">Description</span><span class="sxs-lookup"><span data-stu-id="b26e8-147">Description</span></span>
:---|:---|:---
<span data-ttu-id="b26e8-148">Indicateurs</span><span class="sxs-lookup"><span data-stu-id="b26e8-148">Indicators</span></span> | <span data-ttu-id="b26e8-149">List<[Indicator](ti-indicator.md)></span><span class="sxs-lookup"><span data-stu-id="b26e8-149">List<[Indicator](ti-indicator.md)></span></span> | <span data-ttu-id="b26e8-150">Liste des [indicateurs](ti-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="b26e8-150">List of [Indicators](ti-indicator.md).</span></span> <span data-ttu-id="b26e8-151">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="b26e8-151">**Required**</span></span>


## <a name="response"></a><span data-ttu-id="b26e8-152">Réponse</span><span class="sxs-lookup"><span data-stu-id="b26e8-152">Response</span></span>
- <span data-ttu-id="b26e8-153">Si elle réussit, cette méthode renvoie un code de réponse 200 - OK avec une liste de résultats d’importation par indicateur, voir l’exemple ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="b26e8-153">If successful, this method returns 200 - OK response code with a list of import results per indicator, see example below.</span></span>
- <span data-ttu-id="b26e8-154">Si elle ne réussit pas : cette méthode retourne 400 - Demande non bonne.</span><span class="sxs-lookup"><span data-stu-id="b26e8-154">If not successful: this method return 400 - Bad Request.</span></span> <span data-ttu-id="b26e8-155">Une demande incorrecte indique généralement un corps incorrect.</span><span class="sxs-lookup"><span data-stu-id="b26e8-155">Bad request usually indicates incorrect body.</span></span>

## <a name="example"></a><span data-ttu-id="b26e8-156">Exemple</span><span class="sxs-lookup"><span data-stu-id="b26e8-156">Example</span></span>

<span data-ttu-id="b26e8-157">**Demande**</span><span class="sxs-lookup"><span data-stu-id="b26e8-157">**Request**</span></span>

<span data-ttu-id="b26e8-158">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="b26e8-158">Here is an example of the request.</span></span>

```http
POST https://api.securitycenter.microsoft.com/api/indicators/import
```

```json
{
    "Indicators":
    [
        {
            "indicatorValue": "220e7d15b011d7fac48f2bd61114db1022197f7f",
            "indicatorType": "FileSha1",
            "title": "demo",
            "application": "demo-test",
            "expirationTime": "2021-12-12T00:00:00Z",
            "action": "Alert",
            "severity": "Informational",
            "description": "demo2",
            "recommendedActions": "nothing",
            "rbacGroupNames": ["group1", "group2"]
        },
        {
            "indicatorValue": "2233223322332233223322332233223322332233223322332233223322332222",
            "indicatorType": "FileSha256",
            "title": "demo2",
            "application": "demo-test2",
            "expirationTime": "2021-12-12T00:00:00Z",
            "action": "Alert",
            "severity": "Medium",
            "description": "demo2",
            "recommendedActions": "nothing",
            "rbacGroupNames": []
        }
    ]
}
```

<span data-ttu-id="b26e8-159">**Réponse**</span><span class="sxs-lookup"><span data-stu-id="b26e8-159">**Response**</span></span>

<span data-ttu-id="b26e8-160">Voici un exemple de réponse.</span><span class="sxs-lookup"><span data-stu-id="b26e8-160">Here is an example of the response.</span></span>

```json
{
    "value": [
        {
            "id": "2841",
            "indicator": "220e7d15b011d7fac48f2bd61114db1022197f7f",
            "isFailed": false,
            "failureReason": null
        },
        {
            "id": "2842",
            "indicator": "2233223322332233223322332233223322332233223322332233223322332222",
            "isFailed": false,
            "failureReason": null
        }
    ]
}
```

## <a name="related-topic"></a><span data-ttu-id="b26e8-161">Rubrique connexe</span><span class="sxs-lookup"><span data-stu-id="b26e8-161">Related topic</span></span>
- [<span data-ttu-id="b26e8-162">Gérer les indicateurs</span><span class="sxs-lookup"><span data-stu-id="b26e8-162">Manage indicators</span></span>](manage-indicators.md)
