---
title: 'Étape 1 : Planifier les utilisateurs et les groupes'
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 03/13/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
ms.custom: ''
description: Planifiez l’ensemble des utilisateurs et des groupes qui travailleront pour votre organisation.
ms.openlocfilehash: 8062cc2b681f0ae45a8114a6d827f5d1ece2fe3e
ms.sourcegitcommit: eb1a77e4cc4e8f564a1c78d2ef53d7245fe4517a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/28/2018
ms.locfileid: "26866831"
---
# <a name="step-1-plan-for-users-and-groups"></a><span data-ttu-id="410f8-103">Étape 1 : Planifier les utilisateurs et les groupes</span><span class="sxs-lookup"><span data-stu-id="410f8-103">Step 1: Plan for users and groups</span></span>

<span data-ttu-id="410f8-104">*Cette étape est requise et s’applique aux versions E3 et E5 de Microsoft 365 Entreprise*</span><span class="sxs-lookup"><span data-stu-id="410f8-104">*This step is required and applies to both the E3 and E5 versions of Microsoft 365 Enterprise*</span></span>

![](./media/deploy-foundation-infrastructure/identity_icon-small.png)

<span data-ttu-id="410f8-p101">À cette étape, vous allez créer votre infrastructure d’identités qui combine des utilisateurs, des groupes et l’appartenance à un groupe avec des fonctionnalités de sécurité dans la configuration correcte. Vous pouvez ainsi :</span><span class="sxs-lookup"><span data-stu-id="410f8-p101">In this step, you'll create your identity infrastructure that combines users, groups, and group membership with security features in the correct configuration. This allows you to:</span></span>

- <span data-ttu-id="410f8-107">contrôler qui a accès aux ressources dans votre environnement ;</span><span class="sxs-lookup"><span data-stu-id="410f8-107">Maintain control over who has access to resources in your environment.</span></span>
- <span data-ttu-id="410f8-108">sécuriser l’accès avec des contrôles qui garantissent de fortes assurances concernant l’identité (les utilisateurs sont ce qu’ils déclarent être) et l’accès à partir d’appareils approuvés ;</span><span class="sxs-lookup"><span data-stu-id="410f8-108">Secure access with controls that ensure strong assurances of identity (users are who they say they are) and access from safe devices.</span></span>
- <span data-ttu-id="410f8-109">configurer des ressources dans votre environnement avec des autorisations appropriées pour réduire le risque potentiel de fuite des données.</span><span class="sxs-lookup"><span data-stu-id="410f8-109">Provision resources in your environment with appropriate permissions to reduce the potential for harm and data leakage.</span></span> 
- <span data-ttu-id="410f8-110">surveiller votre environnement afin de contrôler les comportements d’utilisateur anormaux et agir automatiquement.</span><span class="sxs-lookup"><span data-stu-id="410f8-110">Monitor your environment for anomalous user behavior and automatically taking action.</span></span>

## <a name="plan-your-primary-identity-provider"></a><span data-ttu-id="410f8-111">Planifier votre fournisseur d’identité principal</span><span class="sxs-lookup"><span data-stu-id="410f8-111">Plan your primary identity provider</span></span>

<span data-ttu-id="410f8-p102">Pour créer votre infrastructure d’identités, vous désignerez un fournisseur d’identité principal. Ce service stocke les comptes d’utilisateur et leurs attributs, groupes et appartenances, et prend en charge leur administration continue.</span><span class="sxs-lookup"><span data-stu-id="410f8-p102">To create your identity infrastructure, you'll designate a primary identity provider. This service stores user accounts and their attributes, groups and their memberships, and supports their ongoing administration.</span></span>

<span data-ttu-id="410f8-114">Lorsque votre organisation adopte Microsoft 365 Entreprise, votre fournisseur d’identité principal peut être :</span><span class="sxs-lookup"><span data-stu-id="410f8-114">When your organization adopts Microsoft 365 Enterprise, your primary identity provider is either:</span></span>

- <span data-ttu-id="410f8-p103">**Windows Server Active Directory (AD)**, un fournisseur d’identité intranet hébergé sur des ordinateurs exécutant Windows Server. Cela est généralement utilisé par les organisations qui ont un fournisseur d’identité local existant.</span><span class="sxs-lookup"><span data-stu-id="410f8-p103">**Windows Server Active Directory (AD)**, an intranet identity provider hosted on computers running Windows Server. This is typically used by organizations that have an existing on-premises identity provider.</span></span>
- <span data-ttu-id="410f8-p104">**Azure Active Directory (Azure AD**), une identité basée sur le cloud en tant que Service (IDaaS) qui fournit un large éventail de fonctionnalités pour la gestion et la protection de votre environnement. Cela est généralement utilisé par les organisations qui n’ont aucune infrastructure locale existante.</span><span class="sxs-lookup"><span data-stu-id="410f8-p104">**Azure Active Directory (Azure AD**), a cloud-based Identity as a Service (IDaaS) that provides a broad range of capabilities for managing and protecting your environment. This is typically used by organizations that have no existing on-premises infrastructure.</span></span>

<span data-ttu-id="410f8-p105">Si votre organisation a un fournisseur d’identité local existant, vous devez synchroniser vos groupes et comptes d’utilisateur de Windows Server AD avec Azure AD pour fournir un accès plus transparent aux services basés sur le cloud de Microsoft 365 Entreprise. Vous pouvez également utiliser Azure AD pour créer et gérer des groupes qui existent uniquement dans le cloud Microsoft.</span><span class="sxs-lookup"><span data-stu-id="410f8-p105">If your organization has an existing on-premises identity provider, you need to synchronize your user accounts and groups from Windows Server AD to Azure AD to provide more seamless access to the cloud-based services of Microsoft 365 Enterprise. You can also use Azure AD to create and manage groups that exist only in the Microsoft cloud.</span></span>

<span data-ttu-id="410f8-121">Une fois que vous avez vos utilisateurs et groupes dans Azure AD, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="410f8-121">After you have your users and groups in Azure AD, you can:</span></span>

- <span data-ttu-id="410f8-122">gérer tous les comptes Azure AD pour toutes vos applications cloud ;</span><span class="sxs-lookup"><span data-stu-id="410f8-122">Manage all the Azure AD accounts for all your cloud applications.</span></span> 
- <span data-ttu-id="410f8-123">utiliser le même ensemble de contrôles pour protéger l’accès aux applications au sein de votre environnement ;</span><span class="sxs-lookup"><span data-stu-id="410f8-123">Use the same set of controls to protect access to applications across your environment.</span></span>
- <span data-ttu-id="410f8-124">collaborer avec des partenaires externes ;</span><span class="sxs-lookup"><span data-stu-id="410f8-124">Collaborate with external partners.</span></span>
- <span data-ttu-id="410f8-125">surveiller un comportement de compte anormal (comme des tentatives de connexion suspectes) et agir automatiquement.</span><span class="sxs-lookup"><span data-stu-id="410f8-125">Monitor anomalous account behavior, such as suspicious sign-in attempts, and automatically act.</span></span>

<span data-ttu-id="410f8-126">Lisez les instructions des deux sections suivantes pour planifier et implémenter vos groupes et comptes d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="410f8-126">Follow the instructions in the next two sections to plan for and implement your user accounts and groups.</span></span>

## <a name="categorize-your-users"></a><span data-ttu-id="410f8-127">Classer vos utilisateurs</span><span class="sxs-lookup"><span data-stu-id="410f8-127">Categorize your users</span></span>
<span data-ttu-id="410f8-p106">Les utilisateurs dans les organisations peuvent être classés de plusieurs façons. Par exemple, certains utilisateurs sont des employés qui ont un statut permanent. Certains sont des fournisseurs, des entrepreneurs ou des partenaires qui ont un statut temporaire. Certains sont des utilisateurs externes qui n’ont aucun compte d’utilisateur mais doivent avoir accès à des ressources et services spécifiques pour prendre en charge l’interaction et la collaboration. Par exemple :</span><span class="sxs-lookup"><span data-stu-id="410f8-p106">Users in organizations can be categorized in a number of ways. For example, some are employees and have a permanent status. Some are vendors, contractors, or partners that have a temporary status. Some are external users that have no user accounts but must still be granted access to specific services and resources to support interaction and collaboration. For example:</span></span>

- <span data-ttu-id="410f8-133">Les comptes client représentent les utilisateurs au sein de votre organisation auxquels vous octroyez une licence pour les services cloud</span><span class="sxs-lookup"><span data-stu-id="410f8-133">Tenant accounts represent users within your organization that you license for cloud services</span></span>
- <span data-ttu-id="410f8-134">Les comptes B2B représentent les utilisateurs externes à votre organisation que vous invitez à participer à la collaboration</span><span class="sxs-lookup"><span data-stu-id="410f8-134">Business to Business (B2B) accounts represent users outside your organization that you invite to participate in collaboration</span></span>

<span data-ttu-id="410f8-p107">Répertoriez les types d’utilisateurs de votre organisation. Quels sont les regroupements ? Par exemple, vous pouvez regrouper des utilisateurs par fonction de haut niveau ou par objectif pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="410f8-p107">Take stock of the types of users to your organization. What are the groupings? For example, you can group users by high-level function or purpose to your organization.</span></span>

<span data-ttu-id="410f8-p108">Par ailleurs, certains services cloud peuvent être partagés avec des utilisateurs externes à votre organisation sans comptes d’utilisateur. Vous devrez identifier ces groupes d’utilisateurs également.</span><span class="sxs-lookup"><span data-stu-id="410f8-p108">Additionally, some cloud services can be shared with users outside your organization without any user accounts. You'll need to identify these groups of users as well.</span></span>

## <a name="plan-for-windows-server-ad-and-azure-ad-groups"></a><span data-ttu-id="410f8-140">Planifier pour des groupes Windows Server AD et Azure AD</span><span class="sxs-lookup"><span data-stu-id="410f8-140">Plan for Windows Server AD and Azure AD groups</span></span>

<span data-ttu-id="410f8-p109">Vous pouvez utiliser des groupes dans Azure AD à plusieurs fins qui simplifient la gestion de votre environnement cloud. Par exemple, pour les groupes Azure AD, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="410f8-p109">You can use groups in Azure AD for several purposes that simplify management of your cloud environment. For example, for Azure AD groups, you can:</span></span>

- <span data-ttu-id="410f8-143">utiliser la gestion des licences par groupes pour attribuer des licences pour Office 365 et Enterprise Mobility + Security (EMS) à vos comptes d’utilisateur automatiquement dès qu’ils sont ajoutés dans Azure AD ou synchronisés à partir de Windows Server AD ;</span><span class="sxs-lookup"><span data-stu-id="410f8-143">Use group-based licensing to assign licenses for Office 365 and Enterprise Mobility + Security (EMS) to your user accounts automatically as soon as they are added in Azure AD or synchronized from Windows Server AD.</span></span> 
- <span data-ttu-id="410f8-144">ajouter des comptes d’utilisateur à des groupes spécifiques dynamiquement basés sur des attributs de compte d’utilisateur, comme l’attribut service ;</span><span class="sxs-lookup"><span data-stu-id="410f8-144">Add user accounts to specific groups dynamically based on user account attributes, such as department.</span></span>  
- <span data-ttu-id="410f8-145">configurer automatiquement des utilisateurs pour des applications SaaS et protéger l’accès à ces applications avec l’authentification multifacteur et d’autres règles d’accès conditionnel ;</span><span class="sxs-lookup"><span data-stu-id="410f8-145">Automatically provision users for Software as a Service (SaaS) applications and to protect access to those applications with multi-factor authentication and other conditional access rules.</span></span>
- <span data-ttu-id="410f8-p110">configurer les autorisations et niveaux d’accès pour les sites d’équipe SharePoint Online. Les groupes Azure AD peuvent également être utilisés avec des stratégies Azure Information Protection limitées pour protéger des fichiers avec le chiffrement et les autorisations.</span><span class="sxs-lookup"><span data-stu-id="410f8-p110">Provision permissions and levels of access for SharePoint Online team sites. Azure AD groups can also be used with scoped Azure Information Protection policies to protect files with encryption and permissions.</span></span> 

## <a name="results"></a><span data-ttu-id="410f8-148">Résultats</span><span class="sxs-lookup"><span data-stu-id="410f8-148">Results</span></span>

<span data-ttu-id="410f8-149">Lorsque vous terminez cette étape, vous avez :</span><span class="sxs-lookup"><span data-stu-id="410f8-149">When you complete this step, you’ll have:</span></span>

- <span data-ttu-id="410f8-150">une liste de comptes d’utilisateur dans Azure AD qui correspondent aux employés au sein de votre organisation et les fournisseurs, entrepreneurs et partenaires qui travaillent pour ou avec votre organisation ;</span><span class="sxs-lookup"><span data-stu-id="410f8-150">A list of user accounts in Azure AD that correspond to the employees in your organization and the vendors, contractors, and external partners that work for or with your organization.</span></span>
- <span data-ttu-id="410f8-151">un ensemble de groupes et leur appartenance dans Azure AD qui représentent des ensembles logiques de comptes d’utilisateur et d’autres groupes pour l’attribution de paramètres de sécurité pour les services de cloud computing Microsoft et l’attribution automatique de licences.</span><span class="sxs-lookup"><span data-stu-id="410f8-151">A set of groups and their membership in Azure AD that reflect logical sets of user accounts and other groups for automatic licensing provisioning of security settings for Microsoft cloud services.</span></span>

<span data-ttu-id="410f8-152">Comme point de vérification intermédiaire, vous pouvez consulter les [critères de sortie](identity-exit-criteria.md#crit-identity-user-groups) pour cette étape.</span><span class="sxs-lookup"><span data-stu-id="410f8-152">As an interim checkpoint, you can see the [exit criteria](identity-exit-criteria.md#crit-identity-user-groups) for this step.</span></span>


## <a name="next-step"></a><span data-ttu-id="410f8-153">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="410f8-153">Next step</span></span>

|||
|:-------|:-----|
|![](./media/stepnumbers/Step2.png)| [<span data-ttu-id="410f8-154">Protéger des comptes Administrateur général</span><span class="sxs-lookup"><span data-stu-id="410f8-154">Protect global administrator accounts</span></span>](identity-designate-protect-admin-accounts.md) |

