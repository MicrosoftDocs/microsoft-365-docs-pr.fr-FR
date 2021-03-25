---
title: API d’indicateur d’soumission ou de mise à jour
description: Découvrez comment utiliser l’API d’indicateur d’soumission ou de mise à jour pour soumettre ou mettre à jour une nouvelle entité d’indicateur dans Microsoft Defender pour le point de terminaison.
keywords: api, api de graphique, api pris en charge, envoyer, ti, indicateur, mettre à jour
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
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
ms.technology: mde
ms.openlocfilehash: 42bab0a9d20d5e1ef78b98b3538cef209240d890
ms.sourcegitcommit: 6f2288e0c863496dfd0ee38de754bd43096ab3e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51187255"
---
# <a name="submit-or-update-indicator-api"></a><span data-ttu-id="ffa4f-104">API d’indicateur d’soumission ou de mise à jour</span><span class="sxs-lookup"><span data-stu-id="ffa4f-104">Submit or Update Indicator API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="ffa4f-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="ffa4f-105">**Applies to:**</span></span>
- [<span data-ttu-id="ffa4f-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="ffa4f-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="ffa4f-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="ffa4f-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="ffa4f-108">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="ffa4f-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="ffa4f-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="ffa4f-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 


[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]

## <a name="api-description"></a><span data-ttu-id="ffa4f-110">Description de l’API</span><span class="sxs-lookup"><span data-stu-id="ffa4f-110">API description</span></span>
<span data-ttu-id="ffa4f-111">Envoie ou met à jour une nouvelle [entité d’indicateur.](ti-indicator.md)</span><span class="sxs-lookup"><span data-stu-id="ffa4f-111">Submits or Updates new [Indicator](ti-indicator.md) entity.</span></span>
<br><span data-ttu-id="ffa4f-112">La notation CIDR pour les IPs n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="ffa4f-112">CIDR notation for IPs is not supported.</span></span>

## <a name="limitations"></a><span data-ttu-id="ffa4f-113">Limites</span><span class="sxs-lookup"><span data-stu-id="ffa4f-113">Limitations</span></span>
1. <span data-ttu-id="ffa4f-114">Les limites de taux pour cette API sont de 100 appels par minute et de 1 500 appels par heure.</span><span class="sxs-lookup"><span data-stu-id="ffa4f-114">Rate limitations for this API are 100 calls per minute and 1500 calls per hour.</span></span>
2. <span data-ttu-id="ffa4f-115">Il existe une limite de 15 000 indicateurs actifs par client.</span><span class="sxs-lookup"><span data-stu-id="ffa4f-115">There is a limit of 15,000 active indicators per tenant.</span></span> 


## <a name="permissions"></a><span data-ttu-id="ffa4f-116">Autorisations</span><span class="sxs-lookup"><span data-stu-id="ffa4f-116">Permissions</span></span>
<span data-ttu-id="ffa4f-117">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="ffa4f-117">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="ffa4f-118">Pour en savoir plus, notamment sur le choix des autorisations, consultez La mise [en place](apis-intro.md)</span><span class="sxs-lookup"><span data-stu-id="ffa4f-118">To learn more, including how to choose permissions, see [Get started](apis-intro.md)</span></span>

<span data-ttu-id="ffa4f-119">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="ffa4f-119">Permission type</span></span> |   <span data-ttu-id="ffa4f-120">Autorisation</span><span class="sxs-lookup"><span data-stu-id="ffa4f-120">Permission</span></span>  |   <span data-ttu-id="ffa4f-121">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="ffa4f-121">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="ffa4f-122">Application</span><span class="sxs-lookup"><span data-stu-id="ffa4f-122">Application</span></span> |   <span data-ttu-id="ffa4f-123">Ti.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ffa4f-123">Ti.ReadWrite</span></span> |  <span data-ttu-id="ffa4f-124">« Lire et écrire des indicateurs »</span><span class="sxs-lookup"><span data-stu-id="ffa4f-124">'Read and write Indicators'</span></span>
<span data-ttu-id="ffa4f-125">Application</span><span class="sxs-lookup"><span data-stu-id="ffa4f-125">Application</span></span> |   <span data-ttu-id="ffa4f-126">Ti.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ffa4f-126">Ti.ReadWrite.All</span></span> |  <span data-ttu-id="ffa4f-127">« Lire et écrire tous les indicateurs »</span><span class="sxs-lookup"><span data-stu-id="ffa4f-127">'Read and write All Indicators'</span></span>
<span data-ttu-id="ffa4f-128">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="ffa4f-128">Delegated (work or school account)</span></span> |    <span data-ttu-id="ffa4f-129">Ti.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ffa4f-129">Ti.ReadWrite</span></span> |  <span data-ttu-id="ffa4f-130">« Lire et écrire des indicateurs »</span><span class="sxs-lookup"><span data-stu-id="ffa4f-130">'Read and write Indicators'</span></span>


## <a name="http-request"></a><span data-ttu-id="ffa4f-131">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="ffa4f-131">HTTP request</span></span>
```
POST https://api.securitycenter.microsoft.com/api/indicators
```

## <a name="request-headers"></a><span data-ttu-id="ffa4f-132">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="ffa4f-132">Request headers</span></span>

<span data-ttu-id="ffa4f-133">Nom</span><span class="sxs-lookup"><span data-stu-id="ffa4f-133">Name</span></span> | <span data-ttu-id="ffa4f-134">Type</span><span class="sxs-lookup"><span data-stu-id="ffa4f-134">Type</span></span> | <span data-ttu-id="ffa4f-135">Description</span><span class="sxs-lookup"><span data-stu-id="ffa4f-135">Description</span></span>
:---|:---|:---
<span data-ttu-id="ffa4f-136">Autorisation</span><span class="sxs-lookup"><span data-stu-id="ffa4f-136">Authorization</span></span> | <span data-ttu-id="ffa4f-137">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ffa4f-137">String</span></span> | <span data-ttu-id="ffa4f-138">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="ffa4f-138">Bearer {token}.</span></span> <span data-ttu-id="ffa4f-139">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="ffa4f-139">**Required**.</span></span>
<span data-ttu-id="ffa4f-140">Content-Type</span><span class="sxs-lookup"><span data-stu-id="ffa4f-140">Content-Type</span></span> | <span data-ttu-id="ffa4f-141">string</span><span class="sxs-lookup"><span data-stu-id="ffa4f-141">string</span></span> | <span data-ttu-id="ffa4f-142">application/json.</span><span class="sxs-lookup"><span data-stu-id="ffa4f-142">application/json.</span></span> <span data-ttu-id="ffa4f-143">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="ffa4f-143">**Required**.</span></span>

## <a name="request-body"></a><span data-ttu-id="ffa4f-144">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="ffa4f-144">Request body</span></span>
<span data-ttu-id="ffa4f-145">Dans le corps de la demande, fournissons un objet JSON avec les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="ffa4f-145">In the request body, supply a JSON object with the following parameters:</span></span>

<span data-ttu-id="ffa4f-146">Paramètre</span><span class="sxs-lookup"><span data-stu-id="ffa4f-146">Parameter</span></span> | <span data-ttu-id="ffa4f-147">Type</span><span class="sxs-lookup"><span data-stu-id="ffa4f-147">Type</span></span>    | <span data-ttu-id="ffa4f-148">Description</span><span class="sxs-lookup"><span data-stu-id="ffa4f-148">Description</span></span>
:---|:---|:---
<span data-ttu-id="ffa4f-149">indicatorValue</span><span class="sxs-lookup"><span data-stu-id="ffa4f-149">indicatorValue</span></span> | <span data-ttu-id="ffa4f-150">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ffa4f-150">String</span></span> | <span data-ttu-id="ffa4f-151">Identité de [l’entité Indicateur.](ti-indicator.md)</span><span class="sxs-lookup"><span data-stu-id="ffa4f-151">Identity of the [Indicator](ti-indicator.md) entity.</span></span> <span data-ttu-id="ffa4f-152">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="ffa4f-152">**Required**</span></span>
<span data-ttu-id="ffa4f-153">indicatorType</span><span class="sxs-lookup"><span data-stu-id="ffa4f-153">indicatorType</span></span> | <span data-ttu-id="ffa4f-154">Énum</span><span class="sxs-lookup"><span data-stu-id="ffa4f-154">Enum</span></span> | <span data-ttu-id="ffa4f-155">Type de l’indicateur.</span><span class="sxs-lookup"><span data-stu-id="ffa4f-155">Type of the indicator.</span></span> <span data-ttu-id="ffa4f-156">Les valeurs possibles sont les suivantes : « FileSha1 », « FileSha256 », « IpAddress », « DomainName » et « Url ».</span><span class="sxs-lookup"><span data-stu-id="ffa4f-156">Possible values are: "FileSha1", "FileSha256", "IpAddress", "DomainName" and "Url".</span></span> <span data-ttu-id="ffa4f-157">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="ffa4f-157">**Required**</span></span>
<span data-ttu-id="ffa4f-158">action</span><span class="sxs-lookup"><span data-stu-id="ffa4f-158">action</span></span> | <span data-ttu-id="ffa4f-159">Énum</span><span class="sxs-lookup"><span data-stu-id="ffa4f-159">Enum</span></span> | <span data-ttu-id="ffa4f-160">Action qui sera entreprise si l’indicateur est détecté dans l’organisation.</span><span class="sxs-lookup"><span data-stu-id="ffa4f-160">The action that will be taken if the indicator will be discovered in the organization.</span></span> <span data-ttu-id="ffa4f-161">Les valeurs possibles sont : « Alert », « AlertAndBlock » et « Allowed ».</span><span class="sxs-lookup"><span data-stu-id="ffa4f-161">Possible values are: "Alert", "AlertAndBlock", and "Allowed".</span></span> <span data-ttu-id="ffa4f-162">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="ffa4f-162">**Required**</span></span>
<span data-ttu-id="ffa4f-163">application</span><span class="sxs-lookup"><span data-stu-id="ffa4f-163">application</span></span> | <span data-ttu-id="ffa4f-164">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ffa4f-164">String</span></span> | <span data-ttu-id="ffa4f-165">Application associée à l’indicateur.</span><span class="sxs-lookup"><span data-stu-id="ffa4f-165">The application associated with the indicator.</span></span> <span data-ttu-id="ffa4f-166">**Optional**</span><span class="sxs-lookup"><span data-stu-id="ffa4f-166">**Optional**</span></span>
<span data-ttu-id="ffa4f-167">title</span><span class="sxs-lookup"><span data-stu-id="ffa4f-167">title</span></span> | <span data-ttu-id="ffa4f-168">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ffa4f-168">String</span></span> | <span data-ttu-id="ffa4f-169">Titre de l’alerte de l’indicateur.</span><span class="sxs-lookup"><span data-stu-id="ffa4f-169">Indicator alert title.</span></span> <span data-ttu-id="ffa4f-170">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="ffa4f-170">**Required**</span></span>
<span data-ttu-id="ffa4f-171">description</span><span class="sxs-lookup"><span data-stu-id="ffa4f-171">description</span></span> | <span data-ttu-id="ffa4f-172">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ffa4f-172">String</span></span> | <span data-ttu-id="ffa4f-173">Description de l’indicateur.</span><span class="sxs-lookup"><span data-stu-id="ffa4f-173">Description of the indicator.</span></span> <span data-ttu-id="ffa4f-174">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="ffa4f-174">**Required**</span></span>
<span data-ttu-id="ffa4f-175">expirationTime</span><span class="sxs-lookup"><span data-stu-id="ffa4f-175">expirationTime</span></span> | <span data-ttu-id="ffa4f-176">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ffa4f-176">DateTimeOffset</span></span> | <span data-ttu-id="ffa4f-177">Heure d’expiration de l’indicateur.</span><span class="sxs-lookup"><span data-stu-id="ffa4f-177">The expiration time of the indicator.</span></span> <span data-ttu-id="ffa4f-178">**Optional**</span><span class="sxs-lookup"><span data-stu-id="ffa4f-178">**Optional**</span></span>
<span data-ttu-id="ffa4f-179">Sévérité </span><span class="sxs-lookup"><span data-stu-id="ffa4f-179">severity</span></span> | <span data-ttu-id="ffa4f-180">Énum</span><span class="sxs-lookup"><span data-stu-id="ffa4f-180">Enum</span></span> | <span data-ttu-id="ffa4f-181">Gravité de l’indicateur.</span><span class="sxs-lookup"><span data-stu-id="ffa4f-181">The severity of the indicator.</span></span> <span data-ttu-id="ffa4f-182">les valeurs possibles sont : « Informational », « Low », « Medium » et « High ».</span><span class="sxs-lookup"><span data-stu-id="ffa4f-182">possible values are: "Informational", "Low", "Medium" and "High".</span></span> <span data-ttu-id="ffa4f-183">**Optional**</span><span class="sxs-lookup"><span data-stu-id="ffa4f-183">**Optional**</span></span>
<span data-ttu-id="ffa4f-184">recommendedActions</span><span class="sxs-lookup"><span data-stu-id="ffa4f-184">recommendedActions</span></span> | <span data-ttu-id="ffa4f-185">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ffa4f-185">String</span></span> | <span data-ttu-id="ffa4f-186">Actions recommandées pour l’alerte d’indicateur TI.</span><span class="sxs-lookup"><span data-stu-id="ffa4f-186">TI indicator alert recommended actions.</span></span> <span data-ttu-id="ffa4f-187">**Optional**</span><span class="sxs-lookup"><span data-stu-id="ffa4f-187">**Optional**</span></span>
<span data-ttu-id="ffa4f-188">rbacGroupNames</span><span class="sxs-lookup"><span data-stu-id="ffa4f-188">rbacGroupNames</span></span> | <span data-ttu-id="ffa4f-189">Chaîne</span><span class="sxs-lookup"><span data-stu-id="ffa4f-189">String</span></span> | <span data-ttu-id="ffa4f-190">Liste séparée par des virgules des noms de groupe RBAC à appliquer à l’indicateur.</span><span class="sxs-lookup"><span data-stu-id="ffa4f-190">Comma-separated list of RBAC group names the indicator would be applied to.</span></span> <span data-ttu-id="ffa4f-191">**Optional**</span><span class="sxs-lookup"><span data-stu-id="ffa4f-191">**Optional**</span></span>


## <a name="response"></a><span data-ttu-id="ffa4f-192">Réponse</span><span class="sxs-lookup"><span data-stu-id="ffa4f-192">Response</span></span>
- <span data-ttu-id="ffa4f-193">Si elle réussit, cette méthode renvoie le code de réponse [](ti-indicator.md) 200 - OK et l’entité d’indicateur créée/mise à jour dans le corps de la réponse.</span><span class="sxs-lookup"><span data-stu-id="ffa4f-193">If successful, this method returns 200 - OK response code and the created / updated [Indicator](ti-indicator.md) entity in the response body.</span></span>
- <span data-ttu-id="ffa4f-194">Si elle ne réussit pas : cette méthode retourne 400 - Demande non bonne.</span><span class="sxs-lookup"><span data-stu-id="ffa4f-194">If not successful: this method return 400 - Bad Request.</span></span> <span data-ttu-id="ffa4f-195">Une demande incorrecte indique généralement un corps incorrect.</span><span class="sxs-lookup"><span data-stu-id="ffa4f-195">Bad request usually indicates incorrect body.</span></span>

## <a name="example"></a><span data-ttu-id="ffa4f-196">Exemple</span><span class="sxs-lookup"><span data-stu-id="ffa4f-196">Example</span></span>

<span data-ttu-id="ffa4f-197">**Demande**</span><span class="sxs-lookup"><span data-stu-id="ffa4f-197">**Request**</span></span>

<span data-ttu-id="ffa4f-198">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="ffa4f-198">Here is an example of the request.</span></span>

```http
POST https://api.securitycenter.microsoft.com/api/indicators
```

```json
{
    "indicatorValue": "220e7d15b011d7fac48f2bd61114db1022197f7f",
    "indicatorType": "FileSha1",
    "title": "test",
    "application": "demo-test",
    "expirationTime": "2020-12-12T00:00:00Z",
    "action": "AlertAndBlock",
    "severity": "Informational",
    "description": "test",
    "recommendedActions": "nothing",
    "rbacGroupNames": ["group1", "group2"]
}
```

## <a name="related-topic"></a><span data-ttu-id="ffa4f-199">Rubrique connexe</span><span class="sxs-lookup"><span data-stu-id="ffa4f-199">Related topic</span></span>
- [<span data-ttu-id="ffa4f-200">Gérer les indicateurs</span><span class="sxs-lookup"><span data-stu-id="ffa4f-200">Manage indicators</span></span>](manage-indicators.md)
