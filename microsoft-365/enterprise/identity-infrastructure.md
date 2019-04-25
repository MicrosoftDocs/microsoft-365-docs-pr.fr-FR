---
title: 'Phase 2 : Identité'
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 04/16/2019
ms.audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- M365-identity-device-management
- Strat_O365_Enterprise
ms.custom: ''
description: Les étapes de déploiement de l’infrastructure d’identités pour Microsoft 365 Entreprise.
ms.openlocfilehash: 932b6fb2cfeb86edcf708bdfdea55cdd8b580838
ms.sourcegitcommit: 81273a9df49647286235b187fa2213c5ec7e8b62
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288734"
---
# <a name="phase-2-identity"></a><span data-ttu-id="24275-103">Phase 2 : Identité</span><span class="sxs-lookup"><span data-stu-id="24275-103">Phase 2: Identity</span></span>

![](./media/deploy-foundation-infrastructure/identity_icon.png)

<span data-ttu-id="24275-104">Dans Microsoft 365 Entreprise, une infrastructure d’identités bien planifiée et exécutée ouvre la voie à une sécurité plus forte et à un accès à vos charges de travail de productivité et à leurs données uniquement par des utilisateurs et appareils authentifiés.</span><span class="sxs-lookup"><span data-stu-id="24275-104">In Microsoft 365 Enterprise, a well-planned and executed identity infrastructure paves the way for stronger security and access to your productivity workloads and their data only by authenticated users and devices.</span></span>

>[!Note]
><span data-ttu-id="24275-105">Si vous avez déjà déployé une infrastructure d’identités, consultez les [critères de sortie d’identité](identity-exit-criteria.md) pour vous assurer que vous répondez aux conditions requises et facultatives pour Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="24275-105">If you’ve already deployed an identity infrastructure, please see the [identity exit criteria](identity-exit-criteria.md) to make sure that you meet the required and optional conditions for Microsoft 365 Enterprise.</span></span>
>

## <a name="plan-and-deploy-your-microsoft-365-enterprise-identity-infrastructure"></a><span data-ttu-id="24275-106">Planifier et déployer votre infrastructure d’identités de Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="24275-106">Plan and deploy your Microsoft 365 Enterprise identity infrastructure</span></span> 

<span data-ttu-id="24275-107">Avant de commencer, regardez cette vidéo pour obtenir une vue d’ensemble des modèles d’identité et de l’authentification pour Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="24275-107">Before you begin, watch this video for an overview of identity models and authentication for Microsoft 365.</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE2Pjwu]

<span data-ttu-id="24275-p101">Procédez comme suit pour planifier et déployer votre nouvelle infrastructure d’identités dans le cloud. Vous pouvez également utiliser ces étapes pour adapter votre infrastructure d’identités locale ou hybride et l’utiliser avec Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="24275-p101">Use the following steps to plan and deploy your new identity infrastructure in the cloud. You can also use these steps to adapt your existing on-premises or hybrid identity infrastructure to work with Microsoft 365 Enterprise.</span></span> 

|||
|:-------|:-----|
|![](./media/stepnumbers/Step1.png)| [<span data-ttu-id="24275-110">Planifier les utilisateurs et les groupes</span><span class="sxs-lookup"><span data-stu-id="24275-110">Plan for users and groups</span></span>](identity-plan-users-groups.md) |
|![](./media/stepnumbers/Step2.png)| [<span data-ttu-id="24275-111">Sécuriser vos identités privilégiées</span><span class="sxs-lookup"><span data-stu-id="24275-111">Secure your privileged identities</span></span>](identity-designate-protect-admin-accounts.md) |
|![](./media/stepnumbers/Step3.png)| [<span data-ttu-id="24275-112">Configurer une identité hybride</span><span class="sxs-lookup"><span data-stu-id="24275-112">Configure hybrid identity</span></span>](identity-azure-ad-connect.md) |
|![](./media/stepnumbers/Step4.png)| [<span data-ttu-id="24275-113">Configurer l’authentification utilisateur sécurisée</span><span class="sxs-lookup"><span data-stu-id="24275-113">Configure secure user authentication</span></span>](identity-multi-factor-authentication.md) |
|![](./media/stepnumbers/Step5.png)| [<span data-ttu-id="24275-114">Simplifier l’accès pour les utilisateurs</span><span class="sxs-lookup"><span data-stu-id="24275-114">Simplify access for users</span></span>](identity-password-reset.md) |
|![](./media/stepnumbers/Step6.png)| [<span data-ttu-id="24275-115">Utiliser des groupes pour faciliter la gestion</span><span class="sxs-lookup"><span data-stu-id="24275-115">Use groups for easier management</span></span>](identity-self-service-group-management.md) |

<span data-ttu-id="24275-116">Lorsque vous avez terminé ces étapes, accédez aux [critères de sortie](identity-exit-criteria.md) de cette phase pour vous assurer que vous répondez aux conditions requises et facultatives pour Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="24275-116">When you've completed these steps, go to the [exit criteria](identity-exit-criteria.md) for this phase to ensure that you meet the required and optional conditions for Microsoft 365 Enterprise.</span></span>

## <a name="identity-and-device-access-recommendations"></a><span data-ttu-id="24275-117">Recommandations en matière d’identité et d’accès aux appareils</span><span class="sxs-lookup"><span data-stu-id="24275-117">Identity and device access recommendations</span></span>

<span data-ttu-id="24275-p102">Microsoft fournit un ensemble de recommandations en matière d’[identité et d’accès aux appareils](microsoft-365-policies-configurations.md) afin de garantir un personnel sécurisé et productif. Pour l’identité, utilisez les recommandations et les paramètres des articles suivants, ainsi que les étapes décrites dans cette phase :</span><span class="sxs-lookup"><span data-stu-id="24275-p102">Microsoft provides a set of recommendations for [identity and device access](microsoft-365-policies-configurations.md) to ensure a secure and productive workforce. For identity, use the recommendations and settings in the following articles along with the steps in this phase:</span></span>

- [<span data-ttu-id="24275-120">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="24275-120">Prerequisites</span></span>](identity-access-prerequisites.md)
- [<span data-ttu-id="24275-121">Stratégies communes pour les identités et l’accès aux appareils</span><span class="sxs-lookup"><span data-stu-id="24275-121">Common identity and device access policies</span></span>](identity-access-policies.md)

## <a name="how-microsoft-does-microsoft-365-enterprise"></a><span data-ttu-id="24275-122">Comment Microsoft gère-t-il Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="24275-122">How Microsoft does Microsoft 365 Enterprise</span></span>

<span data-ttu-id="24275-123">Découvrez comment les experts informatiques de Microsoft ont conçu et déployé les fonctionnalités d’identité de Microsoft 365 Entreprise en consultant les ressources suivantes :</span><span class="sxs-lookup"><span data-stu-id="24275-123">Learn how IT experts at Microsoft planned for and deployed the identity capabilities of Microsoft 365 Enterprise with these resources:</span></span>

- [<span data-ttu-id="24275-124">Gestion des identités d’utilisateur et accès sécurisé à Microsoft</span><span class="sxs-lookup"><span data-stu-id="24275-124">Managing user identities and secure access at Microsoft</span></span>](https://www.microsoft.com/itshowcase/Article/Content/931/Managing-user-identities-and-secure-access-at-Microsoft)
- [<span data-ttu-id="24275-125">Utilisation d’Azure AD Privileged Identity Management pour un accès privilégié</span><span class="sxs-lookup"><span data-stu-id="24275-125">Using Azure AD Privileged Identity Management for elevated access</span></span>](https://www.microsoft.com/itshowcase/Article/Content/887/Using-Azure-AD-Privileged-Identity-Management-for-elevated-access)

## <a name="how-contoso-did-microsoft-365-enterprise"></a><span data-ttu-id="24275-126">Comment Contoso est-elle passée à Microsoft 365 Entreprise ?</span><span class="sxs-lookup"><span data-stu-id="24275-126">How Contoso did Microsoft 365 Enterprise</span></span>

<span data-ttu-id="24275-127">Découvrez comment Contoso Corporation, une entreprise multinationale fictive mais représentative, [a déployé une infrastructure d’identité hybride](contoso-identity.md) pour les services cloud Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="24275-127">See how the Contoso Corporation, a fictional but representative multi-national business, [deployed a hybrid identity infrastructure](contoso-identity.md) for Microsoft 365 cloud services.</span></span>

![](./media/contoso-overview/contoso-icon.png)


## <a name="next-step"></a><span data-ttu-id="24275-128">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="24275-128">Next step</span></span>

|||
|:-------|:-----|
|![](./media/stepnumbers/Step1.png)| [<span data-ttu-id="24275-129">Planifiez les utilisateurs et les groupes</span><span class="sxs-lookup"><span data-stu-id="24275-129">Plan for users and groups</span></span>](identity-plan-users-groups.md) |
