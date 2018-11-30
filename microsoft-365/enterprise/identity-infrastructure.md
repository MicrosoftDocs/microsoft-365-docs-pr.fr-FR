---
title: 'Phase 2 : Identité'
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 09/18/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
ms.custom: ''
description: Les étapes de déploiement de l’infrastructure d’identités pour Microsoft 365 Entreprise.
ms.openlocfilehash: 7b5d62f5c09a1ea6d46449b113bff59dbf07ebad
ms.sourcegitcommit: eb1a77e4cc4e8f564a1c78d2ef53d7245fe4517a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/28/2018
ms.locfileid: "26867244"
---
# <a name="phase-2-identity"></a><span data-ttu-id="dcb73-103">Phase 2 : Identité</span><span class="sxs-lookup"><span data-stu-id="dcb73-103">Phase 2: Identity</span></span>

![](./media/deploy-foundation-infrastructure/identity_icon.png)

<span data-ttu-id="dcb73-104">Dans Microsoft 365 Entreprise, une infrastructure d’identités bien planifiée et exécutée ouvre la voie à une sécurité plus forte et à un accès à vos charges de travail de productivité et à leurs données uniquement par des utilisateurs et appareils authentifiés.</span><span class="sxs-lookup"><span data-stu-id="dcb73-104">In Microsoft 365 Enterprise, a well-planned and executed identity infrastructure paves the way for stronger security and access to your productivity workloads and their data only by authenticated users and devices.</span></span>

>[!Note]
><span data-ttu-id="dcb73-105">Si vous avez déjà déployé une infrastructure d’identités, consultez les [critères de sortie d’identité](identity-exit-criteria.md) pour vous assurer que vous répondez aux conditions requises et facultatives pour Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="dcb73-105">If you’ve already deployed an identity infrastructure, please see the [identity exit criteria](identity-exit-criteria.md) to make sure that you meet the required and optional conditions for Microsoft 365 Enterprise.</span></span>
>

## <a name="plan-and-deploy-your-microsoft-365-enterprise-identity-infrastructure"></a><span data-ttu-id="dcb73-106">Planifier et déployer votre infrastructure d’identités de Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="dcb73-106">Plan and deploy your Microsoft 365 Enterprise identity infrastructure</span></span> 

<span data-ttu-id="dcb73-p101">Procédez comme suit pour planifier et déployer votre nouvelle infrastructure d’identités dans le cloud. Vous pouvez également utiliser ces étapes pour adapter votre infrastructure d’identités locale ou hybride et l’utiliser avec Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="dcb73-p101">Use the following steps to plan and deploy your new identity infrastructure in the cloud. You can also use these steps to adapt your existing on-premises or hybrid identity infrastructure to work with Microsoft 365 Enterprise.</span></span> 

|||
|:-------|:-----|
|![](./media/stepnumbers/Step1.png)| [<span data-ttu-id="dcb73-109">Planifiez les utilisateurs et les groupes</span><span class="sxs-lookup"><span data-stu-id="dcb73-109">Plan for users and groups</span></span>](identity-plan-users-groups.md) |
|![](./media/stepnumbers/Step2.png)| [<span data-ttu-id="dcb73-110">Protéger des comptes Administrateur général</span><span class="sxs-lookup"><span data-stu-id="dcb73-110">Protect global administrator accounts</span></span>](identity-designate-protect-admin-accounts.md) |
|![](./media/stepnumbers/Step3.png)| [<span data-ttu-id="dcb73-111">Configurez des administrateurs généraux à la demande</span><span class="sxs-lookup"><span data-stu-id="dcb73-111">Set up on-demand global administrators</span></span>](identity-privileged-identity-management.md) |
|![](./media/stepnumbers/Step4.png)| [<span data-ttu-id="dcb73-112">Simplifiez les réinitialisations du mot de passe</span><span class="sxs-lookup"><span data-stu-id="dcb73-112">Simplify password resets</span></span>](identity-password-reset.md) |
|![](./media/stepnumbers/Step5.png)| [<span data-ttu-id="dcb73-113">Configurer l’authentification multifacteur</span><span class="sxs-lookup"><span data-stu-id="dcb73-113">Set up multi-factor authentication</span></span>](identity-multi-factor-authentication.md) |
|![](./media/stepnumbers/Step6.png)| [<span data-ttu-id="dcb73-114">Protégez-vous contre la compromission de confidentialité</span><span class="sxs-lookup"><span data-stu-id="dcb73-114">Protect against credential compromise</span></span>](identity-azure-ad-identity-protection.md) |
|![](./media/stepnumbers/Step7.png)| [<span data-ttu-id="dcb73-115">Synchronisez des annuaires</span><span class="sxs-lookup"><span data-stu-id="dcb73-115">Synchronize directories</span></span>](identity-azure-ad-connect.md) |
|![](./media/stepnumbers/Step8.png)| [<span data-ttu-id="dcb73-116">Surveillez l’état de la synchronisation</span><span class="sxs-lookup"><span data-stu-id="dcb73-116">Monitor synchronization health</span></span>](identity-azure-ad-connect-health.md) |
|![](./media/stepnumbers/Step9.png)| [<span data-ttu-id="dcb73-117">Simplifiez les mises à jour du mot de passe</span><span class="sxs-lookup"><span data-stu-id="dcb73-117">Simplify password updates</span></span>](identity-password-writeback.md) |
|![](./media/stepnumbers/Step10.png)| [<span data-ttu-id="dcb73-118">Simplifiez la connexion de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="dcb73-118">Simplify user sign-in</span></span>](identity-single-sign-on.md) |
|![](./media/stepnumbers/Step11.png)| [<span data-ttu-id="dcb73-119">Personnaliser la page de connexion à Office 365</span><span class="sxs-lookup"><span data-stu-id="dcb73-119">Customize the Office 365 sign-in page</span></span>](identity-customize-office-365-sign-in.md) |
|![](./media/stepnumbers/Step12.png)| [<span data-ttu-id="dcb73-120">Configurez la gestion des licences automatique</span><span class="sxs-lookup"><span data-stu-id="dcb73-120">Set up automatic licensing</span></span>](identity-group-based-licensing.md) |
|![](./media/stepnumbers/Step13.png)| [<span data-ttu-id="dcb73-121">Surveillez l’activité de connexion et du client</span><span class="sxs-lookup"><span data-stu-id="dcb73-121">Monitor tenant and sign-in activity</span></span>](identity-azure-ad-access-usage-reporting.md) |
|![](./media/stepnumbers/Step14.png)| [<span data-ttu-id="dcb73-122">Autorisez les utilisateurs à créer et gérer leurs propres groupes</span><span class="sxs-lookup"><span data-stu-id="dcb73-122">Allow users to create and manage their own groups</span></span>](identity-self-service-group-management.md) |
|![](./media/stepnumbers/Step15.png)| [<span data-ttu-id="dcb73-123">Configurez l’appartenance à un groupe dynamique</span><span class="sxs-lookup"><span data-stu-id="dcb73-123">Set up dynamic group membership</span></span>](identity-automatic-group-membership.md) |

<span data-ttu-id="dcb73-124">Lorsque vous avez terminé ces étapes, accédez aux [critères de sortie](identity-exit-criteria.md) de cette phase pour vous assurer que vous répondez aux conditions requises et facultatives pour Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="dcb73-124">When you've completed these steps, go to the [exit criteria](identity-exit-criteria.md) for this phase to ensure that you meet the required and optional conditions for Microsoft 365 Enterprise.</span></span>

## <a name="identity-and-device-access-recommendations"></a><span data-ttu-id="dcb73-125">Recommandations en matière d’identité et d’accès aux appareils</span><span class="sxs-lookup"><span data-stu-id="dcb73-125">Identity and device access prerequisites</span></span>

<span data-ttu-id="dcb73-p102">Microsoft fournit un ensemble de recommandations en matière d’[identité et d’accès aux appareils](microsoft-365-policies-configurations.md) afin de garantir un personnel sécurisé et productif. Pour l’identité, utilisez les recommandations et les paramètres des articles suivants, ainsi que les étapes décrites dans cette phase :</span><span class="sxs-lookup"><span data-stu-id="dcb73-p102">Microsoft provides a set of recommendations for [identity and device access](microsoft-365-policies-configurations.md) to ensure a secure and productive workforce. For identity, use the recommendations and settings in the following articles along with the steps in this phase:</span></span>

- [<span data-ttu-id="dcb73-128">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="dcb73-128">Prerequisites</span></span>](identity-access-prerequisites.md)
- [<span data-ttu-id="dcb73-129">Stratégies communes pour les identités et l’accès aux appareils</span><span class="sxs-lookup"><span data-stu-id="dcb73-129">Common identity and device access policies</span></span>](identity-access-policies.md)

## <a name="how-microsoft-does-microsoft-365-enterprise"></a><span data-ttu-id="dcb73-130">Comment Microsoft gère-t-il Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="dcb73-130">How Microsoft does Microsoft 365 Enterprise</span></span>

<span data-ttu-id="dcb73-131">Découvrez comment les experts informatiques de Microsoft ont conçu et déployé les fonctionnalités d’identité de Microsoft 365 Entreprise en consultant les ressources suivantes :</span><span class="sxs-lookup"><span data-stu-id="dcb73-131">Learn how IT experts at Microsoft planned for and deployed the identity capabilities of Microsoft 365 Enterprise with these resources:</span></span>

- [<span data-ttu-id="dcb73-132">Gestion des identités d’utilisateur et accès sécurisé à Microsoft</span><span class="sxs-lookup"><span data-stu-id="dcb73-132">Managing user identities and secure access at Microsoft</span></span>](https://www.microsoft.com/itshowcase/Article/Content/931/Managing-user-identities-and-secure-access-at-Microsoft)
- [<span data-ttu-id="dcb73-133">Utilisation d’Azure AD Privileged Identity Management pour un accès privilégié</span><span class="sxs-lookup"><span data-stu-id="dcb73-133">Using Azure AD Privileged Identity Management for elevated access</span></span>](https://www.microsoft.com/itshowcase/Article/Content/887/Using-Azure-AD-Privileged-Identity-Management-for-elevated-access)

## <a name="how-contoso-did-microsoft-365-enterprise"></a><span data-ttu-id="dcb73-134">Comment Contoso est-elle passée à Microsoft 365 Entreprise ?</span><span class="sxs-lookup"><span data-stu-id="dcb73-134">How Contoso did Microsoft 365 Enterprise</span></span>

<span data-ttu-id="dcb73-135">Découvrez comment Contoso Corporation, une entreprise multinationale fictive mais représentative, [a déployé une infrastructure d’identité hybride](contoso-identity.md) pour les services cloud Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="dcb73-135">See how the Contoso Corporation, a fictional but representative multi-national business, [optimized their network](contoso-identity.md) for Microsoft 365 cloud services.</span></span>

![](./media/contoso-overview/contoso-icon.png)


## <a name="next-step"></a><span data-ttu-id="dcb73-136">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="dcb73-136">Next step</span></span>

|||
|:-------|:-----|
|![](./media/stepnumbers/Step1.png)| [<span data-ttu-id="dcb73-137">Planifiez les utilisateurs et les groupes</span><span class="sxs-lookup"><span data-stu-id="dcb73-137">Plan for users and groups</span></span>](identity-plan-users-groups.md) |
