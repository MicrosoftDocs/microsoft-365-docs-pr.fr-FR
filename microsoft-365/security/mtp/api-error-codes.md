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
ms.openlocfilehash: aceb376662f2b27397aa2332f8929a57d5a3ee03
ms.sourcegitcommit: 815229e39a0f905d9f06717f00dc82e2a028fa7c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2020
ms.locfileid: "48846007"
---
# <a name="common-microsoft-365-defender-rest-api-error-codes"></a><span data-ttu-id="0ab62-104">Codes d’erreur de l’API REST Microsoft 365 Defender courants</span><span class="sxs-lookup"><span data-stu-id="0ab62-104">Common Microsoft 365 Defender REST API error codes</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="0ab62-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="0ab62-105">**Applies to:**</span></span>
- <span data-ttu-id="0ab62-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="0ab62-106">Microsoft 365 Defender</span></span>

>[!IMPORTANT] 
><span data-ttu-id="0ab62-107">Certaines informations se rapportent à des produits précommercialisés susceptibles d’être modifiés de manière substantielle avant leur publication commerciale.</span><span class="sxs-lookup"><span data-stu-id="0ab62-107">Some information relates to prereleased product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="0ab62-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span><span class="sxs-lookup"><span data-stu-id="0ab62-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span></span>

<span data-ttu-id="0ab62-109">Les codes d’erreur figurant dans le tableau suivant peuvent être renvoyés par une opération sur l’une des API Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="0ab62-109">The error codes listed in the following table may be returned by an operation on any of Microsoft 365 Defender APIs.</span></span>

<span data-ttu-id="0ab62-110">Chaque réponse d’erreur contient un message d’erreur qui peut vous aider à résoudre le problème.</span><span class="sxs-lookup"><span data-stu-id="0ab62-110">Every error response contains an error message, which can help resolving the problem.</span></span>

<span data-ttu-id="0ab62-111">Le message est un texte libre qui peut être modifié.</span><span class="sxs-lookup"><span data-stu-id="0ab62-111">The message is a free text that can be changed.</span></span>

<span data-ttu-id="0ab62-112">Au bas de la page, vous trouverez des exemples de réponses.</span><span class="sxs-lookup"><span data-stu-id="0ab62-112">At the bottom of the page, you can find response examples.</span></span>

<span data-ttu-id="0ab62-113">Code d'erreur</span><span class="sxs-lookup"><span data-stu-id="0ab62-113">Error code</span></span> |<span data-ttu-id="0ab62-114">Code d’état HTTP</span><span class="sxs-lookup"><span data-stu-id="0ab62-114">HTTP status code</span></span> |<span data-ttu-id="0ab62-115">Message</span><span class="sxs-lookup"><span data-stu-id="0ab62-115">Message</span></span> 
:---|:---|:---
<span data-ttu-id="0ab62-116">BadRequest</span><span class="sxs-lookup"><span data-stu-id="0ab62-116">BadRequest</span></span> | <span data-ttu-id="0ab62-117">BadRequest (400)</span><span class="sxs-lookup"><span data-stu-id="0ab62-117">BadRequest (400)</span></span> | <span data-ttu-id="0ab62-118">Message d’erreur de requête incorrecte générale.</span><span class="sxs-lookup"><span data-stu-id="0ab62-118">General Bad Request error message.</span></span>
<span data-ttu-id="0ab62-119">ODataError</span><span class="sxs-lookup"><span data-stu-id="0ab62-119">ODataError</span></span> | <span data-ttu-id="0ab62-120">BadRequest (400)</span><span class="sxs-lookup"><span data-stu-id="0ab62-120">BadRequest (400)</span></span> | <span data-ttu-id="0ab62-121">Requête URI OData non valide (l’erreur spécifique est spécifiée).</span><span class="sxs-lookup"><span data-stu-id="0ab62-121">Invalid OData URI query (the specific error is specified).</span></span>
<span data-ttu-id="0ab62-122">InvalidInput</span><span class="sxs-lookup"><span data-stu-id="0ab62-122">InvalidInput</span></span> | <span data-ttu-id="0ab62-123">BadRequest (400)</span><span class="sxs-lookup"><span data-stu-id="0ab62-123">BadRequest (400)</span></span> | <span data-ttu-id="0ab62-124">Entrée non valide {entrée incorrecte}.</span><span class="sxs-lookup"><span data-stu-id="0ab62-124">Invalid input {the invalid input}.</span></span>
<span data-ttu-id="0ab62-125">InvalidRequestBody</span><span class="sxs-lookup"><span data-stu-id="0ab62-125">InvalidRequestBody</span></span> | <span data-ttu-id="0ab62-126">BadRequest (400)</span><span class="sxs-lookup"><span data-stu-id="0ab62-126">BadRequest (400)</span></span> | <span data-ttu-id="0ab62-127">Corps de la requête non valide.</span><span class="sxs-lookup"><span data-stu-id="0ab62-127">Invalid request body.</span></span>
<span data-ttu-id="0ab62-128">InvalidHashValue</span><span class="sxs-lookup"><span data-stu-id="0ab62-128">InvalidHashValue</span></span> | <span data-ttu-id="0ab62-129">BadRequest (400)</span><span class="sxs-lookup"><span data-stu-id="0ab62-129">BadRequest (400)</span></span> | <span data-ttu-id="0ab62-130">Valeur de hachage {le hachage incorrect} n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="0ab62-130">Hash value {the invalid hash} is invalid.</span></span>
<span data-ttu-id="0ab62-131">InvalidDomainName</span><span class="sxs-lookup"><span data-stu-id="0ab62-131">InvalidDomainName</span></span> | <span data-ttu-id="0ab62-132">BadRequest (400)</span><span class="sxs-lookup"><span data-stu-id="0ab62-132">BadRequest (400)</span></span> | <span data-ttu-id="0ab62-133">Nom de domaine {domaine non valide} non valide.</span><span class="sxs-lookup"><span data-stu-id="0ab62-133">Domain name {the invalid domain} is invalid.</span></span>
<span data-ttu-id="0ab62-134">InvalidIpAddress</span><span class="sxs-lookup"><span data-stu-id="0ab62-134">InvalidIpAddress</span></span> | <span data-ttu-id="0ab62-135">BadRequest (400)</span><span class="sxs-lookup"><span data-stu-id="0ab62-135">BadRequest (400)</span></span> | <span data-ttu-id="0ab62-136">Adresse IP {l’adresse IP incorrecte} n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="0ab62-136">IP address {the invalid IP} is invalid.</span></span>
<span data-ttu-id="0ab62-137">InvalidUrl</span><span class="sxs-lookup"><span data-stu-id="0ab62-137">InvalidUrl</span></span> | <span data-ttu-id="0ab62-138">BadRequest (400)</span><span class="sxs-lookup"><span data-stu-id="0ab62-138">BadRequest (400)</span></span> | <span data-ttu-id="0ab62-139">URL {l’URL incorrecte} n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="0ab62-139">URL {the invalid URL} is invalid.</span></span>
<span data-ttu-id="0ab62-140">MaximumBatchSizeExceeded</span><span class="sxs-lookup"><span data-stu-id="0ab62-140">MaximumBatchSizeExceeded</span></span> | <span data-ttu-id="0ab62-141">BadRequest (400)</span><span class="sxs-lookup"><span data-stu-id="0ab62-141">BadRequest (400)</span></span> | <span data-ttu-id="0ab62-142">Taille maximale de lot dépassée.</span><span class="sxs-lookup"><span data-stu-id="0ab62-142">Maximum batch size exceeded.</span></span> <span data-ttu-id="0ab62-143">Reçu : {taille de lot reçue}, autorisée : {taille du lot autorisée}.</span><span class="sxs-lookup"><span data-stu-id="0ab62-143">Received: {batch size received}, allowed: {batch size allowed}.</span></span>
<span data-ttu-id="0ab62-144">MissingRequiredParameter</span><span class="sxs-lookup"><span data-stu-id="0ab62-144">MissingRequiredParameter</span></span> | <span data-ttu-id="0ab62-145">BadRequest (400)</span><span class="sxs-lookup"><span data-stu-id="0ab62-145">BadRequest (400)</span></span> | <span data-ttu-id="0ab62-146">Paramètre {le paramètre manquant} est manquant.</span><span class="sxs-lookup"><span data-stu-id="0ab62-146">Parameter {the missing parameter} is missing.</span></span>
<span data-ttu-id="0ab62-147">OsPlatformNotSupported</span><span class="sxs-lookup"><span data-stu-id="0ab62-147">OsPlatformNotSupported</span></span> | <span data-ttu-id="0ab62-148">BadRequest (400)</span><span class="sxs-lookup"><span data-stu-id="0ab62-148">BadRequest (400)</span></span> | <span data-ttu-id="0ab62-149">Plateforme de système d’exploitation {la plateforme de système d’exploitation client} n’est pas prise en charge pour cette action.</span><span class="sxs-lookup"><span data-stu-id="0ab62-149">OS Platform {the client OS Platform} is not supported for this action.</span></span>
<span data-ttu-id="0ab62-150">ClientVersionNotSupported</span><span class="sxs-lookup"><span data-stu-id="0ab62-150">ClientVersionNotSupported</span></span> | <span data-ttu-id="0ab62-151">BadRequest (400)</span><span class="sxs-lookup"><span data-stu-id="0ab62-151">BadRequest (400)</span></span> | <span data-ttu-id="0ab62-152">{L’action demandée} est prise en charge sur la version du client {version du client pris en charge} et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="0ab62-152">{The requested action} is supported on client version {supported client version} and above.</span></span>
<span data-ttu-id="0ab62-153">Non autorisé (Unauthorized)</span><span class="sxs-lookup"><span data-stu-id="0ab62-153">Unauthorized</span></span> | <span data-ttu-id="0ab62-154">Non autorisé (401)</span><span class="sxs-lookup"><span data-stu-id="0ab62-154">Unauthorized (401)</span></span> | <span data-ttu-id="0ab62-155">Non autorisé (en général, en en-tête d’autorisation ou expiré).</span><span class="sxs-lookup"><span data-stu-id="0ab62-155">Unauthorized (usually invalid or expired authorization header).</span></span>
<span data-ttu-id="0ab62-156">Interdit (Forbidden)</span><span class="sxs-lookup"><span data-stu-id="0ab62-156">Forbidden</span></span> | <span data-ttu-id="0ab62-157">Interdit (403)</span><span class="sxs-lookup"><span data-stu-id="0ab62-157">Forbidden (403)</span></span> | <span data-ttu-id="0ab62-158">Interdit (jeton valide, mais autorisation insuffisante pour l’action).</span><span class="sxs-lookup"><span data-stu-id="0ab62-158">Forbidden (valid token but insufficient permission for the action).</span></span>
<span data-ttu-id="0ab62-159">DisabledFeature</span><span class="sxs-lookup"><span data-stu-id="0ab62-159">DisabledFeature</span></span> | <span data-ttu-id="0ab62-160">Interdit (403)</span><span class="sxs-lookup"><span data-stu-id="0ab62-160">Forbidden (403)</span></span> | <span data-ttu-id="0ab62-161">La fonctionnalité de client n’est pas activée.</span><span class="sxs-lookup"><span data-stu-id="0ab62-161">Tenant feature is not enabled.</span></span>
<span data-ttu-id="0ab62-162">DisallowedOperation</span><span class="sxs-lookup"><span data-stu-id="0ab62-162">DisallowedOperation</span></span> | <span data-ttu-id="0ab62-163">Interdit (403)</span><span class="sxs-lookup"><span data-stu-id="0ab62-163">Forbidden (403)</span></span> | <span data-ttu-id="0ab62-164">{l’opération non autorisée et la raison}.</span><span class="sxs-lookup"><span data-stu-id="0ab62-164">{the disallowed operation and the reason}.</span></span>
<span data-ttu-id="0ab62-165">NotFound</span><span class="sxs-lookup"><span data-stu-id="0ab62-165">NotFound</span></span> | <span data-ttu-id="0ab62-166">Introuvable (404)</span><span class="sxs-lookup"><span data-stu-id="0ab62-166">Not Found (404)</span></span> | <span data-ttu-id="0ab62-167">Message d’erreur général introuvable.</span><span class="sxs-lookup"><span data-stu-id="0ab62-167">General Not Found error message.</span></span>
<span data-ttu-id="0ab62-168">ResourceNotFound</span><span class="sxs-lookup"><span data-stu-id="0ab62-168">ResourceNotFound</span></span> | <span data-ttu-id="0ab62-169">Introuvable (404)</span><span class="sxs-lookup"><span data-stu-id="0ab62-169">Not Found (404)</span></span> | <span data-ttu-id="0ab62-170">Ressource {la ressource demandée} est introuvable.</span><span class="sxs-lookup"><span data-stu-id="0ab62-170">Resource {the requested resource} was not found.</span></span>
<span data-ttu-id="0ab62-171">InternalServerError</span><span class="sxs-lookup"><span data-stu-id="0ab62-171">InternalServerError</span></span> | <span data-ttu-id="0ab62-172">Erreur de serveur interne (500)</span><span class="sxs-lookup"><span data-stu-id="0ab62-172">Internal Server Error (500)</span></span> | <span data-ttu-id="0ab62-173">(Aucun message d’erreur, retentez l’opération ou contactez-nous s’il n’est pas résolu)</span><span class="sxs-lookup"><span data-stu-id="0ab62-173">(No error message,  retry the operation or contact us if it does not get resolved)</span></span>

## <a name="body-parameters-are-case-sensitive"></a><span data-ttu-id="0ab62-174">Les paramètres Body respectent la casse</span><span class="sxs-lookup"><span data-stu-id="0ab62-174">Body parameters are case-sensitive</span></span>

<span data-ttu-id="0ab62-175">Les paramètres de corps soumis respectent actuellement la casse.</span><span class="sxs-lookup"><span data-stu-id="0ab62-175">The submitted body parameters are currently case-sensitive.</span></span>
<br><span data-ttu-id="0ab62-176">Si vous constatez une erreur **InvalidRequestBody** ou **MissingRequiredParameter** , il peut s’agir d’un paramètre incorrect ou d’une lettre minuscule.</span><span class="sxs-lookup"><span data-stu-id="0ab62-176">If you experience an **InvalidRequestBody** or **MissingRequiredParameter** errors, it might be caused from a wrong parameter capital or lower-case letter.</span></span>
<br><span data-ttu-id="0ab62-177">Nous vous recommandons de consulter la page relative à la documentation de l’API et de vérifier que les paramètres soumis correspondent à l’exemple approprié.</span><span class="sxs-lookup"><span data-stu-id="0ab62-177">We recommend that you review the API documentation page and check that the submitted parameters match the relevant example.</span></span>

## <a name="correlation-request-id"></a><span data-ttu-id="0ab62-178">ID de demande de corrélation</span><span class="sxs-lookup"><span data-stu-id="0ab62-178">Correlation request ID</span></span>

<span data-ttu-id="0ab62-179">Chaque réponse d’erreur contient un paramètre ID unique pour le suivi.</span><span class="sxs-lookup"><span data-stu-id="0ab62-179">Each error response contains a unique ID parameter for tracking.</span></span>
<br><span data-ttu-id="0ab62-180">Le nom de la propriété de ce paramètre est « cible ».</span><span class="sxs-lookup"><span data-stu-id="0ab62-180">The property name of this parameter is "target".</span></span>
<br><span data-ttu-id="0ab62-181">Lors de la création d’une erreur, la liaison de cet ID vous permettra de trouver la cause première du problème.</span><span class="sxs-lookup"><span data-stu-id="0ab62-181">When contacting us about an error, attaching this ID will help find the root cause of the problem.</span></span>

## <a name="examples"></a><span data-ttu-id="0ab62-182">範例</span><span class="sxs-lookup"><span data-stu-id="0ab62-182">Examples</span></span>

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

