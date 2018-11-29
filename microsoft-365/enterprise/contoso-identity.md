---
title: Identité de Contoso Corporation
author: JoeDavies-MSFT
ms.author: josephd
manager: laurawi
ms.date: 09/13/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
ms.custom: ''
description: Découvrez comment Contoso tire parti de la solution de gestion des identités IDaaS et propose à ses employés une authentification basée sur le cloud, et une authentification fédérée à ses partenaires et ses clients.
ms.openlocfilehash: 7571aa455cac4da9e56d7d2001ae4421c3769c94
ms.sourcegitcommit: eb1a77e4cc4e8f564a1c78d2ef53d7245fe4517a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/28/2018
ms.locfileid: "26867308"
---
# <a name="identity-for-the-contoso-corporation"></a><span data-ttu-id="39fb5-103">Identité de Contoso Corporation</span><span class="sxs-lookup"><span data-stu-id="39fb5-103">Identity for the Contoso Corporation</span></span>

<span data-ttu-id="39fb5-104">**Résumé :** Découvrez comment Contoso tire parti de la solution de gestion des identités IDaaS et propose à ses employés une authentification basée sur le cloud, et une authentification fédérée à ses partenaires et ses clients.</span><span class="sxs-lookup"><span data-stu-id="39fb5-104">**Summary:** How Contoso takes advantage of Identity as a Service (IDaaS) and provides cloud-based authentication for its employees and federated authentication for its partners and customers.</span></span>

<span data-ttu-id="39fb5-p101">Microsoft propose une solution de gestion des identités IDaaS dans toutes ses offres cloud dotées d’Azure Active Directory (AD). Pour adopter Microsoft 365 Entreprise, la solution IDaaS de Contoso doit tirer parti de son fournisseur d’identités local et continuer d’intégrer l’authentification fédérée avec ses fournisseurs d’identité tiers approuvés existants.</span><span class="sxs-lookup"><span data-stu-id="39fb5-p101">Microsoft provides an Identity as a Service (IDaaS) across its cloud offerings with Azure Active Directory (AD). To adopt Microsoft 365 Enterprise, Contoso's IDaaS solution had to leverage their on-premises identity provider and still include federated authentication with their existing trusted, third-party identity providers.</span></span>

## <a name="contosos-windows-server-ad-forest"></a><span data-ttu-id="39fb5-107">Forêt Windows Server AD de Contoso</span><span class="sxs-lookup"><span data-stu-id="39fb5-107">Contoso's Windows Server AD forest</span></span>

<span data-ttu-id="39fb5-p102">Contoso utilise une forêt Windows Server AD (Active Directory) unique pour sept sous-domaines de contoso.com, un pour chaque région du monde. Le siège social, les bureaux régionaux et les succursales possèdent des contrôleurs de domaine pour l’authentification et l’autorisation locales.</span><span class="sxs-lookup"><span data-stu-id="39fb5-p102">Contoso uses a single Windows Server Active Directory (AD) forest for contoso.com with seven sub-domains, one for each region of the world. The headquarters, regional hub offices, and satellite offices contain domain controllers for local authentication and authorization.</span></span>

<span data-ttu-id="39fb5-110">La Figure 1 présente la forêt et les domaines régionaux de Contoso dans les régions du monde où se trouvent des centres régionaux.</span><span class="sxs-lookup"><span data-stu-id="39fb5-110">Figure 1 shows the Contoso forest with regional domains for the different parts of the world that contain regional hubs.</span></span>

![](./media/contoso-identity/contoso-identity-fig1.png)
 
<span data-ttu-id="39fb5-111">**Figure 1 : forêt et domaines de Contoso dans le monde**</span><span class="sxs-lookup"><span data-stu-id="39fb5-111">**Figure 1: Contoso's forest and domains worldwide**</span></span>

<span data-ttu-id="39fb5-112">Contoso souhaite utiliser les comptes et les groupes de la forêt contoso.com pour faciliter l’authentification et l’autorisation de ses applications et de ses charges de travail dans le cloud.</span><span class="sxs-lookup"><span data-stu-id="39fb5-112">Contoso wants to use the accounts and groups in the contoso.com forest for authentication and authorization for its cloud-based apps and workloads.</span></span>

## <a name="contosos-federated-authentication-infrastructure"></a><span data-ttu-id="39fb5-113">Infrastructure d’authentification fédérée de Contoso</span><span class="sxs-lookup"><span data-stu-id="39fb5-113">Contoso's federated authentication infrastructure</span></span>

<span data-ttu-id="39fb5-114">Contoso autorise les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="39fb5-114">Contoso allows:</span></span>

- <span data-ttu-id="39fb5-115">Les clients ont le droit d’utiliser leurs comptes Microsoft, Facebook ou Google Mail pour se connecter à leur site web public.</span><span class="sxs-lookup"><span data-stu-id="39fb5-115">Customers to use their Microsoft, Facebook, or Google Mail accounts to sign in to their public web site.</span></span>
- <span data-ttu-id="39fb5-116">Les fournisseurs et les partenaires peuvent utiliser leurs comptes LinkedIn, Salesforce ou Google Mail pour se connecter à l’extranet des partenaires.</span><span class="sxs-lookup"><span data-stu-id="39fb5-116">Vendors and partners to use their LinkedIn, Salesforce, or Google Mail accounts to sign in to the partner extranet.</span></span>

<span data-ttu-id="39fb5-p103">La Figure 2 montre que le réseau de périmètre de Contoso comprend un site web public, un extranet des partenaires et des serveurs pour les services ADFS (services de fédération Active Directory). Le réseau de périmètre est connecté à Internet, qui contient des clients, des partenaires et des services Internet.</span><span class="sxs-lookup"><span data-stu-id="39fb5-p103">Figure 2 shows the Contoso DMZ containing a public web site, a partner extranet, and a set of Active Directory Federation Services (AD FS) servers. The DMZ is connected to the Internet that contains customers, partners, and Internet services.</span></span>

![](./media/contoso-identity/contoso-identity-fig2.png)

<span data-ttu-id="39fb5-119">**Figure 2 : prise en charge de l’authentification fédérée par Contoso pour ses clients et ses partenaires**</span><span class="sxs-lookup"><span data-stu-id="39fb5-119">**Figure 2: Contoso's support for federated authentication for customers and partners**</span></span>
 
<span data-ttu-id="39fb5-120">Les serveurs des services ADFS du réseau de périmètre utilisent leurs informations d’identification client pour se connecter au site web public et leurs informations d’identification partenaire pour accéder à l’extranet des partenaires.</span><span class="sxs-lookup"><span data-stu-id="39fb5-120">AD FS servers in the DMZ authenticate customer credentials for access to the public web site and partner credentials for access to the partner extranet.</span></span>

<span data-ttu-id="39fb5-p104">Contoso a décidé de conserver cette infrastructure pour la dédier à l’authentification des clients et des partenaires. Les ingénieurs en identité de Contoso examinent actuellement la possibilité de convertir cette infrastructure en solutions [B2B](https://docs.microsoft.com/azure/active-directory/b2b/hybrid-organizations) et [B2C](https://docs.microsoft.com/azure/active-directory-b2c/solution-articles) Azure AD.</span><span class="sxs-lookup"><span data-stu-id="39fb5-p104">Contoso decided to keep this infrastructure and dedicate it to customer and partner authentications. Contoso identity engineers are investigating the conversion of this infrastructure to Azure AD [B2B](https://docs.microsoft.com/azure/active-directory/b2b/hybrid-organizations) and [B2C](https://docs.microsoft.com/azure/active-directory-b2c/solution-articles) solutions.</span></span>

## <a name="hybrid-identity-with-pass-through-authentication-for-cloud-based-authentication"></a><span data-ttu-id="39fb5-123">Identité hybride avec authentification directe pour l’authentification basée sur le cloud</span><span class="sxs-lookup"><span data-stu-id="39fb5-123">Hybrid identity with pass-through authentication for cloud-based authentication</span></span>

<span data-ttu-id="39fb5-p105">Contoso voulait tirer parti de sa forêt Windows Server AD locale pour configurer l’authentification aux ressources cloud de Microsoft 365. L’entreprise a opté pour l’authentification directe avec la synchronisation de hachage de mot de passe.</span><span class="sxs-lookup"><span data-stu-id="39fb5-p105">Contoso wanted to leverage its on-premises Windows Server AD forest for authentication to Microsoft 365 cloud resources. It decided on pass-through authentication (PTA) with password hash synchronization (PHS).</span></span>

### <a name="pta-authentication"></a><span data-ttu-id="39fb5-126">Authentification directe</span><span class="sxs-lookup"><span data-stu-id="39fb5-126">PTA authentication</span></span>

<span data-ttu-id="39fb5-p106">Pour l’authentification des informations d’identification utilisateur, Contoso utilise l’authentification directe. Quand un utilisateur Contoso accède à des ressources cloud, les informations d’identification envoyées sont transmises par Azure AD à un serveur qui exécute un agent d’authentification dans le centre de données du siège de Contoso. L’un des serveurs de l’agent d’authentification valide les informations d’identification utilisateur au nom d’Azure AD.</span><span class="sxs-lookup"><span data-stu-id="39fb5-p106">For authentication of user credentials, Contoso is using PTA. When a Contoso user accesses a cloud-based resources, the credentials it sends are passed by Azure AD to a server running an Authentication Agent in the Contoso headquarters datacenter. One of these Authentication Agent servers validates the user credentials on behalf of Azure AD.</span></span>

<span data-ttu-id="39fb5-130">La Figure 3 montre un ensemble de serveurs situés au siège de Contoso, qui exécutent l’agent d’authentification, lequel traite les demandes d’authentification transmises par Azure AD.</span><span class="sxs-lookup"><span data-stu-id="39fb5-130">Figure 3 shows a set of servers in the Contoso headquarters running the Authentication Agent, which process authentication requests passed to it from Azure AD.</span></span> 

![](./media/contoso-identity/contoso-identity-fig3.png)
 
<span data-ttu-id="39fb5-131">**Figure 3 : infrastructure de l’authentification directe de Contoso**</span><span class="sxs-lookup"><span data-stu-id="39fb5-131">**Figure 3: Contoso's pass-through authentication infrastructure**</span></span>

<span data-ttu-id="39fb5-132">Contoso a opté pour l’authentification directe pour répondre à l’une de ses mesures de sécurité, à savoir évaluer toutes les tentatives d’authentification qui présenteraient un changement d’état du compte d’utilisateur, de stratégie de mot de passe et d’heure de connexion apporté à la forêt Windows Server AD locale.</span><span class="sxs-lookup"><span data-stu-id="39fb5-132">Contoso chose PTA to fulfill its security requirement that all authentication attempts be evaluated for immediate changes to user account states, password policies, and sign-in hours made to the on-premises Windows Server AD forest.</span></span>

### <a name="phs"></a><span data-ttu-id="39fb5-133">Synchronisation de hachage de mot de passe</span><span class="sxs-lookup"><span data-stu-id="39fb5-133">PHS</span></span>

<span data-ttu-id="39fb5-p107">La synchronisation de hachage de mot de passe synchronise la forêt Windows Server AD locale avec le client Azure AD de l’abonnement Microsoft 365 Entreprise, en copiant les comptes d’utilisateur et de groupe et une version hachée des mots de passe des comptes d’utilisateur. Contoso a opté pour la synchronisation de hachage de mot de passe pour proposer une autre méthode d’authentification avec le client Azure AD au cas où l’authentification directe ne serait pas disponible.</span><span class="sxs-lookup"><span data-stu-id="39fb5-p107">PHS synchronizes the on-premises Windows Server AD forest with the Azure AD tenant of their Microsoft 365 Enterprise subscription, copying user and group accounts and a hashed version of user account passwords. Contoso decided on PHS to provide an alternate method of authentication directly with the Azure AD tenant in the event that PTA is not available.</span></span>

<span data-ttu-id="39fb5-p108">Pour procéder à la synchronisation de hachage de mot de passe en cours, Contoso a déployé l’outil Azure AD Connect sur un serveur de son centre de données situé à Paris. La Figure 4 montre le serveur exécutant Azure AD Connect qui interroge la forêt Windows Server AD de Contoso pour trouver d’éventuelles modifications et synchronise ces modifications avec le client Azure AD.</span><span class="sxs-lookup"><span data-stu-id="39fb5-p108">To perform the ongoing directory synchronization, Contoso has deployed the Azure AD Connect tool on a server in its Paris datacenter. Figure 4 shows the server running Azure AD Connect polling the Contoso Windows Server AD forest for changes and then synchronizing those changes with the Azure AD tenant.</span></span>

![](./media/contoso-identity/contoso-identity-fig4.png)
 
<span data-ttu-id="39fb5-138">**Figure 4 : infrastructure de la synchronisation d’annuaires de synchronisation de hachage de mot de passe de Contoso**</span><span class="sxs-lookup"><span data-stu-id="39fb5-138">**Figure 4: Contoso's PHS directory synchronization infrastructure**</span></span>

## <a name="conditional-access-policies-for-identity"></a><span data-ttu-id="39fb5-139">Stratégies d’accès conditionnel basées sur l’identité</span><span class="sxs-lookup"><span data-stu-id="39fb5-139">Conditional access policies for identity</span></span>

<span data-ttu-id="39fb5-140">Contoso a créé un ensemble de [stratégies d’accès conditionnel](identity-access-policies.md) Azure AD pour garantir l’application des modifications de mot de passe et de l’authentification multifacteur quand Azure AD détecte un risque de connexion pour une demande d’authentification.</span><span class="sxs-lookup"><span data-stu-id="39fb5-140">Contoso created a set of Azure AD [conditional access policies](identity-access-policies.md) to ensure that multi-factor authentication and password changes are enforced when Azure AD determines there is sign-in risk for an authentication request.</span></span>

<span data-ttu-id="39fb5-141">La Figure 5 montre l’ensemble de stratégies d’accès conditionnel basées sur l’identité de Contoso.</span><span class="sxs-lookup"><span data-stu-id="39fb5-141">Figure 5 shows their resulting set of conditional access policies for identity.</span></span>

![](./media/contoso-identity/contoso-identity-fig5.png)
 
<span data-ttu-id="39fb5-142">**Figure 5 : stratégies d’accès conditionnel basées sur l’identité de Contoso**</span><span class="sxs-lookup"><span data-stu-id="39fb5-142">**Figure 5: Contoso’s identity-based conditional access policies**</span></span>

## <a name="next-step"></a><span data-ttu-id="39fb5-143">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="39fb5-143">Next step</span></span>

<span data-ttu-id="39fb5-144">[Découvrez](contoso-win10.md) comment Contoso tire parti de son infrastructure System Center Configuration Manager pour déployer et maintenir à jour Windows 10 Entreprise au sein de son organisation.</span><span class="sxs-lookup"><span data-stu-id="39fb5-144">[Learn](contoso-win10.md) how Contoso is leveraging its System Center Configuration Manager infrastructure to deploy and keep current Windows 10 Enterprise across its organization.</span></span>

## <a name="see-also"></a><span data-ttu-id="39fb5-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="39fb5-145">See also</span></span>

[<span data-ttu-id="39fb5-146">Identité pour Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="39fb5-146">Identity for Microsoft 365 Enterprise</span></span>](identity-infrastructure.md)

[<span data-ttu-id="39fb5-147">Guide de déploiement</span><span class="sxs-lookup"><span data-stu-id="39fb5-147">Deployment guide</span></span>](deploy-microsoft-365-enterprise.md)

[<span data-ttu-id="39fb5-148">Guides de laboratoire de test</span><span class="sxs-lookup"><span data-stu-id="39fb5-148">Test lab guides</span></span>](m365-enterprise-test-lab-guides.md)
