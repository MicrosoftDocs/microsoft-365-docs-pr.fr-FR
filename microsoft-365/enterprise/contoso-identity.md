---
title: Identité de Contoso Corporation
author: JoeDavies-MSFT
ms.author: josephd
manager: laurawi
ms.date: 01/17/2019
ms.audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- M365-identity-device-management
- Strat_O365_Enterprise
ms.custom: ''
description: Découvrez comment Contoso tire parti de la solution de gestion des identités IDaaS et propose à ses employés une authentification basée sur le cloud, et une authentification fédérée à ses partenaires et ses clients.
ms.openlocfilehash: bcd83eaafb5df86d9a660aeb74b2e97f7bdc6b7b
ms.sourcegitcommit: 81273a9df49647286235b187fa2213c5ec7e8b62
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32277577"
---
# <a name="identity-for-the-contoso-corporation"></a><span data-ttu-id="e274e-103">Identité de Contoso Corporation</span><span class="sxs-lookup"><span data-stu-id="e274e-103">Identity for the Contoso Corporation</span></span>

<span data-ttu-id="e274e-104">**Résumé :** Découvrez comment Contoso tire parti de la solution de gestion des identités IDaaS et propose à ses employés une authentification basée sur le cloud, et une authentification fédérée à ses partenaires et ses clients.</span><span class="sxs-lookup"><span data-stu-id="e274e-104">**Summary:** How Contoso takes advantage of Identity as a Service (IDaaS) and provides cloud-based authentication for its employees and federated authentication for its partners and customers.</span></span>

<span data-ttu-id="e274e-105">Microsoft fournit une IDaaS dans toutes ses offres cloud avec Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="e274e-105">Microsoft provides an Identity as a Service (IDaaS) across its cloud offerings with Azure Active Directory (Azure AD).</span></span> <span data-ttu-id="e274e-106">Pour adopter Microsoft 365 Entreprise, la solution IDaaS de Contoso doit tirer parti de son fournisseur d’identités local et intégrer l’authentification fédérée avec ses fournisseurs d’identité tiers approuvés existants.</span><span class="sxs-lookup"><span data-stu-id="e274e-106">Microsoft provides an Identity as a Service (IDaaS) across its cloud offerings with Azure Active Directory (AD). To adopt Microsoft 365 Enterprise, Contoso's IDaaS solution had to leverage their on-premises identity provider and still include federated authentication with their existing trusted, third-party identity providers.</span></span>

## <a name="contosos-active-directory-domain-services-forest"></a><span data-ttu-id="e274e-107">Ensemble des services de domaine Active Directory Domain Services de Contoso</span><span class="sxs-lookup"><span data-stu-id="e274e-107">Contoso's Active Directory Domain Services forest</span></span>

<span data-ttu-id="e274e-108">Contoso utilise une seule forêt Windows Server Active Directory Domain Services (AD DS) pour contoso.com et sept sous-domaines (un par région).</span><span class="sxs-lookup"><span data-stu-id="e274e-108">Contoso uses a single Windows Server Active Directory (AD) forest for contoso.com with seven domains, one for each region of the world.</span></span> <span data-ttu-id="e274e-109">Le siège social, les centres régionaux et les succursales disposent de contrôleurs de domaine pour l’authentification locale et l’autorisation.</span><span class="sxs-lookup"><span data-stu-id="e274e-109">The headquarters, regional hub offices, and satellite offices contain domain controllers for local authentication and authorization.</span></span>

<span data-ttu-id="e274e-110">La Figure 1 présente la forêt et les domaines régionaux de Contoso dans les régions du monde où se trouvent des centres régionaux.</span><span class="sxs-lookup"><span data-stu-id="e274e-110">Figure 1 shows the Contoso forest with regional domains for the different parts of the world that contain regional hubs.</span></span>

![](./media/contoso-identity/contoso-identity-fig1.png)
 
<span data-ttu-id="e274e-111">**Figure 1 : forêt et domaines de Contoso dans le monde**</span><span class="sxs-lookup"><span data-stu-id="e274e-111">**Figure 1: Contoso's forest and domains worldwide**</span></span>

<span data-ttu-id="e274e-112">Contoso souhaitait utiliser les comptes et les groupes de la forêt contoso.com pour faciliter l’authentification et l’autorisation de ses services et de ses charges de travail Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="e274e-112">Contoso wants to use the accounts and groups in the contoso.com forest for authentication and authorization for its cloud-based apps and workloads.</span></span>

## <a name="contosos-federated-authentication-infrastructure"></a><span data-ttu-id="e274e-113">Infrastructure d’authentification fédérée de Contoso</span><span class="sxs-lookup"><span data-stu-id="e274e-113">Contoso's federated authentication infrastructure</span></span>

<span data-ttu-id="e274e-114">Contoso autorise les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="e274e-114">Contoso allows:</span></span>

- <span data-ttu-id="e274e-115">Les clients ont le droit d’utiliser leurs comptes Microsoft, Facebook ou Google Mail pour se connecter à leur site web public.</span><span class="sxs-lookup"><span data-stu-id="e274e-115">Customers to use their Microsoft, Facebook, or Google Mail accounts to sign in to their public web site.</span></span>
- <span data-ttu-id="e274e-116">Les fournisseurs et les partenaires peuvent utiliser leurs comptes LinkedIn, Salesforce ou Google Mail pour se connecter à l’extranet des partenaires.</span><span class="sxs-lookup"><span data-stu-id="e274e-116">Vendors and partners to use their LinkedIn, Salesforce, or Google Mail accounts to sign in to the partner extranet.</span></span>

<span data-ttu-id="e274e-p103">La Figure 2 montre que le réseau de périmètre de Contoso comprend un site web public, un extranet des partenaires et des serveurs pour les services ADFS (services de fédération Active Directory). Le réseau de périmètre est connecté à Internet, qui contient des clients, des partenaires et des services Internet.</span><span class="sxs-lookup"><span data-stu-id="e274e-p103">Figure 2 shows the Contoso DMZ containing a public web site, a partner extranet, and a set of Active Directory Federation Services (AD FS) servers. The DMZ is connected to the Internet that contains customers, partners, and Internet services.</span></span>

![](./media/contoso-identity/contoso-identity-fig2.png)

<span data-ttu-id="e274e-119">**Figure 2 : prise en charge de l’authentification fédérée par Contoso pour ses clients et ses partenaires**</span><span class="sxs-lookup"><span data-stu-id="e274e-119">**Figure 2: Contoso's support for federated authentication for customers and partners**</span></span>
 
<span data-ttu-id="e274e-120">Les serveurs des services ADFS du réseau de périmètre utilisent leurs informations d’identification client pour se connecter au site web public et leurs informations d’identification partenaire pour accéder à l’extranet des partenaires.</span><span class="sxs-lookup"><span data-stu-id="e274e-120">AD FS servers in the DMZ authenticate customer credentials for access to the public web site and partner credentials for access to the partner extranet.</span></span>

<span data-ttu-id="e274e-p104">Contoso a décidé de conserver cette infrastructure pour la dédier à l’authentification des clients et des partenaires. Les ingénieurs en identité de Contoso examinent actuellement la possibilité de convertir cette infrastructure en solutions [B2B](https://docs.microsoft.com/azure/active-directory/b2b/hybrid-organizations) et [B2C](https://docs.microsoft.com/azure/active-directory-b2c/solution-articles) Azure AD.</span><span class="sxs-lookup"><span data-stu-id="e274e-p104">Contoso decided to keep this infrastructure and dedicate it to customer and partner authentications. Contoso identity engineers are investigating the conversion of this infrastructure to Azure AD [B2B](https://docs.microsoft.com/azure/active-directory/b2b/hybrid-organizations) and [B2C](https://docs.microsoft.com/azure/active-directory-b2c/solution-articles) solutions.</span></span>

## <a name="hybrid-identity-with-password-hash-synchronization-for-cloud-based-authentication"></a><span data-ttu-id="e274e-123">Identité hybride avec authentification directe pour l’authentification basée sur le cloud</span><span class="sxs-lookup"><span data-stu-id="e274e-123">Hybrid identity with password hash synchronization for cloud-based authentication</span></span>

<span data-ttu-id="e274e-124">Contoso souhaite tirer parti de son ensemble local AD DS pour l’authentification aux ressources cloud de Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="e274e-124">Contoso wanted to leverage its on-premises Windows Server AD forest for authentication to Microsoft 365 cloud resources. It decided on pass-through authentication (PTA) with password hash synchronization (PHS).</span></span> <span data-ttu-id="e274e-125">Il a décidé du hachage de synchronisation du mot de passe (PHS).</span><span class="sxs-lookup"><span data-stu-id="e274e-125">It decided on password hash synchronization (PHS).</span></span>

<span data-ttu-id="e274e-126">PBS synchronise la version de l’ensemble local AD DS avec le client Azure AD de l’abonnement Microsoft 365 Entreprise, copie des comptes d’utilisateur et de groupe et une version hachurée de mots de passe du compte utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e274e-126">PHS synchronizes the on-premises Windows Server AD forest with the Azure AD tenant of their Microsoft 365 Enterprise subscription, copying user and group accounts and a hashed version of user account passwords. Contoso decided on PHS to provide an alternate method of authentication directly with the Azure AD tenant in the event that PTA is not available.</span></span> 

<span data-ttu-id="e274e-127">Pour effectuer la synchronisation d’annuaire en cours, Contoso a déployé l’outil Azure AD Connect sur un serveur dans son centre de données de Paris.</span><span class="sxs-lookup"><span data-stu-id="e274e-127">To perform the ongoing directory synchronization, Contoso has deployed the Azure AD Connect tool on a server in its Paris datacenter. Figure 4 shows the server running Azure AD Connect polling the Contoso Windows Server AD forest for changes and then synchronizing those changes with the Azure AD tenant.</span></span> <span data-ttu-id="e274e-128">La figure 3 montre le serveur exécutant la connexion Azure Active Directory Connect interrogeant l’ensemble Contoso AD DS pour les modifications de l’interrogation et la synchronisation de ces modifications avec le client Azure AD.</span><span class="sxs-lookup"><span data-stu-id="e274e-128">To perform the ongoing directory synchronization, Contoso has deployed the Azure AD Connect tool on a server in its Paris datacenter. Figure 4 shows the server running Azure AD Connect polling the Contoso Windows Server AD forest for changes and then synchronizing those changes with the Azure AD tenant.</span></span>

![](./media/contoso-identity/contoso-identity-fig4.png)
 
<span data-ttu-id="e274e-129">**Figure 3 : infrastructure de la synchronisation d’annuaires de synchronisation de hachage de mot de passe de Contoso**</span><span class="sxs-lookup"><span data-stu-id="e274e-129">**Figure 3: Contoso's directory synchronization infrastructure**</span></span>


## <a name="conditional-access-policies-for-identity-and-device-access"></a><span data-ttu-id="e274e-130">Stratégies d’accès conditionnel basé sur l’identité et l’appareil</span><span class="sxs-lookup"><span data-stu-id="e274e-130">Conditional access policies for identity and device access</span></span>

<span data-ttu-id="e274e-131">Contoso a créé un jeu d’Azure AD et Intune [stratégies d’accès conditionnel](identity-access-policies.md) pour trois niveaux de protection :</span><span class="sxs-lookup"><span data-stu-id="e274e-131">Contoso created a set of Azure AD and Intune [conditional access policies](identity-access-policies.md) for three protection levels:</span></span>

- <span data-ttu-id="e274e-132">**Référence** les protections s’appliquent à tous les comptes d’utilisateurs</span><span class="sxs-lookup"><span data-stu-id="e274e-132">**Baseline** protections apply to all user accounts</span></span>
- <span data-ttu-id="e274e-133">**Sensibles**les protections s’appliquent aux cadres dirigeants et membres du personnel exécutif</span><span class="sxs-lookup"><span data-stu-id="e274e-133">**Sensitive** protections apply to senior leadership and executive staff</span></span>
- <span data-ttu-id="e274e-134">**Hautement réglementée**les protections s’appliquent à des utilisateurs spécifiques financiers, légaux et leur emplacement géographique de recherche ayant accès aux données hautement réglementées</span><span class="sxs-lookup"><span data-stu-id="e274e-134">**Highly Regulated** protections apply to specific users in the finance, legal, and research departments that have access to highly regulated data</span></span>

<span data-ttu-id="e274e-135">La Figure 4 montre l’ensemble de stratégies d’accès conditionnel basées sur l’identité et l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e274e-135">Figure 5 shows their resulting set of conditional access policies for identity.</span></span>

![](./media/contoso-identity/contoso-identity-fig5.png)
 
<span data-ttu-id="e274e-136">**Figure 4 : stratégies d’accès conditionnel basées sur l’identité et l’appareil de Contoso**</span><span class="sxs-lookup"><span data-stu-id="e274e-136">**Figure 4: Contoso’s identity and device conditional access policies**</span></span>

## <a name="next-step"></a><span data-ttu-id="e274e-137">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="e274e-137">Next step</span></span>

<span data-ttu-id="e274e-138">[Découvrez](contoso-win10.md) comment Contoso tire parti de son infrastructure System Center Configuration Manager pour déployer et maintenir à jour Windows 10 Entreprise au sein de son organisation.</span><span class="sxs-lookup"><span data-stu-id="e274e-138">[Learn](contoso-win10.md) how Contoso is leveraging its System Center Configuration Manager infrastructure to deploy and keep current Windows 10 Enterprise across its organization.</span></span>

## <a name="see-also"></a><span data-ttu-id="e274e-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e274e-139">See also</span></span>

[<span data-ttu-id="e274e-140">Identité pour Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="e274e-140">Identity for Microsoft 365 Enterprise</span></span>](identity-infrastructure.md)

[<span data-ttu-id="e274e-141">Guide de déploiement</span><span class="sxs-lookup"><span data-stu-id="e274e-141">Deployment guide</span></span>](deploy-microsoft-365-enterprise.md)

[<span data-ttu-id="e274e-142">Guides de laboratoire de test</span><span class="sxs-lookup"><span data-stu-id="e274e-142">Test lab guides</span></span>](m365-enterprise-test-lab-guides.md)
