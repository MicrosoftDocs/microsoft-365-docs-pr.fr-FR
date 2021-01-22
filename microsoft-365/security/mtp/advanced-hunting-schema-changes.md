---
title: Changements d’appellation dans le schéma de recherche avancée Microsoft 365 Defender
description: Suivre et passer en revue les tables et les colonnes des modifications d’attribution de noms dans le schéma de recherche avancé
keywords: advanced hunting, threat hunting, cyber threat hunting, microsoft threat protection, microsoft 365, mtp, m365, search, query, telemetry, schema reference, kusto, table, data, naming changes, rename, Microsoft Threat Protection
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
ms.openlocfilehash: 483fedd1fb152e3df5311c981b305e621ec2aec3
ms.sourcegitcommit: 855719ee21017cf87dfa98cbe62806763bcb78ac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/22/2021
ms.locfileid: "49932201"
---
# <a name="advanced-hunting-schema---naming-changes"></a><span data-ttu-id="8823f-104">Schéma de recherche avancé : modifications d’attribution de noms</span><span class="sxs-lookup"><span data-stu-id="8823f-104">Advanced hunting schema - Naming changes</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="8823f-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="8823f-105">**Applies to:**</span></span>
- <span data-ttu-id="8823f-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="8823f-106">Microsoft 365 Defender</span></span>

[!INCLUDE [Prerelease information](../includes/prerelease.md)]

<span data-ttu-id="8823f-107">Le [schéma de recherche avancée est mis à jour](advanced-hunting-schema-tables.md) régulièrement pour ajouter de nouvelles tables et colonnes.</span><span class="sxs-lookup"><span data-stu-id="8823f-107">The [advanced hunting schema](advanced-hunting-schema-tables.md) is updated regularly to add new tables and columns.</span></span> <span data-ttu-id="8823f-108">Dans certains cas, les noms des colonnes existantes sont renommés ou remplacés pour améliorer l’expérience utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8823f-108">In some cases, existing columns names are renamed or replaced to improve the user experience.</span></span> <span data-ttu-id="8823f-109">Reportez-vous à cet article pour passer en revue les modifications d’attribution de noms qui peuvent avoir un impact sur vos requêtes.</span><span class="sxs-lookup"><span data-stu-id="8823f-109">Refer to this article to review naming changes that could impact your queries.</span></span>

<span data-ttu-id="8823f-110">Les modifications d’attribution de noms sont automatiquement appliquées aux requêtes enregistrées dans le centre de sécurité, y compris les requêtes utilisées par les règles de détection personnalisées.</span><span class="sxs-lookup"><span data-stu-id="8823f-110">Naming changes are automatically applied to queries that are saved in the security center, including queries used by custom detection rules.</span></span> <span data-ttu-id="8823f-111">Vous n’avez pas besoin de mettre à jour ces requêtes manuellement.</span><span class="sxs-lookup"><span data-stu-id="8823f-111">You don't need to update these queries manually.</span></span> <span data-ttu-id="8823f-112">Toutefois, vous devrez mettre à jour les requêtes suivantes :</span><span class="sxs-lookup"><span data-stu-id="8823f-112">However, you will need to update the following queries:</span></span>
- <span data-ttu-id="8823f-113">Requêtes qui sont exécutés à l’aide de l’API</span><span class="sxs-lookup"><span data-stu-id="8823f-113">Queries that are run using the API</span></span>
- <span data-ttu-id="8823f-114">Requêtes enregistrées ailleurs en dehors du centre de sécurité</span><span class="sxs-lookup"><span data-stu-id="8823f-114">Queries that are saved elsewhere outside the security center</span></span>

## <a name="december-2020"></a><span data-ttu-id="8823f-115">Décembre 2020</span><span class="sxs-lookup"><span data-stu-id="8823f-115">December 2020</span></span>

| <span data-ttu-id="8823f-116">Nom du tableau</span><span class="sxs-lookup"><span data-stu-id="8823f-116">Table name</span></span> | <span data-ttu-id="8823f-117">Nom de colonne d’origine</span><span class="sxs-lookup"><span data-stu-id="8823f-117">Original column name</span></span> | <span data-ttu-id="8823f-118">Nouveau nom de colonne</span><span class="sxs-lookup"><span data-stu-id="8823f-118">New column name</span></span> | <span data-ttu-id="8823f-119">Raison du changement</span><span class="sxs-lookup"><span data-stu-id="8823f-119">Reason for change</span></span>
|--|--|--|--|
| [<span data-ttu-id="8823f-120">EmailEvents</span><span class="sxs-lookup"><span data-stu-id="8823f-120">EmailEvents</span></span>](advanced-hunting-emailevents-table.md) | <span data-ttu-id="8823f-121">FinalEmailAction</span><span class="sxs-lookup"><span data-stu-id="8823f-121">FinalEmailAction</span></span> | <span data-ttu-id="8823f-122">EmailAction</span><span class="sxs-lookup"><span data-stu-id="8823f-122">EmailAction</span></span> | <span data-ttu-id="8823f-123">Commentaires des clients.</span><span class="sxs-lookup"><span data-stu-id="8823f-123">Customer feedback</span></span> |
| [<span data-ttu-id="8823f-124">EmailEvents</span><span class="sxs-lookup"><span data-stu-id="8823f-124">EmailEvents</span></span>](advanced-hunting-emailevents-table.md) | <span data-ttu-id="8823f-125">FinalEmailActionPolicy</span><span class="sxs-lookup"><span data-stu-id="8823f-125">FinalEmailActionPolicy</span></span> | <span data-ttu-id="8823f-126">EmailActionPolicy</span><span class="sxs-lookup"><span data-stu-id="8823f-126">EmailActionPolicy</span></span> | <span data-ttu-id="8823f-127">Commentaires des clients.</span><span class="sxs-lookup"><span data-stu-id="8823f-127">Customer feedback</span></span> |
| [<span data-ttu-id="8823f-128">EmailEvents</span><span class="sxs-lookup"><span data-stu-id="8823f-128">EmailEvents</span></span>](advanced-hunting-emailevents-table.md) | <span data-ttu-id="8823f-129">FinalEmailActionPolicyGuid</span><span class="sxs-lookup"><span data-stu-id="8823f-129">FinalEmailActionPolicyGuid</span></span> | <span data-ttu-id="8823f-130">EmailActionPolicyGuid</span><span class="sxs-lookup"><span data-stu-id="8823f-130">EmailActionPolicyGuid</span></span> | <span data-ttu-id="8823f-131">Commentaires des clients.</span><span class="sxs-lookup"><span data-stu-id="8823f-131">Customer feedback</span></span> |

## <a name="related-topics"></a><span data-ttu-id="8823f-132">Rubriques associées</span><span class="sxs-lookup"><span data-stu-id="8823f-132">Related topics</span></span>
- [<span data-ttu-id="8823f-133">Vue d’ensemble du repérage avancé</span><span class="sxs-lookup"><span data-stu-id="8823f-133">Advanced hunting overview</span></span>](advanced-hunting-overview.md)
- [<span data-ttu-id="8823f-134">Comprendre le schéma</span><span class="sxs-lookup"><span data-stu-id="8823f-134">Understand the schema</span></span>](advanced-hunting-schema-tables.md)