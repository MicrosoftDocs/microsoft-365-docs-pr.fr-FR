---
title: Vue d’ensemble Microsoft 365 API Defender
description: En savoir plus sur les API disponibles dans Microsoft 365 Defender
keywords: api, api, vue d’ensemble, incident, incidents, recherche de menace, microsoft 365 defender
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: macapara
author: mjcaparas
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: conceptual
search.appverid:
- MOE150
- MET150
ms.technology: m365d
ms.openlocfilehash: b19a6072be5f97b90c117f053ccae4593587c43d
ms.sourcegitcommit: e8f5d88f0fe54620308d3bec05263568f9da2931
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2021
ms.locfileid: "52730893"
---
# <a name="overview-of--microsoft-365-defender-apis"></a><span data-ttu-id="38dbc-104">Vue d’ensemble Microsoft 365 API Defender</span><span class="sxs-lookup"><span data-stu-id="38dbc-104">Overview of  Microsoft 365 Defender APIs</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

<span data-ttu-id="38dbc-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="38dbc-105">**Applies to:**</span></span>

- <span data-ttu-id="38dbc-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="38dbc-106">Microsoft 365 Defender</span></span>

> [!IMPORTANT]
> <span data-ttu-id="38dbc-107">Certaines informations ont trait à un produit préalablement publié, qui peut être modifié de manière significative avant sa publication commerciale.</span><span class="sxs-lookup"><span data-stu-id="38dbc-107">Some information relates to prereleased product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="38dbc-108">Microsoft n’offre aucune garantie, explicite ou implicite, concernant les informations fournies ici.</span><span class="sxs-lookup"><span data-stu-id="38dbc-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span></span>

<span data-ttu-id="38dbc-109">Microsoft 365 Defender repose sur une plateforme prête pour l’intégration.</span><span class="sxs-lookup"><span data-stu-id="38dbc-109">Microsoft 365 Defender is built on top of an integration-ready platform.</span></span>

<span data-ttu-id="38dbc-110">Utilisez les API Microsoft 365 Defender pour automatiser les flux de travail en fonction de l’incident partagé et des tables de recherche avancées.</span><span class="sxs-lookup"><span data-stu-id="38dbc-110">Use the Microsoft 365 Defender APIs to automate workflows based on the shared incident and advanced hunting tables.</span></span>

- <span data-ttu-id="38dbc-111">**[File d’attente d’incidents combinés](api-incident.md)** : concentrez-vous sur ce qui est critique en groupant l’étendue d’attaque complète et toutes les ressources impactées sous l’API d’incident.</span><span class="sxs-lookup"><span data-stu-id="38dbc-111">**[Combined incidents queue](api-incident.md)** - Focus on what's critical by grouping the full attack scope and all impacted assets together under the incident API.</span></span>

- <span data-ttu-id="38dbc-112">Recherche de menaces entre produits : tirez parti des connaissances organisationnelles de votre équipe de sécurité pour chercher des signes de compromission, en créant vos propres requêtes personnalisées pour passer en **[arrière-plan](api-advanced-hunting.md)** les données brutes collectées sur plusieurs produits de protection.</span><span class="sxs-lookup"><span data-stu-id="38dbc-112">**[Cross-product threat hunting](api-advanced-hunting.md)** - Leverage your security team's organizational knowledge to hunt for signs of compromise, by creating your own custom queries to sift over raw data collected across multiple protection products.</span></span>

<span data-ttu-id="38dbc-113">Utilisez [l’API de diffusion en](../defender-endpoint/raw-data-export.md) continu pour expédier des événements et des alertes en temps réel à partir d’instances telles qu’elles se produisent dans un flux de données unique.</span><span class="sxs-lookup"><span data-stu-id="38dbc-113">Use the [Streaming API](../defender-endpoint/raw-data-export.md) to ship real-time events and alerts from instances as they occur within a single data stream.</span></span>


<span data-ttu-id="38dbc-114">Parallèlement à ces MICROSOFT 365 spécifiques à Defender, chacun de [](api-articles.md) nos autres produits de sécurité expose des API supplémentaires pour vous aider à tirer parti de leurs fonctionnalités uniques.</span><span class="sxs-lookup"><span data-stu-id="38dbc-114">Along with these Microsoft 365 Defender-specific APIs, each of our other security products expose [additional APIs](api-articles.md) to help you take advantage of their unique capabilities.</span></span>


> [!NOTE]
> <span data-ttu-id="38dbc-115">La transition vers le portail unifié ne doit pas affecter les tableaux de bord PowerBi basés sur les API Microsoft Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="38dbc-115">The transition to the unified portal should not affect the PowerBi dashboards based on Microsoft Defender for Endpoint APIs.</span></span> <span data-ttu-id="38dbc-116">Vous pouvez continuer à travailler avec les API existantes, quelle que soit la transition du portail interactif.</span><span class="sxs-lookup"><span data-stu-id="38dbc-116">You can continue to work with the existing APIs regardless of the interactive portal transition.</span></span>


## <a name="learn-more"></a><span data-ttu-id="38dbc-117">En savoir plus</span><span class="sxs-lookup"><span data-stu-id="38dbc-117">Learn more</span></span>

| <span data-ttu-id="38dbc-118">**Comprendre comment accéder aux API**</span><span class="sxs-lookup"><span data-stu-id="38dbc-118">**Understand how to access the APIs**</span></span> |
|-|
| [<span data-ttu-id="38dbc-119">En savoir plus sur les quotas d’API et les licences</span><span class="sxs-lookup"><span data-stu-id="38dbc-119">Learn about API quotas and licensing</span></span>](api-terms.md) |
| [<span data-ttu-id="38dbc-120">Accéder aux API Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="38dbc-120">Access the Microsoft 365 Defender APIs</span></span>](api-access.md) |
| <span data-ttu-id="38dbc-121">**Créer des applications**</span><span class="sxs-lookup"><span data-stu-id="38dbc-121">**Build apps**</span></span> |
| [<span data-ttu-id="38dbc-122">Créer une application « Hello World »</span><span class="sxs-lookup"><span data-stu-id="38dbc-122">Create a 'Hello world' app</span></span>](api-hello-world.md) |
| [<span data-ttu-id="38dbc-123">Créer une application pour accéder Microsoft 365 API Defender au nom d’un utilisateur</span><span class="sxs-lookup"><span data-stu-id="38dbc-123">Create an app to access Microsoft 365 Defender APIs on behalf of a user</span></span>](api-create-app-user-context.md) |
| [<span data-ttu-id="38dbc-124">Créer une application pour accéder à Microsoft 365 Defender sans utilisateur</span><span class="sxs-lookup"><span data-stu-id="38dbc-124">Create an app to access Microsoft 365 Defender without a user</span></span>](api-create-app-web.md) |
| [<span data-ttu-id="38dbc-125">Créer une application avec un accès partenaire multi-locataire aux API Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="38dbc-125">Create an app with multi-tenant partner access to Microsoft 365 Defender APIs</span></span>](api-partner-access.md) |
| <span data-ttu-id="38dbc-126">**Résoudre les problèmes et gérer vos applications**</span><span class="sxs-lookup"><span data-stu-id="38dbc-126">**Troubleshoot and maintain your apps**</span></span> |
| [<span data-ttu-id="38dbc-127">Comprendre les codes d’erreur de l’API</span><span class="sxs-lookup"><span data-stu-id="38dbc-127">Understand API error codes</span></span>](api-error-codes.md) |
| [<span data-ttu-id="38dbc-128">Gérer les secrets dans vos applications avec Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="38dbc-128">Manage secrets in your apps with Azure Key Vault</span></span>](/learn/modules/manage-secrets-with-azure-key-vault/) |
| [<span data-ttu-id="38dbc-129">Implémenter l’autorisation OAuth 2.0 pour la signature utilisateur</span><span class="sxs-lookup"><span data-stu-id="38dbc-129">Implement OAuth 2.0 authorization for user sign in</span></span>](/azure/active-directory/develop/active-directory-v2-protocols-oauth-code) |