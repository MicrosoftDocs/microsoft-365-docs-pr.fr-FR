---
title: Quotas de recherche avancés et paramètres d’utilisation dans Microsoft 365 Defender
description: Comprendre les différents quotas et paramètres d’utilisation (limites de service) qui conservent la réactivité du service de recherche avancée
keywords: advanced hunting, threat hunting, cyber threat hunting, Microsoft 365 Defender, microsoft 365, m365, search, query, telemetry, schema, kusto, CPU limit, query limit, resources, maximum results, quota, parameters, allocation
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: maccruz
author: schmurky
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
- m365initiative-m365-defender
ms.topic: article
ms.technology: m365d
ms.openlocfilehash: d7563a8299bbe7d543b065bb25eeb3bc90a854b9
ms.sourcegitcommit: ff20f5b4e3268c7c98a84fb1cbe7db7151596b6d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/06/2021
ms.locfileid: "52245599"
---
# <a name="advanced-hunting-quotas-and-usage-parameters"></a><span data-ttu-id="0bf4e-104">Quotas de recherche avancés et paramètres d’utilisation</span><span class="sxs-lookup"><span data-stu-id="0bf4e-104">Advanced hunting quotas and usage parameters</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="0bf4e-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="0bf4e-105">**Applies to:**</span></span>
- <span data-ttu-id="0bf4e-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="0bf4e-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="0bf4e-107">Pour que le service reste performant et réactif, le service de recherche avancée définit différents quotas et paramètres d’utilisation (également appelés « limites de service »).</span><span class="sxs-lookup"><span data-stu-id="0bf4e-107">To keep the service performant and responsive, advanced hunting sets various quotas and usage parameters (also known as "service limits").</span></span> <span data-ttu-id="0bf4e-108">Ces quotas et paramètres s’appliquent séparément aux requêtes qui s’exécutent manuellement et aux requêtes qui s’exécutent à l’aide de [règles de détection personnalisées.](custom-detection-rules.md)</span><span class="sxs-lookup"><span data-stu-id="0bf4e-108">These quotas and parameters apply separately to queries run manually and to queries run using [custom detection rules](custom-detection-rules.md).</span></span> <span data-ttu-id="0bf4e-109">Les clients qui exécutent plusieurs requêtes régulièrement doivent tenir compte de ces limites et appliquer les meilleures pratiques d’optimisation [pour](advanced-hunting-best-practices.md) minimiser les perturbations.</span><span class="sxs-lookup"><span data-stu-id="0bf4e-109">Customers who run multiple queries regularly should be mindful of these limits and [apply optimization best practices](advanced-hunting-best-practices.md) to minimize disruptions.</span></span>

<span data-ttu-id="0bf4e-110">Reportez-vous au tableau suivant pour comprendre les quotas et paramètres d’utilisation existants.</span><span class="sxs-lookup"><span data-stu-id="0bf4e-110">Refer to the following table to understand existing quotas and usage parameters.</span></span>

| <span data-ttu-id="0bf4e-111">Quota ou paramètre</span><span class="sxs-lookup"><span data-stu-id="0bf4e-111">Quota or parameter</span></span> | <span data-ttu-id="0bf4e-112">Size</span><span class="sxs-lookup"><span data-stu-id="0bf4e-112">Size</span></span> | <span data-ttu-id="0bf4e-113">Cycle d’actualisation</span><span class="sxs-lookup"><span data-stu-id="0bf4e-113">Refresh cycle</span></span> | <span data-ttu-id="0bf4e-114">Description</span><span class="sxs-lookup"><span data-stu-id="0bf4e-114">Description</span></span> |
|--|--|--|--|
| <span data-ttu-id="0bf4e-115">Plage de données</span><span class="sxs-lookup"><span data-stu-id="0bf4e-115">Data range</span></span> | <span data-ttu-id="0bf4e-116">30 jours</span><span class="sxs-lookup"><span data-stu-id="0bf4e-116">30 days</span></span> | <span data-ttu-id="0bf4e-117">Chaque requête</span><span class="sxs-lookup"><span data-stu-id="0bf4e-117">Every query</span></span> | <span data-ttu-id="0bf4e-118">Chaque requête peut rechercher des données depuis les 30 derniers jours.</span><span class="sxs-lookup"><span data-stu-id="0bf4e-118">Each query can look up data from up to the past 30 days.</span></span> |
| <span data-ttu-id="0bf4e-119">Jeu de résultats</span><span class="sxs-lookup"><span data-stu-id="0bf4e-119">Result set</span></span> | <span data-ttu-id="0bf4e-120">10 000 lignes</span><span class="sxs-lookup"><span data-stu-id="0bf4e-120">10,000 rows</span></span> | <span data-ttu-id="0bf4e-121">Chaque requête</span><span class="sxs-lookup"><span data-stu-id="0bf4e-121">Every query</span></span> | <span data-ttu-id="0bf4e-122">Chaque requête peut renvoyer jusqu’à 10 000 enregistrements.</span><span class="sxs-lookup"><span data-stu-id="0bf4e-122">Each query can return up to 10,000 records.</span></span> |
| <span data-ttu-id="0bf4e-123">Timeout</span><span class="sxs-lookup"><span data-stu-id="0bf4e-123">Timeout</span></span> | <span data-ttu-id="0bf4e-124">10 minutes</span><span class="sxs-lookup"><span data-stu-id="0bf4e-124">10 minutes</span></span> | <span data-ttu-id="0bf4e-125">Chaque requête</span><span class="sxs-lookup"><span data-stu-id="0bf4e-125">Every query</span></span> | <span data-ttu-id="0bf4e-126">Chaque requête peut s’exécuter pendant 10 minutes.</span><span class="sxs-lookup"><span data-stu-id="0bf4e-126">Each query can run for up to 10 minutes.</span></span> <span data-ttu-id="0bf4e-127">S’il ne se termine pas dans les 10 minutes, le service affiche une erreur.</span><span class="sxs-lookup"><span data-stu-id="0bf4e-127">If it does not complete within 10 minutes, the service displays an error.</span></span>
| <span data-ttu-id="0bf4e-128">Ressources processeur</span><span class="sxs-lookup"><span data-stu-id="0bf4e-128">CPU resources</span></span> | <span data-ttu-id="0bf4e-129">En fonction de la taille du client</span><span class="sxs-lookup"><span data-stu-id="0bf4e-129">Based on tenant size</span></span> | <span data-ttu-id="0bf4e-130">Toutes les 15 minutes</span><span class="sxs-lookup"><span data-stu-id="0bf4e-130">Every 15 minutes</span></span> | <span data-ttu-id="0bf4e-131">Le [portail affiche une erreur](advanced-hunting-errors.md) chaque fois qu’une requête s’exécute et que le client a consommé plus de 10 % des ressources allouées.</span><span class="sxs-lookup"><span data-stu-id="0bf4e-131">The [portal displays an error](advanced-hunting-errors.md) whenever a query runs and the tenant has consumed over 10% of allocated resources.</span></span> <span data-ttu-id="0bf4e-132">Les requêtes sont bloquées si le client a atteint 100 % jusqu’au terme du cycle de 15 minutes suivant.</span><span class="sxs-lookup"><span data-stu-id="0bf4e-132">Queries are blocked if the tenant has reached 100% until after the next 15-minute cycle.</span></span> |

>[!NOTE] 
><span data-ttu-id="0bf4e-133">Un ensemble distinct de quotas et de paramètres s’applique aux requêtes de recherche avancées effectuées via l’API.</span><span class="sxs-lookup"><span data-stu-id="0bf4e-133">A separate set of quotas and parameters apply to advanced hunting queries performed through the API.</span></span> [<span data-ttu-id="0bf4e-134">En savoir plus sur les API de recherche avancée</span><span class="sxs-lookup"><span data-stu-id="0bf4e-134">Read about advanced hunting APIs</span></span>](./api-advanced-hunting.md)

## <a name="related-topics"></a><span data-ttu-id="0bf4e-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0bf4e-135">Related topics</span></span>

- [<span data-ttu-id="0bf4e-136">Meilleures pratiques de recherche avancée</span><span class="sxs-lookup"><span data-stu-id="0bf4e-136">Advanced hunting best practices</span></span>](advanced-hunting-best-practices.md)
- [<span data-ttu-id="0bf4e-137">Gérer les erreurs de recherche avancée</span><span class="sxs-lookup"><span data-stu-id="0bf4e-137">Handle advanced hunting errors</span></span>](advanced-hunting-errors.md)
- [<span data-ttu-id="0bf4e-138">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="0bf4e-138">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="0bf4e-139">Vue d’ensemble des détections personnalisées</span><span class="sxs-lookup"><span data-stu-id="0bf4e-139">Custom detections overview</span></span>](custom-detections-overview.md)