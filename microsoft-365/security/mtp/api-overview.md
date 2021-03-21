---
title: Vue d’ensemble des API Microsoft 365 Defender
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
ms.localizationpriority: medium
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: conceptual
search.appverid:
- MOE150
- MET150
ms.technology: m365d
ms.openlocfilehash: 0fbe8751a9f82a8e264f1a38207744d091b57474
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50922185"
---
# <a name="overview-of--microsoft-365-defender-apis"></a><span data-ttu-id="2d0f1-104">Vue d’ensemble des API Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="2d0f1-104">Overview of  Microsoft 365 Defender APIs</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

<span data-ttu-id="2d0f1-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="2d0f1-105">**Applies to:**</span></span>

- <span data-ttu-id="2d0f1-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="2d0f1-106">Microsoft 365 Defender</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2d0f1-107">Certaines informations concernent des produits pré-publiés qui peuvent être considérablement modifiés avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="2d0f1-107">Some information relates to prereleased product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="2d0f1-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span><span class="sxs-lookup"><span data-stu-id="2d0f1-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span></span>

<span data-ttu-id="2d0f1-109">Microsoft 365 Defender repose sur une plateforme prête à l’intégration.</span><span class="sxs-lookup"><span data-stu-id="2d0f1-109">Microsoft 365 Defender is built on top of an integration-ready platform.</span></span>

<span data-ttu-id="2d0f1-110">Utilisez les API Microsoft 365 Defender pour automatiser les flux de travail en fonction de l’incident partagé et des tables de recherche avancées.</span><span class="sxs-lookup"><span data-stu-id="2d0f1-110">Use the Microsoft 365 Defender APIs to automate workflows based on the shared incident and advanced hunting tables.</span></span>

- <span data-ttu-id="2d0f1-111">**[File d’attente d’incidents combinés](api-incident.md)** : concentrez-vous sur les éléments critiques en groupant l’étendue d’attaque complète et tous les biens touchés ensemble sous l’API d’incident.</span><span class="sxs-lookup"><span data-stu-id="2d0f1-111">**[Combined incidents queue](api-incident.md)** - Focus on what's critical by grouping the full attack scope and all impacted assets together under the incident API.</span></span>

- <span data-ttu-id="2d0f1-112">Recherche de menaces entre produits : tirez parti des connaissances organisationnelles de votre équipe de sécurité pour chercher des signes de compromission, en créant vos propres requêtes personnalisées pour passer en **[arrière-plan](api-advanced-hunting.md)** les données brutes collectées dans plusieurs produits de protection.</span><span class="sxs-lookup"><span data-stu-id="2d0f1-112">**[Cross-product threat hunting](api-advanced-hunting.md)** - Leverage your security team's organizational knowledge to hunt for signs of compromise, by creating your own custom queries to sift over raw data collected across multiple protection products.</span></span>

<span data-ttu-id="2d0f1-113">En plus de ces API propres à Microsoft 365 [](api-articles.md) Defender, chacun de nos autres produits de sécurité expose des API supplémentaires pour vous aider à tirer parti de leurs fonctionnalités uniques.</span><span class="sxs-lookup"><span data-stu-id="2d0f1-113">Along with these Microsoft 365 Defender-specific APIs, each of our other security products expose [additional APIs](api-articles.md) to help you take advantage of their unique capabilities.</span></span>

## <a name="learn-more"></a><span data-ttu-id="2d0f1-114">Si vous souhaitez en savoir plus</span><span class="sxs-lookup"><span data-stu-id="2d0f1-114">Learn more</span></span>

| <span data-ttu-id="2d0f1-115">**Comprendre comment accéder aux API**</span><span class="sxs-lookup"><span data-stu-id="2d0f1-115">**Understand how to access the APIs**</span></span> |
|-|
| [<span data-ttu-id="2d0f1-116">En savoir plus sur les quotas d’API et les licences</span><span class="sxs-lookup"><span data-stu-id="2d0f1-116">Learn about API quotas and licensing</span></span>](api-terms.md) |
| [<span data-ttu-id="2d0f1-117">Accéder aux API Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="2d0f1-117">Access the Microsoft 365 Defender APIs</span></span>](api-access.md) |
| <span data-ttu-id="2d0f1-118">**Créer des applications**</span><span class="sxs-lookup"><span data-stu-id="2d0f1-118">**Build apps**</span></span> |
| [<span data-ttu-id="2d0f1-119">Créer une application « Hello World »</span><span class="sxs-lookup"><span data-stu-id="2d0f1-119">Create a 'Hello world' app</span></span>](api-hello-world.md) |
| [<span data-ttu-id="2d0f1-120">Créer une application pour accéder aux API Microsoft 365 Defender au nom d’un utilisateur</span><span class="sxs-lookup"><span data-stu-id="2d0f1-120">Create an app to access Microsoft 365 Defender APIs on behalf of a user</span></span>](api-create-app-user-context.md) |
| [<span data-ttu-id="2d0f1-121">Créer une application pour accéder à Microsoft 365 Defender sans utilisateur</span><span class="sxs-lookup"><span data-stu-id="2d0f1-121">Create an app to access Microsoft 365 Defender without a user</span></span>](api-create-app-web.md) |
| [<span data-ttu-id="2d0f1-122">Créer une application avec un accès partenaire multi-locataire aux API Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="2d0f1-122">Create an app with multi-tenant partner access to Microsoft 365 Defender APIs</span></span>](api-partner-access.md) |
| <span data-ttu-id="2d0f1-123">**Résoudre les problèmes et gérer vos applications**</span><span class="sxs-lookup"><span data-stu-id="2d0f1-123">**Troubleshoot and maintain your apps**</span></span> |
| [<span data-ttu-id="2d0f1-124">Comprendre les codes d’erreur de l’API</span><span class="sxs-lookup"><span data-stu-id="2d0f1-124">Understand API error codes</span></span>](api-error-codes.md) |
| [<span data-ttu-id="2d0f1-125">Gérer les secrets dans vos applications avec Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="2d0f1-125">Manage secrets in your apps with Azure Key Vault</span></span>](/learn/modules/manage-secrets-with-azure-key-vault/) |
| [<span data-ttu-id="2d0f1-126">Implémenter l’autorisation OAuth 2.0 pour la signature utilisateur</span><span class="sxs-lookup"><span data-stu-id="2d0f1-126">Implement OAuth 2.0 authorization for user sign in</span></span>](/azure/active-directory/develop/active-directory-v2-protocols-oauth-code) |