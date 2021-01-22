---
title: Quotas de recherche avancés et paramètres d’utilisation dans Microsoft 365 Defender
description: Comprendre les différents quotas et paramètres d’utilisation (limites de service) qui conservent la réactivité du service de recherche avancée
keywords: advanced hunting, threat hunting, cyber threat hunting, microsoft threat protection, microsoft 365, mtp, m365, search, query, telemetry, schema, kusto, CPU limit, query limit, resources, maximum results, quota, parameters, allocation
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: lomayor
author: lomayor
ms.localizationpriority: medium
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
- m365initiative-m365-defender
ms.topic: article
ms.technology: m365d
ms.openlocfilehash: 3d3b1055408b51e8d217f2abcb0e83ef7dd74949
ms.sourcegitcommit: 855719ee21017cf87dfa98cbe62806763bcb78ac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/22/2021
ms.locfileid: "49929789"
---
# <a name="advanced-hunting-quotas-and-usage-parameters"></a><span data-ttu-id="fde4b-104">Quotas de recherche avancés et paramètres d’utilisation</span><span class="sxs-lookup"><span data-stu-id="fde4b-104">Advanced hunting quotas and usage parameters</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="fde4b-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="fde4b-105">**Applies to:**</span></span>
- <span data-ttu-id="fde4b-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="fde4b-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="fde4b-107">Pour que le service reste performant et réactif, le service de recherche avancée définit différents quotas et paramètres d’utilisation (également appelés « limites de service »).</span><span class="sxs-lookup"><span data-stu-id="fde4b-107">To keep the service performant and responsive, advanced hunting sets various quotas and usage parameters (also known as "service limits").</span></span> <span data-ttu-id="fde4b-108">Ces quotas et paramètres s’appliquent aux requêtes qui s’exécutent manuellement et par des [règles de détection personnalisées.](custom-detection-rules.md)</span><span class="sxs-lookup"><span data-stu-id="fde4b-108">These quotas and parameters apply to queries run manually and by [custom detection rules](custom-detection-rules.md).</span></span> <span data-ttu-id="fde4b-109">Les clients qui exécutent plusieurs requêtes régulièrement doivent suivre la consommation et appliquer les meilleures [pratiques](advanced-hunting-best-practices.md) d’optimisation pour minimiser les interruptions.</span><span class="sxs-lookup"><span data-stu-id="fde4b-109">Customers who run multiple queries regularly should track consumption and [apply optimization best practices](advanced-hunting-best-practices.md) to minimize disruptions.</span></span>

<span data-ttu-id="fde4b-110">Reportez-vous au tableau suivant pour comprendre les quotas et paramètres d’utilisation existants.</span><span class="sxs-lookup"><span data-stu-id="fde4b-110">Refer to the following table to understand existing quotas and usage parameters.</span></span>

| <span data-ttu-id="fde4b-111">Quota ou paramètre</span><span class="sxs-lookup"><span data-stu-id="fde4b-111">Quota or parameter</span></span> | <span data-ttu-id="fde4b-112">Size</span><span class="sxs-lookup"><span data-stu-id="fde4b-112">Size</span></span> | <span data-ttu-id="fde4b-113">Cycle d’actualisation</span><span class="sxs-lookup"><span data-stu-id="fde4b-113">Refresh cycle</span></span> | <span data-ttu-id="fde4b-114">Description</span><span class="sxs-lookup"><span data-stu-id="fde4b-114">Description</span></span> |
|--|--|--|--|
| <span data-ttu-id="fde4b-115">Plage de données</span><span class="sxs-lookup"><span data-stu-id="fde4b-115">Data range</span></span> | <span data-ttu-id="fde4b-116">30 jours</span><span class="sxs-lookup"><span data-stu-id="fde4b-116">30 days</span></span> | <span data-ttu-id="fde4b-117">Chaque requête</span><span class="sxs-lookup"><span data-stu-id="fde4b-117">Every query</span></span> | <span data-ttu-id="fde4b-118">Chaque requête peut rechercher des données depuis les 30 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="fde4b-118">Each query can look up data from up to the past 30 days.</span></span> |
| <span data-ttu-id="fde4b-119">Jeu de résultats</span><span class="sxs-lookup"><span data-stu-id="fde4b-119">Result set</span></span> | <span data-ttu-id="fde4b-120">10 000 lignes</span><span class="sxs-lookup"><span data-stu-id="fde4b-120">10,000 rows</span></span> | <span data-ttu-id="fde4b-121">Chaque requête</span><span class="sxs-lookup"><span data-stu-id="fde4b-121">Every query</span></span> | <span data-ttu-id="fde4b-122">Chaque requête peut renvoyer jusqu’à 10 000 enregistrements.</span><span class="sxs-lookup"><span data-stu-id="fde4b-122">Each query can return up to 10,000 records.</span></span> |
| <span data-ttu-id="fde4b-123">Timeout</span><span class="sxs-lookup"><span data-stu-id="fde4b-123">Timeout</span></span> | <span data-ttu-id="fde4b-124">10 minutes</span><span class="sxs-lookup"><span data-stu-id="fde4b-124">10 minutes</span></span> | <span data-ttu-id="fde4b-125">Chaque requête</span><span class="sxs-lookup"><span data-stu-id="fde4b-125">Every query</span></span> | <span data-ttu-id="fde4b-126">Chaque requête peut s’exécuter pendant 10 minutes.</span><span class="sxs-lookup"><span data-stu-id="fde4b-126">Each query can run for up to 10 minutes.</span></span> <span data-ttu-id="fde4b-127">S’il ne se termine pas dans les 10 minutes, le service affiche une erreur.</span><span class="sxs-lookup"><span data-stu-id="fde4b-127">If it does not complete within 10 minutes, the service displays an error.</span></span>
| <span data-ttu-id="fde4b-128">Ressources processeur</span><span class="sxs-lookup"><span data-stu-id="fde4b-128">CPU resources</span></span> | <span data-ttu-id="fde4b-129">En fonction de la taille du client</span><span class="sxs-lookup"><span data-stu-id="fde4b-129">Based on tenant size</span></span> | <span data-ttu-id="fde4b-130">- À l’heure, puis toutes les 15 minutes</span><span class="sxs-lookup"><span data-stu-id="fde4b-130">- On the hour and then every 15 minutes</span></span><br><span data-ttu-id="fde4b-131">- Tous les jours à minuit</span><span class="sxs-lookup"><span data-stu-id="fde4b-131">- Daily at 12 midnight</span></span> | <span data-ttu-id="fde4b-132">Le service applique le quota quotidien et le quota de 15 minutes séparément.</span><span class="sxs-lookup"><span data-stu-id="fde4b-132">The service enforces the daily and the 15-minute quota separately.</span></span> <span data-ttu-id="fde4b-133">Pour chaque quota, [le](advanced-hunting-errors.md) portail affiche une erreur chaque fois qu’une requête s’exécute et que le client a consommé plus de 10 % des ressources allouées.</span><span class="sxs-lookup"><span data-stu-id="fde4b-133">For each quota, the [portal displays an error](advanced-hunting-errors.md) whenever a query runs and the tenant has consumed over 10% of allocated resources.</span></span> <span data-ttu-id="fde4b-134">Les requêtes sont bloquées si le client a atteint 100 % jusqu’au terme du cycle quotidien suivant ou de 15 minutes.</span><span class="sxs-lookup"><span data-stu-id="fde4b-134">Queries are blocked if the tenant has reached 100% until after the next daily or 15-minute cycle.</span></span> |

>[!NOTE] 
><span data-ttu-id="fde4b-135">Un ensemble distinct de quotas et de paramètres s’applique aux requêtes de recherche avancées effectuées via l’API.</span><span class="sxs-lookup"><span data-stu-id="fde4b-135">A separate set of quotas and parameters apply to advanced hunting queries performed through the API.</span></span> [<span data-ttu-id="fde4b-136">En savoir plus sur les API de recherche avancée</span><span class="sxs-lookup"><span data-stu-id="fde4b-136">Read about advanced hunting APIs</span></span>](https://docs.microsoft.com/microsoft-365/security/mtp/api-advanced-hunting)

## <a name="related-topics"></a><span data-ttu-id="fde4b-137">Rubriques associées</span><span class="sxs-lookup"><span data-stu-id="fde4b-137">Related topics</span></span>

- [<span data-ttu-id="fde4b-138">Meilleures pratiques de recherche avancée</span><span class="sxs-lookup"><span data-stu-id="fde4b-138">Advanced hunting best practices</span></span>](advanced-hunting-best-practices.md)
- [<span data-ttu-id="fde4b-139">Gérer les erreurs de recherche avancée</span><span class="sxs-lookup"><span data-stu-id="fde4b-139">Handle advanced hunting errors</span></span>](advanced-hunting-errors.md)
- [<span data-ttu-id="fde4b-140">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="fde4b-140">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="fde4b-141">Vue d’ensemble des détections personnalisées</span><span class="sxs-lookup"><span data-stu-id="fde4b-141">Custom detections overview</span></span>](custom-detections-overview.md)