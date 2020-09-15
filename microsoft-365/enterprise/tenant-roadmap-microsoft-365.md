---
title: Feuille de route de client pour Microsoft 365
f1.keywords:
- NOCSH
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 08/10/2020
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Normal
ms.collection: M365-subscription-management
ms.custom: it-pro
description: La feuille de route pour configurer vos clients pour Microsoft 365.
ms.openlocfilehash: 7834e8b7f9ff8a1b33f2f2a7ccc4a499e4da7c69
ms.sourcegitcommit: 13ae76220b4ad688438a5d1031a6e1b5300ffa23
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/15/2020
ms.locfileid: "47775146"
---
# <a name="tenant-roadmap-for-microsoft-365"></a><span data-ttu-id="83cf8-103">Feuille de route de client pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="83cf8-103">Tenant roadmap for Microsoft 365</span></span>

<span data-ttu-id="83cf8-104">Votre client Microsoft 365 est l’ensemble des services affectés à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="83cf8-104">Your Microsoft 365 tenant is the set of services assigned to your organization.</span></span> <span data-ttu-id="83cf8-105">En règle générale, ce client est associé à un ou plusieurs de vos noms de domaine DNS et agit comme un conteneur central pour différents abonnements et les licences que vous affectez aux comptes d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="83cf8-105">Typically, this tenant is associated with one or more of your DNS domain names and acts as a central container for different subscriptions and the licenses within them that you assign to user accounts.</span></span>

<span data-ttu-id="83cf8-106">Lorsque vous créez un client Microsoft 365, affectez-le à un emplacement géographique spécifique.</span><span class="sxs-lookup"><span data-stu-id="83cf8-106">When you create a Microsoft 365 tenant, you assign it to a specific geographical location.</span></span> <span data-ttu-id="83cf8-107">Vous pouvez également disposer d’un client disposant de plusieurs emplacements géographiques et déplacer votre client d’un emplacement à un autre.</span><span class="sxs-lookup"><span data-stu-id="83cf8-107">You can also have a tenant with multiple geographical locations and move your tenant from one location to another.</span></span>

<span data-ttu-id="83cf8-108">Pour préparer votre client pour les services de base de mise en réseau et d’identité, il est essentiel de planifier et d’exécuter soigneusement votre configuration client.</span><span class="sxs-lookup"><span data-stu-id="83cf8-108">To get your tenant ready for the foundational services of networking and identity, it's critical to carefully plan and execute your tenant configuration.</span></span>

## <a name="plan"></a><span data-ttu-id="83cf8-109">Prévision</span><span class="sxs-lookup"><span data-stu-id="83cf8-109">Plan</span></span>

<span data-ttu-id="83cf8-110">Pour planifier l’implémentation de votre client, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="83cf8-110">To plan for your tenant implementation:</span></span>

- [<span data-ttu-id="83cf8-111">Comprendre les abonnements, les licences et les clients Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="83cf8-111">Understand subscriptions, licenses, and Azure Active Directory (Azure AD) tenants</span></span>](subscriptions-licenses-accounts-and-tenants-for-microsoft-cloud-offerings.md)
- [<span data-ttu-id="83cf8-112">Comprendre comment utiliser des certificats SSL tiers</span><span class="sxs-lookup"><span data-stu-id="83cf8-112">Understand how to use third-party SSL certificates</span></span>](plan-for-third-party-ssl-certificates.md)
- [<span data-ttu-id="83cf8-113">Accéder aux guides de configuration dans le centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="83cf8-113">Access setup guides in the Microsoft 365 admin center</span></span>](setup-guides-for-microsoft-365.md)
- [<span data-ttu-id="83cf8-114">Comprendre comment un client Microsoft 365 est intégré à Azure AD services</span><span class="sxs-lookup"><span data-stu-id="83cf8-114">Understand the ways a Microsoft 365 tenant is integrated with Azure AD services</span></span>](integrated-apps-and-azure-ads.md)
- [<span data-ttu-id="83cf8-115">Planifier la prise en charge des applications clientes</span><span class="sxs-lookup"><span data-stu-id="83cf8-115">Plan for client app support</span></span>](microsoft-365-client-support-certificate-based-authentication.md)
- [<span data-ttu-id="83cf8-116">Déterminer comment utiliser l’authentification moderne hybride</span><span class="sxs-lookup"><span data-stu-id="83cf8-116">Determine how to use hybrid modern authentication</span></span>](hybrid-modern-auth-overview.md)
- [<span data-ttu-id="83cf8-117">Planifier les mises à niveau d’Office 2007 et d’Office 2010</span><span class="sxs-lookup"><span data-stu-id="83cf8-117">Plan for Office 2007 and Office 2010 upgrades</span></span>](plan-upgrade-previous-versions-office.md)
- [<span data-ttu-id="83cf8-118">Comprendre l’isolation du client</span><span class="sxs-lookup"><span data-stu-id="83cf8-118">Understand tenant isolation</span></span>](microsoft-365-tenant-isolation-overview.md)
- [<span data-ttu-id="83cf8-119">Obtenir des informations sur l’assurance de service Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="83cf8-119">Get the details on Microsoft 365 service assurance</span></span>](https://docs.microsoft.com/microsoft-365/compliance/service-assurance)

## <a name="deploy"></a><span data-ttu-id="83cf8-120">Déployer</span><span class="sxs-lookup"><span data-stu-id="83cf8-120">Deploy</span></span>

<span data-ttu-id="83cf8-121">Pour déployer votre client, [Ajoutez les domaines DNS](https://docs.microsoft.com/microsoft-365/admin/setup/add-domain) de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="83cf8-121">To deploy your tenant, [add the DNS domains](https://docs.microsoft.com/microsoft-365/admin/setup/add-domain) for your organization.</span></span>

## <a name="tenants-with-multiple-geographic-locations"></a><span data-ttu-id="83cf8-122">Clients disposant de plusieurs emplacements géographiques</span><span class="sxs-lookup"><span data-stu-id="83cf8-122">Tenants with multiple geographic locations</span></span>

<span data-ttu-id="83cf8-123">Avec Microsoft 365 Multi-Geo, votre organisation peut étendre sa présence Microsoft 365 à plusieurs régions ou pays au sein de votre client existant.</span><span class="sxs-lookup"><span data-stu-id="83cf8-123">With Microsoft 365 Multi-Geo, your organization can expand its Microsoft 365 presence to multiple geographic regions and/or countries within your existing tenant.</span></span>

<span data-ttu-id="83cf8-124">Pour plus d’informations sur Microsoft 365 multi-géo, notamment sur la planification, la configuration et l’administration, [Démarrez ici](microsoft-365-multi-geo.md).</span><span class="sxs-lookup"><span data-stu-id="83cf8-124">For information about Microsoft 365 Multi-Geo, including how to plan, configure, and administer it, [start here](microsoft-365-multi-geo.md).</span></span>

## <a name="move-a-tenants-geographic-locations"></a><span data-ttu-id="83cf8-125">Déplacer les emplacements géographiques d’un client</span><span class="sxs-lookup"><span data-stu-id="83cf8-125">Move a tenant's geographic locations</span></span>

<span data-ttu-id="83cf8-126">Microsoft continue d’ouvrir les nouveaux emplacements géographiques des centres de régions centres (Centre de ressources) pour les services Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="83cf8-126">Microsoft continues to open new datacenter geographic locations (geos) for Microsoft 365 services.</span></span> <span data-ttu-id="83cf8-127">Ces nouveaux centres de régions centres ajoutent de la capacité et des ressources de calcul afin de prendre en charge la demande des clients et la croissance de l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="83cf8-127">These new datacenter geos add capacity and compute resources to support customer demand and usage growth.</span></span> <span data-ttu-id="83cf8-128">En outre, les nouvelles régions de centre de données permettent d'héberger des données dans la région pour les données client essentielles.</span><span class="sxs-lookup"><span data-stu-id="83cf8-128">Additionally, the new datacenter geos offer in-geo data residency for core customer data.</span></span>

<span data-ttu-id="83cf8-129">Pour plus d’informations sur la région de centre de données Microsoft 365, notamment sur la demande d’un déplacement de données géographiques, [commencez ici](moving-data-to-new-datacenter-geos.md).</span><span class="sxs-lookup"><span data-stu-id="83cf8-129">For information about Microsoft 365 datacenter geo, including how to request a geo data move, [start here](moving-data-to-new-datacenter-geos.md).</span></span>

## <a name="next-step"></a><span data-ttu-id="83cf8-130">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="83cf8-130">Next step</span></span>

<span data-ttu-id="83cf8-131">Démarrez votre planification client avec des [abonnements, des licences, des comptes et des clients](subscriptions-licenses-accounts-and-tenants-for-microsoft-cloud-offerings.md).</span><span class="sxs-lookup"><span data-stu-id="83cf8-131">Start your tenant planning with [Subscriptions, licenses, accounts, and tenants](subscriptions-licenses-accounts-and-tenants-for-microsoft-cloud-offerings.md).</span></span>

