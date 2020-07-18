---
title: Prise en main du contrôle d’application
description: ''
keywords: Bureau géré Microsoft, Microsoft 365, service, documentation
ms.service: m365-md
author: jaimeo
ms.author: jaimeo
manager: laurawi
audience: ITpro
ms.topic: article
ms.localizationpriority: normal
ms.collection: M365-modern-desktop
ms.openlocfilehash: 12df7b074019ea47f2e293b71c6b0b25fe46f66f
ms.sourcegitcommit: 63887d742c59cc660fc85537b335e98a9dc66fbe
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/18/2020
ms.locfileid: "45170694"
---
# <a name="get-started-with-app-control"></a><span data-ttu-id="2cb18-103">Prise en main du contrôle d’application</span><span class="sxs-lookup"><span data-stu-id="2cb18-103">Get started with app control</span></span>

<span data-ttu-id="2cb18-104">Avant d’activer le contrôle d’application dans votre environnement, veillez à consulter et à comprendre [Comment Microsoft Managed Desktop l’implémente](../service-description/app-control.md) , ainsi que vos rôles et responsabilités.</span><span class="sxs-lookup"><span data-stu-id="2cb18-104">Before you enable app control in your environment, be sure to review and understand [how Microsoft Managed Desktop implements it](../service-description/app-control.md) and your roles and responsibilities.</span></span>

<span data-ttu-id="2cb18-105">Microsoft Managed Desktop simplifie le contrôle des applications en prenant en charge les aspects les plus délicats de l’obtention d’une stratégie de base sécurisée.</span><span class="sxs-lookup"><span data-stu-id="2cb18-105">Microsoft Managed Desktop simplifies app control by taking care of the more challenging aspects of getting a secure base policy.</span></span> <span data-ttu-id="2cb18-106">Vos administrateurs informatiques doivent toujours tester vos applications dans l’anneau de test et consulter les journaux pour rechercher des erreurs ou des avertissements.</span><span class="sxs-lookup"><span data-stu-id="2cb18-106">Your IT Administrators must still test your apps in the Test ring and review the logs for any warnings or errors.</span></span> <span data-ttu-id="2cb18-107">Si une application a besoin d’une exemption, vous pouvez classer une requête ou l’opération de bureau géré Microsoft peut, en fonction de qui la détecte au préalable.</span><span class="sxs-lookup"><span data-stu-id="2cb18-107">If an app needs an exemption, you can file a request, or Microsoft Managed Desktop Operation might, depending on who detects it first.</span></span>

## <a name="initial-deployment-of-apps"></a><span data-ttu-id="2cb18-108">Déploiement initial d’applications</span><span class="sxs-lookup"><span data-stu-id="2cb18-108">Initial deployment of apps</span></span>

<span data-ttu-id="2cb18-109">Lorsque vous déployez pour la première fois des applications, le bureau géré Microsoft doit évaluer son comportement actuel.</span><span class="sxs-lookup"><span data-stu-id="2cb18-109">When you first deploy apps, Microsoft Managed Desktop needs to assess their current behavior.</span></span> <span data-ttu-id="2cb18-110">Les étapes exactes d’activation du contrôle d’application varient selon que des appareils ont déjà été déployés dans votre environnement.</span><span class="sxs-lookup"><span data-stu-id="2cb18-110">The exact steps for enabling app control depend on whether devices have already been deployed in your environment.</span></span>

### <a name="devices-already-in-use"></a><span data-ttu-id="2cb18-111">Appareils déjà utilisés</span><span class="sxs-lookup"><span data-stu-id="2cb18-111">Devices already in use</span></span>

<span data-ttu-id="2cb18-112">Si au moins un périphérique de bureau géré Microsoft est déjà utilisé, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="2cb18-112">If already have at least one Microsoft Managed Desktop device in use, follow these steps:</span></span>

1. <span data-ttu-id="2cb18-113">Ouvrez un ticket de service avec les opérations de bureau géré Microsoft qui demandent que nous activions le contrôle des applications.</span><span class="sxs-lookup"><span data-stu-id="2cb18-113">Open a service ticket with Microsoft Managed Desktop Operations requesting that we turn on app control.</span></span> <span data-ttu-id="2cb18-114">Les opérations déploient une [stratégie d’audit](../service-description/app-control.md#audit-policy) sur tous les appareils.</span><span class="sxs-lookup"><span data-stu-id="2cb18-114">Operations will deploy an [Audit policy](../service-description/app-control.md#audit-policy) to all devices.</span></span>
2. <span data-ttu-id="2cb18-115">[Testez vos applications](../working-with-managed-desktop/work-with-app-control.md#add-a-new-app) pour déterminer si elles seraient bloquées.</span><span class="sxs-lookup"><span data-stu-id="2cb18-115">[Test your applications](../working-with-managed-desktop/work-with-app-control.md#add-a-new-app) to see if any would be blocked.</span></span> <span data-ttu-id="2cb18-116">Si une application est bloquée, ouvrez une [demande de signataire](../working-with-managed-desktop/work-with-app-control.md#add-or-remove-a-trusted-signer).</span><span class="sxs-lookup"><span data-stu-id="2cb18-116">If an application would be blocked, open a [signer request](../working-with-managed-desktop/work-with-app-control.md#add-or-remove-a-trusted-signer).</span></span> 
3. <span data-ttu-id="2cb18-117">Une fois que vous avez terminé le test (quel que soit le résultat), informez les opérations en notant les demandes de signataire en attente.</span><span class="sxs-lookup"><span data-stu-id="2cb18-117">Once you have completed your testing (whatever the results), notify Operations, noting any pending signer requests.</span></span> <span data-ttu-id="2cb18-118">Les opérations déploient progressivement des stratégies vers des groupes de déploiement suivant cette planification :</span><span class="sxs-lookup"><span data-stu-id="2cb18-118">Operations will progressively deploy policies to deployment groups following this schedule:</span></span>

|<span data-ttu-id="2cb18-119">Groupe de déploiement</span><span class="sxs-lookup"><span data-stu-id="2cb18-119">Deployment group</span></span>  |<span data-ttu-id="2cb18-120">Type de stratégie</span><span class="sxs-lookup"><span data-stu-id="2cb18-120">Policy type</span></span>  |<span data-ttu-id="2cb18-121">Calendrier</span><span class="sxs-lookup"><span data-stu-id="2cb18-121">Timing</span></span>  |
|---------|---------|---------|
|<span data-ttu-id="2cb18-122">Tester</span><span class="sxs-lookup"><span data-stu-id="2cb18-122">Test</span></span>     |  <span data-ttu-id="2cb18-123">Audit</span><span class="sxs-lookup"><span data-stu-id="2cb18-123">Audit</span></span>       |  <span data-ttu-id="2cb18-124">Jour 0</span><span class="sxs-lookup"><span data-stu-id="2cb18-124">Day 0</span></span>       |
|<span data-ttu-id="2cb18-125">Premier</span><span class="sxs-lookup"><span data-stu-id="2cb18-125">First</span></span>     | <span data-ttu-id="2cb18-126">Enforced</span><span class="sxs-lookup"><span data-stu-id="2cb18-126">Enforced</span></span>        | <span data-ttu-id="2cb18-127">Jour 1</span><span class="sxs-lookup"><span data-stu-id="2cb18-127">Day 1</span></span>        |
|<span data-ttu-id="2cb18-128">Rapide</span><span class="sxs-lookup"><span data-stu-id="2cb18-128">Fast</span></span>     | <span data-ttu-id="2cb18-129">Enforced</span><span class="sxs-lookup"><span data-stu-id="2cb18-129">Enforced</span></span>        |  <span data-ttu-id="2cb18-130">Jour 3</span><span class="sxs-lookup"><span data-stu-id="2cb18-130">Day 3</span></span>       |
|<span data-ttu-id="2cb18-131">Larges</span><span class="sxs-lookup"><span data-stu-id="2cb18-131">Broad</span></span>     | <span data-ttu-id="2cb18-132">Enforced</span><span class="sxs-lookup"><span data-stu-id="2cb18-132">Enforced</span></span>        |  <span data-ttu-id="2cb18-133">Jour 7</span><span class="sxs-lookup"><span data-stu-id="2cb18-133">Day 7</span></span>       |

<span data-ttu-id="2cb18-134">Vous pouvez toujours ouvrir une autre demande de service pour suspendre ou restaurer une partie de ce déploiement à tout moment pendant le déploiement.</span><span class="sxs-lookup"><span data-stu-id="2cb18-134">You can always open another service request to pause or roll back part of this deployment at any time during the rollout.</span></span>

### <a name="devices-not-yet-in-use"></a><span data-ttu-id="2cb18-135">Appareils qui ne sont pas encore utilisés</span><span class="sxs-lookup"><span data-stu-id="2cb18-135">Devices not yet in use</span></span>

<span data-ttu-id="2cb18-136">Si vous n’avez pas encore de périphériques en cours d’utilisation, ouvrez un ticket de service avec Microsoft Managed Desktop Operations demandant à activer le contrôle des applications.</span><span class="sxs-lookup"><span data-stu-id="2cb18-136">If you don't yet have any devices in use, open a service ticket with Microsoft Managed Desktop Operations requesting that we turn on app control.</span></span> <span data-ttu-id="2cb18-137">Les opérations déploient progressivement des stratégies vers des groupes de déploiement suivant cette planification :</span><span class="sxs-lookup"><span data-stu-id="2cb18-137">Operations will progressively deploy policies to deployment groups following this schedule:</span></span>

|<span data-ttu-id="2cb18-138">Groupe de déploiement</span><span class="sxs-lookup"><span data-stu-id="2cb18-138">Deployment group</span></span>  |<span data-ttu-id="2cb18-139">Type de stratégie</span><span class="sxs-lookup"><span data-stu-id="2cb18-139">Policy type</span></span>  |<span data-ttu-id="2cb18-140">Calendrier</span><span class="sxs-lookup"><span data-stu-id="2cb18-140">Timing</span></span>  |
|---------|---------|---------|
|<span data-ttu-id="2cb18-141">Tester</span><span class="sxs-lookup"><span data-stu-id="2cb18-141">Test</span></span>     |  <span data-ttu-id="2cb18-142">Audit</span><span class="sxs-lookup"><span data-stu-id="2cb18-142">Audit</span></span>       |  <span data-ttu-id="2cb18-143">Jour 0</span><span class="sxs-lookup"><span data-stu-id="2cb18-143">Day 0</span></span>       |
|<span data-ttu-id="2cb18-144">Premier</span><span class="sxs-lookup"><span data-stu-id="2cb18-144">First</span></span>     | <span data-ttu-id="2cb18-145">Enforced</span><span class="sxs-lookup"><span data-stu-id="2cb18-145">Enforced</span></span>        | <span data-ttu-id="2cb18-146">Jour 1</span><span class="sxs-lookup"><span data-stu-id="2cb18-146">Day 1</span></span>        |
|<span data-ttu-id="2cb18-147">Rapide</span><span class="sxs-lookup"><span data-stu-id="2cb18-147">Fast</span></span>     | <span data-ttu-id="2cb18-148">Enforced</span><span class="sxs-lookup"><span data-stu-id="2cb18-148">Enforced</span></span>        |  <span data-ttu-id="2cb18-149">Jour 3</span><span class="sxs-lookup"><span data-stu-id="2cb18-149">Day 3</span></span>       |
|<span data-ttu-id="2cb18-150">Larges</span><span class="sxs-lookup"><span data-stu-id="2cb18-150">Broad</span></span>     | <span data-ttu-id="2cb18-151">Enforced</span><span class="sxs-lookup"><span data-stu-id="2cb18-151">Enforced</span></span>        |  <span data-ttu-id="2cb18-152">Jour 7</span><span class="sxs-lookup"><span data-stu-id="2cb18-152">Day 7</span></span>       |

<span data-ttu-id="2cb18-153">Vous pouvez toujours ouvrir une autre demande de service pour suspendre ou restaurer une partie de ce déploiement à tout moment pendant le déploiement.</span><span class="sxs-lookup"><span data-stu-id="2cb18-153">You can always open another service request to pause or roll back part of this deployment at any time during the rollout.</span></span>

