---
title: Limites de recherche avancées dans Microsoft Defender ATP
description: Comprendre les différentes limites de service qui conservent la réactivité du service de recherche avancée
keywords: advanced hunting, threat hunting, cyber threat hunting, mdatp, microsoft defender atp, wdatp, search, query, telemetry, schema, kusto, CPU limit, query limit, resources, maximum results
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: lomayor
author: lomayor
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.technology: mde
ms.openlocfilehash: 127ebc8c0eaba433710bc272a2cf602e7c9a9730
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51067945"
---
# <a name="advanced-hunting-service-limits"></a><span data-ttu-id="c3610-104">Limites du service de recherche avancée</span><span class="sxs-lookup"><span data-stu-id="c3610-104">Advanced hunting service limits</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="c3610-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="c3610-105">**Applies to:**</span></span>
- [<span data-ttu-id="c3610-106">Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="c3610-106">Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/?linkid=2154037)

><span data-ttu-id="c3610-107">Vous souhaitez faire l’expérience de Defender for Endpoint ?</span><span class="sxs-lookup"><span data-stu-id="c3610-107">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="c3610-108">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="c3610-108">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-advancedhunting-abovefoldlink)

<span data-ttu-id="c3610-109">Pour que le service reste performant et réactif, le repérage avancé définit différentes limites pour les requêtes qui s’exécutent manuellement et par des [règles de détection personnalisées.](custom-detection-rules.md)</span><span class="sxs-lookup"><span data-stu-id="c3610-109">To keep the service performant and responsive, advanced hunting sets various limits for queries run manually and by [custom detection rules](custom-detection-rules.md).</span></span> <span data-ttu-id="c3610-110">Reportez-vous au tableau suivant pour comprendre ces limites.</span><span class="sxs-lookup"><span data-stu-id="c3610-110">Refer to the following table to understand these limits.</span></span>

| <span data-ttu-id="c3610-111">Limite</span><span class="sxs-lookup"><span data-stu-id="c3610-111">Limit</span></span> | <span data-ttu-id="c3610-112">Size</span><span class="sxs-lookup"><span data-stu-id="c3610-112">Size</span></span> | <span data-ttu-id="c3610-113">Cycle d’actualisation</span><span class="sxs-lookup"><span data-stu-id="c3610-113">Refresh cycle</span></span> | <span data-ttu-id="c3610-114">Description</span><span class="sxs-lookup"><span data-stu-id="c3610-114">Description</span></span> |
|--|--|--|--|
| <span data-ttu-id="c3610-115">Plage de données</span><span class="sxs-lookup"><span data-stu-id="c3610-115">Data range</span></span> | <span data-ttu-id="c3610-116">30 jours</span><span class="sxs-lookup"><span data-stu-id="c3610-116">30 days</span></span> | <span data-ttu-id="c3610-117">Chaque requête</span><span class="sxs-lookup"><span data-stu-id="c3610-117">Every query</span></span> | <span data-ttu-id="c3610-118">Chaque requête peut rechercher des données depuis les 30 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="c3610-118">Each query can look up data from up to the past 30 days.</span></span> |
| <span data-ttu-id="c3610-119">Jeu de résultats</span><span class="sxs-lookup"><span data-stu-id="c3610-119">Result set</span></span> | <span data-ttu-id="c3610-120">10 000 lignes</span><span class="sxs-lookup"><span data-stu-id="c3610-120">10,000 rows</span></span> | <span data-ttu-id="c3610-121">Chaque requête</span><span class="sxs-lookup"><span data-stu-id="c3610-121">Every query</span></span> | <span data-ttu-id="c3610-122">Chaque requête peut renvoyer jusqu’à 10 000 enregistrements.</span><span class="sxs-lookup"><span data-stu-id="c3610-122">Each query can return up to 10,000 records.</span></span> |
| <span data-ttu-id="c3610-123">Timeout</span><span class="sxs-lookup"><span data-stu-id="c3610-123">Timeout</span></span> | <span data-ttu-id="c3610-124">10 minutes</span><span class="sxs-lookup"><span data-stu-id="c3610-124">10 minutes</span></span> | <span data-ttu-id="c3610-125">Chaque requête</span><span class="sxs-lookup"><span data-stu-id="c3610-125">Every query</span></span> | <span data-ttu-id="c3610-126">Chaque requête peut s’exécuter pendant 10 minutes.</span><span class="sxs-lookup"><span data-stu-id="c3610-126">Each query can run for up to 10 minutes.</span></span> <span data-ttu-id="c3610-127">S’il ne se termine pas dans les 10 minutes, le service affiche une erreur.</span><span class="sxs-lookup"><span data-stu-id="c3610-127">If it does not complete within 10 minutes, the service displays an error.</span></span>
| <span data-ttu-id="c3610-128">Ressources processeur</span><span class="sxs-lookup"><span data-stu-id="c3610-128">CPU resources</span></span> | <span data-ttu-id="c3610-129">En fonction de la taille du client</span><span class="sxs-lookup"><span data-stu-id="c3610-129">Based on tenant size</span></span> | <span data-ttu-id="c3610-130">- À l’heure, puis toutes les 15 minutes</span><span class="sxs-lookup"><span data-stu-id="c3610-130">- On the hour and then every 15 minutes</span></span><br><span data-ttu-id="c3610-131">- Tous les jours à minuit</span><span class="sxs-lookup"><span data-stu-id="c3610-131">- Daily at 12 midnight</span></span> | <span data-ttu-id="c3610-132">Le service applique séparément la limite quotidienne et la limite de 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="c3610-132">The service enforces the daily and the 15-minute limit separately.</span></span> <span data-ttu-id="c3610-133">Pour chaque limite, [le](advanced-hunting-errors.md) portail affiche une erreur chaque fois qu’une requête s’exécute et que le client a consommé plus de 10 % des ressources allouées.</span><span class="sxs-lookup"><span data-stu-id="c3610-133">For each limit, the [portal displays an error](advanced-hunting-errors.md) whenever a query runs and the tenant has consumed over 10% of allocated resources.</span></span> <span data-ttu-id="c3610-134">Les requêtes sont bloquées si le client a atteint 100 % jusqu’au terme du cycle quotidien suivant ou de 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="c3610-134">Queries are blocked if the tenant has reached 100% until after the next daily or 15-minute cycle.</span></span> |

>[!NOTE] 
><span data-ttu-id="c3610-135">Un ensemble distinct de limites s’applique aux requêtes de recherche avancées effectuées via l’API.</span><span class="sxs-lookup"><span data-stu-id="c3610-135">A separate set of limits apply to advanced hunting queries performed through the API.</span></span> [<span data-ttu-id="c3610-136">En savoir plus sur les API de recherche avancée</span><span class="sxs-lookup"><span data-stu-id="c3610-136">Read about advanced hunting APIs</span></span>](run-advanced-query-api.md)

<span data-ttu-id="c3610-137">Les clients qui exécutent plusieurs [](advanced-hunting-best-practices.md) requêtes régulièrement doivent suivre la consommation et appliquer les meilleures pratiques d’optimisation afin de minimiser les perturbations résultant du dépassement de ces limites.</span><span class="sxs-lookup"><span data-stu-id="c3610-137">Customers who run multiple queries regularly should track consumption and [apply optimization best practices](advanced-hunting-best-practices.md) to minimize disruption resulting from exceeding these limits.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c3610-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c3610-138">Related topics</span></span>

- [<span data-ttu-id="c3610-139">Meilleures pratiques de recherche avancée</span><span class="sxs-lookup"><span data-stu-id="c3610-139">Advanced hunting best practices</span></span>](advanced-hunting-best-practices.md)
- [<span data-ttu-id="c3610-140">Gérer les erreurs de recherche avancée</span><span class="sxs-lookup"><span data-stu-id="c3610-140">Handle advanced hunting errors</span></span>](advanced-hunting-errors.md)
- [<span data-ttu-id="c3610-141">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="c3610-141">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="c3610-142">Règles de détection personnalisées</span><span class="sxs-lookup"><span data-stu-id="c3610-142">Custom detections rules</span></span>](custom-detection-rules.md)
