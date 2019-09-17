---
title: 'Phase 2 : Identité'
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 09/06/2019
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- M365-identity-device-management
- Strat_O365_Enterprise
ms.custom: ''
description: Les étapes de déploiement de l’infrastructure d’identités pour Microsoft 365 Entreprise.
ms.openlocfilehash: 07f95a249912826b80e0654cac4063b3d5763267
ms.sourcegitcommit: 91ff1d4339f0f043c2b43997d87d84677c79e279
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/14/2019
ms.locfileid: "36981948"
---
# <a name="phase-2-identity"></a><span data-ttu-id="d631d-103">Phase 2 : Identité</span><span class="sxs-lookup"><span data-stu-id="d631d-103">Phase 2: Identity</span></span>

![](./media/deploy-foundation-infrastructure/identity_icon.png)

<span data-ttu-id="d631d-104">Dans Microsoft 365 Entreprise, une infrastructure d’identités bien planifiée et exécutée ouvre la voie à une sécurité plus forte et à un accès à vos charges de travail de productivité et à leurs données uniquement par des utilisateurs et appareils authentifiés.</span><span class="sxs-lookup"><span data-stu-id="d631d-104">In Microsoft 365 Enterprise, a well-planned and executed identity infrastructure paves the way for stronger security and access to your productivity workloads and their data only by authenticated users and devices.</span></span>

<span data-ttu-id="d631d-105">Regardez cette vidéo pour obtenir une vue d’ensemble des modèles d’identité et de l’authentification pour Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="d631d-105">Before you begin, watch this video for an overview of identity models and authentication for Microsoft 365.</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE2Pjwu]

>[!Note]
><span data-ttu-id="d631d-106">Si vous avez déjà déployé une infrastructure d’identités, consultez les [critères de sortie d’identité](identity-exit-criteria.md) pour vous assurer que vous répondez aux conditions requises et facultatives pour Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="d631d-106">If you’ve already deployed an identity infrastructure, please see the [identity exit criteria](identity-exit-criteria.md) to make sure that you meet the required and optional conditions for Microsoft 365 Enterprise.</span></span>
>

<span data-ttu-id="d631d-107">Pour plus d’informations sur les fonctionnalités d’identité de chaque offre Microsoft 365 Entreprise, le rôle Azure Active Directory (Azure AD), les composants locaux et cloud, ainsi que les configurations d’authentification les plus courantes, consultez l’[affiche Infrastructure d’identités](media/identity-infrastructure/M365E-ID-Infra.pdf).</span><span class="sxs-lookup"><span data-stu-id="d631d-107">For the identity features of each Microsoft 365 Enterprise plan, the role of Azure Active Directory (Azure AD), on-premises and cloud-based components, and the most common authentication configurations, see the [Identity Infrastructure poster](media/identity-infrastructure/M365E-ID-Infra.pdf).</span></span>

<span data-ttu-id="d631d-108">[![Affiche Infrastructure d’identités](./media/identity-infrastructure/m365e-identity-arch-poster.png)](media/identity-infrastructure/M365E-ID-Infra.pdf)</span><span class="sxs-lookup"><span data-stu-id="d631d-108">[![The Identity Infrastructure poster](./media/identity-infrastructure/m365e-identity-arch-poster.png)](media/identity-infrastructure/M365E-ID-Infra.pdf)</span></span>

<span data-ttu-id="d631d-109">Cette affiche en double page permet de bien comprendre les concepts et configurations d’identités pour Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="d631d-109">This two-page poster is a quick way to ramp up on identity concepts and configurations for Microsoft 365 Enterprise.</span></span>

<span data-ttu-id="d631d-110">Vous pouvez également [télécharger cette affiche](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/enterprise/media/identity-infrastructure/M365E-ID-Infra.pdf) et l’imprimer au format lettre, légal ou tabloïd (11 x 17).</span><span class="sxs-lookup"><span data-stu-id="d631d-110">You can also [download this poster](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/enterprise/media/identity-infrastructure/M365E-ID-Infra.pdf) and print it in letter, legal, or tabloid (11 x 17) formats.</span></span>

## <a name="plan-and-deploy-your-microsoft-365-enterprise-identity-infrastructure"></a><span data-ttu-id="d631d-111">Planifier et déployer votre infrastructure d’identités de Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="d631d-111">Plan and deploy your Microsoft 365 Enterprise identity infrastructure</span></span> 

<span data-ttu-id="d631d-p101">Procédez comme suit pour planifier et déployer votre nouvelle infrastructure d’identités dans le cloud. Vous pouvez également utiliser ces étapes pour adapter votre infrastructure d’identités locale ou hybride et l’utiliser avec Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="d631d-p101">Use the following steps to plan and deploy your new identity infrastructure in the cloud. You can also use these steps to adapt your existing on-premises or hybrid identity infrastructure to work with Microsoft 365 Enterprise.</span></span> 

|||
|:-------|:-----|
|![](./media/stepnumbers/Step1.png)| [<span data-ttu-id="d631d-114">Planifier les utilisateurs et les groupes</span><span class="sxs-lookup"><span data-stu-id="d631d-114">Plan for users and groups</span></span>](identity-plan-users-groups.md) |
|![](./media/stepnumbers/Step2.png)| [<span data-ttu-id="d631d-115">Sécuriser vos identités privilégiées</span><span class="sxs-lookup"><span data-stu-id="d631d-115">Secure your privileged identities</span></span>](identity-designate-protect-admin-accounts.md) |
|![](./media/stepnumbers/Step3.png)| [<span data-ttu-id="d631d-116">Configurer une identité hybride</span><span class="sxs-lookup"><span data-stu-id="d631d-116">Configure hybrid identity</span></span>](identity-azure-ad-connect.md) |
|![](./media/stepnumbers/Step4.png)| [<span data-ttu-id="d631d-117">Configurer l’authentification utilisateur sécurisée</span><span class="sxs-lookup"><span data-stu-id="d631d-117">Configure secure user authentication</span></span>](identity-multi-factor-authentication.md) |
|![](./media/stepnumbers/Step5.png)| [<span data-ttu-id="d631d-118">Simplifier l’accès pour les utilisateurs</span><span class="sxs-lookup"><span data-stu-id="d631d-118">Simplify access for users</span></span>](identity-password-reset.md) |
|![](./media/stepnumbers/Step6.png)| [<span data-ttu-id="d631d-119">Utiliser des groupes pour faciliter la gestion</span><span class="sxs-lookup"><span data-stu-id="d631d-119">Use groups for easier management</span></span>](identity-self-service-group-management.md) |
|![](./media/stepnumbers/Step7.png)| [<span data-ttu-id="d631d-120">Configurer la gouvernance des identités</span><span class="sxs-lookup"><span data-stu-id="d631d-120">Configure identity governance</span></span>](identity-governance.md) |

<span data-ttu-id="d631d-121">Lorsque vous avez terminé ces étapes, accédez aux [critères de sortie](identity-exit-criteria.md) de cette phase pour vous assurer que vous répondez aux conditions requises et facultatives pour l’identité Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="d631d-121">When you've completed these steps, go to the [exit criteria](identity-exit-criteria.md) for this phase to ensure that you meet the required and optional conditions for Microsoft 365 Enterprise.</span></span>

## <a name="identity-and-device-access-recommendations"></a><span data-ttu-id="d631d-122">Recommandations en matière d’identité et d’accès aux appareils</span><span class="sxs-lookup"><span data-stu-id="d631d-122">Identity and device access recommendations</span></span>

<span data-ttu-id="d631d-p102">Microsoft fournit un ensemble de recommandations en matière d’[identité et d’accès aux appareils](microsoft-365-policies-configurations.md) afin de garantir un personnel sécurisé et productif. Pour l’identité, utilisez les recommandations et les paramètres des articles suivants, ainsi que les étapes décrites dans cette phase :</span><span class="sxs-lookup"><span data-stu-id="d631d-p102">Microsoft provides a set of recommendations for [identity and device access](microsoft-365-policies-configurations.md) to ensure a secure and productive workforce. For identity, use the recommendations and settings in the following articles along with the steps in this phase:</span></span>

- [<span data-ttu-id="d631d-125">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="d631d-125">Prerequisites</span></span>](identity-access-prerequisites.md)
- [<span data-ttu-id="d631d-126">Stratégies communes pour les identités et l’accès aux appareils</span><span class="sxs-lookup"><span data-stu-id="d631d-126">Common identity and device access policies</span></span>](identity-access-policies.md)

## <a name="how-microsoft-does-microsoft-365-enterprise"></a><span data-ttu-id="d631d-127">Comment Microsoft gère-t-il Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="d631d-127">How Microsoft does Microsoft 365 Enterprise</span></span>

<span data-ttu-id="d631d-128">Découvrez comment les experts informatiques de [Microsoft gèrent les identités et la sécurisation des accès](https://www.microsoft.com/fr-FR/itshowcase/deploying-and-managing-microsoft-365#primaryR5).</span><span class="sxs-lookup"><span data-stu-id="d631d-128">Learn how IT experts at Microsoft [manage identities and secure access](https://www.microsoft.com/fr-FR/itshowcase/deploying-and-managing-microsoft-365#primaryR5).</span></span>

## <a name="how-contoso-did-microsoft-365-enterprise"></a><span data-ttu-id="d631d-129">Comment Contoso est-elle passée à Microsoft 365 Entreprise ?</span><span class="sxs-lookup"><span data-stu-id="d631d-129">How Contoso did Microsoft 365 Enterprise</span></span>

<span data-ttu-id="d631d-130">Découvrez comment Contoso Corporation, une entreprise multinationale fictive mais représentative, [a déployé une infrastructure d’identité hybride](contoso-identity.md) pour les services cloud Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="d631d-130">See how the Contoso Corporation, a fictional but representative multi-national business, [deployed a hybrid identity infrastructure](contoso-identity.md) for Microsoft 365 cloud services.</span></span>

![](./media/contoso-overview/contoso-icon.png)


## <a name="next-step"></a><span data-ttu-id="d631d-131">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="d631d-131">Next step</span></span>

|||
|:-------|:-----|
|![](./media/stepnumbers/Step1.png)| [<span data-ttu-id="d631d-132">Planifiez les utilisateurs et les groupes</span><span class="sxs-lookup"><span data-stu-id="d631d-132">Plan for users and groups</span></span>](identity-plan-users-groups.md) |
