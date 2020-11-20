---
title: Nouveautés de Microsoft Secure score
description: Décrit les nouvelles modifications apportées à Microsoft Secure score dans le centre de sécurité Microsoft 365.
keywords: score de sécurité Microsoft, score de sécurisation, score de sécurité Office 365, score de sécurité Microsoft, centre de sécurité Microsoft 365
ms.prod: microsoft-365-enterprise
ms.mktglfcycl: deploy
ms.localizationpriority: medium
f1.keywords:
- NOCSH
ms.author: ellevin
author: levinec
manager: dansimp
audience: ITPro
ms.collection:
- M365-security-compliance
ms.topic: article
search.appverid:
- MOE150
- MET150
ms.custom:
- seo-marvel-apr2020
- seo-marvel-jun2020
ms.openlocfilehash: 0ba3d7a5e46f7e0f8677ce2844c5551bf70739e3
ms.sourcegitcommit: 001e64f89f9c3cd6bbd4a25459f5bee3b966820c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2020
ms.locfileid: "49367109"
---
# <a name="whats-new-in-microsoft-secure-score"></a><span data-ttu-id="eed4f-104">Nouveautés de Microsoft Secure score</span><span class="sxs-lookup"><span data-stu-id="eed4f-104">What's new in Microsoft Secure Score</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

<span data-ttu-id="eed4f-105">Pour faire en sorte que Microsoft Secure score un meilleur représentant de votre position de sécurité, nous avons apporté des modifications.</span><span class="sxs-lookup"><span data-stu-id="eed4f-105">To make Microsoft Secure Score a better representative of your security posture, we have made some changes.</span></span> <span data-ttu-id="eed4f-106">Pour en savoir plus sur les modifications planifiées, consultez [la rubrique what’s from Microsoft Secure score ?](microsoft-secure-score-whats-coming.md).</span><span class="sxs-lookup"><span data-stu-id="eed4f-106">To learn about planned changes, see [What's coming in Microsoft Secure Score?](microsoft-secure-score-whats-coming.md).</span></span>

## <a name="november-2020"></a><span data-ttu-id="eed4f-107">Novembre 2020</span><span class="sxs-lookup"><span data-stu-id="eed4f-107">November 2020</span></span>

### <a name="added-3-services-related-improvement-actions-for-microsoft-defender-for-endpoint-previously-microsoft-defender-atp"></a><span data-ttu-id="eed4f-108">Ajout des trois actions d’amélioration liées aux services pour Microsoft Defender pour le point de terminaison (précédemment Microsoft Defender ATP) :</span><span class="sxs-lookup"><span data-stu-id="eed4f-108">Added 3 services-related improvement actions for Microsoft Defender for Endpoint (previously Microsoft Defender ATP):</span></span>

- <span data-ttu-id="eed4f-109">Corriger le chemin d’accès non quoted service pour les services Windows</span><span class="sxs-lookup"><span data-stu-id="eed4f-109">Fix unquoted service path for Windows services</span></span>
- <span data-ttu-id="eed4f-110">Modifier le chemin d’accès exécutable de service en un emplacement protégé courant</span><span class="sxs-lookup"><span data-stu-id="eed4f-110">Change service executable path to a common protected location</span></span>
- <span data-ttu-id="eed4f-111">Modifier le compte de service pour éviter le mot de passe mis en cache dans le Registre Windows</span><span class="sxs-lookup"><span data-stu-id="eed4f-111">Change service account to avoid cached password in windows registry</span></span>

## <a name="october-2020"></a><span data-ttu-id="eed4f-112">Octobre 2020</span><span class="sxs-lookup"><span data-stu-id="eed4f-112">October 2020</span></span>

### <a name="remove-improvement-action-related-to-microsoft-defender-for-endpoint"></a><span data-ttu-id="eed4f-113">Supprimer l’action d’amélioration liée à Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="eed4f-113">Remove improvement action related to Microsoft Defender for Endpoint</span></span>

- <span data-ttu-id="eed4f-114">Activer la vérification du contenu Web de l’application Windows Store SmartScreen de Microsoft Defender pour avertir</span><span class="sxs-lookup"><span data-stu-id="eed4f-114">Set Microsoft Defender SmartScreen Windows Store app web content checking to warn</span></span>

## <a name="august-2020"></a><span data-ttu-id="eed4f-115">Août 2020</span><span class="sxs-lookup"><span data-stu-id="eed4f-115">August 2020</span></span>

### <a name="updated-improvement-action-for-azure-active-directory"></a><span data-ttu-id="eed4f-116">Action d’amélioration mise à jour pour Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="eed4f-116">Updated improvement action for Azure Active Directory</span></span>

- <span data-ttu-id="eed4f-117">Activer la stratégie pour bloquer l’authentification héritée</span><span class="sxs-lookup"><span data-stu-id="eed4f-117">Enable policy to block legacy authentication</span></span>

## <a name="incompatibility-with-identity-secure-score-and-graph-api"></a><span data-ttu-id="eed4f-118">Incompatibilité avec le score de sécurité d’identité et l’API Graph</span><span class="sxs-lookup"><span data-stu-id="eed4f-118">Incompatibility with Identity Secure Score and Graph API</span></span>

<span data-ttu-id="eed4f-119">Dans la version récente de Microsoft Secure score, un modèle de notation amélioré a été publié.</span><span class="sxs-lookup"><span data-stu-id="eed4f-119">In the recent release of Microsoft Secure Score, an improved scoring model has been released.</span></span> <span data-ttu-id="eed4f-120">Ces modifications permettent d’obtenir une vue plus flexible et précise de votre position de sécurité.</span><span class="sxs-lookup"><span data-stu-id="eed4f-120">These changes allow for a more flexible and accurate view of your security posture.</span></span> <span data-ttu-id="eed4f-121">Toutefois, ces mises à jour ont rendu le score de sécurité Microsoft incompatible temporairement avec le score de sécurité d’identité et l’API Graph.</span><span class="sxs-lookup"><span data-stu-id="eed4f-121">However, these updates have made Microsoft Secure Score temporarily incompatible with Identity Secure Score and the Graph API.</span></span>

<span data-ttu-id="eed4f-122">Dans le temps, le score de sécurité d’identité et l’API Graph adopteront le nouveau modèle de notation.</span><span class="sxs-lookup"><span data-stu-id="eed4f-122">In time, Identity Secure Score and the Graph API will adopt the new scoring model.</span></span> <span data-ttu-id="eed4f-123">Jusqu’à ce moment, les clients verront les différences entre les scores communiqués par Microsoft Secure score, Identity Secure score et l’API Graph.</span><span class="sxs-lookup"><span data-stu-id="eed4f-123">Until then, customers will see differences in the scores reported by Microsoft Secure Score, Identity Secure Score, and the Graph API.</span></span> <span data-ttu-id="eed4f-124">Nous nous excusons des désagréments que cela peut entraîner et nous travaillons pour garantir que ces expériences sont plus compatibles à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="eed4f-124">We apologize for any inconvenience this causes, and are working to ensure these experiences are more compatible in the future.</span></span>

## <a name="updated-improvement-actions"></a><span data-ttu-id="eed4f-125">Actions d’amélioration mises à jour</span><span class="sxs-lookup"><span data-stu-id="eed4f-125">Updated improvement actions</span></span>

- <span data-ttu-id="eed4f-126">Ajout d’actions d’amélioration Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="eed4f-126">Added Azure Active Directory improvement actions</span></span>
- <span data-ttu-id="eed4f-127">Ajout de Microsoft Defender pour les actions d’amélioration de l’identité</span><span class="sxs-lookup"><span data-stu-id="eed4f-127">Added Microsoft Defender for Identity improvement actions</span></span>
- <span data-ttu-id="eed4f-128">Prise en charge des recommandations de sécurité pour la gestion des vulnérabilités de Microsoft Defender [& Vulnerability Management](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/next-gen-threat-and-vuln-mgt)</span><span class="sxs-lookup"><span data-stu-id="eed4f-128">Support for Microsoft Defender for Endpoint [Threat & Vulnerability Management](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/next-gen-threat-and-vuln-mgt) security recommendations</span></span>
    - <span data-ttu-id="eed4f-129">Toutes les recommandations de sécurité fournies par TVM sont désormais disponibles</span><span class="sxs-lookup"><span data-stu-id="eed4f-129">All released security recommendations supplied by TVM are now available</span></span>

## <a name="updated-interface-and-functionality"></a><span data-ttu-id="eed4f-130">Interface et fonctionnalité mises à jour</span><span class="sxs-lookup"><span data-stu-id="eed4f-130">Updated interface and functionality</span></span>

* <span data-ttu-id="eed4f-131">Toutes les nouvelles mesures et tendances pour les CISO et les discussions au niveau des prospects</span><span class="sxs-lookup"><span data-stu-id="eed4f-131">All new metrics and trends views for CISO and lead level discussions</span></span>
* <span data-ttu-id="eed4f-132">Nouvelles façons de suivre et d’évaluer votre score</span><span class="sxs-lookup"><span data-stu-id="eed4f-132">New ways to track and benchmark your score</span></span>
* <span data-ttu-id="eed4f-133">Meilleure approche et compréhension pour les régressions de score</span><span class="sxs-lookup"><span data-stu-id="eed4f-133">Better tracking and understanding for score regressions</span></span>
* <span data-ttu-id="eed4f-134">Filtrage, balisage, recherche et regroupement de vos actions d’amélioration</span><span class="sxs-lookup"><span data-stu-id="eed4f-134">Filter, tag, search, and group your improvement actions</span></span>
* <span data-ttu-id="eed4f-135">Gérer vos objectifs à venir à l’aide de projections de score et des actions planifiées</span><span class="sxs-lookup"><span data-stu-id="eed4f-135">Manage towards your future goals using score projections and planned actions</span></span>
* <span data-ttu-id="eed4f-136">Et bien plus encore !</span><span class="sxs-lookup"><span data-stu-id="eed4f-136">And more!</span></span>

## <a name="we-want-to-hear-from-you"></a><span data-ttu-id="eed4f-137">Nous souhaitons être informés</span><span class="sxs-lookup"><span data-stu-id="eed4f-137">We want to hear from you</span></span>

<span data-ttu-id="eed4f-138">Si vous rencontrez des problèmes, informez-le en publiant dans la communauté [Security, Privacy & Compliance](https://techcommunity.microsoft.com/t5/Security-Privacy-Compliance/bd-p/security_privacy) .</span><span class="sxs-lookup"><span data-stu-id="eed4f-138">If you have any issues, let us know by posting in the [Security, Privacy & Compliance](https://techcommunity.microsoft.com/t5/Security-Privacy-Compliance/bd-p/security_privacy) community.</span></span> <span data-ttu-id="eed4f-139">Nous Surveillez la communauté et vous fournirons de l’aide.</span><span class="sxs-lookup"><span data-stu-id="eed4f-139">We're monitoring the community and will provide help.</span></span>

## <a name="related-resources"></a><span data-ttu-id="eed4f-140">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="eed4f-140">Related resources</span></span>

- [<span data-ttu-id="eed4f-141">Évaluez votre posture de sécurité</span><span class="sxs-lookup"><span data-stu-id="eed4f-141">Assess your security posture</span></span>](microsoft-secure-score-improvement-actions.md)
- [<span data-ttu-id="eed4f-142">Suivi de votre historique de score sécurisé Microsoft et atteindre les objectifs</span><span class="sxs-lookup"><span data-stu-id="eed4f-142">Track your Microsoft Secure Score history and meet goals</span></span>](microsoft-secure-score-history-metrics-trends.md)
- [<span data-ttu-id="eed4f-143">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="eed4f-143">What's coming</span></span>](microsoft-secure-score-whats-coming.md)
