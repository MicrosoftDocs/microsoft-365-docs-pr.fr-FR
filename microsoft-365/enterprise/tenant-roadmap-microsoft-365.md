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
ms.openlocfilehash: 540d1bc53ac06b85d22a8a60a62e51761e10339c
ms.sourcegitcommit: 19515d787246d38c4e0da579a767ce67b9dbc2bc
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2020
ms.locfileid: "47315752"
---
# <a name="tenant-roadmap-for-microsoft-365"></a><span data-ttu-id="9ad2a-103">Feuille de route de client pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="9ad2a-103">Tenant roadmap for Microsoft 365</span></span>

<span data-ttu-id="9ad2a-104">Votre client Microsoft 365 est l’ensemble des services affectés à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="9ad2a-104">Your Microsoft 365 tenant is the set of services assigned to your organization.</span></span> <span data-ttu-id="9ad2a-105">Ce client est généralement associé à un ou plusieurs de vos noms de domaine DNS et agit comme un conteneur central pour différents abonnements et les licences que vous affectez aux comptes d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9ad2a-105">This tenant is typically associated with one or more of your DNS domain names and acts as a central container for different subscriptions and the licenses within them that you assign to user accounts.</span></span> 

<span data-ttu-id="9ad2a-106">Lorsque vous créez un client Microsoft 365, affectez-le à un emplacement géographique spécifique.</span><span class="sxs-lookup"><span data-stu-id="9ad2a-106">When you create a Microsoft 365 tenant, you assign it to a specific geographical location.</span></span> <span data-ttu-id="9ad2a-107">Vous pouvez également disposer d’un client disposant de plusieurs emplacements géographiques et déplacer votre client d’un emplacement à un autre.</span><span class="sxs-lookup"><span data-stu-id="9ad2a-107">You can also have a tenant with multiple geographical locations and move your tenant from one location to another.</span></span>

<span data-ttu-id="9ad2a-108">Une configuration de client bien planifiée et exécutée est essentielle pour la préparer aux services de base de la mise en réseau et de l’identité.</span><span class="sxs-lookup"><span data-stu-id="9ad2a-108">A well-planned and executed tenant configuration is critical to getting it ready for the foundational services of networking and identity.</span></span>

## <a name="plan"></a><span data-ttu-id="9ad2a-109">Prévision</span><span class="sxs-lookup"><span data-stu-id="9ad2a-109">Plan</span></span>

<span data-ttu-id="9ad2a-110">Pour planifier l’implémentation de votre client, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="9ad2a-110">To plan for your tenant implementation:</span></span>

- [<span data-ttu-id="9ad2a-111">Comprendre les abonnements, les licences et les clients Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="9ad2a-111">Understand subscriptions, licenses, and Azure Active Directory (Azure AD) tenants</span></span>](subscriptions-licenses-accounts-and-tenants-for-microsoft-cloud-offerings.md)
- [<span data-ttu-id="9ad2a-112">Comprendre comment utiliser des certificats SSL tiers</span><span class="sxs-lookup"><span data-stu-id="9ad2a-112">Understand how to use third-party SSL certificates</span></span>](plan-for-third-party-ssl-certificates.md)
- [<span data-ttu-id="9ad2a-113">Accéder aux guides de configuration dans le centre d’administration Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="9ad2a-113">Access setup guides in the Microsoft 365 admin center</span></span>](setup-guides-for-microsoft-365.md)
- [<span data-ttu-id="9ad2a-114">Comprendre comment un client Microsoft 365 est intégré à Azure AD services</span><span class="sxs-lookup"><span data-stu-id="9ad2a-114">Understand the ways a Microsoft 365 tenant is integrated with Azure AD services</span></span>](integrated-apps-and-azure-ads.md)
- [<span data-ttu-id="9ad2a-115">Planifier la prise en charge des applications clientes</span><span class="sxs-lookup"><span data-stu-id="9ad2a-115">Plan for client app support</span></span>](microsoft-365-client-support-certificate-based-authentication.md)
- [<span data-ttu-id="9ad2a-116">Déterminer comment utiliser l’authentification moderne hybride</span><span class="sxs-lookup"><span data-stu-id="9ad2a-116">Determine how to use hybrid modern authentication</span></span>](hybrid-modern-auth-overview.md)
- [<span data-ttu-id="9ad2a-117">Planifier les mises à niveau d’Office 2007 et d’Office 2010</span><span class="sxs-lookup"><span data-stu-id="9ad2a-117">Plan for Office 2007 and Office 2010 upgrades</span></span>](plan-upgrade-previous-versions-office.md)
- [<span data-ttu-id="9ad2a-118">Comprendre l’isolation du client</span><span class="sxs-lookup"><span data-stu-id="9ad2a-118">Understand tenant isolation</span></span>](microsoft-365-tenant-isolation-overview.md)
- [<span data-ttu-id="9ad2a-119">Obtenir des informations sur l’assurance de service Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="9ad2a-119">Get the details on Microsoft 365 service assurance</span></span>](https://docs.microsoft.com/microsoft-365/compliance/service-assurance)

## <a name="deploy"></a><span data-ttu-id="9ad2a-120">Déployer</span><span class="sxs-lookup"><span data-stu-id="9ad2a-120">Deploy</span></span>

<span data-ttu-id="9ad2a-121">Pour déployer votre client, [Ajoutez les domaines DNS](https://docs.microsoft.com/microsoft-365/admin/setup/add-domain) de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="9ad2a-121">To deploy your tenant, [add the DNS domains](https://docs.microsoft.com/microsoft-365/admin/setup/add-domain) for your organization.</span></span>

## <a name="tenants-with-multiple-geographic-locations"></a><span data-ttu-id="9ad2a-122">Clients disposant de plusieurs emplacements géographiques</span><span class="sxs-lookup"><span data-stu-id="9ad2a-122">Tenants with multiple geographic locations</span></span>

<span data-ttu-id="9ad2a-123">Avec Microsoft 365 Multi-Geo, votre organisation peut étendre sa présence Microsoft 365 à plusieurs régions ou pays au sein de votre client existant.</span><span class="sxs-lookup"><span data-stu-id="9ad2a-123">With Microsoft 365 Multi-Geo, your organization can expand its Microsoft 365 presence to multiple geographic regions and/or countries within your existing tenant.</span></span>

<span data-ttu-id="9ad2a-124">[Commencez à comprendre](microsoft-365-multi-geo.md) , planifier, configurer et administrer avec Microsoft 365 multi-géo.</span><span class="sxs-lookup"><span data-stu-id="9ad2a-124">[Get started](microsoft-365-multi-geo.md) in understanding, planning, configuring, and then administering with Microsoft 365 Multi-Geo.</span></span>

## <a name="move-a-tenants-geographic-locations"></a><span data-ttu-id="9ad2a-125">Déplacer les emplacements géographiques d’un client</span><span class="sxs-lookup"><span data-stu-id="9ad2a-125">Move a tenant's geographic locations</span></span>

<span data-ttu-id="9ad2a-126">Microsoft continue d’ouvrir les nouveaux emplacements géographiques des centres de régions centres (Centre de ressources) pour les services Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="9ad2a-126">Microsoft continues to open new datacenter geographic locations (geos) for Microsoft 365 services.</span></span> <span data-ttu-id="9ad2a-127">Ces nouveaux centres de régions centres ajoutent de la capacité et des ressources de calcul afin de prendre en charge la demande des clients et la croissance de l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="9ad2a-127">These new datacenter geos add capacity and compute resources to support customer demand and usage growth.</span></span> <span data-ttu-id="9ad2a-128">En outre, les nouvelles régions de centre de données permettent d'héberger des données dans la région pour les données client essentielles.</span><span class="sxs-lookup"><span data-stu-id="9ad2a-128">Additionally, the new datacenter geos offer in-geo data residency for core customer data.</span></span>

<span data-ttu-id="9ad2a-129">Prise en main de la compréhension et de la demande d’un déplacement de données géographiques avec [déplacement de données principales vers le nouveau centre de données Microsoft 365](moving-data-to-new-datacenter-geos.md).</span><span class="sxs-lookup"><span data-stu-id="9ad2a-129">Get started in understanding and requesting a geo data move with [Moving core data to new Microsoft 365 datacenter geo](moving-data-to-new-datacenter-geos.md).</span></span>

## <a name="next-step"></a><span data-ttu-id="9ad2a-130">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="9ad2a-130">Next step</span></span>

<span data-ttu-id="9ad2a-131">Démarrez votre planification client avec des [abonnements, des licences, des comptes et des clients](subscriptions-licenses-accounts-and-tenants-for-microsoft-cloud-offerings.md).</span><span class="sxs-lookup"><span data-stu-id="9ad2a-131">Start your tenant planning with [Subscriptions, licenses, accounts, and tenants](subscriptions-licenses-accounts-and-tenants-for-microsoft-cloud-offerings.md).</span></span>

