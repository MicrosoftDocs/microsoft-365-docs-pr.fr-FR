---
title: Détecter Microsoft Defender pour les points de terminaison à l'aide de l'API REST
description: Découvrez comment appeler un point de terminaison de l'API Microsoft Defender for Endpoint pour tirer les détections au format JSON à l'aide de l'API REST SIEM.
keywords: détections, détections de pull, api rest, demande, réponse
search.product: eADQiWindows 10XVcnh
search.appverid: met150
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
ms.openlocfilehash: 06028f64a3340aeeef52269bc8a1e739d18e6db7
ms.sourcegitcommit: 13ce4b31303a1a21ca53700a54bcf8d91ad2f8c1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/20/2021
ms.locfileid: "51903117"
---
# <a name="pull-microsoft-defender-for-endpoint-detections-using-siem-rest-api"></a><span data-ttu-id="e9360-104">Détecter Microsoft Defender pour les points de terminaison à l'aide de l'API REST SIEM</span><span class="sxs-lookup"><span data-stu-id="e9360-104">Pull Microsoft Defender for Endpoint detections using SIEM REST API</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="e9360-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="e9360-105">**Applies to:**</span></span>
- [<span data-ttu-id="e9360-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="e9360-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="e9360-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="e9360-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

><span data-ttu-id="e9360-108">Vous souhaitez faire l'expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="e9360-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="e9360-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="e9360-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-pullalerts-abovefoldlink) 


[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

>[!Note]
>- <span data-ttu-id="e9360-110">[Microsoft Defender pour l'alerte de point de terminaison](alerts.md) se compose d'une ou de plusieurs détections.</span><span class="sxs-lookup"><span data-stu-id="e9360-110">[Microsoft Defender for Endpoint Alert](alerts.md) is composed from one or more detections.</span></span>
>- <span data-ttu-id="e9360-111">[Microsoft Defender pour la détection des points](api-portal-mapping.md) de terminaison est composé de l'événement suspect qui s'est produit sur l'appareil et de ses détails d'alerte associés.</span><span class="sxs-lookup"><span data-stu-id="e9360-111">[Microsoft Defender for Endpoint Detection](api-portal-mapping.md) is composed from the suspicious event occurred on the Device and its related Alert details.</span></span>
><span data-ttu-id="e9360-112">-The Microsoft Defender for Endpoint Alert API is the latest API for alert consumption and contain a detailed list of related evidence for each alert.</span><span class="sxs-lookup"><span data-stu-id="e9360-112">-The Microsoft Defender for Endpoint Alert API is the latest API for alert consumption and contain a detailed list of related evidence for each alert.</span></span> <span data-ttu-id="e9360-113">Pour plus d'informations, voir [Méthodes et propriétés d'alerte et](alerts.md) Liste des [alertes.](get-alerts.md)</span><span class="sxs-lookup"><span data-stu-id="e9360-113">For more information, see [Alert methods and properties](alerts.md) and [List alerts](get-alerts.md).</span></span>

<span data-ttu-id="e9360-114">Microsoft Defender pour le point de terminaison prend en charge le protocole OAuth 2.0 pour tirer les détections de l'API.</span><span class="sxs-lookup"><span data-stu-id="e9360-114">Microsoft Defender for Endpoint supports the OAuth 2.0 protocol to pull detections from the API.</span></span>

<span data-ttu-id="e9360-115">En règle générale, le protocole OAuth 2.0 prend en charge quatre types de flux :</span><span class="sxs-lookup"><span data-stu-id="e9360-115">In general, the OAuth 2.0 protocol supports four types of flows:</span></span>
- <span data-ttu-id="e9360-116">Flux d'octroi d'autorisation</span><span class="sxs-lookup"><span data-stu-id="e9360-116">Authorization grant flow</span></span>
- <span data-ttu-id="e9360-117">Flux implicite</span><span class="sxs-lookup"><span data-stu-id="e9360-117">Implicit flow</span></span>
- <span data-ttu-id="e9360-118">Flux d'informations d'identification du client</span><span class="sxs-lookup"><span data-stu-id="e9360-118">Client credentials flow</span></span>
- <span data-ttu-id="e9360-119">Flux du propriétaire de la ressource</span><span class="sxs-lookup"><span data-stu-id="e9360-119">Resource owner flow</span></span>

<span data-ttu-id="e9360-120">Pour plus d'informations sur les spécifications OAuth, voir le site [web OAuth.](http://www.oauth.net)</span><span class="sxs-lookup"><span data-stu-id="e9360-120">For more information about the OAuth specifications, see the [OAuth Website](http://www.oauth.net).</span></span>

<span data-ttu-id="e9360-121">Microsoft Defender pour le  point de terminaison prend en charge le flux d'octroi d'autorisation et le flux d'informations d'identification du _client_ pour obtenir l'accès aux détections de pull, avec Azure Active Directory (AAD) comme serveur d'autorisation.</span><span class="sxs-lookup"><span data-stu-id="e9360-121">Microsoft Defender for Endpoint supports the _Authorization grant flow_ and _Client credential flow_ to obtain access to pull detections, with Azure Active Directory (AAD) as the authorization server.</span></span>

<span data-ttu-id="e9360-122">Le _flux d'octroi d'autorisation_ utilise les informations d'identification de l'utilisateur pour obtenir un code d'autorisation, qui est ensuite utilisé pour obtenir un jeton d'accès.</span><span class="sxs-lookup"><span data-stu-id="e9360-122">The _Authorization grant flow_ uses user credentials to get an authorization code, which is then used to obtain an access token.</span></span>

<span data-ttu-id="e9360-123">Le _flux d'informations d'identification_ du client utilise les informations d'identification du client pour s'authentifier par rapport à l'URL du point de terminaison Microsoft Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="e9360-123">The _Client credential flow_ uses client credentials to authenticate against the Microsoft Defender for Endpoint endpoint URL.</span></span> <span data-ttu-id="e9360-124">Ce flux convient aux scénarios où un client OAuth crée des demandes à une API qui ne nécessite pas d'informations d'identification utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e9360-124">This flow is suitable for scenarios when an OAuth client creates requests to an API that doesn't require user credentials.</span></span>

<span data-ttu-id="e9360-125">Utilisez la méthode suivante dans l'API Microsoft Defender for Endpoint pour tirer les détections au format JSON.</span><span class="sxs-lookup"><span data-stu-id="e9360-125">Use the following method in the Microsoft Defender for Endpoint API to pull detections in JSON format.</span></span>

>[!NOTE]
><span data-ttu-id="e9360-126">Le Centre de sécurité Microsoft Defender fusionne des détections d'alertes similaires en une seule alerte.</span><span class="sxs-lookup"><span data-stu-id="e9360-126">Microsoft Defender Security Center merges similar alert detections into a single alert.</span></span> <span data-ttu-id="e9360-127">Cette API tire les détections d'alertes dans sa forme brute en fonction des paramètres de requête que vous définissez, ce qui vous permet d'appliquer vos propres regroupements et filtrages.</span><span class="sxs-lookup"><span data-stu-id="e9360-127">This API pulls alert detections in its raw form based on the query parameters you set, enabling you to apply your own grouping and filtering.</span></span> 

## <a name="before-you-begin"></a><span data-ttu-id="e9360-128">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="e9360-128">Before you begin</span></span>
- <span data-ttu-id="e9360-129">Avant d'appeler le point de terminaison Microsoft Defender pour point de terminaison pour tirer les détections, vous devez activer l'application d'intégration SIEM dans Azure Active Directory (AAD).</span><span class="sxs-lookup"><span data-stu-id="e9360-129">Before calling the Microsoft Defender for Endpoint endpoint to pull detections, you'll need to enable the SIEM integration application in Azure Active Directory (AAD).</span></span> <span data-ttu-id="e9360-130">Pour plus d'informations, voir [Enable SIEM integration in Microsoft Defender for Endpoint](enable-siem-integration.md).</span><span class="sxs-lookup"><span data-stu-id="e9360-130">For more information, see [Enable SIEM integration in Microsoft Defender for Endpoint](enable-siem-integration.md).</span></span>

- <span data-ttu-id="e9360-p106">Prenez note des valeurs suivantes dans l’inscription de votre application Azure. Ces valeurs sont nécessaires pour configurer le flux OAuth dans votre application de service ou de démon.</span><span class="sxs-lookup"><span data-stu-id="e9360-p106">Take note of the following values in your Azure application registration. You need these values to configure the OAuth flow in your service or daemon app:</span></span>
  - <span data-ttu-id="e9360-133">ID d’application (unique pour votre application)</span><span class="sxs-lookup"><span data-stu-id="e9360-133">Application ID (unique to your application)</span></span>
  - <span data-ttu-id="e9360-134">Clé d’application ou question secrète de l’application (unique pour votre application)</span><span class="sxs-lookup"><span data-stu-id="e9360-134">App key, or secret (unique to your application)</span></span>
  - <span data-ttu-id="e9360-135">Point de terminaison du jeton OAuth 2.0 de votre application</span><span class="sxs-lookup"><span data-stu-id="e9360-135">Your app's OAuth 2.0 token endpoint</span></span>
    - <span data-ttu-id="e9360-p107">Recherchez cette valeur en cliquant sur **Points de terminaison** en bas du portail de gestion Azure dans la page de votre application. Le point de terminaison ressemblera à `https://login.microsoftonline.com/{tenantId}/oauth2/token`.</span><span class="sxs-lookup"><span data-stu-id="e9360-p107">Find this value by clicking **View Endpoints** at the bottom of the Azure Management Portal in your app's page. The endpoint will look like `https://login.microsoftonline.com/{tenantId}/oauth2/token`.</span></span>

## <a name="get-an-access-token"></a><span data-ttu-id="e9360-138">Obtenir un jeton d’accès</span><span class="sxs-lookup"><span data-stu-id="e9360-138">Get an access token</span></span>
<span data-ttu-id="e9360-139">Avant de créer des appels au point de terminaison, vous devez obtenir un jeton d'accès.</span><span class="sxs-lookup"><span data-stu-id="e9360-139">Before creating calls to the endpoint, you'll need to get an access token.</span></span>

<span data-ttu-id="e9360-140">Vous utiliserez le jeton d'accès pour accéder à la ressource protégée, c'est-à-dire les détections dans Microsoft Defender pour le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="e9360-140">You'll use the access token to access the protected resource, which is detections in Microsoft Defender for Endpoint.</span></span>

<span data-ttu-id="e9360-141">Pour obtenir un jeton d'accès, vous devez faire une demande POST au point de terminaison émettant le jeton.</span><span class="sxs-lookup"><span data-stu-id="e9360-141">To get an access token, you'll need to do a POST request to the token issuing endpoint.</span></span> <span data-ttu-id="e9360-142">Voici un exemple de requête :</span><span class="sxs-lookup"><span data-stu-id="e9360-142">Here is a sample request:</span></span>

```http

POST /72f988bf-86f1-41af-91ab-2d7cd011db47/oauth2/token HTTP/1.1
Host: login.microsoftonline.com
Content-Type: application/x-www-form-urlencoded

resource=https%3A%2F%2Fgraph.windows.net&client_id=35e0f735-5fe4-4693-9e68-3de80f1d3745&client_secret=IKXc6PxB2eoFNJ%2FIT%2Bl2JZZD9d9032VXz6Ul3D2WyUQ%3D&grant_type=client_credentials
```
<span data-ttu-id="e9360-143">La réponse inclura un jeton d’accès et des informations sur l’expiration.</span><span class="sxs-lookup"><span data-stu-id="e9360-143">The response will include an access token and expiry information.</span></span>

```json
{
  "token_type": "Bearer",
  "expires_in": 3599,
  "ext_expires_in": 0,
  "expires_on": 1488720683,
  "not_before": 1488720683,
  "resource": "https://graph.windows.net",
  "access_token":"eyJ0eXaioJJOIneiowiouqSuzNiZ345FYOVkaJL0625TueyaJasjhIjEnbMlWqP..."
}
```
<span data-ttu-id="e9360-144">Vous pouvez désormais utiliser la valeur dans le *champ access_token* dans une demande à l'API Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="e9360-144">You can now use the value in the *access_token* field in a request to the Defender for Endpoint API.</span></span>

## <a name="request"></a><span data-ttu-id="e9360-145">Demande</span><span class="sxs-lookup"><span data-stu-id="e9360-145">Request</span></span>
<span data-ttu-id="e9360-146">Avec un jeton d'accès, votre application peut effectuer des demandes authentifiées à l'API Microsoft Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="e9360-146">With an access token, your app can make authenticated requests to the Microsoft Defender for Endpoint API.</span></span> <span data-ttu-id="e9360-147">Votre application doit ajouter le jeton d’accès à l’en-tête Authorization de chaque demande.</span><span class="sxs-lookup"><span data-stu-id="e9360-147">Your app must append the access token to the Authorization header of each request.</span></span>

### <a name="request-syntax"></a><span data-ttu-id="e9360-148">Syntaxe de la requête</span><span class="sxs-lookup"><span data-stu-id="e9360-148">Request syntax</span></span>
<span data-ttu-id="e9360-149">Méthode</span><span class="sxs-lookup"><span data-stu-id="e9360-149">Method</span></span> | <span data-ttu-id="e9360-150">URI de demande</span><span class="sxs-lookup"><span data-stu-id="e9360-150">Request URI</span></span>
:---|:---|
<span data-ttu-id="e9360-151">GET</span><span class="sxs-lookup"><span data-stu-id="e9360-151">GET</span></span>| <span data-ttu-id="e9360-152">Utilisez l'URI applicable pour votre région.</span><span class="sxs-lookup"><span data-stu-id="e9360-152">Use the URI applicable for your region.</span></span> <br><br> <span data-ttu-id="e9360-153">**Pour l'UE**: `https://wdatp-alertexporter-eu.windows.com/api/alerts`</span><span class="sxs-lookup"><span data-stu-id="e9360-153">**For EU**: `https://wdatp-alertexporter-eu.windows.com/api/alerts`</span></span> </br> <span data-ttu-id="e9360-154">**Pour les États-Unis**: `https://wdatp-alertexporter-us.windows.com/api/alerts`</span><span class="sxs-lookup"><span data-stu-id="e9360-154">**For US**: `https://wdatp-alertexporter-us.windows.com/api/alerts`</span></span> <br> <span data-ttu-id="e9360-155">**Pour le Royaume-Uni**: `https://wdatp-alertexporter-uk.windows.com/api/alerts`</span><span class="sxs-lookup"><span data-stu-id="e9360-155">**For UK**: `https://wdatp-alertexporter-uk.windows.com/api/alerts`</span></span> 

### <a name="request-header"></a><span data-ttu-id="e9360-156">En-tête de demande</span><span class="sxs-lookup"><span data-stu-id="e9360-156">Request header</span></span>
<span data-ttu-id="e9360-157">En-tête</span><span class="sxs-lookup"><span data-stu-id="e9360-157">Header</span></span> | <span data-ttu-id="e9360-158">Type</span><span class="sxs-lookup"><span data-stu-id="e9360-158">Type</span></span> | <span data-ttu-id="e9360-159">Description</span><span class="sxs-lookup"><span data-stu-id="e9360-159">Description</span></span>|
:--|:--|:--
<span data-ttu-id="e9360-160">Autorisation</span><span class="sxs-lookup"><span data-stu-id="e9360-160">Authorization</span></span> | <span data-ttu-id="e9360-161">string</span><span class="sxs-lookup"><span data-stu-id="e9360-161">string</span></span> | <span data-ttu-id="e9360-162">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="e9360-162">Required.</span></span> <span data-ttu-id="e9360-163">Jeton d'accès Azure AD sous la forme **d'un jeton du** &lt; *porteur.* &gt;</span><span class="sxs-lookup"><span data-stu-id="e9360-163">The Azure AD access token in the form **Bearer** &lt;*token*&gt;.</span></span> |

### <a name="request-parameters"></a><span data-ttu-id="e9360-164">Paramètres de la requête</span><span class="sxs-lookup"><span data-stu-id="e9360-164">Request parameters</span></span>

<span data-ttu-id="e9360-165">Utilisez des paramètres de requête facultatifs pour spécifier et contrôler la quantité de données renvoyées dans une réponse.</span><span class="sxs-lookup"><span data-stu-id="e9360-165">Use optional query parameters to specify and control the amount of data returned in a response.</span></span> <span data-ttu-id="e9360-166">Si vous appelez cette méthode sans paramètres, la réponse contient toutes les alertes de votre organisation au cours des 2 dernières heures.</span><span class="sxs-lookup"><span data-stu-id="e9360-166">If you call this method without parameters, the response contains all the alerts in your organization in the last 2 hours.</span></span>

<span data-ttu-id="e9360-167">Nom</span><span class="sxs-lookup"><span data-stu-id="e9360-167">Name</span></span> | <span data-ttu-id="e9360-168">Valeur</span><span class="sxs-lookup"><span data-stu-id="e9360-168">Value</span></span>| <span data-ttu-id="e9360-169">Description</span><span class="sxs-lookup"><span data-stu-id="e9360-169">Description</span></span>
:---|:---|:---
<span data-ttu-id="e9360-170">sinceTimeUtc</span><span class="sxs-lookup"><span data-stu-id="e9360-170">sinceTimeUtc</span></span> | <span data-ttu-id="e9360-171">Date/heure</span><span class="sxs-lookup"><span data-stu-id="e9360-171">DateTime</span></span> | <span data-ttu-id="e9360-172">Définit les alertes liées au temps inférieur à partir de, en fonction du champ :</span><span class="sxs-lookup"><span data-stu-id="e9360-172">Defines the lower time bound alerts are retrieved from, based on field:</span></span> <br> `LastProcessedTimeUtc` <br> <span data-ttu-id="e9360-173">L'intervalle de temps sera : de l'heure sinceTimeUtc à l'heure actuelle.</span><span class="sxs-lookup"><span data-stu-id="e9360-173">The time range will be: from sinceTimeUtc time to current time.</span></span> <br><br> <span data-ttu-id="e9360-174">**REMARQUE**: lorsqu'elle n'est pas spécifiée, toutes les alertes générées au cours des deux dernières heures sont récupérées.</span><span class="sxs-lookup"><span data-stu-id="e9360-174">**NOTE**: When not specified, all alerts generated in the last two hours are retrieved.</span></span>
<span data-ttu-id="e9360-175">untilTimeUtc</span><span class="sxs-lookup"><span data-stu-id="e9360-175">untilTimeUtc</span></span> | <span data-ttu-id="e9360-176">Date/heure</span><span class="sxs-lookup"><span data-stu-id="e9360-176">DateTime</span></span> | <span data-ttu-id="e9360-177">Définit les alertes liées au temps supérieur qui sont récupérées.</span><span class="sxs-lookup"><span data-stu-id="e9360-177">Defines the upper time bound alerts are retrieved.</span></span> <br> <span data-ttu-id="e9360-178">La plage de temps sera : de `sinceTimeUtc` temps en `untilTimeUtc` temps.</span><span class="sxs-lookup"><span data-stu-id="e9360-178">The time range will be: from `sinceTimeUtc` time to `untilTimeUtc` time.</span></span> <br><br> <span data-ttu-id="e9360-179">**REMARQUE**: lorsqu'elle n'est pas spécifiée, la valeur par défaut est l'heure actuelle.</span><span class="sxs-lookup"><span data-stu-id="e9360-179">**NOTE**: When not specified, the default value will be the current time.</span></span>
<span data-ttu-id="e9360-180">ago</span><span class="sxs-lookup"><span data-stu-id="e9360-180">ago</span></span> | <span data-ttu-id="e9360-181">string</span><span class="sxs-lookup"><span data-stu-id="e9360-181">string</span></span> | <span data-ttu-id="e9360-182">Pulls alerts in the following time range: from `(current_time - ago)` time to `current_time` time.</span><span class="sxs-lookup"><span data-stu-id="e9360-182">Pulls alerts in the following time range: from `(current_time - ago)` time to `current_time` time.</span></span> <br><br> <span data-ttu-id="e9360-183">La valeur doit être définie selon le format de durée **ISO 8601**</span><span class="sxs-lookup"><span data-stu-id="e9360-183">Value should be set according to **ISO 8601** duration format</span></span> <br> <span data-ttu-id="e9360-184">Exemple : `ago=PT10M` tirera les alertes reçues au cours des 10 dernières minutes.</span><span class="sxs-lookup"><span data-stu-id="e9360-184">Example: `ago=PT10M` will pull alerts received in the last 10 minutes.</span></span>
<span data-ttu-id="e9360-185">limit</span><span class="sxs-lookup"><span data-stu-id="e9360-185">limit</span></span> | <span data-ttu-id="e9360-186">entier</span><span class="sxs-lookup"><span data-stu-id="e9360-186">int</span></span> | <span data-ttu-id="e9360-187">Définit le nombre d'alertes à récupérer.</span><span class="sxs-lookup"><span data-stu-id="e9360-187">Defines the number of alerts to be retrieved.</span></span> <span data-ttu-id="e9360-188">Les alertes les plus récentes sont récupérées en fonction du nombre défini.</span><span class="sxs-lookup"><span data-stu-id="e9360-188">Most recent alerts will be retrieved based on the number defined.</span></span><br><br> <span data-ttu-id="e9360-189">**REMARQUE**: lorsqu'elle n'est pas spécifiée, toutes les alertes disponibles dans l'plage de temps sont récupérées.</span><span class="sxs-lookup"><span data-stu-id="e9360-189">**NOTE**: When not specified, all alerts available in the time range will be retrieved.</span></span>
<span data-ttu-id="e9360-190">machinegroups</span><span class="sxs-lookup"><span data-stu-id="e9360-190">machinegroups</span></span> | <span data-ttu-id="e9360-191">string</span><span class="sxs-lookup"><span data-stu-id="e9360-191">string</span></span> | <span data-ttu-id="e9360-192">Spécifie les groupes d'appareils à partir des appareils à partir des alertes.</span><span class="sxs-lookup"><span data-stu-id="e9360-192">Specifies device groups to pull alerts from.</span></span> <br><br> <span data-ttu-id="e9360-193">**REMARQUE**: lorsqu'elle n'est pas spécifiée, les alertes de tous les groupes d'appareils sont récupérées.</span><span class="sxs-lookup"><span data-stu-id="e9360-193">**NOTE**: When not specified, alerts from all device groups will be retrieved.</span></span> <br><br> <span data-ttu-id="e9360-194">Exemple :</span><span class="sxs-lookup"><span data-stu-id="e9360-194">Example:</span></span> <br><br> ```https://wdatp-alertexporter-eu.securitycenter.windows.com/api/alerts/?machinegroups=UKMachines&machinegroups=FranceMachines```
<span data-ttu-id="e9360-195">DeviceCreatedMachineTags</span><span class="sxs-lookup"><span data-stu-id="e9360-195">DeviceCreatedMachineTags</span></span> | <span data-ttu-id="e9360-196">string</span><span class="sxs-lookup"><span data-stu-id="e9360-196">string</span></span> | <span data-ttu-id="e9360-197">Balise d'appareil unique à partir du Registre.</span><span class="sxs-lookup"><span data-stu-id="e9360-197">Single device tag from the registry.</span></span>
<span data-ttu-id="e9360-198">CloudCreatedMachineTags</span><span class="sxs-lookup"><span data-stu-id="e9360-198">CloudCreatedMachineTags</span></span> | <span data-ttu-id="e9360-199">string</span><span class="sxs-lookup"><span data-stu-id="e9360-199">string</span></span> | <span data-ttu-id="e9360-200">Balises d'appareil créées dans le Centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="e9360-200">Device tags that were created in Microsoft Defender Security Center.</span></span>

### <a name="request-example"></a><span data-ttu-id="e9360-201">Exemple de requête</span><span class="sxs-lookup"><span data-stu-id="e9360-201">Request example</span></span>
<span data-ttu-id="e9360-202">L'exemple suivant montre comment récupérer toutes les détections dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="e9360-202">The following example demonstrates how to retrieve all the detections in your organization.</span></span>

```http
GET  https://wdatp-alertexporter-eu.windows.com/api/alerts
Authorization: Bearer <your access token>
```

<span data-ttu-id="e9360-203">L'exemple suivant illustre une demande d'obtenir les 20 dernières détections depuis 2016-09-12 00:00:00.</span><span class="sxs-lookup"><span data-stu-id="e9360-203">The following example demonstrates a request to get the last 20 detections since 2016-09-12 00:00:00.</span></span>

```http
GET  https://wdatp-alertexporter-eu.windows.com/api/alerts?limit=20&sinceTimeUtc=2016-09-12T00:00:00.000
Authorization: Bearer <your access token>
```

## <a name="response"></a><span data-ttu-id="e9360-204">Réponse</span><span class="sxs-lookup"><span data-stu-id="e9360-204">Response</span></span>
<span data-ttu-id="e9360-205">La valeur de retour est un tableau d'objets d'alerte au format JSON.</span><span class="sxs-lookup"><span data-stu-id="e9360-205">The return value is an array of alert objects in JSON format.</span></span>

<span data-ttu-id="e9360-206">Voici un exemple de valeur de retour :</span><span class="sxs-lookup"><span data-stu-id="e9360-206">Here is an example return value:</span></span>

```json 
[
{        
        "AlertTime": "2020-09-30T14:09:20.35743Z",
        "ComputerDnsName": "mymachine1.domain.com",
        "AlertTitle": "Suspicious File Activity",
        "Category": "Malware",
        "Severity": "High",
        "AlertId": "da637370718981685665_16349121",
        "Actor": "",
        "LinkToWDATP": "https://securitycenter.windows.com/alert/da637370718981685665_16349121",
        "IocName": "",
        "IocValue": "",
        "CreatorIocName": "",
        "CreatorIocValue": "",
        "Sha1": "aabbccddee1122334455aabbccddee1122334455",
        "FileName": "cmdParent.exe",
        "FilePath": "C:\\WINDOWS\\SysWOW64\\boo3\\qwerty",
        "IpAddress": "",
        "Url": "",
        "IoaDefinitionId": "b20af1d2-5990-4672-87f1-acc2a8ff7725",
        "UserName": "",
        "AlertPart": 0,
        "FullId": "da637370718981685665_16349121:R4xEdgAvDb2LQl3BgHoA3NYqKmRSiIAG7dpxAJCYZhY=",
        "LastProcessedTimeUtc": "2020-09-30T14:11:44.0779765Z",
        "ThreatCategory": "",
        "ThreatFamily": "",
        "ThreatName": "",
        "RemediationAction": "",
        "RemediationIsSuccess": null,
        "Source": "EDR",
        "Md5": "854b85cbff2752fcb88606bca76f83c6",
        "Sha256": "",
        "WasExecutingWhileDetected": null,
        "UserDomain": "",
        "LogOnUsers": "",
        "MachineDomain": "domain.com",
        "MachineName": "mymachine1",
        "InternalIPv4List": "",
        "InternalIPv6List": "",
        "FileHash": "aabbccddee1122334455aabbccddee1122334455",
        "DeviceID": "deadbeef000040830ee54503926f556dcaf82bb0",
        "MachineGroup": "",
        "Description": "Test Alert",
        "DeviceCreatedMachineTags": "",
        "CloudCreatedMachineTags": "",
        "CommandLine": "",
        "IncidentLinkToWDATP": "https://securitycenter.windows.com/incidents/byalert?alertId=da637370718981685665_16349121&source=SIEM",
        "ReportID": 1053729833,
        "LinkToMTP": "https://security.microsoft.com/alert/da637370718981685665_16349121",
        "IncidentLinkToMTP": "https://security.microsoft.com/incidents/byalert?alertId=da637370718981685665_16349121&source=SIEM",
        "ExternalId": "31DD0A845DDA4059FDEDE031014645350AECABD3",
        "IocUniqueId": "R4xEdgAvDb2LQl3BgHoA3NYqKmRSiIAG7dpxAJCYZhY="
}
]
```

## <a name="code-examples"></a><span data-ttu-id="e9360-207">Exemples de code</span><span class="sxs-lookup"><span data-stu-id="e9360-207">Code examples</span></span>
### <a name="get-access-token"></a><span data-ttu-id="e9360-208">Obtenir un jeton d'accès</span><span class="sxs-lookup"><span data-stu-id="e9360-208">Get access token</span></span>
<span data-ttu-id="e9360-209">Les exemples de code suivants montrent comment obtenir un jeton d'accès pour appeler l'API SIEM de Microsoft Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="e9360-209">The following code examples demonstrate how to obtain an access token for calling the Microsoft Defender for Endpoint SIEM API.</span></span>

```csharp
AuthenticationContext context = new AuthenticationContext(string.Format("https://login.microsoftonline.com/{0}", tenantId));
ClientCredential clientCredentials = new ClientCredential(clientId, clientSecret);
AuthenticationResult authenticationResult = context.AcquireTokenAsync(detectionsResource, clientCredentials).GetAwaiter().GetResult();
```

```PowerShell
#Get current working directory
$scriptDir = Split-Path -Path $MyInvocation.MyCommand.Definition -Parent

#Paste below your Tenant ID, App ID and App Secret (App key).
$tenantId = '' ### Paste your tenant ID here
$appId = '' ### Paste your Application ID here
$appSecret = '' ### Paste your Application secret here

$resourceAppIdUri = 'https://graph.windows.net'
$oAuthUri = "https://login.microsoftonline.com/$tenantId/oauth2/token"
$authBody = [Ordered] @{
    resource = "$resourceAppIdUri"
    client_id = "$appId"
    client_secret = "$appSecret"
    grant_type = 'client_credentials'
}

#call API
$authResponse = Invoke-RestMethod -Method Post -Uri $oAuthUri -Body $authBody -ErrorAction Stop
$authResponse
Out-File -FilePath "$scriptDir\LatestSIEM-token.txt" -InputObject $authResponse.access_token
```

```Bash
tenantId='' ### Paste your tenant ID here
appId='' ### Paste your Application ID here
appSecret='' ### Paste your Application secret here
resourceAppIdUri='https://graph.windows.net'
oAuthUri="https://login.microsoftonline.com/$tenantId/oauth2/token"
scriptDir=$(pwd)

apiResponse=$(curl -s X POST "$oAuthUri" -d "resource=$resourceAppIdUri&client_id=$appId&client_secret=$appSecret&\
        grant_type=client_credentials" | cut -d "{" -f2 | cut -d "}" -f1)
IFS=","
apiResponseArr=($apiResponse)
IFS=":"
tokenArr=(${apiResponseArr[6]})
echo ${tokenArr[1]} | cut -d "\"" -f2 | cut -d "\"" -f1 >> $scriptDir/LatestSIEM-token.txt
```

### <a name="use-token-to-connect-to-the-detections-endpoint"></a><span data-ttu-id="e9360-210">Utiliser un jeton pour se connecter au point de terminaison des détections</span><span class="sxs-lookup"><span data-stu-id="e9360-210">Use token to connect to the detections endpoint</span></span>
<span data-ttu-id="e9360-211">Les exemples de code suivants montrent comment utiliser un jeton d'accès pour appeler l'API SIEM Defender for Endpoint pour obtenir des alertes.</span><span class="sxs-lookup"><span data-stu-id="e9360-211">The following code examples demonstrate how to use an access token for calling the Defender for Endpoint SIEM API to get alerts.</span></span>

```csharp
HttpClient httpClient = new HttpClient();
httpClient.DefaultRequestHeaders.Authorization = new AuthenticationHeaderValue(authenticationResult.AccessTokenType, authenticationResult.AccessToken);
HttpResponseMessage response = httpClient.GetAsync("https://wdatp-alertexporter-eu.windows.com/api/alert").GetAwaiter().GetResult();
string detectionsJson = response.Content.ReadAsStringAsync().Result;
Console.WriteLine("Got detections list: {0}", detectionsJson);
```

```PowerShell
#Get current working directory
$scriptDir = Split-Path -Path $MyInvocation.MyCommand.Definition -Parent

#run the script Get-Token.ps1  - make sure you are running this script from the same folder of Get-SIEMToken.ps1
$token = Get-Content "$scriptDir\LatestSIEM-token.txt"

#Get Alert from the last xx hours 200 in this example. Make sure you have alerts in that time frame.
$dateTime = (Get-Date).ToUniversalTime().AddHours(-200).ToString("o")

#test SIEM API
$url = 'https://wdatp-alertexporter-us.windows.com/api/alerts?limit=20&sinceTimeUtc=2020-01-01T00:00:00.000'

#Set the WebRequest headers
$headers = @{ 
    'Content-Type' = 'application/json'
    Accept = 'application/json'
    Authorization = "Bearer $token" 
}

#Send the webrequest and get the results. 
$response = Invoke-WebRequest -Method Get -Uri $url -Headers $headers -ErrorAction Stop
$response
Write-Host

#Extract the alerts from the results.  This works for SIEM API:
$alerts =  $response.Content | ConvertFrom-Json | ConvertTo-Json

#Get string with the execution time. We concatenate that string to the output file to avoid overwrite the file
$dateTimeForFileName = Get-Date -Format o | foreach {$_ -replace ":", "."}    

#Save the result as json and as csv
$outputJsonPath = "$scriptDir\Latest Alerts $dateTimeForFileName.json"     
$outputCsvPath = "$scriptDir\Latest Alerts $dateTimeForFileName.csv"

Out-File -FilePath $outputJsonPath -InputObject $alerts
Get-Content -Path $outputJsonPath -Raw | ConvertFrom-Json | Select-Object -ExpandProperty value | Export-CSV $outputCsvPath -NoTypeInformation
```

```Bash
#Get current working directory
scriptDir=$(pwd)

#get the token
token=$(<$scriptDir/LatestSIEM-token.txt)

#test the SIEM API, get alerts since 1/1/2020
url='https://wdatp-alertexporter-us.windows.com/api/alerts?limit=20&sinceTimeUtc=2020-01-01T00:00:00.000'

#send web requst to API and echo JSON content
apiResponse=$(curl -s X GET "$url" -H "Content-Type: application/json" -H "Accept: application/json"\
         -H "Authorization: Bearer $token" | cut -d "[" -f2 | cut -d "]" -f1)
echo "If you see Alert info in JSON format, congratulations you accessed the MDATP SIEM API!"
echo
echo $apiResponse
```

## <a name="error-codes"></a><span data-ttu-id="e9360-212">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="e9360-212">Error codes</span></span>
<span data-ttu-id="e9360-213">L'API REST Microsoft Defender pour point de terminaison renvoie les codes d'erreur suivants causés par une demande non valide.</span><span class="sxs-lookup"><span data-stu-id="e9360-213">The Microsoft Defender for Endpoint REST API returns the following error codes caused by an invalid request.</span></span>

<span data-ttu-id="e9360-214">Code d’erreur HTTP</span><span class="sxs-lookup"><span data-stu-id="e9360-214">HTTP error code</span></span> | <span data-ttu-id="e9360-215">Description</span><span class="sxs-lookup"><span data-stu-id="e9360-215">Description</span></span>
:---|:---
<span data-ttu-id="e9360-216">401</span><span class="sxs-lookup"><span data-stu-id="e9360-216">401</span></span> | <span data-ttu-id="e9360-217">Demande incorrecte ou jeton non valide.</span><span class="sxs-lookup"><span data-stu-id="e9360-217">Malformed request or invalid token.</span></span>
<span data-ttu-id="e9360-218">403</span><span class="sxs-lookup"><span data-stu-id="e9360-218">403</span></span> | <span data-ttu-id="e9360-219">Exception non autorisée : l'un des domaines n'est pas géré par l'administrateur client ou l'état du client est supprimé.</span><span class="sxs-lookup"><span data-stu-id="e9360-219">Unauthorized exception - any of the domains is not managed by the tenant administrator or tenant state is deleted.</span></span>
<span data-ttu-id="e9360-220">500</span><span class="sxs-lookup"><span data-stu-id="e9360-220">500</span></span> | <span data-ttu-id="e9360-221">Erreur dans le service.</span><span class="sxs-lookup"><span data-stu-id="e9360-221">Error in the service.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e9360-222">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e9360-222">Related topics</span></span>
- [<span data-ttu-id="e9360-223">Activer l'intégration SIEM dans Microsoft Defender pour endpoint</span><span class="sxs-lookup"><span data-stu-id="e9360-223">Enable SIEM integration in Microsoft Defender for Endpoint</span></span>](enable-siem-integration.md)
- [<span data-ttu-id="e9360-224">Configurer ArcSight pour tirer Microsoft Defender pour les détections de points de terminaison</span><span class="sxs-lookup"><span data-stu-id="e9360-224">Configure ArcSight to pull Microsoft Defender for Endpoint detections</span></span>](configure-arcsight.md)
- [<span data-ttu-id="e9360-225">Tirer les détections vers vos outils SIEM</span><span class="sxs-lookup"><span data-stu-id="e9360-225">Pull detections to your SIEM tools</span></span>](configure-siem.md)
- [<span data-ttu-id="e9360-226">Champs Microsoft Defender pour la détection des points de terminaison</span><span class="sxs-lookup"><span data-stu-id="e9360-226">Microsoft Defender for Endpoint Detection fields</span></span>](api-portal-mapping.md)
- [<span data-ttu-id="e9360-227">Résoudre des problèmes d’intégration de l’outil SIEM</span><span class="sxs-lookup"><span data-stu-id="e9360-227">Troubleshoot SIEM tool integration issues</span></span>](troubleshoot-siem.md)
