---
title: Feuille de route du client pour Microsoft 365
f1.keywords:
- NOCSH
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Normal
ms.collection:
- M365-subscription-management
- m365initiative-coredeploy
ms.custom: it-pro
description: Feuille de route pour configurer vos clients pour Microsoft 365.
ms.openlocfilehash: d2640a036eedda0b0962a15a03dcf0211ea0209b
ms.sourcegitcommit: c84cceb07e748969723a31b350e37f3ec79255ab
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/09/2020
ms.locfileid: "48948396"
---
# <a name="tenant-roadmap-for-microsoft-365"></a><span data-ttu-id="11e07-103">Feuille de route du client pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="11e07-103">Tenant roadmap for Microsoft 365</span></span>

<span data-ttu-id="11e07-104">Votre client Microsoft 365 est l’ensemble des services affectés à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="11e07-104">Your Microsoft 365 tenant is the set of services assigned to your organization.</span></span> <span data-ttu-id="11e07-105">En règle générale, ce client est associé à un ou plusieurs de vos noms de domaine DNS publics et agit comme un conteneur central et isolé pour différents abonnements et les licences que vous attribuez aux comptes d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="11e07-105">Typically, this tenant is associated with one or more of your public DNS domain names and acts as a central and isolated container for different subscriptions and the licenses within them that you assign to user accounts.</span></span> <span data-ttu-id="11e07-106">Pour plus d’informations, voir [Subscriptions, licenses, accounts, and tenants for Microsoft’s cloud offerings](subscriptions-licenses-accounts-and-tenants-for-microsoft-cloud-offerings.md).</span><span class="sxs-lookup"><span data-stu-id="11e07-106">For more information, see [Subscriptions, licenses, accounts, and tenants for Microsoft's cloud offerings](subscriptions-licenses-accounts-and-tenants-for-microsoft-cloud-offerings.md).</span></span>

<span data-ttu-id="11e07-107">Lorsque vous créez un client Microsoft 365, vous l’affectez à un emplacement géographique spécifique.</span><span class="sxs-lookup"><span data-stu-id="11e07-107">When you create a Microsoft 365 tenant, you assign it to a specific geographical location.</span></span> <span data-ttu-id="11e07-108">Vous pouvez également avoir un client avec plusieurs emplacements géographiques et déplacer votre client d’un emplacement à un autre.</span><span class="sxs-lookup"><span data-stu-id="11e07-108">You can also have a tenant with multiple geographical locations and move your tenant from one location to another.</span></span>

<span data-ttu-id="11e07-109">Pour préparer votre client pour les utilisateurs, les groupes, les licences et les applications cloud, il est essentiel de planifier et d’exécuter avec soin la configuration de votre client.</span><span class="sxs-lookup"><span data-stu-id="11e07-109">To get your tenant ready for user, groups, licenses, and cloud apps, it's critical to carefully plan and execute your tenant configuration.</span></span>

## <a name="set-up-your-microsoft-365-tenant"></a><span data-ttu-id="11e07-110">Configurer votre client Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="11e07-110">Set up your Microsoft 365 tenant</span></span>

<span data-ttu-id="11e07-111">Une fois que vous vous êtes assuré que votre réseau est optimisé pour l’accès à Microsoft 365 pour les travailleurs locaux et distants, vos prochaines tâches importantes sont la planification et la configuration de votre client Microsoft 365 pour les noms de domaine DNS, les services communs et pour cette infrastructure d’identité qui prend en charge la connectez-vous utilisateur sécurisée.</span><span class="sxs-lookup"><span data-stu-id="11e07-111">After ensuring that your networking is optimized for access to Microsoft 365 for both on-premises and remote workers, your next big tasks are planning for and then configuring your Microsoft 365 tenant for DNS domain names, common services, and for that identity infrastructure that supports secure user sign-in.</span></span>

### <a name="plan"></a><span data-ttu-id="11e07-112">Planification</span><span class="sxs-lookup"><span data-stu-id="11e07-112">Plan</span></span>

<span data-ttu-id="11e07-113">Pour planifier l’implémentation de votre client :</span><span class="sxs-lookup"><span data-stu-id="11e07-113">To plan for your tenant implementation:</span></span>

- [<span data-ttu-id="11e07-114">Comprendre les abonnements, les licences et les locataires Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="11e07-114">Understand subscriptions, licenses, and Azure Active Directory (Azure AD) tenants</span></span>](subscriptions-licenses-accounts-and-tenants-for-microsoft-cloud-offerings.md)
- [<span data-ttu-id="11e07-115">Comprendre comment utiliser des certificats SSL tiers</span><span class="sxs-lookup"><span data-stu-id="11e07-115">Understand how to use third-party SSL certificates</span></span>](plan-for-third-party-ssl-certificates.md)
- [<span data-ttu-id="11e07-116">Comprendre la façon dont un client Microsoft 365 est intégré aux services Azure AD</span><span class="sxs-lookup"><span data-stu-id="11e07-116">Understand the ways a Microsoft 365 tenant is integrated with Azure AD services</span></span>](integrated-apps-and-azure-ads.md)
- [<span data-ttu-id="11e07-117">Planifier la prise en charge des applications clientes</span><span class="sxs-lookup"><span data-stu-id="11e07-117">Plan for client app support</span></span>](microsoft-365-client-support-certificate-based-authentication.md)
- [<span data-ttu-id="11e07-118">Déterminer comment utiliser l’authentification moderne hybride</span><span class="sxs-lookup"><span data-stu-id="11e07-118">Determine how to use hybrid modern authentication</span></span>](hybrid-modern-auth-overview.md)
- [<span data-ttu-id="11e07-119">Planifier les mises à niveau d’Office 2007 et d’Office 2010</span><span class="sxs-lookup"><span data-stu-id="11e07-119">Plan for Office 2007 and Office 2010 upgrades</span></span>](plan-upgrade-previous-versions-office.md)
- [<span data-ttu-id="11e07-120">Comprendre l’isolation du client</span><span class="sxs-lookup"><span data-stu-id="11e07-120">Understand tenant isolation</span></span>](microsoft-365-tenant-isolation-overview.md)

### <a name="deploy"></a><span data-ttu-id="11e07-121">Déployer</span><span class="sxs-lookup"><span data-stu-id="11e07-121">Deploy</span></span>

<span data-ttu-id="11e07-122">Pour déployer votre client :</span><span class="sxs-lookup"><span data-stu-id="11e07-122">To deploy your tenant:</span></span> 

- <span data-ttu-id="11e07-123">Ajoutez [les domaines DNS](https://docs.microsoft.com/microsoft-365/admin/setup/add-domain) pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="11e07-123">Add the [DNS domains](https://docs.microsoft.com/microsoft-365/admin/setup/add-domain) for your organization.</span></span>
- <span data-ttu-id="11e07-124">Utilisez les [guides de configuration dans le Centre d’administration Microsoft 365.](setup-guides-for-microsoft-365.md)</span><span class="sxs-lookup"><span data-stu-id="11e07-124">Use the [setup guides in the Microsoft 365 admin center](setup-guides-for-microsoft-365.md).</span></span>
- <span data-ttu-id="11e07-125">Créez votre [infrastructure d’identité](identity-roadmap-microsoft-365.md) [et sécurisation de vos utilisateurs.](microsoft-365-secure-sign-in.md)</span><span class="sxs-lookup"><span data-stu-id="11e07-125">Build out your [identity infrastructure](identity-roadmap-microsoft-365.md) and [secure your user sign-ins](microsoft-365-secure-sign-in.md).</span></span>

### <a name="move-a-tenants-geographic-locations"></a><span data-ttu-id="11e07-126">Déplacer les emplacements géographiques d’un client</span><span class="sxs-lookup"><span data-stu-id="11e07-126">Move a tenant's geographic locations</span></span>

<span data-ttu-id="11e07-127">Microsoft continue d’ouvrir de nouveaux emplacements géographiques de centres de données (régions) pour les services Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="11e07-127">Microsoft continues to open new datacenter geographic locations (geos) for Microsoft 365 services.</span></span> <span data-ttu-id="11e07-128">Ces nouvelles géos de centres de données ajoutent de la capacité et des ressources de calcul pour prendre en charge la demande des clients et la croissance de l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="11e07-128">These new datacenter geos add capacity and compute resources to support customer demand and usage growth.</span></span> <span data-ttu-id="11e07-129">En outre, les nouvelles régions de centre de données permettent d'héberger des données dans la région pour les données client essentielles.</span><span class="sxs-lookup"><span data-stu-id="11e07-129">Additionally, the new datacenter geos offer in-geo data residency for core customer data.</span></span>

<span data-ttu-id="11e07-130">Pour plus d’informations, voir Déplacement de données principales vers de nouvelles géos de centres de données [Microsoft 365.](moving-data-to-new-datacenter-geos.md)</span><span class="sxs-lookup"><span data-stu-id="11e07-130">For more information, see [Moving core data to new Microsoft 365 datacenter geos](moving-data-to-new-datacenter-geos.md).</span></span>


## <a name="deploy-microsoft-365-multi-geo"></a><span data-ttu-id="11e07-131">Déployer Microsoft 365 Multi-Géo</span><span class="sxs-lookup"><span data-stu-id="11e07-131">Deploy Microsoft 365 Multi-Geo</span></span>

<span data-ttu-id="11e07-132">Avec Microsoft 365 Multi-Geo, votre organisation peut étendre sa présence Microsoft 365 à plusieurs régions ou pays au sein de votre client existant.</span><span class="sxs-lookup"><span data-stu-id="11e07-132">With Microsoft 365 Multi-Geo, your organization can expand its Microsoft 365 presence to multiple geographic regions and/or countries within your existing tenant.</span></span>

<span data-ttu-id="11e07-133">Pour en savoir plus, consultez [Microsoft 365 Multigéographie](microsoft-365-multi-geo.md).</span><span class="sxs-lookup"><span data-stu-id="11e07-133">For more information, see [Microsoft 365 Multi-Geo](microsoft-365-multi-geo.md).</span></span>

## <a name="manage-multiple-microsoft-365-tenants"></a><span data-ttu-id="11e07-134">Gérer plusieurs clients Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="11e07-134">Manage multiple Microsoft 365 tenants</span></span> 

<span data-ttu-id="11e07-135">Bien qu’il soit idéal d’avoir un seul client pour votre oganisation, vous pouvez être l’une des nombreuses organisations qui ont plusieurs locataires.</span><span class="sxs-lookup"><span data-stu-id="11e07-135">Although having a single tenant for your oganization is ideal, you may be one of many organizations that have multiple tenants.</span></span> <span data-ttu-id="11e07-136">Les raisons peuvent inclure des fusions et des acquisitions, une isolation administrative ou une administration décentralisée.</span><span class="sxs-lookup"><span data-stu-id="11e07-136">Reasons can include mergers and aquisitions, you want administrative isolation, or you have a decentralized IT.</span></span>

<span data-ttu-id="11e07-137">Si vous avez plusieurs clients Microsoft 365, consultez ces articles pour plus d’informations sur :</span><span class="sxs-lookup"><span data-stu-id="11e07-137">If you have multiple Microsoft 365 tenants, see these articles for more information about:</span></span>

- [<span data-ttu-id="11e07-138">Collaboration inter-clients</span><span class="sxs-lookup"><span data-stu-id="11e07-138">Inter-tenant collaboration</span></span>](microsoft-365-inter-tenant-collaboration.md)
- [<span data-ttu-id="11e07-139">Migration de boîtes aux lettres inter-clients</span><span class="sxs-lookup"><span data-stu-id="11e07-139">Cross-tenant mailbox migration</span></span>](cross-tenant-mailbox-migration.md)
- [<span data-ttu-id="11e07-140">Migrations client vers client</span><span class="sxs-lookup"><span data-stu-id="11e07-140">Tenant-to-tenant migrations</span></span>](microsoft-365-tenant-to-tenant-migrations.md)

## <a name="next-step"></a><span data-ttu-id="11e07-141">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="11e07-141">Next step</span></span>

<span data-ttu-id="11e07-142">Commencez la planification de votre client [avec des abonnements, des licences, des comptes et des locataires.](subscriptions-licenses-accounts-and-tenants-for-microsoft-cloud-offerings.md)</span><span class="sxs-lookup"><span data-stu-id="11e07-142">Start your tenant planning with [Subscriptions, licenses, accounts, and tenants](subscriptions-licenses-accounts-and-tenants-for-microsoft-cloud-offerings.md).</span></span>
