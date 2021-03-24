---
title: Erreurs courantes de l’API Microsoft Defender ATP
description: Liste des erreurs d’API Microsoft Defender ATP courantes avec descriptions.
keywords: api, api mdatp, erreurs, résolution des problèmes
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
ms.openlocfilehash: ddbbe07bc477ae3a5016feb795b5bad5ed82a30a
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51064377"
---
# <a name="common-rest-api-error-codes"></a><span data-ttu-id="d1e64-104">Codes d’erreur courants de l’API REST</span><span class="sxs-lookup"><span data-stu-id="d1e64-104">Common REST API error codes</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


* <span data-ttu-id="d1e64-105">Les codes d’erreur répertoriés dans le tableau suivant peuvent être renvoyés par une opération sur n’importe quelle API Microsoft Defender pour point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="d1e64-105">The error codes listed in the following table may be returned by an operation on any of Microsoft Defender for Endpoint APIs.</span></span>
* <span data-ttu-id="d1e64-106">En plus du code d’erreur, chaque réponse d’erreur contient un message d’erreur, qui peut aider à résoudre le problème.</span><span class="sxs-lookup"><span data-stu-id="d1e64-106">In addition to the error code, every error response contains an error message, which can help resolve the problem.</span></span>
* <span data-ttu-id="d1e64-107">Le message est un texte libre qui peut être modifié.</span><span class="sxs-lookup"><span data-stu-id="d1e64-107">The message is a free text that can be changed.</span></span>
* <span data-ttu-id="d1e64-108">En bas de la page, vous trouverez des exemples de réponse.</span><span class="sxs-lookup"><span data-stu-id="d1e64-108">At the bottom of the page, you can find response examples.</span></span>

><span data-ttu-id="d1e64-109">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="d1e64-109">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="d1e64-110">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="d1e64-110">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-assignaccess-abovefoldlink)

<span data-ttu-id="d1e64-111">Code d’erreur</span><span class="sxs-lookup"><span data-stu-id="d1e64-111">Error code</span></span> |<span data-ttu-id="d1e64-112">Code d’état HTTP</span><span class="sxs-lookup"><span data-stu-id="d1e64-112">HTTP status code</span></span> |<span data-ttu-id="d1e64-113">Message</span><span class="sxs-lookup"><span data-stu-id="d1e64-113">Message</span></span> 
:---|:---|:---
<span data-ttu-id="d1e64-114">BadRequest</span><span class="sxs-lookup"><span data-stu-id="d1e64-114">BadRequest</span></span> | <span data-ttu-id="d1e64-115">BadRequest (400)</span><span class="sxs-lookup"><span data-stu-id="d1e64-115">BadRequest (400)</span></span> | <span data-ttu-id="d1e64-116">Message d’erreur Général Bad Request.</span><span class="sxs-lookup"><span data-stu-id="d1e64-116">General Bad Request error message.</span></span>
<span data-ttu-id="d1e64-117">ODataError</span><span class="sxs-lookup"><span data-stu-id="d1e64-117">ODataError</span></span> | <span data-ttu-id="d1e64-118">BadRequest (400)</span><span class="sxs-lookup"><span data-stu-id="d1e64-118">BadRequest (400)</span></span> | <span data-ttu-id="d1e64-119">Requête URI OData non valide (l’erreur spécifique est spécifiée).</span><span class="sxs-lookup"><span data-stu-id="d1e64-119">Invalid OData URI query (the specific error is specified).</span></span>
<span data-ttu-id="d1e64-120">InvalidInput</span><span class="sxs-lookup"><span data-stu-id="d1e64-120">InvalidInput</span></span> | <span data-ttu-id="d1e64-121">BadRequest (400)</span><span class="sxs-lookup"><span data-stu-id="d1e64-121">BadRequest (400)</span></span> | <span data-ttu-id="d1e64-122">Entrée non valide {l’entrée non valide}.</span><span class="sxs-lookup"><span data-stu-id="d1e64-122">Invalid input {the invalid input}.</span></span>
<span data-ttu-id="d1e64-123">InvalidRequestBody</span><span class="sxs-lookup"><span data-stu-id="d1e64-123">InvalidRequestBody</span></span> | <span data-ttu-id="d1e64-124">BadRequest (400)</span><span class="sxs-lookup"><span data-stu-id="d1e64-124">BadRequest (400)</span></span> | <span data-ttu-id="d1e64-125">Corps de la demande non valide.</span><span class="sxs-lookup"><span data-stu-id="d1e64-125">Invalid request body.</span></span>
<span data-ttu-id="d1e64-126">InvalidHashValue</span><span class="sxs-lookup"><span data-stu-id="d1e64-126">InvalidHashValue</span></span> | <span data-ttu-id="d1e64-127">BadRequest (400)</span><span class="sxs-lookup"><span data-stu-id="d1e64-127">BadRequest (400)</span></span> | <span data-ttu-id="d1e64-128">La valeur de hachage {le hachage non valide} n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="d1e64-128">Hash value {the invalid hash} is invalid.</span></span>
<span data-ttu-id="d1e64-129">InvalidDomainName</span><span class="sxs-lookup"><span data-stu-id="d1e64-129">InvalidDomainName</span></span> | <span data-ttu-id="d1e64-130">BadRequest (400)</span><span class="sxs-lookup"><span data-stu-id="d1e64-130">BadRequest (400)</span></span> | <span data-ttu-id="d1e64-131">Nom de domaine {le domaine non valide} non valide.</span><span class="sxs-lookup"><span data-stu-id="d1e64-131">Domain name {the invalid domain} is invalid.</span></span>
<span data-ttu-id="d1e64-132">InvalidIpAddress</span><span class="sxs-lookup"><span data-stu-id="d1e64-132">InvalidIpAddress</span></span> | <span data-ttu-id="d1e64-133">BadRequest (400)</span><span class="sxs-lookup"><span data-stu-id="d1e64-133">BadRequest (400)</span></span> | <span data-ttu-id="d1e64-134">Adresse IP {l’adresse IP non valide} n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="d1e64-134">IP address {the invalid IP} is invalid.</span></span>
<span data-ttu-id="d1e64-135">InvalidUrl</span><span class="sxs-lookup"><span data-stu-id="d1e64-135">InvalidUrl</span></span> | <span data-ttu-id="d1e64-136">BadRequest (400)</span><span class="sxs-lookup"><span data-stu-id="d1e64-136">BadRequest (400)</span></span> | <span data-ttu-id="d1e64-137">URL {l’URL non valide} n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="d1e64-137">URL {the invalid URL} is invalid.</span></span>
<span data-ttu-id="d1e64-138">MaximumBatchSizeExceeded</span><span class="sxs-lookup"><span data-stu-id="d1e64-138">MaximumBatchSizeExceeded</span></span> | <span data-ttu-id="d1e64-139">BadRequest (400)</span><span class="sxs-lookup"><span data-stu-id="d1e64-139">BadRequest (400)</span></span> | <span data-ttu-id="d1e64-140">La taille maximale du lot est dépassée.</span><span class="sxs-lookup"><span data-stu-id="d1e64-140">Maximum batch size exceeded.</span></span> <span data-ttu-id="d1e64-141">Received: {batch size received}, allowed: {batch size allowed}.</span><span class="sxs-lookup"><span data-stu-id="d1e64-141">Received: {batch size received}, allowed: {batch size allowed}.</span></span>
<span data-ttu-id="d1e64-142">MissingRequiredParameter</span><span class="sxs-lookup"><span data-stu-id="d1e64-142">MissingRequiredParameter</span></span> | <span data-ttu-id="d1e64-143">BadRequest (400)</span><span class="sxs-lookup"><span data-stu-id="d1e64-143">BadRequest (400)</span></span> | <span data-ttu-id="d1e64-144">Le paramètre {le paramètre manquant} est manquant.</span><span class="sxs-lookup"><span data-stu-id="d1e64-144">Parameter {the missing parameter} is missing.</span></span>
<span data-ttu-id="d1e64-145">OsPlatformNotSupported</span><span class="sxs-lookup"><span data-stu-id="d1e64-145">OsPlatformNotSupported</span></span> | <span data-ttu-id="d1e64-146">BadRequest (400)</span><span class="sxs-lookup"><span data-stu-id="d1e64-146">BadRequest (400)</span></span> | <span data-ttu-id="d1e64-147">La plateforme du système d’exploitation {la plateforme de système d’exploitation cliente} n’est pas prise en charge pour cette action.</span><span class="sxs-lookup"><span data-stu-id="d1e64-147">OS Platform {the client OS Platform} is not supported for this action.</span></span>
<span data-ttu-id="d1e64-148">ClientVersionNotSupported</span><span class="sxs-lookup"><span data-stu-id="d1e64-148">ClientVersionNotSupported</span></span> | <span data-ttu-id="d1e64-149">BadRequest (400)</span><span class="sxs-lookup"><span data-stu-id="d1e64-149">BadRequest (400)</span></span> | <span data-ttu-id="d1e64-150">{The requested action} is supported on client version {supported client version} and above.</span><span class="sxs-lookup"><span data-stu-id="d1e64-150">{The requested action} is supported on client version {supported client version} and above.</span></span>
<span data-ttu-id="d1e64-151">Non autorisé (Unauthorized)</span><span class="sxs-lookup"><span data-stu-id="d1e64-151">Unauthorized</span></span> | <span data-ttu-id="d1e64-152">Non autorisé (401)</span><span class="sxs-lookup"><span data-stu-id="d1e64-152">Unauthorized (401)</span></span> | <span data-ttu-id="d1e64-153">Non autorisé (en-tête d’autorisation non valide ou expiré).</span><span class="sxs-lookup"><span data-stu-id="d1e64-153">Unauthorized (invalid or expired authorization header).</span></span>
<span data-ttu-id="d1e64-154">Interdit (Forbidden)</span><span class="sxs-lookup"><span data-stu-id="d1e64-154">Forbidden</span></span> | <span data-ttu-id="d1e64-155">Interdit (403)</span><span class="sxs-lookup"><span data-stu-id="d1e64-155">Forbidden (403)</span></span> | <span data-ttu-id="d1e64-156">Interdit (jeton valide mais autorisation insuffisante pour l’action).</span><span class="sxs-lookup"><span data-stu-id="d1e64-156">Forbidden (valid token but insufficient permission for the action).</span></span>
<span data-ttu-id="d1e64-157">DisabledFeature</span><span class="sxs-lookup"><span data-stu-id="d1e64-157">DisabledFeature</span></span> | <span data-ttu-id="d1e64-158">Interdit (403)</span><span class="sxs-lookup"><span data-stu-id="d1e64-158">Forbidden (403)</span></span> | <span data-ttu-id="d1e64-159">La fonctionnalité client n’est pas activée.</span><span class="sxs-lookup"><span data-stu-id="d1e64-159">Tenant feature is not enabled.</span></span>
<span data-ttu-id="d1e64-160">DisallowedOperation</span><span class="sxs-lookup"><span data-stu-id="d1e64-160">DisallowedOperation</span></span> | <span data-ttu-id="d1e64-161">Interdit (403)</span><span class="sxs-lookup"><span data-stu-id="d1e64-161">Forbidden (403)</span></span> | <span data-ttu-id="d1e64-162">{l’opération nonallée et la raison}.</span><span class="sxs-lookup"><span data-stu-id="d1e64-162">{the disallowed operation and the reason}.</span></span>
<span data-ttu-id="d1e64-163">NotFound</span><span class="sxs-lookup"><span data-stu-id="d1e64-163">NotFound</span></span> | <span data-ttu-id="d1e64-164">In found (404)</span><span class="sxs-lookup"><span data-stu-id="d1e64-164">Not Found (404)</span></span> | <span data-ttu-id="d1e64-165">Message d’erreur Général in trouvé.</span><span class="sxs-lookup"><span data-stu-id="d1e64-165">General Not Found error message.</span></span>
<span data-ttu-id="d1e64-166">ResourceNotFound</span><span class="sxs-lookup"><span data-stu-id="d1e64-166">ResourceNotFound</span></span> | <span data-ttu-id="d1e64-167">In found (404)</span><span class="sxs-lookup"><span data-stu-id="d1e64-167">Not Found (404)</span></span> | <span data-ttu-id="d1e64-168">Ressource {la ressource demandée} in trouvée.</span><span class="sxs-lookup"><span data-stu-id="d1e64-168">Resource {the requested resource} was not found.</span></span>
<span data-ttu-id="d1e64-169">InternalServerError</span><span class="sxs-lookup"><span data-stu-id="d1e64-169">InternalServerError</span></span> | <span data-ttu-id="d1e64-170">Erreur interne du serveur (500)</span><span class="sxs-lookup"><span data-stu-id="d1e64-170">Internal Server Error (500)</span></span> | <span data-ttu-id="d1e64-171">(Aucun message d’erreur, nouvelle tentative de l’opération)</span><span class="sxs-lookup"><span data-stu-id="d1e64-171">(No error message, retry the operation)</span></span>
<span data-ttu-id="d1e64-172">TooManyRequests</span><span class="sxs-lookup"><span data-stu-id="d1e64-172">TooManyRequests</span></span> | <span data-ttu-id="d1e64-173">Trop de demandes (429)</span><span class="sxs-lookup"><span data-stu-id="d1e64-173">Too Many Requests (429)</span></span> | <span data-ttu-id="d1e64-174">La réponse représente l’atteinte de la limite de quota soit par nombre de demandes, soit par processeur.</span><span class="sxs-lookup"><span data-stu-id="d1e64-174">Response will represent reaching quota limit either by number of requests or by CPU.</span></span>

## <a name="body-parameters-are-case-sensitive"></a><span data-ttu-id="d1e64-175">Les paramètres body sont sensibles à la cas</span><span class="sxs-lookup"><span data-stu-id="d1e64-175">Body parameters are case-sensitive</span></span>

<span data-ttu-id="d1e64-176">Les paramètres du corps soumis sont actuellement sensibles à la cas.</span><span class="sxs-lookup"><span data-stu-id="d1e64-176">The submitted body parameters are currently case-sensitive.</span></span>
<br><span data-ttu-id="d1e64-177">Si vous faites l’expérience d’erreurs **InvalidRequestBody** ou **MissingRequiredParameter,** cela peut être dû à une majuscule de paramètre incorrecte ou à une lettre majuscule incorrecte.</span><span class="sxs-lookup"><span data-stu-id="d1e64-177">If you experience an **InvalidRequestBody** or **MissingRequiredParameter** errors, it might be caused from a wrong parameter capital or lower-case letter.</span></span>
<br><span data-ttu-id="d1e64-178">Consultez la page de documentation de l’API et vérifiez que les paramètres envoyés correspondent à l’exemple approprié.</span><span class="sxs-lookup"><span data-stu-id="d1e64-178">Review the API documentation page and check that the submitted parameters match the relevant example.</span></span>

## <a name="correlation-request-id"></a><span data-ttu-id="d1e64-179">ID de demande de corrélation</span><span class="sxs-lookup"><span data-stu-id="d1e64-179">Correlation request ID</span></span>

<span data-ttu-id="d1e64-180">Chaque réponse d’erreur contient un paramètre d’ID unique pour le suivi.</span><span class="sxs-lookup"><span data-stu-id="d1e64-180">Each error response contains a unique ID parameter for tracking.</span></span>
<br><span data-ttu-id="d1e64-181">Le nom de propriété de ce paramètre est « target ».</span><span class="sxs-lookup"><span data-stu-id="d1e64-181">The property name of this parameter is "target".</span></span>
<br><span data-ttu-id="d1e64-182">Lorsque vous nous contactez à propos d’une erreur, l’attachement de cet ID permet de trouver la cause première du problème.</span><span class="sxs-lookup"><span data-stu-id="d1e64-182">When contacting us about an error, attaching this ID will help find the root cause of the problem.</span></span>

## <a name="examples"></a><span data-ttu-id="d1e64-183">範例</span><span class="sxs-lookup"><span data-stu-id="d1e64-183">Examples</span></span>

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
