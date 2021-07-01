---
title: API prises en charge Microsoft Defender pour point de terminaison
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
MS.technology: mde
ms.custom: api
ms.openlocfilehash: 3f0f7a2b6a10c3469f0689419934fd8d19070999
ms.sourcegitcommit: 48195345b21b409b175d68acdc25d9f2fc4fc5f1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "53228626"
---
# <a name="supported-microsoft-defender-for-endpoint-apis"></a><span data-ttu-id="177eb-104">API prises en charge Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="177eb-104">Supported Microsoft Defender for Endpoint APIs</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="177eb-105">**S’applique à :** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span><span class="sxs-lookup"><span data-stu-id="177eb-105">**Applies to:** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span></span>

- <span data-ttu-id="177eb-106">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="177eb-106">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="177eb-107">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="177eb-107">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

## <a name="endpoint-uri-and-versioning"></a><span data-ttu-id="177eb-108">URI et version des points de terminaison</span><span class="sxs-lookup"><span data-stu-id="177eb-108">Endpoint URI and versioning</span></span>

### <a name="endpoint-uri"></a><span data-ttu-id="177eb-109">URI de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="177eb-109">Endpoint URI</span></span>

> <span data-ttu-id="177eb-110">L’URI de base du service est : [https://api.securitycenter.microsoft.com](https://api.securitycenter.microsoft.com)</span><span class="sxs-lookup"><span data-stu-id="177eb-110">The service base URI is: [https://api.securitycenter.microsoft.com](https://api.securitycenter.microsoft.com)</span></span>
>
> <span data-ttu-id="177eb-111">Les requêtes basées sur OData ont le préfixe « /api ».</span><span class="sxs-lookup"><span data-stu-id="177eb-111">The queries based OData have the '/api' prefix.</span></span> <span data-ttu-id="177eb-112">Par exemple, pour obtenir des alertes, vous pouvez envoyer une requête GET à [https://api.securitycenter.microsoft.com/api/alerts](https://api.securitycenter.microsoft.com/api/alerts)</span><span class="sxs-lookup"><span data-stu-id="177eb-112">For example, to get Alerts you can send GET request to [https://api.securitycenter.microsoft.com/api/alerts](https://api.securitycenter.microsoft.com/api/alerts)</span></span>

### <a name="versioning"></a><span data-ttu-id="177eb-113">Gestion des versions</span><span class="sxs-lookup"><span data-stu-id="177eb-113">Versioning</span></span>

> <span data-ttu-id="177eb-114">L’API prend en charge le gestion des versions.</span><span class="sxs-lookup"><span data-stu-id="177eb-114">The API supports versioning.</span></span>
>
> <span data-ttu-id="177eb-115">La version actuelle **est V1.0**.</span><span class="sxs-lookup"><span data-stu-id="177eb-115">The current version is **V1.0**.</span></span>
>
> <span data-ttu-id="177eb-116">Pour utiliser une version spécifique, utilisez ce format : `https://api.securitycenter.microsoft.com/api/{Version}` .</span><span class="sxs-lookup"><span data-stu-id="177eb-116">To use a specific version, use this format: `https://api.securitycenter.microsoft.com/api/{Version}`.</span></span> <span data-ttu-id="177eb-117">Par exemple : `https://api.securitycenter.microsoft.com/api/v1.0/alerts`</span><span class="sxs-lookup"><span data-stu-id="177eb-117">For example: `https://api.securitycenter.microsoft.com/api/v1.0/alerts`</span></span>
>
> <span data-ttu-id="177eb-118">Si vous ne spécifiez aucune version (par exemple), vous allez obtenir `https://api.securitycenter.microsoft.com/api/alerts` la dernière version.</span><span class="sxs-lookup"><span data-stu-id="177eb-118">If you don't specify any version (e.g. `https://api.securitycenter.microsoft.com/api/alerts`) you will get to the latest version.</span></span>

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]

<span data-ttu-id="177eb-119">En savoir plus sur les entités individuelles pris en charge dans laquelle vous pouvez exécuter des appels d’API et des détails tels que les valeurs de requête HTTP, les en-têtes de requête et les réponses attendues.</span><span class="sxs-lookup"><span data-stu-id="177eb-119">Learn more about the individual supported entities where you can run API calls to and details such as HTTP request values, request headers and expected responses.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="177eb-120">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="177eb-120">In this section</span></span>

<span data-ttu-id="177eb-121">Rubrique</span><span class="sxs-lookup"><span data-stu-id="177eb-121">Topic</span></span> | <span data-ttu-id="177eb-122">Description</span><span class="sxs-lookup"><span data-stu-id="177eb-122">Description</span></span>
:---|:---
[<span data-ttu-id="177eb-123">Repérage avancé</span><span class="sxs-lookup"><span data-stu-id="177eb-123">Advanced Hunting</span></span>](run-advanced-query-api.md) | <span data-ttu-id="177eb-124">Exécuter des requêtes à partir de l’API.</span><span class="sxs-lookup"><span data-stu-id="177eb-124">Run queries from API.</span></span>
[<span data-ttu-id="177eb-125">Méthodes et propriétés de l’alerte</span><span class="sxs-lookup"><span data-stu-id="177eb-125">Alert methods and properties</span></span>](alerts.md) | <span data-ttu-id="177eb-126">Exécutez des appels d’API tels \- que obtenir des alertes, créer une alerte, mettre à jour une alerte, etc.</span><span class="sxs-lookup"><span data-stu-id="177eb-126">Run API calls such as \- get alerts, create alert, update alert and more.</span></span>
[<span data-ttu-id="177eb-127">Exporter les méthodes et propriétés d’évaluation par appareil</span><span class="sxs-lookup"><span data-stu-id="177eb-127">Export assessment methods and properties per device</span></span>](get-assessment-methods-properties.md) | <span data-ttu-id="177eb-128">Exécutez des appels d’API pour collecter des évaluations des vulnérabilités par appareil, telles que : exporter l’évaluation de la configuration sécurisée, exporter l’évaluation de l’inventaire logiciel, exporter l’évaluation des vulnérabilités logicielles et exporter delta l’évaluation des vulnérabilités \- logicielles.</span><span class="sxs-lookup"><span data-stu-id="177eb-128">Run API calls to gather vulnerability assessments on a per-device basis, such as: \- export secure configuration assessment, export software inventory assessment,  export software vulnerabilities assessment, and delta export software vulnerabilities assessment.</span></span>
[<span data-ttu-id="177eb-129">Méthodes et propriétés d’investigation automatisée</span><span class="sxs-lookup"><span data-stu-id="177eb-129">Automated Investigation methods and properties</span></span>](investigation.md) | <span data-ttu-id="177eb-130">Exécutez des appels d’API tels \- que obtenir la collection d’examens.</span><span class="sxs-lookup"><span data-stu-id="177eb-130">Run API calls such as \- get collection of Investigation.</span></span>
[<span data-ttu-id="177eb-131">Obtenir des alertes liées au domaine</span><span class="sxs-lookup"><span data-stu-id="177eb-131">Get domain related alerts</span></span>](get-domain-related-alerts.md) | <span data-ttu-id="177eb-132">Exécutez des appels d’API tels \- que l’get domain-related devices, domain statistics and more.</span><span class="sxs-lookup"><span data-stu-id="177eb-132">Run API calls such as \- get domain-related devices, domain statistics and more.</span></span>
[<span data-ttu-id="177eb-133">Soumettre des méthodes et propriétés</span><span class="sxs-lookup"><span data-stu-id="177eb-133">File methods and properties</span></span>](files.md) | <span data-ttu-id="177eb-134">Exécutez des appels d’API tels que obtenir des informations sur les fichiers, des alertes liées aux fichiers, des périphériques liés \- aux fichiers et des statistiques sur les fichiers.</span><span class="sxs-lookup"><span data-stu-id="177eb-134">Run API calls such as \- get file information, file related alerts, file related devices, and file statistics.</span></span>
[<span data-ttu-id="177eb-135">Méthodes et propriétés des indicateurs</span><span class="sxs-lookup"><span data-stu-id="177eb-135">Indicators methods and properties</span></span>](ti-indicator.md) | <span data-ttu-id="177eb-136">Exécutez un appel d’API tel que obtenir des indicateurs, créer un \- indicateur et supprimer des indicateurs.</span><span class="sxs-lookup"><span data-stu-id="177eb-136">Run API call such as \- get Indicators, create Indicator, and delete Indicators.</span></span>
[<span data-ttu-id="177eb-137">Obtenir des alertes liées à l’IP</span><span class="sxs-lookup"><span data-stu-id="177eb-137">Get IP related alerts</span></span>](get-ip-related-alerts.md) | <span data-ttu-id="177eb-138">Exécutez des appels d’API tels \- que l’get IP-related alerts and get IP statistics.</span><span class="sxs-lookup"><span data-stu-id="177eb-138">Run API calls such as \- get IP-related alerts and get IP statistics.</span></span>
[<span data-ttu-id="177eb-139">Méthodes et propriétés de l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="177eb-139">Machine methods and properties</span></span>](machine.md) | <span data-ttu-id="177eb-140">Exécutez des appels d’API tels que obtenir des appareils, obtenir des appareils par ID, des informations sur les utilisateurs connectés, modifier des \- balises, etc.</span><span class="sxs-lookup"><span data-stu-id="177eb-140">Run API calls such as \- get devices, get devices by ID, information about logged on users, edit tags and more.</span></span>
[<span data-ttu-id="177eb-141">Méthodes et propriétés de l’action de l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="177eb-141">Machine Action methods and properties</span></span>](machineaction.md) | <span data-ttu-id="177eb-142">Exécutez un appel d’API tel \- que Isolation, Exécuter une analyse antivirus et bien plus encore.</span><span class="sxs-lookup"><span data-stu-id="177eb-142">Run API call such as \- Isolation, Run anti-virus scan and more.</span></span>
[<span data-ttu-id="177eb-143">Méthodes et propriétés de l’action d'amélioration</span><span class="sxs-lookup"><span data-stu-id="177eb-143">Recommendation methods and properties</span></span>](recommendation.md) | <span data-ttu-id="177eb-144">Exécutez des appels d’API tels \- que obtenir une recommandation par ID.</span><span class="sxs-lookup"><span data-stu-id="177eb-144">Run API calls such as \- get recommendation by ID.</span></span>
[<span data-ttu-id="177eb-145">Méthodes et propriétés des activités de correction</span><span class="sxs-lookup"><span data-stu-id="177eb-145">Remediation activity methods and properties</span></span>](get-remediation-methods-properties.md) | <span data-ttu-id="177eb-146">Exécutez un appel d’API comme obtenir toutes les tâches de correction, obtenir une tâche de correction des appareils exposés et obtenir une tâche de correction \- par ID.</span><span class="sxs-lookup"><span data-stu-id="177eb-146">Run API call such as \- get all remediation tasks, get exposed devices remediation task and get one remediation task by id.</span></span>
[<span data-ttu-id="177eb-147">Méthodes et propriétés du score</span><span class="sxs-lookup"><span data-stu-id="177eb-147">Score methods and properties</span></span>](score.md) | <span data-ttu-id="177eb-148">Exécutez des appels d’API tels \- que obtenir le score d’exposition ou obtenir le score de sécurité de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="177eb-148">Run API calls such as \- get exposure score or get device secure score.</span></span>
[<span data-ttu-id="177eb-149">Méthodes et propriétés du logiciel</span><span class="sxs-lookup"><span data-stu-id="177eb-149">Software methods and properties</span></span>](software.md) | <span data-ttu-id="177eb-150">Exécutez des appels d’API tels que \- des vulnérabilités de liste par logiciel.</span><span class="sxs-lookup"><span data-stu-id="177eb-150">Run API calls such as \- list vulnerabilities by software.</span></span>
[<span data-ttu-id="177eb-151">Méthodes de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="177eb-151">User methods</span></span>](user.md) | <span data-ttu-id="177eb-152">Exécutez des appels d’API tels que l’accès à des \- alertes liées à l’utilisateur et à des appareils liés à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="177eb-152">Run API calls such as \- get user-related alerts and user-related devices.</span></span>
[<span data-ttu-id="177eb-153">Méthodes et propriétés de la vulnérabilité</span><span class="sxs-lookup"><span data-stu-id="177eb-153">Vulnerability methods and properties</span></span>](vulnerability.md) | <span data-ttu-id="177eb-154">Exécutez des appels d’API tels \- que des périphériques de liste par vulnérabilité.</span><span class="sxs-lookup"><span data-stu-id="177eb-154">Run API calls such as \- list devices by vulnerability.</span></span>

## <a name="see-also"></a><span data-ttu-id="177eb-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="177eb-155">See also</span></span>

- [<span data-ttu-id="177eb-156">API Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="177eb-156">Microsoft Defender for Endpoint APIs</span></span>](apis-intro.md)

- [<span data-ttu-id="177eb-157">Notes de publication de l’API Microsoft Defender for Endpoint</span><span class="sxs-lookup"><span data-stu-id="177eb-157">Microsoft Defender for Endpoint API release notes</span></span>](api-release-notes.md)
