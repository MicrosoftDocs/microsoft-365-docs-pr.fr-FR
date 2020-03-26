---
title: 'Phase 2 : Identité'
f1.keywords:
- NOCSH
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 09/20/2019
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- M365-identity-device-management
- Strat_O365_Enterprise
ms.custom: ''
description: Les étapes de déploiement de l’infrastructure d’identité pour Microsoft 365 Entreprise.
ms.openlocfilehash: 0189da0814d1d526d9e07ad35dbbabcbfe82a4cd
ms.sourcegitcommit: 6adfcf042e64b21f09f2b8e072e8eba6d3479e31
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2020
ms.locfileid: "42952029"
---
# <a name="phase-2-identity"></a><span data-ttu-id="f9811-103">Phase 2 : Identité</span><span class="sxs-lookup"><span data-stu-id="f9811-103">Phase 2: Identity</span></span>

![Phase 2 : Identité](../media/deploy-foundation-infrastructure/identity_icon.png)

<span data-ttu-id="f9811-105">Dans Microsoft 365 Entreprise, une infrastructure d’identités bien planifiée et exécutée ouvre la voie à une sécurité plus forte et à un accès à vos charges de travail de productivité et à leurs données uniquement par des utilisateurs et appareils authentifiés.</span><span class="sxs-lookup"><span data-stu-id="f9811-105">In Microsoft 365 Enterprise, a well-planned and executed identity infrastructure paves the way for stronger security and access to your productivity workloads and their data only by authenticated users and devices.</span></span>

<span data-ttu-id="f9811-106">Regardez cette vidéo pour obtenir une vue d’ensemble des modèles d’identité et de l’authentification pour Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="f9811-106">Watch this video for an overview of identity models and authentication for Microsoft 365 Enterprise.</span></span>

<span data-ttu-id="f9811-107"><p> </p></span><span class="sxs-lookup"><span data-stu-id="f9811-107"><p> </p></span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE2Pjwu]

>[!Note]
><span data-ttu-id="f9811-108">Si vous avez déjà déployé une infrastructure d’identités, consultez les [critères de sortie d’identité](identity-exit-criteria.md) pour vous assurer que vous répondez aux conditions requises et facultatives pour Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="f9811-108">If you’ve already deployed an identity infrastructure, please see the [identity exit criteria](identity-exit-criteria.md) to make sure that you meet the required and optional conditions for Microsoft 365 Enterprise.</span></span>
>

<span data-ttu-id="f9811-109">Pour plus d’informations sur les fonctionnalités d’identité de chaque offre Microsoft 365 Entreprise, le rôle Azure Active Directory (Azure AD), les composants locaux et cloud, ainsi que les configurations d’authentification les plus courantes, consultez l’[affiche Infrastructure d’identités](../media/identity-infrastructure/M365E-ID-Infra.pdf).</span><span class="sxs-lookup"><span data-stu-id="f9811-109">For the identity features of each Microsoft 365 Enterprise plan, the role of Azure Active Directory (Azure AD), on-premises and cloud-based components, and the most common authentication configurations, see the [Identity Infrastructure poster](../media/identity-infrastructure/M365E-ID-Infra.pdf).</span></span>

<span data-ttu-id="f9811-110">[![Affiche Infrastructure d’identités](../media/identity-infrastructure/m365e-identity-arch-poster.png)](../media/identity-infrastructure/M365E-ID-Infra.pdf)</span><span class="sxs-lookup"><span data-stu-id="f9811-110">[![The Identity Infrastructure poster](../media/identity-infrastructure/m365e-identity-arch-poster.png)](../media/identity-infrastructure/M365E-ID-Infra.pdf)</span></span>

<span data-ttu-id="f9811-111">Cette affiche en double page permet de bien comprendre les concepts et configurations d’identités pour Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="f9811-111">This two-page poster is a quick way to ramp up on identity concepts and configurations for Microsoft 365 Enterprise.</span></span>

<span data-ttu-id="f9811-112">Vous pouvez également [télécharger cette affiche](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/media/identity-infrastructure/M365E-ID-Infra.pdf) et l’imprimer au format lettre, légal ou tabloïd (11 x 17).</span><span class="sxs-lookup"><span data-stu-id="f9811-112">You can also [download this poster](https://github.com/MicrosoftDocs/microsoft-365-docs/raw/public/microsoft-365/media/identity-infrastructure/M365E-ID-Infra.pdf) and print it in letter, legal, or tabloid (11 x 17) formats.</span></span>

## <a name="plan-and-deploy-your-microsoft-365-enterprise-identity-infrastructure"></a><span data-ttu-id="f9811-113">Planifier et déployer votre infrastructure d’identités de Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="f9811-113">Plan and deploy your Microsoft 365 Enterprise identity infrastructure</span></span> 

<span data-ttu-id="f9811-p101">Procédez comme suit pour planifier et déployer votre nouvelle infrastructure d’identités dans le cloud. Vous pouvez également utiliser ces étapes pour adapter votre infrastructure d’identités locale ou hybride et l’utiliser avec Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="f9811-p101">Use the following steps to plan and deploy your new identity infrastructure in the cloud. You can also use these steps to adapt your existing on-premises or hybrid identity infrastructure to work with Microsoft 365 Enterprise.</span></span> 

|||
|:-------|:-----|
|![Étape 1](../media/stepnumbers/Step1.png)| [<span data-ttu-id="f9811-117">Créer et protéger vos comptes d’administrateur général</span><span class="sxs-lookup"><span data-stu-id="f9811-117">Create and protect your global admin accounts</span></span>](identity-create-protect-global-admins.md) |
|![Étape 2](../media/stepnumbers/Step2.png)| [<span data-ttu-id="f9811-119">Sécuriser vos mots de passe</span><span class="sxs-lookup"><span data-stu-id="f9811-119">Secure your passwords</span></span>](identity-secure-your-passwords.md) |
|![Étape 3](../media/stepnumbers/Step3.png)| [<span data-ttu-id="f9811-121">Sécuriser et gérer les connexions de vos utilisateurs</span><span class="sxs-lookup"><span data-stu-id="f9811-121">Secure and manage your user sign-ins</span></span>](identity-secure-user-sign-ins.md) |
|![Étape 4](../media/stepnumbers/Step4.png)| [<span data-ttu-id="f9811-123">Ajouter vos comptes d’utilisateurs</span><span class="sxs-lookup"><span data-stu-id="f9811-123">Add your user accounts</span></span>](identity-add-user-accounts.md) |
|![Étape 5](../media/stepnumbers/Step5.png)| [<span data-ttu-id="f9811-125">Utiliser des groupes pour la gestion</span><span class="sxs-lookup"><span data-stu-id="f9811-125">Use groups for management</span></span>](identity-use-group-management.md) |
|![Étape 6](../media/stepnumbers/Step6.png)| [<span data-ttu-id="f9811-127">Configurer la gouvernance des identités</span><span class="sxs-lookup"><span data-stu-id="f9811-127">Configure identity governance</span></span>](identity-configure-identity-governance.md) |

<span data-ttu-id="f9811-128">Lorsque vous avez terminé ces étapes, accédez aux [critères de sortie](identity-exit-criteria.md) de cette phase pour vous assurer que vous répondez aux conditions requises et facultatives pour l’identité Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="f9811-128">When you've completed these steps, go to the [exit criteria](identity-exit-criteria.md) for this phase to ensure that you meet the required and optional conditions for Microsoft 365 Enterprise identity.</span></span>

## <a name="identity-and-device-access-recommendations"></a><span data-ttu-id="f9811-129">Recommandations en matière d’identité et d’accès aux appareils</span><span class="sxs-lookup"><span data-stu-id="f9811-129">Identity and device access recommendations</span></span>

<span data-ttu-id="f9811-p102">Microsoft fournit un ensemble de recommandations en matière d’[identité et d’accès aux appareils](microsoft-365-policies-configurations.md) afin de garantir un personnel sécurisé et productif. Pour l’identité, utilisez les recommandations et les paramètres des articles suivants, ainsi que les étapes décrites dans cette phase :</span><span class="sxs-lookup"><span data-stu-id="f9811-p102">Microsoft provides a set of recommendations for [identity and device access](microsoft-365-policies-configurations.md) to ensure a secure and productive workforce. For identity, use the recommendations and settings in the following articles along with the steps in this phase:</span></span>

- [<span data-ttu-id="f9811-132">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="f9811-132">Prerequisites</span></span>](identity-access-prerequisites.md)
- [<span data-ttu-id="f9811-133">Stratégies communes pour les identités et l’accès aux appareils</span><span class="sxs-lookup"><span data-stu-id="f9811-133">Common identity and device access policies</span></span>](identity-access-policies.md)

## <a name="how-microsoft-does-microsoft-365-enterprise"></a><span data-ttu-id="f9811-134">Comment Microsoft gère-t-il Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="f9811-134">How Microsoft does Microsoft 365 Enterprise</span></span>

<span data-ttu-id="f9811-135">Découvrez comment les experts informatiques de [Microsoft gèrent les identités et la sécurisation des accès](https://www.microsoft.com/itshowcase/deploying-and-managing-microsoft-365#primaryR5).</span><span class="sxs-lookup"><span data-stu-id="f9811-135">Learn how IT experts at Microsoft [manage identities and secure access](https://www.microsoft.com/itshowcase/deploying-and-managing-microsoft-365#primaryR5).</span></span>

## <a name="how-contoso-did-microsoft-365-enterprise"></a><span data-ttu-id="f9811-136">Comment Contoso est-elle passée à Microsoft 365 Entreprise ?</span><span class="sxs-lookup"><span data-stu-id="f9811-136">How Contoso did Microsoft 365 Enterprise</span></span>

<span data-ttu-id="f9811-137">Découvrez comment Contoso Corporation, une entreprise multinationale fictive mais représentative, [a déployé une infrastructure d’identité hybride](contoso-identity.md) pour les services cloud Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="f9811-137">See how the Contoso Corporation, a fictional but representative multi-national business, [deployed a hybrid identity infrastructure](contoso-identity.md) for Microsoft 365 cloud services.</span></span>

![Société Contoso](../media/contoso-overview/contoso-icon.png)


## <a name="next-step"></a><span data-ttu-id="f9811-139">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="f9811-139">Next step</span></span>

|||
|:-------|:-----|
|![Étape 1](../media/stepnumbers/Step1.png)| [<span data-ttu-id="f9811-141">Créer et protéger vos comptes d’administrateur général</span><span class="sxs-lookup"><span data-stu-id="f9811-141">Create and protect your global admin accounts</span></span>](identity-create-protect-global-admins.md) |
