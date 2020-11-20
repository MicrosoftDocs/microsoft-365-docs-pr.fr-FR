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
ms.openlocfilehash: 6d1358da465bd7e31ca7b234f140aa8e48bb7508
ms.sourcegitcommit: aa8d2de6ffac0157fffd14d0ea7f51ef0c287607
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2020
ms.locfileid: "49373994"
---
# <a name="whats-new-in-microsoft-secure-score"></a><span data-ttu-id="4712d-104">Nouveautés de Microsoft Secure score</span><span class="sxs-lookup"><span data-stu-id="4712d-104">What's new in Microsoft Secure Score</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]

<span data-ttu-id="4712d-105">Pour faire en sorte que Microsoft Secure score un meilleur représentant de votre position de sécurité, nous avons apporté des modifications.</span><span class="sxs-lookup"><span data-stu-id="4712d-105">To make Microsoft Secure Score a better representative of your security posture, we have made some changes.</span></span> <span data-ttu-id="4712d-106">Pour en savoir plus sur les modifications planifiées, consultez [la rubrique what’s from Microsoft Secure score ?](microsoft-secure-score-whats-coming.md).</span><span class="sxs-lookup"><span data-stu-id="4712d-106">To learn about planned changes, see [What's coming in Microsoft Secure Score?](microsoft-secure-score-whats-coming.md).</span></span>

<span data-ttu-id="4712d-107">Vous pouvez trouver https://security.microsoft.com/securescore le score de sécurité Microsoft à l’adresse dans le [Centre de sécurité Microsoft 365](overview-security-center.md).</span><span class="sxs-lookup"><span data-stu-id="4712d-107">Microsoft Secure Score can be found at https://security.microsoft.com/securescore in the [Microsoft 365 security center](overview-security-center.md).</span></span>

## <a name="november-2020"></a><span data-ttu-id="4712d-108">Novembre 2020</span><span class="sxs-lookup"><span data-stu-id="4712d-108">November 2020</span></span>

### <a name="added-3-services-related-improvement-actions-for-microsoft-defender-for-endpoint-previously-microsoft-defender-atp"></a><span data-ttu-id="4712d-109">Ajout des trois actions d’amélioration liées aux services pour Microsoft Defender pour le point de terminaison (précédemment Microsoft Defender ATP) :</span><span class="sxs-lookup"><span data-stu-id="4712d-109">Added 3 services-related improvement actions for Microsoft Defender for Endpoint (previously Microsoft Defender ATP):</span></span>

- <span data-ttu-id="4712d-110">Corriger le chemin d’accès non quoted service pour les services Windows</span><span class="sxs-lookup"><span data-stu-id="4712d-110">Fix unquoted service path for Windows services</span></span>
- <span data-ttu-id="4712d-111">Modifier le chemin d’accès exécutable de service en un emplacement protégé courant</span><span class="sxs-lookup"><span data-stu-id="4712d-111">Change service executable path to a common protected location</span></span>
- <span data-ttu-id="4712d-112">Modifier le compte de service pour éviter le mot de passe mis en cache dans le Registre Windows</span><span class="sxs-lookup"><span data-stu-id="4712d-112">Change service account to avoid cached password in windows registry</span></span>

## <a name="october-2020"></a><span data-ttu-id="4712d-113">Octobre 2020</span><span class="sxs-lookup"><span data-stu-id="4712d-113">October 2020</span></span>

### <a name="remove-improvement-action-related-to-microsoft-defender-for-endpoint"></a><span data-ttu-id="4712d-114">Supprimer l’action d’amélioration liée à Microsoft Defender pour le point de terminaison</span><span class="sxs-lookup"><span data-stu-id="4712d-114">Remove improvement action related to Microsoft Defender for Endpoint</span></span>

- <span data-ttu-id="4712d-115">Activer la vérification du contenu Web de l’application Windows Store SmartScreen de Microsoft Defender pour avertir</span><span class="sxs-lookup"><span data-stu-id="4712d-115">Set Microsoft Defender SmartScreen Windows Store app web content checking to warn</span></span>

## <a name="august-2020"></a><span data-ttu-id="4712d-116">Août 2020</span><span class="sxs-lookup"><span data-stu-id="4712d-116">August 2020</span></span>

### <a name="updated-improvement-action-for-azure-active-directory"></a><span data-ttu-id="4712d-117">Action d’amélioration mise à jour pour Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="4712d-117">Updated improvement action for Azure Active Directory</span></span>

- <span data-ttu-id="4712d-118">Activer la stratégie pour bloquer l’authentification héritée</span><span class="sxs-lookup"><span data-stu-id="4712d-118">Enable policy to block legacy authentication</span></span>

## <a name="incompatibility-with-identity-secure-score-and-graph-api"></a><span data-ttu-id="4712d-119">Incompatibilité avec le score de sécurité d’identité et l’API Graph</span><span class="sxs-lookup"><span data-stu-id="4712d-119">Incompatibility with Identity Secure Score and Graph API</span></span>

<span data-ttu-id="4712d-120">Dans la version récente de Microsoft Secure score, un modèle de notation amélioré a été publié.</span><span class="sxs-lookup"><span data-stu-id="4712d-120">In the recent release of Microsoft Secure Score, an improved scoring model has been released.</span></span> <span data-ttu-id="4712d-121">Ces modifications permettent d’obtenir une vue plus flexible et précise de votre position de sécurité.</span><span class="sxs-lookup"><span data-stu-id="4712d-121">These changes allow for a more flexible and accurate view of your security posture.</span></span> <span data-ttu-id="4712d-122">Toutefois, ces mises à jour ont rendu le score de sécurité Microsoft incompatible temporairement avec le score de sécurité d’identité et l’API Graph.</span><span class="sxs-lookup"><span data-stu-id="4712d-122">However, these updates have made Microsoft Secure Score temporarily incompatible with Identity Secure Score and the Graph API.</span></span>

<span data-ttu-id="4712d-123">Dans le temps, le score de sécurité d’identité et l’API Graph adopteront le nouveau modèle de notation.</span><span class="sxs-lookup"><span data-stu-id="4712d-123">In time, Identity Secure Score and the Graph API will adopt the new scoring model.</span></span> <span data-ttu-id="4712d-124">Jusqu’à ce moment, les clients verront les différences entre les scores communiqués par Microsoft Secure score, Identity Secure score et l’API Graph.</span><span class="sxs-lookup"><span data-stu-id="4712d-124">Until then, customers will see differences in the scores reported by Microsoft Secure Score, Identity Secure Score, and the Graph API.</span></span> <span data-ttu-id="4712d-125">Nous nous excusons des désagréments que cela peut entraîner et nous travaillons pour garantir que ces expériences sont plus compatibles à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="4712d-125">We apologize for any inconvenience this causes, and are working to ensure these experiences are more compatible in the future.</span></span>

## <a name="updated-improvement-actions"></a><span data-ttu-id="4712d-126">Actions d’amélioration mises à jour</span><span class="sxs-lookup"><span data-stu-id="4712d-126">Updated improvement actions</span></span>

- <span data-ttu-id="4712d-127">Ajout d’actions d’amélioration Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="4712d-127">Added Azure Active Directory improvement actions</span></span>
- <span data-ttu-id="4712d-128">Ajout de Microsoft Defender pour les actions d’amélioration de l’identité</span><span class="sxs-lookup"><span data-stu-id="4712d-128">Added Microsoft Defender for Identity improvement actions</span></span>
- <span data-ttu-id="4712d-129">Prise en charge des recommandations de sécurité pour la gestion des vulnérabilités de Microsoft Defender [& Vulnerability Management](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/next-gen-threat-and-vuln-mgt)</span><span class="sxs-lookup"><span data-stu-id="4712d-129">Support for Microsoft Defender for Endpoint [Threat & Vulnerability Management](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/next-gen-threat-and-vuln-mgt) security recommendations</span></span>
    - <span data-ttu-id="4712d-130">Toutes les recommandations de sécurité fournies par TVM sont désormais disponibles</span><span class="sxs-lookup"><span data-stu-id="4712d-130">All released security recommendations supplied by TVM are now available</span></span>

## <a name="updated-interface-and-functionality"></a><span data-ttu-id="4712d-131">Interface et fonctionnalité mises à jour</span><span class="sxs-lookup"><span data-stu-id="4712d-131">Updated interface and functionality</span></span>

* <span data-ttu-id="4712d-132">Toutes les nouvelles mesures et tendances pour les CISO et les discussions au niveau des prospects</span><span class="sxs-lookup"><span data-stu-id="4712d-132">All new metrics and trends views for CISO and lead level discussions</span></span>
* <span data-ttu-id="4712d-133">Nouvelles façons de suivre et d’évaluer votre score</span><span class="sxs-lookup"><span data-stu-id="4712d-133">New ways to track and benchmark your score</span></span>
* <span data-ttu-id="4712d-134">Meilleure approche et compréhension pour les régressions de score</span><span class="sxs-lookup"><span data-stu-id="4712d-134">Better tracking and understanding for score regressions</span></span>
* <span data-ttu-id="4712d-135">Filtrage, balisage, recherche et regroupement de vos actions d’amélioration</span><span class="sxs-lookup"><span data-stu-id="4712d-135">Filter, tag, search, and group your improvement actions</span></span>
* <span data-ttu-id="4712d-136">Gérer vos objectifs à venir à l’aide de projections de score et des actions planifiées</span><span class="sxs-lookup"><span data-stu-id="4712d-136">Manage towards your future goals using score projections and planned actions</span></span>
* <span data-ttu-id="4712d-137">Et bien plus encore !</span><span class="sxs-lookup"><span data-stu-id="4712d-137">And more!</span></span>

## <a name="we-want-to-hear-from-you"></a><span data-ttu-id="4712d-138">Nous souhaitons être informés</span><span class="sxs-lookup"><span data-stu-id="4712d-138">We want to hear from you</span></span>

<span data-ttu-id="4712d-139">Si vous rencontrez des problèmes, informez-le en publiant dans la communauté [Security, Privacy & Compliance](https://techcommunity.microsoft.com/t5/Security-Privacy-Compliance/bd-p/security_privacy) .</span><span class="sxs-lookup"><span data-stu-id="4712d-139">If you have any issues, let us know by posting in the [Security, Privacy & Compliance](https://techcommunity.microsoft.com/t5/Security-Privacy-Compliance/bd-p/security_privacy) community.</span></span> <span data-ttu-id="4712d-140">Nous Surveillez la communauté et vous fournirons de l’aide.</span><span class="sxs-lookup"><span data-stu-id="4712d-140">We're monitoring the community and will provide help.</span></span>

## <a name="related-resources"></a><span data-ttu-id="4712d-141">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="4712d-141">Related resources</span></span>

- [<span data-ttu-id="4712d-142">Évaluez votre posture de sécurité</span><span class="sxs-lookup"><span data-stu-id="4712d-142">Assess your security posture</span></span>](microsoft-secure-score-improvement-actions.md)
- [<span data-ttu-id="4712d-143">Suivi de votre historique de score sécurisé Microsoft et atteindre les objectifs</span><span class="sxs-lookup"><span data-stu-id="4712d-143">Track your Microsoft Secure Score history and meet goals</span></span>](microsoft-secure-score-history-metrics-trends.md)
- [<span data-ttu-id="4712d-144">Nouveautés</span><span class="sxs-lookup"><span data-stu-id="4712d-144">What's coming</span></span>](microsoft-secure-score-whats-coming.md)
