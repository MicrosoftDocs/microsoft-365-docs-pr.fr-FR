---
title: Vue d'ensemble des API Microsoft 365 Defender
description: En savoir plus sur les API disponibles dans Microsoft 365 Defender
keywords: api, api, vue d'ensemble, incident, incidents, recherche de menace, microsoft 365 defender
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
ms.openlocfilehash: 496ad5695d9cd491817bad5daf3c76a02addefd1
ms.sourcegitcommit: 13ce4b31303a1a21ca53700a54bcf8d91ad2f8c1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/20/2021
ms.locfileid: "51904187"
---
# <a name="overview-of--microsoft-365-defender-apis"></a><span data-ttu-id="c6219-104">Vue d'ensemble des API Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="c6219-104">Overview of  Microsoft 365 Defender APIs</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

<span data-ttu-id="c6219-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="c6219-105">**Applies to:**</span></span>

- <span data-ttu-id="c6219-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="c6219-106">Microsoft 365 Defender</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c6219-107">Certaines informations ont trait à un produit préalablement publié, qui peut être modifié de manière significative avant sa publication commerciale.</span><span class="sxs-lookup"><span data-stu-id="c6219-107">Some information relates to prereleased product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c6219-108">Microsoft n’offre aucune garantie, explicite ou implicite, concernant les informations fournies ici.</span><span class="sxs-lookup"><span data-stu-id="c6219-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span></span>

<span data-ttu-id="c6219-109">Microsoft 365 Defender repose sur une plateforme prête à l'intégration.</span><span class="sxs-lookup"><span data-stu-id="c6219-109">Microsoft 365 Defender is built on top of an integration-ready platform.</span></span>

<span data-ttu-id="c6219-110">Utilisez les API Microsoft 365 Defender pour automatiser les flux de travail en fonction de l'incident partagé et des tables de recherche avancées.</span><span class="sxs-lookup"><span data-stu-id="c6219-110">Use the Microsoft 365 Defender APIs to automate workflows based on the shared incident and advanced hunting tables.</span></span>

- <span data-ttu-id="c6219-111">**[File d'attente d'incidents combinés](api-incident.md)** : concentrez-vous sur ce qui est critique en groupant l'étendue d'attaque complète et toutes les ressources impactées sous l'API d'incident.</span><span class="sxs-lookup"><span data-stu-id="c6219-111">**[Combined incidents queue](api-incident.md)** - Focus on what's critical by grouping the full attack scope and all impacted assets together under the incident API.</span></span>

- <span data-ttu-id="c6219-112">Recherche de menaces entre produits : tirez parti des connaissances organisationnelles de votre équipe de sécurité pour chercher des signes de compromission, en créant vos propres requêtes personnalisées pour passer en **[arrière-plan](api-advanced-hunting.md)** les données brutes collectées sur plusieurs produits de protection.</span><span class="sxs-lookup"><span data-stu-id="c6219-112">**[Cross-product threat hunting](api-advanced-hunting.md)** - Leverage your security team's organizational knowledge to hunt for signs of compromise, by creating your own custom queries to sift over raw data collected across multiple protection products.</span></span>

<span data-ttu-id="c6219-113">En plus de ces API propres à Microsoft 365 [](api-articles.md) Defender, chacun de nos autres produits de sécurité expose des API supplémentaires pour vous aider à tirer parti de leurs fonctionnalités uniques.</span><span class="sxs-lookup"><span data-stu-id="c6219-113">Along with these Microsoft 365 Defender-specific APIs, each of our other security products expose [additional APIs](api-articles.md) to help you take advantage of their unique capabilities.</span></span>


> [!NOTE]
> <span data-ttu-id="c6219-114">La transition vers le portail unifié ne doit pas affecter les tableaux de bord PowerBi basés sur les API Microsoft Defender for Endpoint.</span><span class="sxs-lookup"><span data-stu-id="c6219-114">The transition to the unified portal should not affect the PowerBi dashboards based on Microsoft Defender for Endpoint APIs.</span></span> <span data-ttu-id="c6219-115">Vous pouvez continuer à travailler avec les API existantes, quelle que soit la transition du portail interactif.</span><span class="sxs-lookup"><span data-stu-id="c6219-115">You can continue to work with the existing APIs regardless of the interactive portal transition.</span></span>


## <a name="learn-more"></a><span data-ttu-id="c6219-116">En savoir plus</span><span class="sxs-lookup"><span data-stu-id="c6219-116">Learn more</span></span>

| <span data-ttu-id="c6219-117">**Comprendre comment accéder aux API**</span><span class="sxs-lookup"><span data-stu-id="c6219-117">**Understand how to access the APIs**</span></span> |
|-|
| [<span data-ttu-id="c6219-118">En savoir plus sur les quotas d'API et les licences</span><span class="sxs-lookup"><span data-stu-id="c6219-118">Learn about API quotas and licensing</span></span>](api-terms.md) |
| [<span data-ttu-id="c6219-119">Accéder aux API Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="c6219-119">Access the Microsoft 365 Defender APIs</span></span>](api-access.md) |
| <span data-ttu-id="c6219-120">**Créer des applications**</span><span class="sxs-lookup"><span data-stu-id="c6219-120">**Build apps**</span></span> |
| [<span data-ttu-id="c6219-121">Créer une application « Hello World »</span><span class="sxs-lookup"><span data-stu-id="c6219-121">Create a 'Hello world' app</span></span>](api-hello-world.md) |
| [<span data-ttu-id="c6219-122">Créer une application pour accéder aux API Microsoft 365 Defender au nom d'un utilisateur</span><span class="sxs-lookup"><span data-stu-id="c6219-122">Create an app to access Microsoft 365 Defender APIs on behalf of a user</span></span>](api-create-app-user-context.md) |
| [<span data-ttu-id="c6219-123">Créer une application pour accéder à Microsoft 365 Defender sans utilisateur</span><span class="sxs-lookup"><span data-stu-id="c6219-123">Create an app to access Microsoft 365 Defender without a user</span></span>](api-create-app-web.md) |
| [<span data-ttu-id="c6219-124">Créer une application avec un accès partenaire multi-locataire aux API Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="c6219-124">Create an app with multi-tenant partner access to Microsoft 365 Defender APIs</span></span>](api-partner-access.md) |
| <span data-ttu-id="c6219-125">**Résoudre les problèmes et gérer vos applications**</span><span class="sxs-lookup"><span data-stu-id="c6219-125">**Troubleshoot and maintain your apps**</span></span> |
| [<span data-ttu-id="c6219-126">Comprendre les codes d'erreur de l'API</span><span class="sxs-lookup"><span data-stu-id="c6219-126">Understand API error codes</span></span>](api-error-codes.md) |
| [<span data-ttu-id="c6219-127">Gérer les secrets dans vos applications avec Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="c6219-127">Manage secrets in your apps with Azure Key Vault</span></span>](/learn/modules/manage-secrets-with-azure-key-vault/) |
| [<span data-ttu-id="c6219-128">Implémenter l'autorisation OAuth 2.0 pour la signature utilisateur</span><span class="sxs-lookup"><span data-stu-id="c6219-128">Implement OAuth 2.0 authorization for user sign in</span></span>](/azure/active-directory/develop/active-directory-v2-protocols-oauth-code) |