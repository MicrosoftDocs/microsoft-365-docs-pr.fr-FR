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
ms.collection:
- M365-subscription-management
- m365initiative-coredeploy
ms.custom: it-pro
description: La feuille de route pour configurer vos clients pour Microsoft 365.
ms.openlocfilehash: 0f1fa91bb81fd6cc87820f2b2d48e00e1b75a0c4
ms.sourcegitcommit: 9a764c2aed7338c37f6e92f5fb487f02b3c4dfa1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/13/2020
ms.locfileid: "48446006"
---
# <a name="tenant-roadmap-for-microsoft-365"></a><span data-ttu-id="ca11d-103">Feuille de route de client pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="ca11d-103">Tenant roadmap for Microsoft 365</span></span>

<span data-ttu-id="ca11d-104">Votre client Microsoft 365 est l’ensemble des services affectés à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="ca11d-104">Your Microsoft 365 tenant is the set of services assigned to your organization.</span></span> <span data-ttu-id="ca11d-105">En règle générale, ce client est associé à un ou plusieurs de vos noms de domaine DNS et agit comme un conteneur central pour différents abonnements et les licences que vous affectez aux comptes d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ca11d-105">Typically, this tenant is associated with one or more of your DNS domain names and acts as a central container for different subscriptions and the licenses within them that you assign to user accounts.</span></span>

<span data-ttu-id="ca11d-106">Lorsque vous créez un client Microsoft 365, affectez-le à un emplacement géographique spécifique.</span><span class="sxs-lookup"><span data-stu-id="ca11d-106">When you create a Microsoft 365 tenant, you assign it to a specific geographical location.</span></span> <span data-ttu-id="ca11d-107">Vous pouvez également disposer d’un client disposant de plusieurs emplacements géographiques et déplacer votre client d’un emplacement à un autre.</span><span class="sxs-lookup"><span data-stu-id="ca11d-107">You can also have a tenant with multiple geographical locations and move your tenant from one location to another.</span></span>

<span data-ttu-id="ca11d-108">Pour préparer votre client pour les services de base de mise en réseau et d’identité, il est essentiel de planifier et d’exécuter soigneusement votre configuration client.</span><span class="sxs-lookup"><span data-stu-id="ca11d-108">To get your tenant ready for the foundational services of networking and identity, it's critical to carefully plan and execute your tenant configuration.</span></span>

## <a name="plan"></a><span data-ttu-id="ca11d-109">Prévision</span><span class="sxs-lookup"><span data-stu-id="ca11d-109">Plan</span></span>

<span data-ttu-id="ca11d-110">Pour planifier l’implémentation de votre client, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="ca11d-110">To plan for your tenant implementation:</span></span>

- [<span data-ttu-id="ca11d-111">Comprendre les abonnements, les licences et les clients Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="ca11d-111">Understand subscriptions, licenses, and Azure Active Directory (Azure AD) tenants</span></span>](subscriptions-licenses-accounts-and-tenants-for-microsoft-cloud-offerings.md)
- [<span data-ttu-id="ca11d-112">Comprendre comment utiliser des certificats SSL tiers</span><span class="sxs-lookup"><span data-stu-id="ca11d-112">Understand how to use third-party SSL certificates</span></span>](plan-for-third-party-ssl-certificates.md)
- [<span data-ttu-id="ca11d-113">Comprendre comment un client Microsoft 365 est intégré à Azure AD services</span><span class="sxs-lookup"><span data-stu-id="ca11d-113">Understand the ways a Microsoft 365 tenant is integrated with Azure AD services</span></span>](integrated-apps-and-azure-ads.md)
- [<span data-ttu-id="ca11d-114">Planifier la prise en charge des applications clientes</span><span class="sxs-lookup"><span data-stu-id="ca11d-114">Plan for client app support</span></span>](microsoft-365-client-support-certificate-based-authentication.md)
- [<span data-ttu-id="ca11d-115">Déterminer comment utiliser l’authentification moderne hybride</span><span class="sxs-lookup"><span data-stu-id="ca11d-115">Determine how to use hybrid modern authentication</span></span>](hybrid-modern-auth-overview.md)
- [<span data-ttu-id="ca11d-116">Planifier les mises à niveau d’Office 2007 et d’Office 2010</span><span class="sxs-lookup"><span data-stu-id="ca11d-116">Plan for Office 2007 and Office 2010 upgrades</span></span>](plan-upgrade-previous-versions-office.md)
- [<span data-ttu-id="ca11d-117">Comprendre l’isolation du client</span><span class="sxs-lookup"><span data-stu-id="ca11d-117">Understand tenant isolation</span></span>](microsoft-365-tenant-isolation-overview.md)
- [<span data-ttu-id="ca11d-118">Obtenir des informations sur l’assurance de service Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="ca11d-118">Get the details on Microsoft 365 service assurance</span></span>](https://docs.microsoft.com/microsoft-365/compliance/service-assurance)

## <a name="deploy"></a><span data-ttu-id="ca11d-119">Déployer</span><span class="sxs-lookup"><span data-stu-id="ca11d-119">Deploy</span></span>

<span data-ttu-id="ca11d-120">Pour déployer votre client, [Ajoutez les domaines DNS](https://docs.microsoft.com/microsoft-365/admin/setup/add-domain) de votre organisation et utilisez les [guides de configuration dans le centre d’administration 365 de Microsoft](setup-guides-for-microsoft-365.md).</span><span class="sxs-lookup"><span data-stu-id="ca11d-120">To deploy your tenant, [add the DNS domains](https://docs.microsoft.com/microsoft-365/admin/setup/add-domain) for your organization and use the [setup guides in the Microsoft 365 admin center](setup-guides-for-microsoft-365.md).</span></span>

## <a name="tenants-with-multiple-geographic-locations"></a><span data-ttu-id="ca11d-121">Clients disposant de plusieurs emplacements géographiques</span><span class="sxs-lookup"><span data-stu-id="ca11d-121">Tenants with multiple geographic locations</span></span>

<span data-ttu-id="ca11d-122">Avec Microsoft 365 Multi-Geo, votre organisation peut étendre sa présence Microsoft 365 à plusieurs régions ou pays au sein de votre client existant.</span><span class="sxs-lookup"><span data-stu-id="ca11d-122">With Microsoft 365 Multi-Geo, your organization can expand its Microsoft 365 presence to multiple geographic regions and/or countries within your existing tenant.</span></span>

<span data-ttu-id="ca11d-123">Pour plus d’informations sur Microsoft 365 multi-géo, notamment sur la planification, la configuration et l’administration, [Démarrez ici](microsoft-365-multi-geo.md).</span><span class="sxs-lookup"><span data-stu-id="ca11d-123">For information about Microsoft 365 Multi-Geo, including how to plan, configure, and administer it, [start here](microsoft-365-multi-geo.md).</span></span>

## <a name="move-a-tenants-geographic-locations"></a><span data-ttu-id="ca11d-124">Déplacer les emplacements géographiques d’un client</span><span class="sxs-lookup"><span data-stu-id="ca11d-124">Move a tenant's geographic locations</span></span>

<span data-ttu-id="ca11d-125">Microsoft continue d’ouvrir les nouveaux emplacements géographiques des centres de régions centres (Centre de ressources) pour les services Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="ca11d-125">Microsoft continues to open new datacenter geographic locations (geos) for Microsoft 365 services.</span></span> <span data-ttu-id="ca11d-126">Ces nouveaux centres de régions centres ajoutent de la capacité et des ressources de calcul afin de prendre en charge la demande des clients et la croissance de l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="ca11d-126">These new datacenter geos add capacity and compute resources to support customer demand and usage growth.</span></span> <span data-ttu-id="ca11d-127">En outre, les nouvelles régions de centre de données permettent d'héberger des données dans la région pour les données client essentielles.</span><span class="sxs-lookup"><span data-stu-id="ca11d-127">Additionally, the new datacenter geos offer in-geo data residency for core customer data.</span></span>

<span data-ttu-id="ca11d-128">Pour plus d’informations sur la région de centre de données Microsoft 365, notamment sur la demande d’un déplacement de données géographiques, [commencez ici](moving-data-to-new-datacenter-geos.md).</span><span class="sxs-lookup"><span data-stu-id="ca11d-128">For information about Microsoft 365 datacenter geo, including how to request a geo data move, [start here](moving-data-to-new-datacenter-geos.md).</span></span>

## <a name="next-step"></a><span data-ttu-id="ca11d-129">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="ca11d-129">Next step</span></span>

<span data-ttu-id="ca11d-130">Démarrez votre planification client avec des [abonnements, des licences, des comptes et des clients](subscriptions-licenses-accounts-and-tenants-for-microsoft-cloud-offerings.md).</span><span class="sxs-lookup"><span data-stu-id="ca11d-130">Start your tenant planning with [Subscriptions, licenses, accounts, and tenants](subscriptions-licenses-accounts-and-tenants-for-microsoft-cloud-offerings.md).</span></span>

