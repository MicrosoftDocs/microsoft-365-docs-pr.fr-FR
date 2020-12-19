---
title: Vue d’ensemble des API Microsoft 365 Defender
description: En savoir plus sur les API disponibles dans Microsoft 365 Defender
keywords: API, API, vue d’ensemble, incident, incidents, chasse aux menaces, Microsoft 365 Defender
search.product: eADQiWindows 10XVcnh
ms.prod: microsoft-365-enterprise
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
ms.openlocfilehash: 1a75a561e60c05208e8ea302505f9644ac0bc044
ms.sourcegitcommit: d6b1da2e12d55f69e4353289e90f5ae2f60066d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2020
ms.locfileid: "49719189"
---
# <a name="overview-of--microsoft-365-defender-apis"></a><span data-ttu-id="038ba-104">Vue d’ensemble des API Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="038ba-104">Overview of  Microsoft 365 Defender APIs</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

<span data-ttu-id="038ba-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="038ba-105">**Applies to:**</span></span>

- <span data-ttu-id="038ba-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="038ba-106">Microsoft 365 Defender</span></span>

> [!IMPORTANT]
> <span data-ttu-id="038ba-107">Certaines informations se rapportent à des produits précommercialisés susceptibles d’être modifiés de manière substantielle avant leur publication commerciale.</span><span class="sxs-lookup"><span data-stu-id="038ba-107">Some information relates to prereleased product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="038ba-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span><span class="sxs-lookup"><span data-stu-id="038ba-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span></span>

<span data-ttu-id="038ba-109">Microsoft 365 Defender est basé sur une plateforme compatible avec l’intégration.</span><span class="sxs-lookup"><span data-stu-id="038ba-109">Microsoft 365 Defender is built on top of an integration-ready platform.</span></span>

<span data-ttu-id="038ba-110">Utilisez les API Microsoft 365 Defender pour automatiser les flux de travail en fonction de l’incident partagé et des tableaux de la chasse avancée.</span><span class="sxs-lookup"><span data-stu-id="038ba-110">Use the Microsoft 365 Defender APIs to automate workflows based on the shared incident and advanced hunting tables.</span></span>

- <span data-ttu-id="038ba-111">Mise en **[file d’attente des incidents combinés](api-incident.md)** : focalisation sur ce qui est essentiel en regroupant l’étendue d’attaque complète et tous les actifs affectés ensemble sous l’API incidente.</span><span class="sxs-lookup"><span data-stu-id="038ba-111">**[Combined incidents queue](api-incident.md)** - Focus on what's critical by grouping the full attack scope and all impacted assets together under the incident API.</span></span>

- <span data-ttu-id="038ba-112">Recherche des **[menaces entre les produits](api-advanced-hunting.md)** : Tirez parti des connaissances de l’organisation de votre équipe de sécurité pour rechercher des signes de compromission, en créant vos propres requêtes personnalisées pour passer en revue les données brutes collectées sur plusieurs produits de protection.</span><span class="sxs-lookup"><span data-stu-id="038ba-112">**[Cross-product threat hunting](api-advanced-hunting.md)** - Leverage your security team's organizational knowledge to hunt for signs of compromise, by creating your own custom queries to sift over raw data collected across multiple protection products.</span></span>

<span data-ttu-id="038ba-113">Outre ces API propres à Microsoft 365 Defender, chacun de nos autres produits de sécurité expose des [API supplémentaires](api-articles.md) pour vous aider à tirer parti de leurs fonctionnalités uniques.</span><span class="sxs-lookup"><span data-stu-id="038ba-113">Along with these Microsoft 365 Defender-specific APIs, each of our other security products expose [additional APIs](api-articles.md) to help you take advantage of their unique capabilities.</span></span>

## <a name="learn-more"></a><span data-ttu-id="038ba-114">En savoir plus</span><span class="sxs-lookup"><span data-stu-id="038ba-114">Learn more</span></span>

| <span data-ttu-id="038ba-115">**Comprendre comment accéder aux API**</span><span class="sxs-lookup"><span data-stu-id="038ba-115">**Understand how to access the APIs**</span></span> |
|-|
| [<span data-ttu-id="038ba-116">En savoir plus sur les quotas d’API et la gestion des licences</span><span class="sxs-lookup"><span data-stu-id="038ba-116">Learn about API quotas and licensing</span></span>](api-terms.md) |
| [<span data-ttu-id="038ba-117">Accéder aux API Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="038ba-117">Access the Microsoft 365 Defender APIs</span></span>](api-access.md) |
| <span data-ttu-id="038ba-118">**Créer des applications**</span><span class="sxs-lookup"><span data-stu-id="038ba-118">**Build apps**</span></span> |
| [<span data-ttu-id="038ba-119">Créer une application « Hello World »</span><span class="sxs-lookup"><span data-stu-id="038ba-119">Create a 'Hello world' app</span></span>](api-hello-world.md) |
| [<span data-ttu-id="038ba-120">Créer une application pour accéder aux API Microsoft 365 Defender au nom d’un utilisateur</span><span class="sxs-lookup"><span data-stu-id="038ba-120">Create an app to access Microsoft 365 Defender APIs on behalf of a user</span></span>](api-create-app-user-context.md) |
| [<span data-ttu-id="038ba-121">Créer une application pour accéder à Microsoft 365 Defender sans utilisateur</span><span class="sxs-lookup"><span data-stu-id="038ba-121">Create an app to access Microsoft 365 Defender without a user</span></span>](api-create-app-web.md) |
| [<span data-ttu-id="038ba-122">Créer une application avec un accès partenaire mutualisée aux API Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="038ba-122">Create an app with multi-tenant partner access to Microsoft 365 Defender APIs</span></span>](api-partner-access.md) |
| <span data-ttu-id="038ba-123">**Dépanner et gérer vos applications**</span><span class="sxs-lookup"><span data-stu-id="038ba-123">**Troubleshoot and maintain your apps**</span></span> |
| [<span data-ttu-id="038ba-124">Comprendre les codes d’erreur d’API</span><span class="sxs-lookup"><span data-stu-id="038ba-124">Understand API error codes</span></span>](api-error-codes.md) |
| [<span data-ttu-id="038ba-125">Gérer les secrets dans vos applications avec Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="038ba-125">Manage secrets in your apps with Azure Key Vault</span></span>](https://docs.microsoft.com/learn/modules/manage-secrets-with-azure-key-vault/) |
| [<span data-ttu-id="038ba-126">Implémentation de l’autorisation OAuth 2,0 pour la connexion de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="038ba-126">Implement OAuth 2.0 authorization for user sign in</span></span>](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-protocols-oauth-code) |
