---
title: Codes d’erreur de l’API REST Microsoft 365 Defender courants
description: En savoir plus sur les codes d’erreur de l’API REST Microsoft 365 Defender courants
keywords: API, erreur, codes, erreurs courantes, MTP, codes d’erreur de l’API
search.product: eADQiWindows 10XVcnh
ms.prod: microsoft-365-enterprise
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: macapara
author: mjcaparas
ms.localizationpriority: medium
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: conceptual
search.appverid:
- MOE150
- MET150
ms.openlocfilehash: 0df741efb7555d587a6033acc23716e93f542d5e
ms.sourcegitcommit: d6b1da2e12d55f69e4353289e90f5ae2f60066d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2020
ms.locfileid: "49719213"
---
# <a name="common-microsoft-365-defender-rest-api-error-codes"></a><span data-ttu-id="6d3a7-104">Codes d’erreur de l’API REST Microsoft 365 Defender courants</span><span class="sxs-lookup"><span data-stu-id="6d3a7-104">Common Microsoft 365 Defender REST API error codes</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

<span data-ttu-id="6d3a7-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="6d3a7-105">**Applies to:**</span></span>

- <span data-ttu-id="6d3a7-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="6d3a7-106">Microsoft Threat Protection</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6d3a7-107">Certaines informations se rapportent à des produits précommercialisés susceptibles d’être modifiés de manière substantielle avant leur publication commerciale.</span><span class="sxs-lookup"><span data-stu-id="6d3a7-107">Some information relates to prereleased product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="6d3a7-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span><span class="sxs-lookup"><span data-stu-id="6d3a7-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span></span>

<span data-ttu-id="6d3a7-109">Les codes d’erreur peuvent être renvoyés par une opération sur l’une des API Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="6d3a7-109">Error codes may be returned by an operation on any of the Microsoft 365 Defender APIs.</span></span> <span data-ttu-id="6d3a7-110">Chaque réponse d’erreur contient un message d’erreur qui peut vous aider à résoudre le problème.</span><span class="sxs-lookup"><span data-stu-id="6d3a7-110">Every error response will contain an error message, which can help resolve the problem.</span></span> <span data-ttu-id="6d3a7-111">La colonne message d’erreur de la section tableau fournit quelques exemples de messages.</span><span class="sxs-lookup"><span data-stu-id="6d3a7-111">The error message column in the table section provides some sample messages.</span></span> <span data-ttu-id="6d3a7-112">Le contenu des véritables messages dépend des facteurs qui ont déclenché la réponse.</span><span class="sxs-lookup"><span data-stu-id="6d3a7-112">The content of actual messages will vary based on the factors that triggered the response.</span></span> <span data-ttu-id="6d3a7-113">Le contenu des variables est indiqué dans le tableau par des chevrons.</span><span class="sxs-lookup"><span data-stu-id="6d3a7-113">Variable content is indicated in the table by angle brackets.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6d3a7-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="6d3a7-114">Error codes</span></span>

<span data-ttu-id="6d3a7-115">Code d'erreur</span><span class="sxs-lookup"><span data-stu-id="6d3a7-115">Error code</span></span> | <span data-ttu-id="6d3a7-116">Code d’état HTTP</span><span class="sxs-lookup"><span data-stu-id="6d3a7-116">HTTP status code</span></span> | <span data-ttu-id="6d3a7-117">Message</span><span class="sxs-lookup"><span data-stu-id="6d3a7-117">Message</span></span>
-|-|-
<span data-ttu-id="6d3a7-118">BadRequest</span><span class="sxs-lookup"><span data-stu-id="6d3a7-118">BadRequest</span></span> | <span data-ttu-id="6d3a7-119">BadRequest (400)</span><span class="sxs-lookup"><span data-stu-id="6d3a7-119">BadRequest (400)</span></span> | <span data-ttu-id="6d3a7-120">Message d’erreur de requête incorrecte générale.</span><span class="sxs-lookup"><span data-stu-id="6d3a7-120">General Bad Request error message.</span></span>
<span data-ttu-id="6d3a7-121">ODataError</span><span class="sxs-lookup"><span data-stu-id="6d3a7-121">ODataError</span></span> | <span data-ttu-id="6d3a7-122">BadRequest (400)</span><span class="sxs-lookup"><span data-stu-id="6d3a7-122">BadRequest (400)</span></span> | <span data-ttu-id="6d3a7-123">Requête URI OData non valide \<the specific error is specified\> .</span><span class="sxs-lookup"><span data-stu-id="6d3a7-123">Invalid OData URI query \<the specific error is specified\>.</span></span>
<span data-ttu-id="6d3a7-124">InvalidInput</span><span class="sxs-lookup"><span data-stu-id="6d3a7-124">InvalidInput</span></span> | <span data-ttu-id="6d3a7-125">BadRequest (400)</span><span class="sxs-lookup"><span data-stu-id="6d3a7-125">BadRequest (400)</span></span> | <span data-ttu-id="6d3a7-126">Entrée non valide \<the invalid input\> .</span><span class="sxs-lookup"><span data-stu-id="6d3a7-126">Invalid input \<the invalid input\>.</span></span>
<span data-ttu-id="6d3a7-127">InvalidRequestBody</span><span class="sxs-lookup"><span data-stu-id="6d3a7-127">InvalidRequestBody</span></span> | <span data-ttu-id="6d3a7-128">BadRequest (400)</span><span class="sxs-lookup"><span data-stu-id="6d3a7-128">BadRequest (400)</span></span> | <span data-ttu-id="6d3a7-129">Corps de la requête non valide.</span><span class="sxs-lookup"><span data-stu-id="6d3a7-129">Invalid request body.</span></span>
<span data-ttu-id="6d3a7-130">InvalidHashValue</span><span class="sxs-lookup"><span data-stu-id="6d3a7-130">InvalidHashValue</span></span> | <span data-ttu-id="6d3a7-131">BadRequest (400)</span><span class="sxs-lookup"><span data-stu-id="6d3a7-131">BadRequest (400)</span></span> | <span data-ttu-id="6d3a7-132">La valeur de hachage \<the invalid hash\> n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="6d3a7-132">Hash value \<the invalid hash\> is invalid.</span></span>
<span data-ttu-id="6d3a7-133">InvalidDomainName</span><span class="sxs-lookup"><span data-stu-id="6d3a7-133">InvalidDomainName</span></span> | <span data-ttu-id="6d3a7-134">BadRequest (400)</span><span class="sxs-lookup"><span data-stu-id="6d3a7-134">BadRequest (400)</span></span> | <span data-ttu-id="6d3a7-135">Le nom de domaine \<the invalid domain\> n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="6d3a7-135">Domain name \<the invalid domain\> is invalid.</span></span>
<span data-ttu-id="6d3a7-136">InvalidIpAddress</span><span class="sxs-lookup"><span data-stu-id="6d3a7-136">InvalidIpAddress</span></span> | <span data-ttu-id="6d3a7-137">BadRequest (400)</span><span class="sxs-lookup"><span data-stu-id="6d3a7-137">BadRequest (400)</span></span> | <span data-ttu-id="6d3a7-138">L’adresse IP \<the invalid IP\> n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="6d3a7-138">IP address \<the invalid IP\> is invalid.</span></span>
<span data-ttu-id="6d3a7-139">InvalidUrl</span><span class="sxs-lookup"><span data-stu-id="6d3a7-139">InvalidUrl</span></span> | <span data-ttu-id="6d3a7-140">BadRequest (400)</span><span class="sxs-lookup"><span data-stu-id="6d3a7-140">BadRequest (400)</span></span> | <span data-ttu-id="6d3a7-141">L’URL \<the invalid URL\> n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="6d3a7-141">URL \<the invalid URL\> is invalid.</span></span>
<span data-ttu-id="6d3a7-142">MaximumBatchSizeExceeded</span><span class="sxs-lookup"><span data-stu-id="6d3a7-142">MaximumBatchSizeExceeded</span></span> | <span data-ttu-id="6d3a7-143">BadRequest (400)</span><span class="sxs-lookup"><span data-stu-id="6d3a7-143">BadRequest (400)</span></span> | <span data-ttu-id="6d3a7-144">Taille maximale de lot dépassée.</span><span class="sxs-lookup"><span data-stu-id="6d3a7-144">Maximum batch size exceeded.</span></span> <span data-ttu-id="6d3a7-145">Received : \<batch size received\> , allowed : {taille de lot autorisée}.</span><span class="sxs-lookup"><span data-stu-id="6d3a7-145">Received: \<batch size received\>, allowed: {batch size allowed}.</span></span>
<span data-ttu-id="6d3a7-146">MissingRequiredParameter</span><span class="sxs-lookup"><span data-stu-id="6d3a7-146">MissingRequiredParameter</span></span> | <span data-ttu-id="6d3a7-147">BadRequest (400)</span><span class="sxs-lookup"><span data-stu-id="6d3a7-147">BadRequest (400)</span></span> | <span data-ttu-id="6d3a7-148">Le paramètre \<the missing parameter\> est manquant.</span><span class="sxs-lookup"><span data-stu-id="6d3a7-148">Parameter \<the missing parameter\> is missing.</span></span>
<span data-ttu-id="6d3a7-149">OsPlatformNotSupported</span><span class="sxs-lookup"><span data-stu-id="6d3a7-149">OsPlatformNotSupported</span></span> | <span data-ttu-id="6d3a7-150">BadRequest (400)</span><span class="sxs-lookup"><span data-stu-id="6d3a7-150">BadRequest (400)</span></span> | <span data-ttu-id="6d3a7-151">La plateforme de système d’exploitation \<the client OS Platform\> n’est pas prise en charge pour cette action.</span><span class="sxs-lookup"><span data-stu-id="6d3a7-151">OS Platform \<the client OS Platform\> is not supported for this action.</span></span>
<span data-ttu-id="6d3a7-152">ClientVersionNotSupported</span><span class="sxs-lookup"><span data-stu-id="6d3a7-152">ClientVersionNotSupported</span></span> | <span data-ttu-id="6d3a7-153">BadRequest (400)</span><span class="sxs-lookup"><span data-stu-id="6d3a7-153">BadRequest (400)</span></span> | <span data-ttu-id="6d3a7-154">\<The requested action\> est pris en charge sur la version du client \<supported client version\> et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="6d3a7-154">\<The requested action\> is supported on client version \<supported client version\> and above.</span></span>
<span data-ttu-id="6d3a7-155">Non autorisé (Unauthorized)</span><span class="sxs-lookup"><span data-stu-id="6d3a7-155">Unauthorized</span></span> | <span data-ttu-id="6d3a7-156">Non autorisé (401)</span><span class="sxs-lookup"><span data-stu-id="6d3a7-156">Unauthorized (401)</span></span> | <span data-ttu-id="6d3a7-157">Non autorisé (Unauthorized)</span><span class="sxs-lookup"><span data-stu-id="6d3a7-157">Unauthorized</span></span> <br /><br /><span data-ttu-id="6d3a7-158">*Remarque : cela est généralement dû à un en-tête d’autorisation non valide ou expiré.*</span><span class="sxs-lookup"><span data-stu-id="6d3a7-158">*Note: Usually caused by an invalid or expired authorization header.*</span></span>
<span data-ttu-id="6d3a7-159">Interdit (Forbidden)</span><span class="sxs-lookup"><span data-stu-id="6d3a7-159">Forbidden</span></span> | <span data-ttu-id="6d3a7-160">Interdit (403)</span><span class="sxs-lookup"><span data-stu-id="6d3a7-160">Forbidden (403)</span></span> | <span data-ttu-id="6d3a7-161">Interdit (Forbidden)</span><span class="sxs-lookup"><span data-stu-id="6d3a7-161">Forbidden</span></span> <br /><br /><span data-ttu-id="6d3a7-162">*Remarque : jeton valide, mais autorisation insuffisante pour l’action*.</span><span class="sxs-lookup"><span data-stu-id="6d3a7-162">*Note: Valid token but insufficient permission for the action*.</span></span>
<span data-ttu-id="6d3a7-163">DisabledFeature</span><span class="sxs-lookup"><span data-stu-id="6d3a7-163">DisabledFeature</span></span> | <span data-ttu-id="6d3a7-164">Interdit (403)</span><span class="sxs-lookup"><span data-stu-id="6d3a7-164">Forbidden (403)</span></span> | <span data-ttu-id="6d3a7-165">La fonctionnalité de client n’est pas activée.</span><span class="sxs-lookup"><span data-stu-id="6d3a7-165">Tenant feature is not enabled.</span></span>
<span data-ttu-id="6d3a7-166">DisallowedOperation</span><span class="sxs-lookup"><span data-stu-id="6d3a7-166">DisallowedOperation</span></span> | <span data-ttu-id="6d3a7-167">Interdit (403)</span><span class="sxs-lookup"><span data-stu-id="6d3a7-167">Forbidden (403)</span></span> | <span data-ttu-id="6d3a7-168">\<the disallowed operation and the reason\>.</span><span class="sxs-lookup"><span data-stu-id="6d3a7-168">\<the disallowed operation and the reason\>.</span></span>
<span data-ttu-id="6d3a7-169">NotFound</span><span class="sxs-lookup"><span data-stu-id="6d3a7-169">NotFound</span></span> | <span data-ttu-id="6d3a7-170">Introuvable (404)</span><span class="sxs-lookup"><span data-stu-id="6d3a7-170">Not Found (404)</span></span> | <span data-ttu-id="6d3a7-171">Message d’erreur général introuvable.</span><span class="sxs-lookup"><span data-stu-id="6d3a7-171">General Not Found error message.</span></span>
<span data-ttu-id="6d3a7-172">ResourceNotFound</span><span class="sxs-lookup"><span data-stu-id="6d3a7-172">ResourceNotFound</span></span> | <span data-ttu-id="6d3a7-173">Introuvable (404)</span><span class="sxs-lookup"><span data-stu-id="6d3a7-173">Not Found (404)</span></span> | <span data-ttu-id="6d3a7-174">Ressource \<the requested resource\> introuvable.</span><span class="sxs-lookup"><span data-stu-id="6d3a7-174">Resource \<the requested resource\> was not found.</span></span>
<span data-ttu-id="6d3a7-175">InternalServerError</span><span class="sxs-lookup"><span data-stu-id="6d3a7-175">InternalServerError</span></span> | <span data-ttu-id="6d3a7-176">Erreur de serveur interne (500)</span><span class="sxs-lookup"><span data-stu-id="6d3a7-176">Internal Server Error (500)</span></span> | <span data-ttu-id="6d3a7-177">*Remarque : aucun message d’erreur, retenter l’opération ou contacter Microsoft s’il n’est pas résolu*</span><span class="sxs-lookup"><span data-stu-id="6d3a7-177">*Note: No error message,  retry the operation or contact Microsoft if it does not get resolved*</span></span>

## <a name="examples"></a><span data-ttu-id="6d3a7-178">Exemples</span><span class="sxs-lookup"><span data-stu-id="6d3a7-178">Examples</span></span>

```json
{
    "error": {
        "code": "ResourceNotFound",
        "message": "Machine 123123123 was not found",
        "target": "43f4cb08-8fac-4b65-9db1-745c2ae65f3a"
    }
}
```

```json
{
    "error": {
        "code": "InvalidRequestBody",
        "message": "Request body is incorrect",
        "target": "1fa66c0f-18bd-4133-b378-36d76f3a2ba0"
    }
}
```

## <a name="body-parameters"></a><span data-ttu-id="6d3a7-179">Paramètres de corps</span><span class="sxs-lookup"><span data-stu-id="6d3a7-179">Body parameters</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6d3a7-180">Les paramètres Body respectent la casse.</span><span class="sxs-lookup"><span data-stu-id="6d3a7-180">Body parameters are case-sensitive.</span></span>

<span data-ttu-id="6d3a7-181">Si vous êtes confronté à une erreur *InvalidRequestBody* ou *MissingRequiredParameter* , elle peut être causée par une faute de frappe.</span><span class="sxs-lookup"><span data-stu-id="6d3a7-181">If you experience an *InvalidRequestBody* or *MissingRequiredParameter* error, it might be caused by a typo.</span></span> <span data-ttu-id="6d3a7-182">Examinez la documentation de l’API et assurez-vous que les paramètres soumis correspondent à l’exemple approprié.</span><span class="sxs-lookup"><span data-stu-id="6d3a7-182">Review the API documentation and check that the submitted parameters match the relevant example.</span></span>

## <a name="tracking-id"></a><span data-ttu-id="6d3a7-183">ID de suivi</span><span class="sxs-lookup"><span data-stu-id="6d3a7-183">Tracking ID</span></span>

<span data-ttu-id="6d3a7-184">Chaque réponse d’erreur contient un paramètre ID unique pour le suivi.</span><span class="sxs-lookup"><span data-stu-id="6d3a7-184">Each error response contains a unique ID parameter for tracking.</span></span> <span data-ttu-id="6d3a7-185">Le nom de la propriété de ce paramètre est *target*.</span><span class="sxs-lookup"><span data-stu-id="6d3a7-185">The property name of this parameter is *target*.</span></span> <span data-ttu-id="6d3a7-186">Lors de la création d’une erreur, joindre cet ID nous permettra de trouver la cause première du problème.</span><span class="sxs-lookup"><span data-stu-id="6d3a7-186">When contacting us about an error, attaching this ID will help us find the root cause of the problem.</span></span>

## <a name="related-articles"></a><span data-ttu-id="6d3a7-187">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="6d3a7-187">Related articles</span></span>

- [<span data-ttu-id="6d3a7-188">Vue d’ensemble des API Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="6d3a7-188">Microsoft 365 Defender APIs overview</span></span>](api-overview.md)
- [<span data-ttu-id="6d3a7-189">API Microsoft 365 Defender prises en charge</span><span class="sxs-lookup"><span data-stu-id="6d3a7-189">Supported Microsoft 365 Defender APIs</span></span>](api-supported.md)
- [<span data-ttu-id="6d3a7-190">Accéder aux API Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="6d3a7-190">Access the Microsoft 365 Defender APIs</span></span>](api-access.md)
- [<span data-ttu-id="6d3a7-191">En savoir plus sur les limites d’API et la gestion des licences</span><span class="sxs-lookup"><span data-stu-id="6d3a7-191">Learn about API limits and licensing</span></span>](api-terms.md)
