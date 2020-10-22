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
ms.openlocfilehash: db0f9552fce460ca6d25ee74ea2031bea388b8dc
ms.sourcegitcommit: 3b1bd8aa1430bc9565743a446bbc27b199f30f73
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/22/2020
ms.locfileid: "48656006"
---
# <a name="tenant-roadmap-for-microsoft-365"></a><span data-ttu-id="cb678-103">Feuille de route de client pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="cb678-103">Tenant roadmap for Microsoft 365</span></span>

<span data-ttu-id="cb678-104">Votre client Microsoft 365 est l’ensemble des services affectés à votre organisation.</span><span class="sxs-lookup"><span data-stu-id="cb678-104">Your Microsoft 365 tenant is the set of services assigned to your organization.</span></span> <span data-ttu-id="cb678-105">En règle générale, ce client est associé à un ou plusieurs de vos noms de domaine DNS et agit comme un conteneur central pour différents abonnements et les licences que vous affectez aux comptes d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cb678-105">Typically, this tenant is associated with one or more of your DNS domain names and acts as a central container for different subscriptions and the licenses within them that you assign to user accounts.</span></span> <span data-ttu-id="cb678-106">Pour plus d’informations, consultez [la rubrique abonnements, licences, comptes et clients pour les offres Cloud de Microsoft](subscriptions-licenses-accounts-and-tenants-for-microsoft-cloud-offerings.md).</span><span class="sxs-lookup"><span data-stu-id="cb678-106">For more information, see [Subscriptions, licenses, accounts, and tenants for Microsoft's cloud offerings](subscriptions-licenses-accounts-and-tenants-for-microsoft-cloud-offerings.md).</span></span>

<span data-ttu-id="cb678-107">Lorsque vous créez un client Microsoft 365, affectez-le à un emplacement géographique spécifique.</span><span class="sxs-lookup"><span data-stu-id="cb678-107">When you create a Microsoft 365 tenant, you assign it to a specific geographical location.</span></span> <span data-ttu-id="cb678-108">Vous pouvez également disposer d’un client disposant de plusieurs emplacements géographiques et déplacer votre client d’un emplacement à un autre.</span><span class="sxs-lookup"><span data-stu-id="cb678-108">You can also have a tenant with multiple geographical locations and move your tenant from one location to another.</span></span>

<span data-ttu-id="cb678-109">Pour obtenir l’identité de votre client, il est essentiel de planifier et d’exécuter soigneusement votre configuration client.</span><span class="sxs-lookup"><span data-stu-id="cb678-109">To get your tenant ready for identity, it's critical to carefully plan and execute your tenant configuration.</span></span>


## <a name="set-up-your-microsoft-365-tenant"></a><span data-ttu-id="cb678-110">Configurer votre client Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="cb678-110">Set up your Microsoft 365 tenant</span></span>

<span data-ttu-id="cb678-111">Une fois que vous avez vérifié que votre réseau est optimisé pour l’accès à Microsoft 365 pour les travailleurs locaux et distants, vos tâches importantes suivantes envisagent de planifier et de configurer votre client Microsoft 365 pour les noms de domaine DNS, les services courants et pour cette infrastructure d’identité qui prend en charge la connexion des utilisateurs sécurisés.</span><span class="sxs-lookup"><span data-stu-id="cb678-111">After ensuring that your networking is optimized for access to Microsoft 365 for both on-premises and remote workers, your next big tasks are planning for and then configuring your Microsoft 365 tenant for DNS domain names, common services, and for that identity infrastructure that supports secure user sign-in.</span></span>

## <a name="plan"></a><span data-ttu-id="cb678-112">Prévision</span><span class="sxs-lookup"><span data-stu-id="cb678-112">Plan</span></span>

<span data-ttu-id="cb678-113">Pour planifier l’implémentation de votre client, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="cb678-113">To plan for your tenant implementation:</span></span>

- [<span data-ttu-id="cb678-114">Comprendre les abonnements, les licences et les clients Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="cb678-114">Understand subscriptions, licenses, and Azure Active Directory (Azure AD) tenants</span></span>](subscriptions-licenses-accounts-and-tenants-for-microsoft-cloud-offerings.md)
- [<span data-ttu-id="cb678-115">Comprendre comment utiliser des certificats SSL tiers</span><span class="sxs-lookup"><span data-stu-id="cb678-115">Understand how to use third-party SSL certificates</span></span>](plan-for-third-party-ssl-certificates.md)
- [<span data-ttu-id="cb678-116">Comprendre comment un client Microsoft 365 est intégré à Azure AD services</span><span class="sxs-lookup"><span data-stu-id="cb678-116">Understand the ways a Microsoft 365 tenant is integrated with Azure AD services</span></span>](integrated-apps-and-azure-ads.md)
- [<span data-ttu-id="cb678-117">Planifier la prise en charge des applications clientes</span><span class="sxs-lookup"><span data-stu-id="cb678-117">Plan for client app support</span></span>](microsoft-365-client-support-certificate-based-authentication.md)
- [<span data-ttu-id="cb678-118">Déterminer comment utiliser l’authentification moderne hybride</span><span class="sxs-lookup"><span data-stu-id="cb678-118">Determine how to use hybrid modern authentication</span></span>](hybrid-modern-auth-overview.md)
- [<span data-ttu-id="cb678-119">Planifier les mises à niveau d’Office 2007 et d’Office 2010</span><span class="sxs-lookup"><span data-stu-id="cb678-119">Plan for Office 2007 and Office 2010 upgrades</span></span>](plan-upgrade-previous-versions-office.md)
- [<span data-ttu-id="cb678-120">Comprendre l’isolation du client</span><span class="sxs-lookup"><span data-stu-id="cb678-120">Understand tenant isolation</span></span>](microsoft-365-tenant-isolation-overview.md)
- [<span data-ttu-id="cb678-121">Obtenir des informations sur l’assurance de service Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="cb678-121">Get the details on Microsoft 365 service assurance</span></span>](microsoft-365-administrative-access-controls-overview.md)

### <a name="deploy"></a><span data-ttu-id="cb678-122">Déployer</span><span class="sxs-lookup"><span data-stu-id="cb678-122">Deploy</span></span>

<span data-ttu-id="cb678-123">Pour déployer votre client :</span><span class="sxs-lookup"><span data-stu-id="cb678-123">To deploy your tenant:</span></span> 

- <span data-ttu-id="cb678-124">Ajoutez les [domaines DNS](https://docs.microsoft.com/microsoft-365/admin/setup/add-domain) de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="cb678-124">Add the [DNS domains](https://docs.microsoft.com/microsoft-365/admin/setup/add-domain) for your organization.</span></span>
- <span data-ttu-id="cb678-125">Utilisez les [guides de configuration dans le centre d’administration Microsoft 365](setup-guides-for-microsoft-365.md).</span><span class="sxs-lookup"><span data-stu-id="cb678-125">Use the [setup guides in the Microsoft 365 admin center](setup-guides-for-microsoft-365.md).</span></span>
- <span data-ttu-id="cb678-126">Créez votre [infrastructure d’identité](identity-roadmap-microsoft-365.md) et [Sécurisez vos connexions utilisateur](microsoft-365-secure-sign-in.md).</span><span class="sxs-lookup"><span data-stu-id="cb678-126">Build out your [identity infrastructure](identity-roadmap-microsoft-365.md) and [secure your user sign-ins](microsoft-365-secure-sign-in.md).</span></span>

### <a name="move-a-tenants-geographic-locations"></a><span data-ttu-id="cb678-127">Déplacer les emplacements géographiques d’un client</span><span class="sxs-lookup"><span data-stu-id="cb678-127">Move a tenant's geographic locations</span></span>

<span data-ttu-id="cb678-128">Microsoft continue d’ouvrir les nouveaux emplacements géographiques des centres de régions centres (Centre de ressources) pour les services Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="cb678-128">Microsoft continues to open new datacenter geographic locations (geos) for Microsoft 365 services.</span></span> <span data-ttu-id="cb678-129">Ces nouveaux centres de régions centres ajoutent de la capacité et des ressources de calcul afin de prendre en charge la demande des clients et la croissance de l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="cb678-129">These new datacenter geos add capacity and compute resources to support customer demand and usage growth.</span></span> <span data-ttu-id="cb678-130">En outre, les nouvelles régions de centre de données permettent d'héberger des données dans la région pour les données client essentielles.</span><span class="sxs-lookup"><span data-stu-id="cb678-130">Additionally, the new datacenter geos offer in-geo data residency for core customer data.</span></span>

<span data-ttu-id="cb678-131">Pour plus d’informations, consultez la rubrique [Moving Data Core to New Microsoft 365 Datacenter régions centres](moving-data-to-new-datacenter-geos.md).</span><span class="sxs-lookup"><span data-stu-id="cb678-131">For more information, see [Moving core data to new Microsoft 365 datacenter geos](moving-data-to-new-datacenter-geos.md).</span></span>


## <a name="deploy-microsoft-365-multi-geo"></a><span data-ttu-id="cb678-132">Déployer Microsoft 365 multi-géo</span><span class="sxs-lookup"><span data-stu-id="cb678-132">Deploy Microsoft 365 Multi-Geo</span></span>

<span data-ttu-id="cb678-133">Avec Microsoft 365 Multi-Geo, votre organisation peut étendre sa présence Microsoft 365 à plusieurs régions ou pays au sein de votre client existant.</span><span class="sxs-lookup"><span data-stu-id="cb678-133">With Microsoft 365 Multi-Geo, your organization can expand its Microsoft 365 presence to multiple geographic regions and/or countries within your existing tenant.</span></span>

<span data-ttu-id="cb678-134">Pour plus d’informations, consultez la rubrique [Microsoft 365 multi-géo](microsoft-365-multi-geo.md).</span><span class="sxs-lookup"><span data-stu-id="cb678-134">For more information, see [Microsoft 365 Multi-Geo](microsoft-365-multi-geo.md).</span></span>

## <a name="manage-multiple-microsoft-365-tenancies"></a><span data-ttu-id="cb678-135">Gérer plusieurs locations Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="cb678-135">Manage multiple Microsoft 365 tenancies</span></span> 

<span data-ttu-id="cb678-136">Bien que le fait d’avoir un seul client pour votre Oganization soit idéal, il peut s’agir de l’une des nombreuses organisations ayant plusieurs locations.</span><span class="sxs-lookup"><span data-stu-id="cb678-136">Although having a single tenant for your oganization is ideal, you may be one of many organizations that have multiple tenancies.</span></span> <span data-ttu-id="cb678-137">Les raisons pour lesquelles plusieurs locations peuvent inclure des fusions et des acquisitions, mais vous souhaitez une isolation administrative ou vous en avez une décentralisée.</span><span class="sxs-lookup"><span data-stu-id="cb678-137">Reasons for multiple tenancies can include mergers and aquisitions, you want administrative isolation, or you have a decentralized IT.</span></span>

<span data-ttu-id="cb678-138">Si vous avez plusieurs locations Microsoft 365, consultez les articles suivants pour plus d’informations sur :</span><span class="sxs-lookup"><span data-stu-id="cb678-138">If you have multiple Microsoft 365 tenancies, see these articles for more information about:</span></span>

- [<span data-ttu-id="cb678-139">Collaboration inter-clients</span><span class="sxs-lookup"><span data-stu-id="cb678-139">Inter-tenant collaboration</span></span>](microsoft-365-inter-tenant-collaboration.md)
- [<span data-ttu-id="cb678-140">Migration de boîtes aux lettres inter-clients</span><span class="sxs-lookup"><span data-stu-id="cb678-140">Cross-tenant mailbox migration</span></span>](cross-tenant-mailbox-migration.md)
- [<span data-ttu-id="cb678-141">Migrations client vers client</span><span class="sxs-lookup"><span data-stu-id="cb678-141">Tenant-to-tenant migrations</span></span>](microsoft-365-tenant-to-tenant-migrations.md)


## <a name="next-step"></a><span data-ttu-id="cb678-142">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="cb678-142">Next step</span></span>

<span data-ttu-id="cb678-143">Démarrez votre planification client avec des [abonnements, des licences, des comptes et des clients](subscriptions-licenses-accounts-and-tenants-for-microsoft-cloud-offerings.md).</span><span class="sxs-lookup"><span data-stu-id="cb678-143">Start your tenant planning with [Subscriptions, licenses, accounts, and tenants](subscriptions-licenses-accounts-and-tenants-for-microsoft-cloud-offerings.md).</span></span>
