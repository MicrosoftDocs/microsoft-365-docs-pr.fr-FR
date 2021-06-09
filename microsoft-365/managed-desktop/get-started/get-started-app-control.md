---
title: Prise en main du contrôle d’application
description: ''
keywords: Bureau géré Microsoft, Microsoft 365, service, documentation
ms.service: m365-md
author: jaimeo
ms.author: jaimeo
manager: laurawi
audience: ITpro
ms.topic: article
ms.localizationpriority: normal
ms.collection: M365-modern-desktop
ms.openlocfilehash: 431e6cb3b8d7ab7e1dd317918fab4821889c7d4e
ms.sourcegitcommit: 583fd1ac1f385c58b93bda648907a1bd8e0a1950
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/28/2020
ms.locfileid: "45430458"
---
# <a name="get-started-with-app-control"></a><span data-ttu-id="1cc52-103">Prise en main du contrôle d’application</span><span class="sxs-lookup"><span data-stu-id="1cc52-103">Get started with app control</span></span>

<span data-ttu-id="1cc52-104">Avant d’activer le contrôle d’application dans votre environnement, n’oubliez pas de passer en revue et de comprendre comment Bureau géré Microsoft l’implémente, ainsi que vos [rôles](../service-description/app-control.md) et responsabilités.</span><span class="sxs-lookup"><span data-stu-id="1cc52-104">Before you enable app control in your environment, be sure to review and understand [how Microsoft Managed Desktop implements it](../service-description/app-control.md) and your roles and responsibilities.</span></span>

<span data-ttu-id="1cc52-105">Bureau géré Microsoft simplifie le contrôle des applications en prenant en charge les aspects les plus complexes liés à l’obtention d’une stratégie de base sécurisée.</span><span class="sxs-lookup"><span data-stu-id="1cc52-105">Microsoft Managed Desktop simplifies app control by taking care of the more challenging aspects of getting a secure base policy.</span></span> <span data-ttu-id="1cc52-106">Vos administrateurs informatiques doivent toujours tester vos applications dans l’anneau Test et consulter les journaux pour y trouver des avertissements ou des erreurs.</span><span class="sxs-lookup"><span data-stu-id="1cc52-106">Your IT Administrators must still test your apps in the Test ring and review the logs for any warnings or errors.</span></span> <span data-ttu-id="1cc52-107">Si une application a besoin d’une exemption, vous pouvez déposer une demande, ou Bureau géré Microsoft operation peut, selon qui la détecte en premier.</span><span class="sxs-lookup"><span data-stu-id="1cc52-107">If an app needs an exemption, you can file a request, or Microsoft Managed Desktop Operation might, depending on who detects it first.</span></span>

## <a name="initial-deployment-of-apps"></a><span data-ttu-id="1cc52-108">Déploiement initial des applications</span><span class="sxs-lookup"><span data-stu-id="1cc52-108">Initial deployment of apps</span></span>

<span data-ttu-id="1cc52-109">Lorsque vous déployez des applications pour la première fois, Bureau géré Microsoft devez évaluer leur comportement actuel.</span><span class="sxs-lookup"><span data-stu-id="1cc52-109">When you first deploy apps, Microsoft Managed Desktop needs to assess their current behavior.</span></span> <span data-ttu-id="1cc52-110">Les étapes exactes d’activation du contrôle d’application varient selon que des appareils ont déjà été déployés dans votre environnement.</span><span class="sxs-lookup"><span data-stu-id="1cc52-110">The exact steps for enabling app control depend on whether devices have already been deployed in your environment.</span></span>

### <a name="devices-not-yet-in-use"></a><span data-ttu-id="1cc52-111">Appareils pas encore utilisés</span><span class="sxs-lookup"><span data-stu-id="1cc52-111">Devices not yet in use</span></span>

<span data-ttu-id="1cc52-112">Si vous n’avez pas encore d’appareils en cours d’utilisation, ouvrez un ticket de service avec Bureau géré Microsoft Operations demandant que nous ouvrez le contrôle d’application.</span><span class="sxs-lookup"><span data-stu-id="1cc52-112">If you don't yet have any devices in use, open a service ticket with Microsoft Managed Desktop Operations requesting that we turn on app control.</span></span> <span data-ttu-id="1cc52-113">Les opérations déploieront progressivement des stratégies dans des groupes de déploiement en suivant cette planification :</span><span class="sxs-lookup"><span data-stu-id="1cc52-113">Operations will progressively deploy policies to deployment groups following this schedule:</span></span>

|<span data-ttu-id="1cc52-114">Groupe de déploiement</span><span class="sxs-lookup"><span data-stu-id="1cc52-114">Deployment group</span></span>  |<span data-ttu-id="1cc52-115">Type de stratégie</span><span class="sxs-lookup"><span data-stu-id="1cc52-115">Policy type</span></span>  |<span data-ttu-id="1cc52-116">Calendrier</span><span class="sxs-lookup"><span data-stu-id="1cc52-116">Timing</span></span>  |
|---------|---------|---------|
|<span data-ttu-id="1cc52-117">Tester</span><span class="sxs-lookup"><span data-stu-id="1cc52-117">Test</span></span>     |  <span data-ttu-id="1cc52-118">Audit</span><span class="sxs-lookup"><span data-stu-id="1cc52-118">Audit</span></span>       |  <span data-ttu-id="1cc52-119">Jour 0</span><span class="sxs-lookup"><span data-stu-id="1cc52-119">Day 0</span></span>       |
|<span data-ttu-id="1cc52-120">Premier</span><span class="sxs-lookup"><span data-stu-id="1cc52-120">First</span></span>     | <span data-ttu-id="1cc52-121">Enforced</span><span class="sxs-lookup"><span data-stu-id="1cc52-121">Enforced</span></span>        | <span data-ttu-id="1cc52-122">Jour 1</span><span class="sxs-lookup"><span data-stu-id="1cc52-122">Day 1</span></span>        |
|<span data-ttu-id="1cc52-123">Rapide</span><span class="sxs-lookup"><span data-stu-id="1cc52-123">Fast</span></span>     | <span data-ttu-id="1cc52-124">Enforced</span><span class="sxs-lookup"><span data-stu-id="1cc52-124">Enforced</span></span>        |  <span data-ttu-id="1cc52-125">Jour 2</span><span class="sxs-lookup"><span data-stu-id="1cc52-125">Day 2</span></span>       |
|<span data-ttu-id="1cc52-126">Larges</span><span class="sxs-lookup"><span data-stu-id="1cc52-126">Broad</span></span>     | <span data-ttu-id="1cc52-127">Enforced</span><span class="sxs-lookup"><span data-stu-id="1cc52-127">Enforced</span></span>        |  <span data-ttu-id="1cc52-128">Jour 3</span><span class="sxs-lookup"><span data-stu-id="1cc52-128">Day 3</span></span>       |

<span data-ttu-id="1cc52-129">Vous pouvez toujours ouvrir une autre demande de service pour suspendre ou revenir en arrière une partie de ce déploiement à tout moment pendant le déploiement.</span><span class="sxs-lookup"><span data-stu-id="1cc52-129">You can always open another service request to pause or roll back part of this deployment at any time during the rollout.</span></span>

### <a name="devices-already-in-use"></a><span data-ttu-id="1cc52-130">Appareils déjà utilisés</span><span class="sxs-lookup"><span data-stu-id="1cc52-130">Devices already in use</span></span>

<span data-ttu-id="1cc52-131">Si vous avez déjà au moins Bureau géré Microsoft appareil en cours d’utilisation, suivez les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="1cc52-131">If already have at least one Microsoft Managed Desktop device in use, follow these steps:</span></span>

1. <span data-ttu-id="1cc52-132">Ouvrez un ticket de service avec Bureau géré Microsoft Operations demandant que nous ouvrez le contrôle d’application.</span><span class="sxs-lookup"><span data-stu-id="1cc52-132">Open a service ticket with Microsoft Managed Desktop Operations requesting that we turn on app control.</span></span> <span data-ttu-id="1cc52-133">Les opérations déploient une [stratégie d’audit](../service-description/app-control.md#audit-policy) sur tous les appareils.</span><span class="sxs-lookup"><span data-stu-id="1cc52-133">Operations will deploy an [Audit policy](../service-description/app-control.md#audit-policy) to all devices.</span></span>
2. <span data-ttu-id="1cc52-134">[Testez vos applications](../working-with-managed-desktop/work-with-app-control.md#add-a-new-app) pour voir si certaines d’entre elles sont bloquées.</span><span class="sxs-lookup"><span data-stu-id="1cc52-134">[Test your applications](../working-with-managed-desktop/work-with-app-control.md#add-a-new-app) to see if any would be blocked.</span></span> <span data-ttu-id="1cc52-135">Si une application est bloquée, ouvrez une demande [de signataire.](../working-with-managed-desktop/work-with-app-control.md#add-or-remove-a-trusted-signer)</span><span class="sxs-lookup"><span data-stu-id="1cc52-135">If an application would be blocked, open a [signer request](../working-with-managed-desktop/work-with-app-control.md#add-or-remove-a-trusted-signer).</span></span> 
3. <span data-ttu-id="1cc52-136">Une fois que vous avez terminé vos tests (quels que soient les résultats), informez les opérations, en notant les demandes de signataire en attente.</span><span class="sxs-lookup"><span data-stu-id="1cc52-136">Once you have completed your testing (whatever the results), notify Operations, noting any pending signer requests.</span></span> <span data-ttu-id="1cc52-137">Les opérations déploieront progressivement des stratégies dans des groupes de déploiement en suivant cette planification :</span><span class="sxs-lookup"><span data-stu-id="1cc52-137">Operations will progressively deploy policies to deployment groups following this schedule:</span></span>

|<span data-ttu-id="1cc52-138">Groupe de déploiement</span><span class="sxs-lookup"><span data-stu-id="1cc52-138">Deployment group</span></span>  |<span data-ttu-id="1cc52-139">Type de stratégie</span><span class="sxs-lookup"><span data-stu-id="1cc52-139">Policy type</span></span>  |<span data-ttu-id="1cc52-140">Calendrier</span><span class="sxs-lookup"><span data-stu-id="1cc52-140">Timing</span></span>  |
|---------|---------|---------|
|<span data-ttu-id="1cc52-141">Tester</span><span class="sxs-lookup"><span data-stu-id="1cc52-141">Test</span></span>     |  <span data-ttu-id="1cc52-142">Audit</span><span class="sxs-lookup"><span data-stu-id="1cc52-142">Audit</span></span>       |  <span data-ttu-id="1cc52-143">Jour 0</span><span class="sxs-lookup"><span data-stu-id="1cc52-143">Day 0</span></span>       |
|<span data-ttu-id="1cc52-144">Premier</span><span class="sxs-lookup"><span data-stu-id="1cc52-144">First</span></span>     | <span data-ttu-id="1cc52-145">Enforced</span><span class="sxs-lookup"><span data-stu-id="1cc52-145">Enforced</span></span>        | <span data-ttu-id="1cc52-146">Jour 1</span><span class="sxs-lookup"><span data-stu-id="1cc52-146">Day 1</span></span>        |
|<span data-ttu-id="1cc52-147">Rapide</span><span class="sxs-lookup"><span data-stu-id="1cc52-147">Fast</span></span>     | <span data-ttu-id="1cc52-148">Enforced</span><span class="sxs-lookup"><span data-stu-id="1cc52-148">Enforced</span></span>        |  <span data-ttu-id="1cc52-149">Suspendu, déploiement sur demande</span><span class="sxs-lookup"><span data-stu-id="1cc52-149">Paused, rollout on request</span></span>       |
|<span data-ttu-id="1cc52-150">Larges</span><span class="sxs-lookup"><span data-stu-id="1cc52-150">Broad</span></span>     | <span data-ttu-id="1cc52-151">Enforced</span><span class="sxs-lookup"><span data-stu-id="1cc52-151">Enforced</span></span>        |  <span data-ttu-id="1cc52-152">Suspendu, déploiement sur demande</span><span class="sxs-lookup"><span data-stu-id="1cc52-152">Paused, rollout on request</span></span>       |

<span data-ttu-id="1cc52-153">Vous pouvez toujours ouvrir une autre demande de service pour suspendre ou revenir en arrière une partie de ce déploiement à tout moment pendant le déploiement.</span><span class="sxs-lookup"><span data-stu-id="1cc52-153">You can always open another service request to pause or roll back part of this deployment at any time during the rollout.</span></span>



