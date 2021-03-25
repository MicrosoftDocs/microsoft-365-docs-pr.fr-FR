---
title: Obtenir le score de sécurité de l’appareil
description: Récupère le score de sécurité de l’appareil de l’organisation.
keywords: api, api de graphique, api pris en charge, obtenir, alertes, récent
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
author: levinec
ms.author: ellevin
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.technology: mde
ms.openlocfilehash: 921334c937e3f211b032a5d24d4244d9a6fb3d61
ms.sourcegitcommit: 2a708650b7e30a53d10a2fe3164c6ed5ea37d868
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51166581"
---
# <a name="get-device-secure-score"></a><span data-ttu-id="af5bf-104">Obtenir le score de sécurité de l’appareil</span><span class="sxs-lookup"><span data-stu-id="af5bf-104">Get device secure score</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="af5bf-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="af5bf-105">**Applies to:**</span></span>
- [<span data-ttu-id="af5bf-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="af5bf-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="af5bf-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="af5bf-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

<span data-ttu-id="af5bf-108">**S’applique à :** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span><span class="sxs-lookup"><span data-stu-id="af5bf-108">**Applies to:** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span></span>

- <span data-ttu-id="af5bf-109">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="af5bf-109">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="af5bf-110">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="af5bf-110">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]


<span data-ttu-id="af5bf-111">Récupère votre [score de sécurité Microsoft pour les appareils.](tvm-microsoft-secure-score-devices.md)</span><span class="sxs-lookup"><span data-stu-id="af5bf-111">Retrieves your [Microsoft Secure Score for Devices](tvm-microsoft-secure-score-devices.md).</span></span> <span data-ttu-id="af5bf-112">Un niveau de sécurité Microsoft plus élevé pour les appareils signifie que vos points de terminaison sont plus résistants aux attaques contre les menaces de cybersécurité.</span><span class="sxs-lookup"><span data-stu-id="af5bf-112">A higher Microsoft Secure Score for Devices means your endpoints are more resilient from cybersecurity threat attacks.</span></span> 

## <a name="permissions"></a><span data-ttu-id="af5bf-113">Autorisations</span><span class="sxs-lookup"><span data-stu-id="af5bf-113">Permissions</span></span>

<span data-ttu-id="af5bf-114">L’une des autorisations suivantes est nécessaire pour appeler cette API.</span><span class="sxs-lookup"><span data-stu-id="af5bf-114">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="af5bf-115">Pour plus d’informations, notamment sur le choix des autorisations, voir [Utiliser Microsoft Defender pour les API de point](apis-intro.md) de terminaison pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="af5bf-115">To learn more, including how to choose permissions, see [Use Microsoft Defender for Endpoint APIs](apis-intro.md) for details.</span></span>

<span data-ttu-id="af5bf-116">Type d’autorisation</span><span class="sxs-lookup"><span data-stu-id="af5bf-116">Permission type</span></span> |   <span data-ttu-id="af5bf-117">Autorisation</span><span class="sxs-lookup"><span data-stu-id="af5bf-117">Permission</span></span>  |   <span data-ttu-id="af5bf-118">Nom d’affichage de l’autorisation</span><span class="sxs-lookup"><span data-stu-id="af5bf-118">Permission display name</span></span>
:---|:---|:---
<span data-ttu-id="af5bf-119">Application</span><span class="sxs-lookup"><span data-stu-id="af5bf-119">Application</span></span> |   <span data-ttu-id="af5bf-120">Score.Read.Alll</span><span class="sxs-lookup"><span data-stu-id="af5bf-120">Score.Read.Alll</span></span> |   <span data-ttu-id="af5bf-121">« Lire le score de gestion des menaces et des vulnérabilités »</span><span class="sxs-lookup"><span data-stu-id="af5bf-121">'Read Threat and Vulnerability Management score'</span></span>
<span data-ttu-id="af5bf-122">Déléguée (compte professionnel ou scolaire)</span><span class="sxs-lookup"><span data-stu-id="af5bf-122">Delegated (work or school account)</span></span> | <span data-ttu-id="af5bf-123">Score.Read</span><span class="sxs-lookup"><span data-stu-id="af5bf-123">Score.Read</span></span> | <span data-ttu-id="af5bf-124">« Lire le score de gestion des menaces et des vulnérabilités »</span><span class="sxs-lookup"><span data-stu-id="af5bf-124">'Read Threat and Vulnerability Management score'</span></span>

## <a name="http-request"></a><span data-ttu-id="af5bf-125">Requête HTTP</span><span class="sxs-lookup"><span data-stu-id="af5bf-125">HTTP request</span></span>

```
GET /api/configurationScore
```

## <a name="request-headers"></a><span data-ttu-id="af5bf-126">En-têtes de demande</span><span class="sxs-lookup"><span data-stu-id="af5bf-126">Request headers</span></span>

<span data-ttu-id="af5bf-127">Nom</span><span class="sxs-lookup"><span data-stu-id="af5bf-127">Name</span></span> | <span data-ttu-id="af5bf-128">Type</span><span class="sxs-lookup"><span data-stu-id="af5bf-128">Type</span></span> | <span data-ttu-id="af5bf-129">Description</span><span class="sxs-lookup"><span data-stu-id="af5bf-129">Description</span></span>
:---|:---|:---
<span data-ttu-id="af5bf-130">Autorisation</span><span class="sxs-lookup"><span data-stu-id="af5bf-130">Authorization</span></span> | <span data-ttu-id="af5bf-131">Chaîne</span><span class="sxs-lookup"><span data-stu-id="af5bf-131">String</span></span> | <span data-ttu-id="af5bf-132">Porteur {token}.</span><span class="sxs-lookup"><span data-stu-id="af5bf-132">Bearer {token}.</span></span> <span data-ttu-id="af5bf-133">**Obligatoire**.</span><span class="sxs-lookup"><span data-stu-id="af5bf-133">**Required**.</span></span>

## <a name="request-body"></a><span data-ttu-id="af5bf-134">Corps de la demande</span><span class="sxs-lookup"><span data-stu-id="af5bf-134">Request body</span></span>

<span data-ttu-id="af5bf-135">Vide</span><span class="sxs-lookup"><span data-stu-id="af5bf-135">Empty</span></span>

## <a name="response"></a><span data-ttu-id="af5bf-136">Réponse</span><span class="sxs-lookup"><span data-stu-id="af5bf-136">Response</span></span>

<span data-ttu-id="af5bf-137">Si elle réussit, cette méthode renvoie 200 OK, avec les données de score sécurisé de l’appareil dans le corps de la réponse.</span><span class="sxs-lookup"><span data-stu-id="af5bf-137">If successful, this method returns 200 OK, with the device secure score data in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="af5bf-138">Exemple</span><span class="sxs-lookup"><span data-stu-id="af5bf-138">Example</span></span>

### <a name="request"></a><span data-ttu-id="af5bf-139">Demande</span><span class="sxs-lookup"><span data-stu-id="af5bf-139">Request</span></span>

<span data-ttu-id="af5bf-140">Voici un exemple de demande.</span><span class="sxs-lookup"><span data-stu-id="af5bf-140">Here is an example of the request.</span></span>

```http
GET https://api.securitycenter.microsoft.com/api/configurationScore
```

### <a name="response"></a><span data-ttu-id="af5bf-141">Réponse</span><span class="sxs-lookup"><span data-stu-id="af5bf-141">Response</span></span>

<span data-ttu-id="af5bf-142">Voici un exemple de réponse.</span><span class="sxs-lookup"><span data-stu-id="af5bf-142">Here is an example of the response.</span></span>

>[!NOTE]
><span data-ttu-id="af5bf-143">La liste de réponses présentée ici peut être tronquée à des raisons de concision.</span><span class="sxs-lookup"><span data-stu-id="af5bf-143">The response list shown here may be truncated for brevity.</span></span> 

```json
{
    "@odata.context": "https://api.securitycenter.microsoft.com/api/$metadata#ConfigurationScore/$entity",
    "time": "2019-12-03T09:15:58.1665846Z",
    "score": 340
}
```

## <a name="see-also"></a><span data-ttu-id="af5bf-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="af5bf-144">See also</span></span>

- [<span data-ttu-id="af5bf-145">Requêtes OData avec Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="af5bf-145">OData queries with Microsoft Defender for Endpoint</span></span>](exposed-apis-odata-samples.md)
