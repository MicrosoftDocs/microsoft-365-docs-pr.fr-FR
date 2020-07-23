---
title: Exemples de configuration des canaux de déploiement et de mise à jour
author: JoeDavies-MSFT
f1.keywords:
- NOCSH
ms.author: josephd
manager: laurawi
ms.date: 07/21/2020
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- Strat_O365_Enterprise
- M365-subscription-management
ms.custom: ''
description: Comment des exemples d’organisation procèdent au déploiement et à la mise à jour des versions à l’aide de canaux.
ms.openlocfilehash: eaf962d7481027b49f26c79163aaae3753fdbb9b
ms.sourcegitcommit: a08103bc120bdec7cfeaf67c1be4e221241e69ad
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/21/2020
ms.locfileid: "45200109"
---
# <a name="deployment-and-update-channel-example-configurations"></a><span data-ttu-id="e4d79-103">Exemples de configuration des canaux de déploiement et de mise à jour</span><span class="sxs-lookup"><span data-stu-id="e4d79-103">Deployment and update channel example configurations</span></span>

<span data-ttu-id="e4d79-104">Le choix des canaux de mise à jour à utiliser pour Windows 10 et Microsoft 365 Apps peut dépendre de votre type d’organisation et de la phase du cycle de développement pendant laquelle vous voulez déployer et utiliser de nouvelles fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="e4d79-104">Choosing which update channels to use for Windows 10 and Microsoft 365 Apps can depend on your type of organization and where on the development cycle you want to be deploying and using new features and capabilities.</span></span> <span data-ttu-id="e4d79-105">Trouvez les canaux de préversion et de production qui conviennent le mieux à vos besoins.</span><span class="sxs-lookup"><span data-stu-id="e4d79-105">Find the pre-release and production channels that best fit your needs.</span></span>

## <a name="pre-release-channels"></a><span data-ttu-id="e4d79-106">Canaux de préversion</span><span class="sxs-lookup"><span data-stu-id="e4d79-106">Pre-release channels</span></span>

| <span data-ttu-id="e4d79-107">Offre client/canal</span><span class="sxs-lookup"><span data-stu-id="e4d79-107">Customer/Channel Offering</span></span> | <span data-ttu-id="e4d79-108">Windows 10</span><span class="sxs-lookup"><span data-stu-id="e4d79-108">Windows 10</span></span> | <span data-ttu-id="e4d79-109">Microsoft 365 Apps for Enterprise (Windows 10)</span><span class="sxs-lookup"><span data-stu-id="e4d79-109">Microsoft 365 Apps for Enterprise (Windows 10)</span></span> |
|:-------|:-------|:-----|
| <span data-ttu-id="e4d79-110">Idéal pour les utilisateurs techniquement expérimentés et les développeurs.</span><span class="sxs-lookup"><span data-stu-id="e4d79-110">Right for highly technical users and developers.</span></span> <br><br> <span data-ttu-id="e4d79-111">Accédez en avant-première aux derniers builds au plus tôt dans le cycle de développement, avec le code le plus récent.</span><span class="sxs-lookup"><span data-stu-id="e4d79-111">Be the first to access the latest builds earliest in the development cycle with the newest code.</span></span> <br><br> <span data-ttu-id="e4d79-112">Certains aspects ne seront pas finalisés et les builds peuvent être instables.</span><span class="sxs-lookup"><span data-stu-id="e4d79-112">There will be rough edges and some instability.</span></span> | <span data-ttu-id="e4d79-113">Dev</span><span class="sxs-lookup"><span data-stu-id="e4d79-113">Dev</span></span> | <span data-ttu-id="e4d79-114">N/A</span><span class="sxs-lookup"><span data-stu-id="e4d79-114">N/A</span></span> |
| <span data-ttu-id="e4d79-115">Idéal pour les utilisateurs précoces et les informaticiens qui souhaitent accéder à des builds plus fiables toujours en cours de développement.</span><span class="sxs-lookup"><span data-stu-id="e4d79-115">Right for early adopters and IT Pros who want more reliable builds that are still in development.</span></span> <br><br> <span data-ttu-id="e4d79-116">Découvrez les nouvelles fonctionnalités et contribuez à les valider.</span><span class="sxs-lookup"><span data-stu-id="e4d79-116">See what’s coming up next and help validate new features.</span></span> | <span data-ttu-id="e4d79-117">Canal bêta</span><span class="sxs-lookup"><span data-stu-id="e4d79-117">Beta Channel</span></span> | <span data-ttu-id="e4d79-118">Canal bêta</span><span class="sxs-lookup"><span data-stu-id="e4d79-118">Beta Channel</span></span> |
| <span data-ttu-id="e4d79-119">Idéal pour les utilisateurs qui souhaitent accéder en avant-première aux prochaines versions.</span><span class="sxs-lookup"><span data-stu-id="e4d79-119">Right for those who want early access to upcoming releases.</span></span> <br><br> <span data-ttu-id="e4d79-120">Pour les entreprises qui découvrent et valident les versions à paraître avant leur déploiement à grande échelle.</span><span class="sxs-lookup"><span data-stu-id="e4d79-120">Where companies preview and validate upcoming releases before broad deployment.</span></span> <br><br> <span data-ttu-id="e4d79-121">Ces versions bénéficient d’un support.</span><span class="sxs-lookup"><span data-stu-id="e4d79-121">These are supported.</span></span> <br>  | <span data-ttu-id="e4d79-122">Préversion</span><span class="sxs-lookup"><span data-stu-id="e4d79-122">Release Preview</span></span> | <span data-ttu-id="e4d79-123">Canal actuel (préversion)</span><span class="sxs-lookup"><span data-stu-id="e4d79-123">Current Channel (Preview)</span></span> <br><br> <span data-ttu-id="e4d79-124">Canal Entreprise semestriel (préversion)</span><span class="sxs-lookup"><span data-stu-id="e4d79-124">Semi-Annual Enterprise Channel (Preview)</span></span>|
||||

## <a name="production-channels-for-broad-deployment"></a><span data-ttu-id="e4d79-125">Canaux de production pour un déploiement à grande échelle</span><span class="sxs-lookup"><span data-stu-id="e4d79-125">Production channels for broad deployment</span></span>

<span data-ttu-id="e4d79-126">Cliquez sur le lien dans la colonne **Exemple** pour passer en revue les groupes et étapes de déploiement d’un exemple d’organisation.</span><span class="sxs-lookup"><span data-stu-id="e4d79-126">Click the link in the **Example** column to step through deployment stages and groups for an example organization.</span></span>

| <span data-ttu-id="e4d79-127">Offre client/canal</span><span class="sxs-lookup"><span data-stu-id="e4d79-127">Customer/Channel Offering</span></span> | <span data-ttu-id="e4d79-128">Windows 10</span><span class="sxs-lookup"><span data-stu-id="e4d79-128">Windows 10</span></span> | <span data-ttu-id="e4d79-129">Microsoft 365 Apps for Enterprise (Windows 10)</span><span class="sxs-lookup"><span data-stu-id="e4d79-129">Microsoft 365 Apps for Enterprise (Windows 10)</span></span> | <span data-ttu-id="e4d79-130">Exemple</span><span class="sxs-lookup"><span data-stu-id="e4d79-130">Example</span></span> |
|:-------|:-------|:-----|:-------|
| <span data-ttu-id="e4d79-131">Idéal pour les clients qui souhaitent accéder aux dernières versions dès qu’elles sont prêtes.</span><span class="sxs-lookup"><span data-stu-id="e4d79-131">Right for customers who want the latest releases as soon as they are ready.</span></span> | <span data-ttu-id="e4d79-132">Canal semi-annuel</span><span class="sxs-lookup"><span data-stu-id="e4d79-132">Semi-Annual Channel</span></span> | [<span data-ttu-id="e4d79-133">Canal actuel</span><span class="sxs-lookup"><span data-stu-id="e4d79-133">Current Channel</span></span>](https://docs.microsoft.com/deployoffice/overview-update-channels#current-channel-overview) | [<span data-ttu-id="e4d79-134">Dernières versions</span><span class="sxs-lookup"><span data-stu-id="e4d79-134">Latest releases</span></span>](deploy-update-channels-examples-rapid-deploy.md) |
| <span data-ttu-id="e4d79-135">Idéal pour les entreprises qui souhaitent accéder à la dernière version avec une prévisibilité supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="e4d79-135">Right for enterprises who want the latest release with additional predictability.</span></span> | <span data-ttu-id="e4d79-136">Canal semi-annuel</span><span class="sxs-lookup"><span data-stu-id="e4d79-136">Semi-Annual Channel</span></span> | [<span data-ttu-id="e4d79-137">Canal Entreprise mensuel</span><span class="sxs-lookup"><span data-stu-id="e4d79-137">Monthly Enterprise Channel</span></span>](https://docs.microsoft.com/deployoffice/overview-update-channels#monthly-enterprise-channel-overview) |  |
| <span data-ttu-id="e4d79-138">Idéal pour les entreprises qui ont besoin d’effectuer des tests informatiques intensifs avant chaque mise à jour.</span><span class="sxs-lookup"><span data-stu-id="e4d79-138">Right for enterprises with need for extensive IT testing before each update.</span></span> | <span data-ttu-id="e4d79-139">Canal semi-annuel</span><span class="sxs-lookup"><span data-stu-id="e4d79-139">Semi-Annual Channel</span></span> | [<span data-ttu-id="e4d79-140">Canal Entreprise semestriel</span><span class="sxs-lookup"><span data-stu-id="e4d79-140">Semi-Annual Enterprise Channel</span></span>](https://docs.microsoft.com/deployoffice/overview-update-channels#semi-annual-enterprise-channel-overview) |  |
|||||


## <a name="see-also"></a><span data-ttu-id="e4d79-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e4d79-141">See also</span></span>

[<span data-ttu-id="e4d79-142">Guide de déploiement</span><span class="sxs-lookup"><span data-stu-id="e4d79-142">Deployment guide</span></span>](deploy-microsoft-365-enterprise.md)

[<span data-ttu-id="e4d79-143">Guides de laboratoire de test</span><span class="sxs-lookup"><span data-stu-id="e4d79-143">Test lab guides</span></span>](m365-enterprise-test-lab-guides.md)
