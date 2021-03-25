---
title: API Microsoft Defender pour point de terminaison prise en charge
ms.reviewer: ''
description: Découvrez les entités Microsoft Defender for Endpoint spécifiques pris en charge dans laquelle vous pouvez créer des appels d’API.
keywords: api, api pris en charge, acteur, alertes, appareil, utilisateur, domaine, ip, fichier, requêtes avancées, recherche avancée
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
ms.openlocfilehash: 77491620f7efa88f8ab249c2b76cd2532ba679dd
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51198320"
---
# <a name="supported-microsoft-defender-for-endpoint-apis"></a><span data-ttu-id="ba0f2-104">API Microsoft Defender pour point de terminaison prise en charge</span><span class="sxs-lookup"><span data-stu-id="ba0f2-104">Supported Microsoft Defender for Endpoint APIs</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="ba0f2-105">**S’applique à :** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span><span class="sxs-lookup"><span data-stu-id="ba0f2-105">**Applies to:** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span></span>

- <span data-ttu-id="ba0f2-106">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="ba0f2-106">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="ba0f2-107">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="ba0f2-107">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

## <a name="endpoint-uri-and-versioning"></a><span data-ttu-id="ba0f2-108">URI et version des points de terminaison</span><span class="sxs-lookup"><span data-stu-id="ba0f2-108">Endpoint URI and versioning</span></span>

### <a name="endpoint-uri"></a><span data-ttu-id="ba0f2-109">URI du point de terminaison :            </span><span class="sxs-lookup"><span data-stu-id="ba0f2-109">Endpoint URI:</span></span>

> <span data-ttu-id="ba0f2-110">L’URI de base du service est : https://api.securitycenter.microsoft.com</span><span class="sxs-lookup"><span data-stu-id="ba0f2-110">The service base URI is: https://api.securitycenter.microsoft.com</span></span>
> 
> <span data-ttu-id="ba0f2-111">Les requêtes basées sur OData ont le préfixe « /api ».</span><span class="sxs-lookup"><span data-stu-id="ba0f2-111">The queries based OData have the '/api' prefix.</span></span> <span data-ttu-id="ba0f2-112">Par exemple, pour obtenir des alertes, vous pouvez envoyer une requête GET à https://api.securitycenter.microsoft.com/api/alerts</span><span class="sxs-lookup"><span data-stu-id="ba0f2-112">For example, to get Alerts you can send GET request to https://api.securitycenter.microsoft.com/api/alerts</span></span>

### <a name="versioning"></a><span data-ttu-id="ba0f2-113">Contrôle de version :</span><span class="sxs-lookup"><span data-stu-id="ba0f2-113">Versioning:</span></span>

> <span data-ttu-id="ba0f2-114">L’API prend en charge le gestion des versions.</span><span class="sxs-lookup"><span data-stu-id="ba0f2-114">The API supports versioning.</span></span>
> 
> <span data-ttu-id="ba0f2-115">La version actuelle **est V1.0**.</span><span class="sxs-lookup"><span data-stu-id="ba0f2-115">The current version is **V1.0**.</span></span>
> 
> <span data-ttu-id="ba0f2-116">Pour utiliser une version spécifique, utilisez ce format : `https://api.securitycenter.microsoft.com/api/{Version}` .</span><span class="sxs-lookup"><span data-stu-id="ba0f2-116">To use a specific version, use this format: `https://api.securitycenter.microsoft.com/api/{Version}`.</span></span> <span data-ttu-id="ba0f2-117">Par exemple : `https://api.securitycenter.microsoft.com/api/v1.0/alerts`</span><span class="sxs-lookup"><span data-stu-id="ba0f2-117">For example: `https://api.securitycenter.microsoft.com/api/v1.0/alerts`</span></span>
> 
> <span data-ttu-id="ba0f2-118">Si vous ne spécifiez aucune version (par exemple), vous allez obtenir https://api.securitycenter.microsoft.com/api/alerts la dernière version.</span><span class="sxs-lookup"><span data-stu-id="ba0f2-118">If you don't specify any version (e.g. https://api.securitycenter.microsoft.com/api/alerts ) you will get to the latest version.</span></span>


[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]


<span data-ttu-id="ba0f2-119">En savoir plus sur les entités individuelles pris en charge dans laquelle vous pouvez exécuter des appels d’API et des détails tels que les valeurs de requête HTTP, les en-têtes de requête et les réponses attendues.</span><span class="sxs-lookup"><span data-stu-id="ba0f2-119">Learn more about the individual supported entities where you can run API calls to and details such as HTTP request values, request headers and expected responses.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ba0f2-120">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="ba0f2-120">In this section</span></span>

<span data-ttu-id="ba0f2-121">Rubrique</span><span class="sxs-lookup"><span data-stu-id="ba0f2-121">Topic</span></span> | <span data-ttu-id="ba0f2-122">Description</span><span class="sxs-lookup"><span data-stu-id="ba0f2-122">Description</span></span>
:---|:---
<span data-ttu-id="ba0f2-123">Recherche avancée</span><span class="sxs-lookup"><span data-stu-id="ba0f2-123">Advanced Hunting</span></span> | <span data-ttu-id="ba0f2-124">Exécuter des requêtes à partir de l’API.</span><span class="sxs-lookup"><span data-stu-id="ba0f2-124">Run queries from API.</span></span>
<span data-ttu-id="ba0f2-125">Alertes</span><span class="sxs-lookup"><span data-stu-id="ba0f2-125">Alerts</span></span> | <span data-ttu-id="ba0f2-126">Exécutez des appels d’API tels que obtenir des alertes, créer une alerte, mettre à jour une alerte, etc.</span><span class="sxs-lookup"><span data-stu-id="ba0f2-126">Run API calls such as get alerts, create alert, update alert and more.</span></span>
<span data-ttu-id="ba0f2-127">Domaines</span><span class="sxs-lookup"><span data-stu-id="ba0f2-127">Domains</span></span> | <span data-ttu-id="ba0f2-128">Exécutez des appels d’API tels que l’get domain-related devices, domain statistics and more.</span><span class="sxs-lookup"><span data-stu-id="ba0f2-128">Run API calls such as get domain-related devices, domain statistics and more.</span></span>
<span data-ttu-id="ba0f2-129">Fichiers</span><span class="sxs-lookup"><span data-stu-id="ba0f2-129">Files</span></span> | <span data-ttu-id="ba0f2-130">Exécutez des appels d’API tels que obtenir des informations sur les fichiers, des alertes liées aux fichiers, des périphériques liés aux fichiers et des statistiques sur les fichiers.</span><span class="sxs-lookup"><span data-stu-id="ba0f2-130">Run API calls such as get file information, file related alerts, file related devices, and file statistics.</span></span>
<span data-ttu-id="ba0f2-131">IPs</span><span class="sxs-lookup"><span data-stu-id="ba0f2-131">IPs</span></span> | <span data-ttu-id="ba0f2-132">Exécutez des appels d’API tels que l’get IP-related alerts and get IP statistics.</span><span class="sxs-lookup"><span data-stu-id="ba0f2-132">Run API calls such as get IP-related alerts and get IP statistics.</span></span>
<span data-ttu-id="ba0f2-133">Ordinateurs</span><span class="sxs-lookup"><span data-stu-id="ba0f2-133">Machines</span></span> | <span data-ttu-id="ba0f2-134">Exécutez des appels d’API tels que obtenir des appareils, obtenir des appareils par ID, des informations sur les utilisateurs connectés, modifier des balises, etc.</span><span class="sxs-lookup"><span data-stu-id="ba0f2-134">Run API calls such as get devices, get devices by ID, information about logged on users, edit tags and more.</span></span>
<span data-ttu-id="ba0f2-135">Actions de l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="ba0f2-135">Machine Actions</span></span> | <span data-ttu-id="ba0f2-136">Exécutez un appel d’API tel que Isolation, Exécuter une analyse antivirus et bien plus encore.</span><span class="sxs-lookup"><span data-stu-id="ba0f2-136">Run API call such as Isolation, Run anti-virus scan and more.</span></span>
<span data-ttu-id="ba0f2-137">Indicateurs</span><span class="sxs-lookup"><span data-stu-id="ba0f2-137">Indicators</span></span> | <span data-ttu-id="ba0f2-138">Exécutez un appel d’API tel que créer un indicateur, obtenir des indicateurs et supprimer des indicateurs.</span><span class="sxs-lookup"><span data-stu-id="ba0f2-138">Run API call such as create Indicator, get Indicators and delete Indicators.</span></span>
<span data-ttu-id="ba0f2-139">Utilisateurs</span><span class="sxs-lookup"><span data-stu-id="ba0f2-139">Users</span></span> | <span data-ttu-id="ba0f2-140">Exécutez des appels d’API tels que l’accès à des alertes liées à l’utilisateur et à des appareils liés à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ba0f2-140">Run API calls such as get user-related alerts and user-related devices.</span></span>
<span data-ttu-id="ba0f2-141">Niveau</span><span class="sxs-lookup"><span data-stu-id="ba0f2-141">Score</span></span> | <span data-ttu-id="ba0f2-142">Exécutez des appels d’API tels que obtenir le score d’exposition ou obtenir le score de sécurité de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ba0f2-142">Run API calls such as get exposure score or get device secure score.</span></span>
<span data-ttu-id="ba0f2-143">Logiciels</span><span class="sxs-lookup"><span data-stu-id="ba0f2-143">Software</span></span> | <span data-ttu-id="ba0f2-144">Exécutez des appels d’API tels que des vulnérabilités de liste par logiciel.</span><span class="sxs-lookup"><span data-stu-id="ba0f2-144">Run API calls such as list vulnerabilities by software.</span></span>
<span data-ttu-id="ba0f2-145">Vulnérabilité</span><span class="sxs-lookup"><span data-stu-id="ba0f2-145">Vulnerability</span></span> | <span data-ttu-id="ba0f2-146">Exécutez des appels d’API tels que des périphériques de liste par vulnérabilité.</span><span class="sxs-lookup"><span data-stu-id="ba0f2-146">Run API calls such as list devices by vulnerability.</span></span>
<span data-ttu-id="ba0f2-147">Recommandation</span><span class="sxs-lookup"><span data-stu-id="ba0f2-147">Recommendation</span></span> | <span data-ttu-id="ba0f2-148">Exécutez des appels d’API tels que Obtenir une recommandation par ID.</span><span class="sxs-lookup"><span data-stu-id="ba0f2-148">Run API calls such as Get recommendation by ID.</span></span>

## <a name="see-also"></a><span data-ttu-id="ba0f2-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ba0f2-149">See also</span></span>
- [<span data-ttu-id="ba0f2-150">API Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="ba0f2-150">Microsoft Defender for Endpoint APIs</span></span>](apis-intro.md)
