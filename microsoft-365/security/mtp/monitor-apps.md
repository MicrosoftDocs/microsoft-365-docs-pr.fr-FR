---
title: Rapports d' & de surveillance des applications-Centre de sécurité
description: Découvrez comment mieux comprendre l’utilisation des applications Cloud dans votre organisation. Inclut différents types d’applications, leur niveau de risque et des alertes.
keywords: sécurité, programmes malveillants, Microsoft 365, M365, centre de sécurité, moniteur, rapport, applications
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
- m365initiative-m365-defender
ms.topic: article
search.appverid: met150
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: dcb7997c8c248c2b4e7d16902b6ebdd7756ccd0b
ms.sourcegitcommit: 815229e39a0f905d9f06717f00dc82e2a028fa7c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2020
ms.locfileid: "48846627"
---
# <a name="app-monitoring-and-reporting-in-the-microsoft-365-security-center"></a><span data-ttu-id="7be2f-105">Surveillance et création de rapports sur les applications dans le centre de sécurité Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="7be2f-105">App monitoring and reporting in the Microsoft 365 security center</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="7be2f-106">Ces rapports fournissent plus d’informations sur la façon dont les applications Cloud sont utilisées dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="7be2f-106">These reports provide more insight into how cloud apps are being used in your organization.</span></span> <span data-ttu-id="7be2f-107">Inclut différents types d’applications, leur niveau de risque et des alertes.</span><span class="sxs-lookup"><span data-stu-id="7be2f-107">Includes different kinds of apps, their level of risk, and alerts.</span></span>

## <a name="monitor-email-accounts-at-risk"></a><span data-ttu-id="7be2f-108">Surveiller les comptes de messagerie à risque</span><span class="sxs-lookup"><span data-stu-id="7be2f-108">Monitor email accounts at risk</span></span>

<span data-ttu-id="7be2f-109">La protection de la **messagerie** affiche les comptes de messagerie à risque.</span><span class="sxs-lookup"><span data-stu-id="7be2f-109">**Email protection** shows email accounts at risk.</span></span> <span data-ttu-id="7be2f-110">Vous pouvez sélectionner un compte pour approfondir vos recherches dans le centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="7be2f-110">You can select an account to investigate further in Microsoft Defender Security Center.</span></span>

![Carte de protection de la messagerie](../../media/email-protection.png)

## <a name="monitor-app-permissions-granted-by-users"></a><span data-ttu-id="7be2f-112">Surveiller les autorisations d’application accordées par les utilisateurs</span><span class="sxs-lookup"><span data-stu-id="7be2f-112">Monitor app permissions granted by users</span></span>

<span data-ttu-id="7be2f-113">**Sécurité des applications Cloud : applications OAuth** répertorie les applications découvertes par la sécurité des applications Cloud auxquelles des autorisations ont été accordées par les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="7be2f-113">**Cloud App Security - OAuth apps** lists apps discovered by Cloud App Security that have been granted permissions by users.</span></span> <span data-ttu-id="7be2f-114">Le catalogue des risques de la sécurité des applications Cloud inclut plus de 16 000 applications évaluées à l’aide de plus de 70 facteurs de risque.</span><span class="sxs-lookup"><span data-stu-id="7be2f-114">Cloud App Security's risk catalog includes over 16,000 apps that are assessed using over 70 risk factors.</span></span>

<span data-ttu-id="7be2f-115">Les facteurs de risque commencent à partir d’informations générales, telles que l’éditeur de l’application.</span><span class="sxs-lookup"><span data-stu-id="7be2f-115">The risk factors start from general information, such as the app publisher.</span></span> <span data-ttu-id="7be2f-116">Il passe ensuite aux mesures et contrôles de sécurité, par exemple si l’application prend en charge le chiffrement au repos ou fournit un journal d’audit de l’activité de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7be2f-116">It then moves to security measures and controls, such as whether the app supports encryption at rest or provides an audit log of user activity.</span></span>

![Carte d’applications OAuth de sécurité d’application Cloud](../../media/cloud-app-security-oauth-apps.png)

## <a name="monitor-cloud-app-user-accounts"></a><span data-ttu-id="7be2f-118">Surveiller les comptes d’utilisateur d’application Cloud</span><span class="sxs-lookup"><span data-stu-id="7be2f-118">Monitor cloud app user accounts</span></span>

<span data-ttu-id="7be2f-119">**Comptes d’application Cloud pour vérifier les** comptes qui peuvent nécessiter votre attention.</span><span class="sxs-lookup"><span data-stu-id="7be2f-119">**Cloud app accounts for review** lists accounts that may require attention.</span></span>

![Carte de révision des comptes d’application Cloud](../../media/cloud-app-accounts-for-review.png)

## <a name="understand-which-cloud-apps-are-used"></a><span data-ttu-id="7be2f-121">Comprendre les applications Cloud utilisées</span><span class="sxs-lookup"><span data-stu-id="7be2f-121">Understand which cloud apps are used</span></span>

<span data-ttu-id="7be2f-122">Les **applications Cloud découvertes (catégories)** montrent quels types d’applications sont utilisées dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="7be2f-122">**Discovered cloud apps (categories)** show what kinds of apps are being used in your organization.</span></span> <span data-ttu-id="7be2f-123">Il se lie au tableau de bord de découverte dans le Cloud dans la sécurité des applications Cloud.</span><span class="sxs-lookup"><span data-stu-id="7be2f-123">It links to the Cloud Discovery dashboard in Cloud App Security.</span></span> <span data-ttu-id="7be2f-124">Pour plus d’informations, consultez la rubrique [QuickStart : utiliser des applications découvertes](https://docs.microsoft.com/cloud-app-security/discovered-apps).</span><span class="sxs-lookup"><span data-stu-id="7be2f-124">For more information, see [Quickstart: Work with discovered apps](https://docs.microsoft.com/cloud-app-security/discovered-apps).</span></span>  

![Carte des catégories d’applications Cloud découvertes](../../media/discovered-cloud-apps-categories.png)

## <a name="monitor-where-users-access-cloud-apps"></a><span data-ttu-id="7be2f-126">Surveiller l’emplacement où les utilisateurs accèdent aux applications Cloud</span><span class="sxs-lookup"><span data-stu-id="7be2f-126">Monitor where users access cloud apps</span></span>

<span data-ttu-id="7be2f-127">Les emplacements des activités de l' **application Cloud** indiquent où les utilisateurs accèdent aux applications Cloud.</span><span class="sxs-lookup"><span data-stu-id="7be2f-127">**Cloud app activity locations** show where users are accessing cloud apps.</span></span>

![Fiche des emplacements des activités de l’application Cloud](../../media/cloud-app-activity-locations.png)

## <a name="monitor-health-for-infrastructure-workloads"></a><span data-ttu-id="7be2f-129">Surveiller l’intégrité des charges de travail d’infrastructure</span><span class="sxs-lookup"><span data-stu-id="7be2f-129">Monitor health for infrastructure workloads</span></span>

<span data-ttu-id="7be2f-130">L’intégrité de l' **infrastructure** indique des alertes d’état d’intégrité pour les charges de travail d’infrastructure dans Azure Defender \*.</span><span class="sxs-lookup"><span data-stu-id="7be2f-130">**Infrastructure health** shows health status alerts for infrastructure workloads in Azure Defender\*.</span></span>

<span data-ttu-id="7be2f-131">Azure Defender \* fournit une gestion de sécurité unifiée et un Defender pour Office 365 sur des charges de travail locales et de Cloud.</span><span class="sxs-lookup"><span data-stu-id="7be2f-131">Azure Defender\* provides unified security management and Defender for Office 365 across on-premises and cloud workloads.</span></span> <span data-ttu-id="7be2f-132">Vous pouvez collecter, Rechercher et analyser des données de sécurité à partir de différentes sources, notamment des pare-feu et d’autres solutions partenaires.</span><span class="sxs-lookup"><span data-stu-id="7be2f-132">You can collect, search, and analyze security data from different sources, including firewalls and other partner solutions.</span></span>

<span data-ttu-id="7be2f-133">Pour plus d’informations, reportez-vous à [Azure Defender \* documentation](https://docs.microsoft.com/azure/security-center/).</span><span class="sxs-lookup"><span data-stu-id="7be2f-133">For more information, see [Azure Defender\* Documentation](https://docs.microsoft.com/azure/security-center/).</span></span>

![Carte d’intégrité de l’infrastructure](../../media/infrastructure-health.png)
