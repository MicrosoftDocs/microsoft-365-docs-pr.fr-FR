---
title: Identité de Contoso Corporation
author: JoeDavies-MSFT
ms.author: josephd
manager: laurawi
ms.date: 10/01/2019
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- M365-identity-device-management
- Strat_O365_Enterprise
ms.custom: ''
description: Découvrez comment Contoso tire parti de la solution de gestion des identités IDaaS et propose à ses employés une authentification basée sur le cloud, et une authentification fédérée à ses partenaires et ses clients.
ms.openlocfilehash: 81a1542edf82bbf773360af6b09e1f940f5fd061
ms.sourcegitcommit: 1d376287f6c1bf5174873e89ed4bf7bb15bc13f6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/14/2019
ms.locfileid: "38627360"
---
# <a name="identity-for-the-contoso-corporation"></a><span data-ttu-id="2381e-103">Identité de Contoso Corporation</span><span class="sxs-lookup"><span data-stu-id="2381e-103">Identity for the Contoso Corporation</span></span>

<span data-ttu-id="2381e-104">**Résumé :** Découvrez comment Contoso tire parti de la solution de gestion des identités IDaaS et propose à ses employés une authentification basée sur le cloud, et une authentification fédérée à ses partenaires et ses clients.</span><span class="sxs-lookup"><span data-stu-id="2381e-104">**Summary:** How Contoso takes advantage of Identity as a Service (IDaaS) and provides cloud-based authentication for its employees and federated authentication for its partners and customers.</span></span>

<span data-ttu-id="2381e-105">Microsoft fournit une IDaaS dans toutes ses offres cloud avec Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="2381e-105">Microsoft provides an Identity as a Service (IDaaS) across its cloud offerings with Azure Active Directory (Azure AD).</span></span> <span data-ttu-id="2381e-106">Pour adopter Microsoft 365 Entreprise, la solution IDaaS de Contoso doit tirer parti de son fournisseur d’identités local et intégrer l’authentification fédérée avec ses fournisseurs d’identité tiers approuvés existants.</span><span class="sxs-lookup"><span data-stu-id="2381e-106">To adopt Microsoft 365 Enterprise, Contoso's IDaaS solution had to leverage their on-premises identity provider and still include federated authentication with their existing trusted, third-party identity providers.</span></span>

## <a name="contosos-active-directory-domain-services-forest"></a><span data-ttu-id="2381e-107">Ensemble des services de domaine Active Directory Domain Services de Contoso</span><span class="sxs-lookup"><span data-stu-id="2381e-107">Contoso's Active Directory Domain Services forest</span></span>

<span data-ttu-id="2381e-108">Contoso utilise une seule forêt Windows Server Active Directory Domain Services (AD DS) pour contoso.com et sept sous-domaines (un par région).</span><span class="sxs-lookup"><span data-stu-id="2381e-108">Contoso uses a single Active Directory Domain Services (AD DS) forest for contoso.com with seven sub-domains, one for each region of the world.</span></span> <span data-ttu-id="2381e-109">Le siège social, les centres régionaux et les succursales disposent de contrôleurs de domaine pour l’authentification locale et l’autorisation.</span><span class="sxs-lookup"><span data-stu-id="2381e-109">The headquarters, regional hub offices, and satellite offices contain domain controllers for local authentication and authorization.</span></span>

<span data-ttu-id="2381e-110">Voici la forêt et les domaines régionaux de Contoso dans les régions du monde où se trouvent des centres régionaux.</span><span class="sxs-lookup"><span data-stu-id="2381e-110">Here is the Contoso forest with regional domains for the different parts of the world that contain regional hubs.</span></span>

![Forêt et domaines de Contoso dans le monde](./media/contoso-identity/contoso-identity-fig1.png)
 
<span data-ttu-id="2381e-112">Contoso souhaitait utiliser les comptes et les groupes de la forêt contoso.com pour faciliter l’authentification et l’autorisation de ses services et de ses charges de travail Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="2381e-112">Contoso wanted to use the accounts and groups in the contoso.com forest for authentication and authorization for its Microsoft 365 workloads and services.</span></span>

## <a name="contosos-federated-authentication-infrastructure"></a><span data-ttu-id="2381e-113">Infrastructure d’authentification fédérée de Contoso</span><span class="sxs-lookup"><span data-stu-id="2381e-113">Contoso's federated authentication infrastructure</span></span>

<span data-ttu-id="2381e-114">Contoso autorise les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="2381e-114">Contoso allows:</span></span>

- <span data-ttu-id="2381e-115">Les clients ont le droit d’utiliser leurs comptes Microsoft, Facebook ou Google Mail pour se connecter à leur site web public.</span><span class="sxs-lookup"><span data-stu-id="2381e-115">Customers to use their Microsoft, Facebook, or Google Mail accounts to sign in to their public web site.</span></span>
- <span data-ttu-id="2381e-116">Les fournisseurs et les partenaires peuvent utiliser leurs comptes LinkedIn, Salesforce ou Google Mail pour se connecter à l’extranet des partenaires.</span><span class="sxs-lookup"><span data-stu-id="2381e-116">Vendors and partners to use their LinkedIn, Salesforce, or Google Mail accounts to sign in to the partner extranet.</span></span>

<span data-ttu-id="2381e-p103">Voici le réseau de périmètre de Contoso comprenant un site web public, un extranet des partenaires et des serveurs pour les services AD FS (services de fédération Active Directory). Le réseau de périmètre est connecté à Internet, qui contient des clients, des partenaires et des services Internet.</span><span class="sxs-lookup"><span data-stu-id="2381e-p103">Here is the Contoso DMZ containing a public web site, a partner extranet, and a set of Active Directory Federation Services (AD FS) servers. The DMZ is connected to the Internet that contains customers, partners, and Internet services.</span></span>

![Prise en charge de l’authentification fédérée par Contoso pour ses clients et ses partenaires](./media/contoso-identity/contoso-identity-fig2.png)
 
<span data-ttu-id="2381e-120">Les serveurs AD FS du DMZ facilitent l’authentification des informations d’identification client par leurs fournisseurs d’identité pour accéder au site web public et des informations d’identification partenaires pour accéder à l’extranet des partenaires.</span><span class="sxs-lookup"><span data-stu-id="2381e-120">AD FS servers in the DMZ facilitate the authentication of customer credentials by their identity providers for access to the public web site and partner credentials for access to the partner extranet.</span></span>

<span data-ttu-id="2381e-p104">Contoso a décidé de conserver cette infrastructure pour la dédier à l’authentification des clients et des partenaires. Les architectes en identité de Contoso examinent actuellement la possibilité de convertir cette infrastructure en solutions [B2B](https://docs.microsoft.com/azure/active-directory/b2b/hybrid-organizations) et [B2C](https://docs.microsoft.com/azure/active-directory-b2c/solution-articles) Azure AD.</span><span class="sxs-lookup"><span data-stu-id="2381e-p104">Contoso decided to keep this infrastructure and dedicate it to customer and partner authentications. Contoso identity architects are investigating the conversion of this infrastructure to Azure AD [B2B](https://docs.microsoft.com/azure/active-directory/b2b/hybrid-organizations) and [B2C](https://docs.microsoft.com/azure/active-directory-b2c/solution-articles) solutions.</span></span>

## <a name="hybrid-identity-with-password-hash-synchronization-for-cloud-based-authentication"></a><span data-ttu-id="2381e-123">Identité hybride avec authentification directe pour l’authentification basée sur le cloud</span><span class="sxs-lookup"><span data-stu-id="2381e-123">Hybrid identity with password hash synchronization for cloud-based authentication</span></span>

<span data-ttu-id="2381e-124">Contoso souhaite tirer parti de son ensemble local AD DS pour l’authentification aux ressources cloud de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="2381e-124">Contoso wanted to leverage its on-premises AD DS forest for authentication to Microsoft 365 cloud resources.</span></span> <span data-ttu-id="2381e-125">Il a décidé du hachage de synchronisation du mot de passe (PHS).</span><span class="sxs-lookup"><span data-stu-id="2381e-125">It decided on password hash synchronization (PHS).</span></span>

<span data-ttu-id="2381e-126">PBS synchronise la version de l’ensemble local AD DS avec le client Azure AD de l’abonnement Microsoft 365 Entreprise, copie des comptes d’utilisateur et de groupe et une version hachurée de mots de passe du compte utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2381e-126">PHS synchronizes the on-premises AD DS forest with the Azure AD tenant of their Microsoft 365 Enterprise subscription, copying user and group accounts and a hashed version of user account passwords.</span></span> 

<span data-ttu-id="2381e-127">Pour effectuer la synchronisation d’annuaire en cours, Contoso a déployé l’outil Azure AD Connect sur un serveur dans son centre de données de Paris.</span><span class="sxs-lookup"><span data-stu-id="2381e-127">To perform the ongoing directory synchronization, Contoso has deployed the Azure AD Connect tool on a server in its Paris datacenter.</span></span> 

<span data-ttu-id="2381e-128">Voici le serveur exécutant la connexion Azure Active Directory Connect interrogeant l’ensemble Contoso AD DS pour les modifications de l’interrogation et la synchronisation de ces modifications avec le client Azure AD.</span><span class="sxs-lookup"><span data-stu-id="2381e-128">Here is the server running Azure AD Connect polling the Contoso AD DS forest for changes and then synchronizing those changes with the Azure AD tenant.</span></span>

![Infrastructure de la synchronisation d’annuaires de synchronisation de hachage de mot de passe de Contoso](./media/contoso-identity/contoso-identity-fig4.png)
 
## <a name="conditional-access-policies-for-identity-and-device-access"></a><span data-ttu-id="2381e-130">Stratégies d’accès conditionnel basé sur l’identité et l’appareil</span><span class="sxs-lookup"><span data-stu-id="2381e-130">Conditional Access policies for identity and device access</span></span>

<span data-ttu-id="2381e-131">Contoso a créé un jeu d’Azure AD et Intune [stratégies d’accès conditionnel](identity-access-policies.md) pour trois niveaux de protection :</span><span class="sxs-lookup"><span data-stu-id="2381e-131">Contoso created a set of Azure AD and Intune [Conditional Access policies](identity-access-policies.md) for three protection levels:</span></span>

- <span data-ttu-id="2381e-132">**Référence** les protections s’appliquent à tous les comptes d’utilisateurs</span><span class="sxs-lookup"><span data-stu-id="2381e-132">**Baseline** protections apply to all user accounts</span></span>
- <span data-ttu-id="2381e-133">**Sensibles**les protections s’appliquent aux cadres dirigeants et membres du personnel exécutif</span><span class="sxs-lookup"><span data-stu-id="2381e-133">**Sensitive** protections apply to senior leadership and executive staff</span></span>
- <span data-ttu-id="2381e-134">**Hautement réglementée**les protections s’appliquent à des utilisateurs spécifiques financiers, légaux et leur emplacement géographique de recherche ayant accès aux données hautement réglementées</span><span class="sxs-lookup"><span data-stu-id="2381e-134">**Highly Regulated** protections apply to specific users in the finance, legal, and research departments that have access to highly regulated data</span></span>

<span data-ttu-id="2381e-135">Voici l’ensemble de stratégies d’accès conditionnel basées sur l’identité et l’appareil de Contoso.</span><span class="sxs-lookup"><span data-stu-id="2381e-135">Here is Contoso's resulting set of identity and device Conditional Access policies.</span></span>

![Stratégies d’accès conditionnel basées sur l’identité et l’appareil de Contoso](./media/contoso-identity/contoso-identity-fig5.png)
 
## <a name="next-step"></a><span data-ttu-id="2381e-137">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="2381e-137">Next step</span></span>

<span data-ttu-id="2381e-138">[Découvrez](contoso-win10.md) comment Contoso tire parti de son infrastructure Microsoft Endpoint Configuration Manager pour déployer et maintenir à jour Windows 10 Entreprise au sein de son organisation.</span><span class="sxs-lookup"><span data-stu-id="2381e-138">[Learn](contoso-win10.md) how Contoso is leveraging its System Center Configuration Manager infrastructure to deploy and keep current Windows 10 Enterprise across its organization.</span></span>

## <a name="see-also"></a><span data-ttu-id="2381e-139">Voir également</span><span class="sxs-lookup"><span data-stu-id="2381e-139">See also</span></span>

[<span data-ttu-id="2381e-140">Identité pour Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="2381e-140">Identity for Microsoft 365 Enterprise</span></span>](identity-infrastructure.md)

[<span data-ttu-id="2381e-141">Guide de déploiement</span><span class="sxs-lookup"><span data-stu-id="2381e-141">Deployment guide</span></span>](deploy-microsoft-365-enterprise.md)

[<span data-ttu-id="2381e-142">Guides de laboratoire de test</span><span class="sxs-lookup"><span data-stu-id="2381e-142">Test lab guides</span></span>](m365-enterprise-test-lab-guides.md)
