---
title: Analyse des applications & rapports - Centre de sécurité
description: Découvrez comment obtenir plus d’informations sur l’utilisation des applications cloud dans votre organisation. Inclut différents types d’applications, leur niveau de risque et les alertes.
keywords: sécurité, programmes malveillants, Microsoft 365, M365, centre de sécurité, surveiller, signaler, applications
ms.prod: m365-security
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
- m365initiative-m365-defender
ms.topic: article
search.appverid: met150
ms.custom: seo-marvel-apr2020
ms.technology: m365d
ms.openlocfilehash: ed5fcfc16c08272a6a1d55af210ab48528538048
ms.sourcegitcommit: 855719ee21017cf87dfa98cbe62806763bcb78ac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/22/2021
ms.locfileid: "49930521"
---
# <a name="app-monitoring-and-reporting-in-the-microsoft-365-security-center"></a><span data-ttu-id="d21a8-105">Surveillance des applications et rapports dans le Centre de sécurité Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="d21a8-105">App monitoring and reporting in the Microsoft 365 security center</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="d21a8-106">Ces rapports fournissent plus d’informations sur la façon dont les applications cloud sont utilisées dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="d21a8-106">These reports provide more insight into how cloud apps are being used in your organization.</span></span> <span data-ttu-id="d21a8-107">Inclut différents types d’applications, leur niveau de risque et les alertes.</span><span class="sxs-lookup"><span data-stu-id="d21a8-107">Includes different kinds of apps, their level of risk, and alerts.</span></span>

## <a name="monitor-email-accounts-at-risk"></a><span data-ttu-id="d21a8-108">Surveiller les comptes de messagerie à risque</span><span class="sxs-lookup"><span data-stu-id="d21a8-108">Monitor email accounts at risk</span></span>

<span data-ttu-id="d21a8-109">**La protection de la** messagerie affiche les comptes de messagerie à risque.</span><span class="sxs-lookup"><span data-stu-id="d21a8-109">**Email protection** shows email accounts at risk.</span></span> <span data-ttu-id="d21a8-110">Vous pouvez sélectionner un compte à examiner plus en détail dans le Centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="d21a8-110">You can select an account to investigate further in Microsoft Defender Security Center.</span></span>

![Carte de protection du courrier électronique](../../media/email-protection.png)

## <a name="monitor-app-permissions-granted-by-users"></a><span data-ttu-id="d21a8-112">Surveiller les autorisations d’application accordées par les utilisateurs</span><span class="sxs-lookup"><span data-stu-id="d21a8-112">Monitor app permissions granted by users</span></span>

<span data-ttu-id="d21a8-113">Sécurité des applications cloud : les applications **OAuth** répertorient les applications découvertes par Cloud App Security qui ont obtenu des autorisations par les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="d21a8-113">**Cloud App Security - OAuth apps** lists apps discovered by Cloud App Security that have been granted permissions by users.</span></span> <span data-ttu-id="d21a8-114">Le catalogue de risques de Cloud App Security inclut plus de 16 000 applications évaluées à l’aide de plus de 70 facteurs de risque.</span><span class="sxs-lookup"><span data-stu-id="d21a8-114">Cloud App Security's risk catalog includes over 16,000 apps that are assessed using over 70 risk factors.</span></span>

<span data-ttu-id="d21a8-115">Les facteurs de risque commencent par des informations générales, telles que l’éditeur d’application.</span><span class="sxs-lookup"><span data-stu-id="d21a8-115">The risk factors start from general information, such as the app publisher.</span></span> <span data-ttu-id="d21a8-116">Il passe ensuite aux mesures et contrôles de sécurité, par exemple si l’application prend en charge le chiffrement au repos ou fournit un journal d’audit de l’activité des utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="d21a8-116">It then moves to security measures and controls, such as whether the app supports encryption at rest or provides an audit log of user activity.</span></span>

![Carte d’application OAuth Cloud App Security](../../media/cloud-app-security-oauth-apps.png)

## <a name="monitor-cloud-app-user-accounts"></a><span data-ttu-id="d21a8-118">Surveiller les comptes d’utilisateur d’application cloud</span><span class="sxs-lookup"><span data-stu-id="d21a8-118">Monitor cloud app user accounts</span></span>

<span data-ttu-id="d21a8-119">**Les comptes d’application cloud pour la révision** répertorient les comptes qui peuvent nécessiter une attention particulière.</span><span class="sxs-lookup"><span data-stu-id="d21a8-119">**Cloud app accounts for review** lists accounts that may require attention.</span></span>

![Comptes d’application cloud pour la carte de révision](../../media/cloud-app-accounts-for-review.png)

## <a name="understand-which-cloud-apps-are-used"></a><span data-ttu-id="d21a8-121">Comprendre quelles applications cloud sont utilisées</span><span class="sxs-lookup"><span data-stu-id="d21a8-121">Understand which cloud apps are used</span></span>

<span data-ttu-id="d21a8-122">**Les applications cloud découvertes (catégories)** indiquent les types d’applications utilisés dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="d21a8-122">**Discovered cloud apps (categories)** show what kinds of apps are being used in your organization.</span></span> <span data-ttu-id="d21a8-123">Il est lié au tableau de bord de découverte cloud dans Cloud App Security.</span><span class="sxs-lookup"><span data-stu-id="d21a8-123">It links to the Cloud Discovery dashboard in Cloud App Security.</span></span> <span data-ttu-id="d21a8-124">Pour plus d’informations, [voir Démarrage rapide : Travailler avec les applications découvertes.](https://docs.microsoft.com/cloud-app-security/discovered-apps)</span><span class="sxs-lookup"><span data-stu-id="d21a8-124">For more information, see [Quickstart: Work with discovered apps](https://docs.microsoft.com/cloud-app-security/discovered-apps).</span></span>  

![Carte des catégories d’applications cloud découvertes](../../media/discovered-cloud-apps-categories.png)

## <a name="monitor-where-users-access-cloud-apps"></a><span data-ttu-id="d21a8-126">Surveiller l’endroit où les utilisateurs accèdent aux applications cloud</span><span class="sxs-lookup"><span data-stu-id="d21a8-126">Monitor where users access cloud apps</span></span>

<span data-ttu-id="d21a8-127">**Les emplacements d’activité des applications cloud** indiquent où les utilisateurs accèdent aux applications cloud.</span><span class="sxs-lookup"><span data-stu-id="d21a8-127">**Cloud app activity locations** show where users are accessing cloud apps.</span></span>

![Carte d’emplacements d’activité de l’application cloud](../../media/cloud-app-activity-locations.png)

## <a name="monitor-health-for-infrastructure-workloads"></a><span data-ttu-id="d21a8-129">Surveiller l’état des charges de travail d’infrastructure</span><span class="sxs-lookup"><span data-stu-id="d21a8-129">Monitor health for infrastructure workloads</span></span>

<span data-ttu-id="d21a8-130">**L’état de l’infrastructure** affiche des alertes d’état pour les charges de travail d’infrastructure dans Azure Defender.</span><span class="sxs-lookup"><span data-stu-id="d21a8-130">**Infrastructure health** shows health status alerts for infrastructure workloads in Azure Defender.</span></span>

<span data-ttu-id="d21a8-131">Azure Defender fournit une gestion unifiée de la sécurité et Defender pour Office 365 sur les charges de travail sur site et dans le cloud.</span><span class="sxs-lookup"><span data-stu-id="d21a8-131">Azure Defender provides unified security management and Defender for Office 365 across on-premises and cloud workloads.</span></span> <span data-ttu-id="d21a8-132">Vous pouvez collecter, rechercher et analyser des données de sécurité à partir de différentes sources, y compris des pare-feux et d’autres solutions partenaires.</span><span class="sxs-lookup"><span data-stu-id="d21a8-132">You can collect, search, and analyze security data from different sources, including firewalls and other partner solutions.</span></span>

<span data-ttu-id="d21a8-133">Pour plus d’informations, [voir la documentation d’Azure Defender.](https://docs.microsoft.com/azure/security-center/)</span><span class="sxs-lookup"><span data-stu-id="d21a8-133">For more information, see [Azure Defender Documentation](https://docs.microsoft.com/azure/security-center/).</span></span>

![Carte d’état de l’infrastructure](../../media/infrastructure-health.png)
