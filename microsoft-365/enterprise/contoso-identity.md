---
title: Identité de Contoso Corporation
author: JoeDavies-MSFT
f1.keywords:
- NOCSH
ms.author: josephd
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Normal
ms.collection:
- M365-identity-device-management
- Strat_O365_Enterprise
ms.custom: ''
description: Découvrez comment Contoso tire parti de la solution de gestion des identités IDaaS et propose à ses employés une authentification basée sur le cloud, et une authentification fédérée à ses partenaires et ses clients.
ms.openlocfilehash: dea0f53ef1c3fdc2ea32256303c6120c614c904d
ms.sourcegitcommit: 66b8fc1d8ba4f17487cd2004ac19cf2fff472f3d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/24/2020
ms.locfileid: "48754635"
---
# <a name="identity-for-the-contoso-corporation"></a><span data-ttu-id="eae35-103">Identité de Contoso Corporation</span><span class="sxs-lookup"><span data-stu-id="eae35-103">Identity for the Contoso Corporation</span></span>

<span data-ttu-id="eae35-104">Microsoft fournit l’identité en tant que service (IDaaS) dans ses offres cloud via Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="eae35-104">Microsoft provides Identity as a Service (IDaaS) across its cloud offerings through Azure Active Directory (Azure AD).</span></span> <span data-ttu-id="eae35-105">Pour adopter Microsoft 365 pour entreprise, la solution Contoso IDaaS devait utiliser son fournisseur d’identité local et inclure l’authentification fédérée avec ses fournisseurs d’identité tiers existants.</span><span class="sxs-lookup"><span data-stu-id="eae35-105">To adopt Microsoft 365 for enterprise, the Contoso IDaaS solution had to use their on-premises identity provider and include federated authentication with their existing trusted, third-party identity providers.</span></span>

## <a name="the-contoso-active-directory-domain-services-forest"></a><span data-ttu-id="eae35-106">Forêt des services de domaine Active Directory contoso</span><span class="sxs-lookup"><span data-stu-id="eae35-106">The Contoso Active Directory Domain Services forest</span></span>

<span data-ttu-id="eae35-107">Contoso utilise une seule forêt AD DS (Active Directory Domain Services) pour contoso com avec sept sous-domaines, un pour chaque région \. du monde.</span><span class="sxs-lookup"><span data-stu-id="eae35-107">Contoso uses a single Active Directory Domain Services (AD DS) forest for contoso\.com with seven subdomains, one for each region of the world.</span></span> <span data-ttu-id="eae35-108">Le siège social, les centres régionaux et les succursales disposent de contrôleurs de domaine pour l’authentification locale et l’autorisation.</span><span class="sxs-lookup"><span data-stu-id="eae35-108">The headquarters, regional hub offices, and satellite offices contain domain controllers for local authentication and authorization.</span></span>

<span data-ttu-id="eae35-109">Voici la forêt Contoso avec des domaines régionaux pour les différentes régions du monde qui contiennent des centres régionaux.</span><span class="sxs-lookup"><span data-stu-id="eae35-109">Here's the Contoso forest with regional domains for the different parts of the world that contain regional hubs.</span></span>

![Forêt et domaines de Contoso dans le monde](../media/contoso-identity/contoso-identity-fig1.png)
 
<span data-ttu-id="eae35-111">Contoso a décidé d’utiliser les comptes et les groupes de la forêt contoso com pour l’authentification et l’autorisation de ses charges de travail et \. services Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="eae35-111">Contoso decided to use the accounts and groups in the contoso\.com forest for authentication and authorization for its Microsoft 365 workloads and services.</span></span>

## <a name="the-contoso-federated-authentication-infrastructure"></a><span data-ttu-id="eae35-112">Infrastructure d’authentification fédérée Contoso</span><span class="sxs-lookup"><span data-stu-id="eae35-112">The Contoso federated authentication infrastructure</span></span>

<span data-ttu-id="eae35-113">Contoso autorise les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="eae35-113">Contoso allows:</span></span>

- <span data-ttu-id="eae35-114">Les clients qui utilisent leurs comptes Microsoft, Facebook ou Google Mail pour se connectent au site web public de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="eae35-114">Customers to use their Microsoft, Facebook, or Google Mail accounts to sign in to the company's public web site.</span></span>
- <span data-ttu-id="eae35-115">Fournisseurs et partenaires qui utilisent leurs comptes LinkedIn, Salesforce ou Google Mail pour se connectent à l’extranet partenaire de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="eae35-115">Vendors and partners to use their LinkedIn, Salesforce, or Google Mail accounts to sign in to the company's partner extranet.</span></span>

<span data-ttu-id="eae35-p103">Voici le DMZ Contoso contenant un site web public, un extranet partenaire et un ensemble de serveurs AD FS (Active Directory Federation Services). Le DMZ est connecté à Internet qui contient des clients, des partenaires et des services Internet.</span><span class="sxs-lookup"><span data-stu-id="eae35-p103">Here's the Contoso DMZ containing a public web site, a partner extranet, and a set of Active Directory Federation Services (AD FS) servers. The DMZ is connected to the internet that contains customers, partners, and internet services.</span></span>

![Prise en charge de Contoso pour l’authentification fédérée pour les clients et les partenaires](../media/contoso-identity/contoso-identity-fig2.png)
 
<span data-ttu-id="eae35-119">Les serveurs AD FS dans la DMZ facilitent l’authentification des informations d’identification client par leurs fournisseurs d’identité pour accéder au site web public et aux informations d’identification des partenaires pour l’accès à l’extranet du partenaire.</span><span class="sxs-lookup"><span data-stu-id="eae35-119">AD FS servers in the DMZ facilitate authentication of customer credentials by their identity providers for access to the public web site and partner credentials for access to the partner extranet.</span></span>

<span data-ttu-id="eae35-p104">Contoso a décidé de conserver cette infrastructure et de la dédier à l’authentification des clients et des partenaires. Les architectes d’identité Contoso examinent la conversion de cette infrastructure en solutions Azure AD [B2B](https://docs.microsoft.com/azure/active-directory/b2b/hybrid-organizations) et [B2C.](https://docs.microsoft.com/azure/active-directory-b2c/solution-articles)</span><span class="sxs-lookup"><span data-stu-id="eae35-p104">Contoso decided to keep this infrastructure and dedicate it to customer and partner authentication. Contoso identity architects are investigating the conversion of this infrastructure to Azure AD [B2B](https://docs.microsoft.com/azure/active-directory/b2b/hybrid-organizations) and [B2C](https://docs.microsoft.com/azure/active-directory-b2c/solution-articles) solutions.</span></span>

## <a name="hybrid-identity-with-password-hash-synchronization-for-cloud-based-authentication"></a><span data-ttu-id="eae35-122">Identité hybride avec authentification directe pour l’authentification basée sur le cloud</span><span class="sxs-lookup"><span data-stu-id="eae35-122">Hybrid identity with password hash synchronization for cloud-based authentication</span></span>

<span data-ttu-id="eae35-123">Contoso souhaitait utiliser sa forêt AD DS sur site pour l’authentification aux ressources cloud de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="eae35-123">Contoso wanted to use its on-premises AD DS forest for authentication to Microsoft 365 cloud resources.</span></span> <span data-ttu-id="eae35-124">Il a décidé d’utiliser la synchronisation de hachage de mot de passe (PHS).</span><span class="sxs-lookup"><span data-stu-id="eae35-124">It decided to use password hash synchronization (PHS).</span></span>

<span data-ttu-id="eae35-125">PHS synchronise la forêt AD DS sur site avec le client Azure AD de son abonnement Microsoft 365 pour entreprise, en copiant les comptes d’utilisateur et de groupe et une version hachée des mots de passe de compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="eae35-125">PHS synchronizes the on-premises AD DS forest with the Azure AD tenant of their Microsoft 365 for enterprise subscription, copying user and group accounts and a hashed version of user account passwords.</span></span>

<span data-ttu-id="eae35-126">Pour la synchronisation d’annuaires, Contoso a déployé l’outil Azure AD Connect sur un serveur dans son centre de données parisien.</span><span class="sxs-lookup"><span data-stu-id="eae35-126">To do directory synchronization, Contoso deployed the Azure AD Connect tool on a server in its Paris datacenter.</span></span>

<span data-ttu-id="eae35-127">Voici le serveur exécutant Azure AD Connect qui recherche des modifications dans la forêt Contoso AD DS, puis synchronise ces modifications avec le client Azure AD.</span><span class="sxs-lookup"><span data-stu-id="eae35-127">Here's the server running Azure AD Connect polling the Contoso AD DS forest for changes and then synchronizing those changes with the Azure AD tenant.</span></span>

![Infrastructure de synchronisation d’annuaires PHS Contoso](../media/contoso-identity/contoso-identity-fig4.png)
 
## <a name="conditional-access-policies-for-identity-and-device-access"></a><span data-ttu-id="eae35-129">Stratégies d’accès conditionnel basé sur l’identité et l’appareil</span><span class="sxs-lookup"><span data-stu-id="eae35-129">Conditional Access policies for identity and device access</span></span>

<span data-ttu-id="eae35-130">Contoso a créé un jeu d’Azure AD et Intune [stratégies d’accès conditionnel](identity-access-policies.md) pour trois niveaux de protection :</span><span class="sxs-lookup"><span data-stu-id="eae35-130">Contoso created a set of Azure AD and Intune [Conditional Access policies](identity-access-policies.md) for three protection levels:</span></span>

- <span data-ttu-id="eae35-131">*Les* protections de référence s’appliquent à tous les comptes d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="eae35-131">*Baseline* protections apply to all user accounts.</span></span>
- <span data-ttu-id="eae35-132">*Les* protections sensibles s’appliquent aux cadres supérieurs et aux cadres.</span><span class="sxs-lookup"><span data-stu-id="eae35-132">*Sensitive* protections apply to senior leadership and executive staff.</span></span>
- <span data-ttu-id="eae35-133">*Les protections hautement réglementées* s’appliquent à des utilisateurs spécifiques des services financiers, juridiques et de recherche qui ont accès aux données hautement réglementées.</span><span class="sxs-lookup"><span data-stu-id="eae35-133">*Highly Regulated* protections apply to specific users in the finance, legal, and research departments who have access to highly regulated data.</span></span>

<span data-ttu-id="eae35-134">Voici l’ensemble des stratégies d’accès conditionnel aux appareils et aux identités Contoso.</span><span class="sxs-lookup"><span data-stu-id="eae35-134">Here's the resulting set of Contoso identity and device Conditional Access policies.</span></span>

![Stratégies d’accès conditionnel basées sur l’identité et l’appareil de Contoso](../media/contoso-identity/contoso-identity-fig5.png)
 
## <a name="next-step"></a><span data-ttu-id="eae35-136">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="eae35-136">Next step</span></span>

<span data-ttu-id="eae35-137">Découvrez comment Contoso utilise son infrastructure Microsoft Endpoint Configuration Manager pour déployer et conserver [windows 10 Entreprise](contoso-win10.md) actuel au sein de son organisation.</span><span class="sxs-lookup"><span data-stu-id="eae35-137">Learn how Contoso uses its Microsoft Endpoint Configuration Manager infrastructure to [deploy and keep current Windows 10 Enterprise](contoso-win10.md) across its organization.</span></span>

## <a name="see-also"></a><span data-ttu-id="eae35-138">Voir également</span><span class="sxs-lookup"><span data-stu-id="eae35-138">See also</span></span>

[<span data-ttu-id="eae35-139">Feuille de route relative à l’identité pour Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="eae35-139">Identity roadmap for Microsoft 365</span></span>](identity-roadmap-microsoft-365.md)

[<span data-ttu-id="eae35-140">Vue d’ensemble de Microsoft 365 pour entreprise</span><span class="sxs-lookup"><span data-stu-id="eae35-140">Microsoft 365 for enterprise overview</span></span>](microsoft-365-overview.md)

[<span data-ttu-id="eae35-141">Guides de laboratoire de test</span><span class="sxs-lookup"><span data-stu-id="eae35-141">Test lab guides</span></span>](m365-enterprise-test-lab-guides.md)
