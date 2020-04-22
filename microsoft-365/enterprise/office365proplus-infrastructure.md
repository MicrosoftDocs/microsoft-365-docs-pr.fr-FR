---
title: 'Phase 4 : Microsoft 365 Apps pour entreprise'
f1.keywords:
- NOCSH
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 10/23/2019
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- M365-modern-desktop
- Strat_O365_Enterprise
ms.custom: ''
description: Les étapes du déploiement de l’infrastructure Microsoft 365 Apps pour entreprise pour Microsoft 365 Entreprise.
ms.openlocfilehash: fe29b8025a8ccf5babf2c52cd62ebc72860a8a5c
ms.sourcegitcommit: 2614f8b81b332f8dab461f4f64f3adaa6703e0d6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2020
ms.locfileid: "43631428"
---
# <a name="phase-4-microsoft-365-apps-for-enterprise"></a><span data-ttu-id="4ca93-103">Phase 4 : Microsoft 365 Apps pour entreprise</span><span class="sxs-lookup"><span data-stu-id="4ca93-103">Phase 4: Microsoft 365 Apps for enterprise</span></span>

![Phase 4 : Microsoft 365 Apps pour entreprise](../media/deploy-foundation-infrastructure/O365proplus_icon.png)

<span data-ttu-id="4ca93-105">*Cela s’applique aux versions E3 et E5 de Microsoft 365 Entreprise et Microsoft 365 Éducation*</span><span class="sxs-lookup"><span data-stu-id="4ca93-105">*This applies to both the E3 and E5 versions of Microsoft 365 Enterprise and Microsoft 365 Education*</span></span>

<span data-ttu-id="4ca93-106">Microsoft 365 Entreprise inclut Microsoft 365 Apps pour entreprise, la version d’abonnement de Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="4ca93-106">Microsoft 365 Enterprise includes Microsoft 365 Apps for enterprise, the subscription version of Office.</span></span> <span data-ttu-id="4ca93-107">Comme Office 2019, Microsoft 365 Apps pour entreprise inclut toutes les applications d’Office. Ces applications sont installées directement sur vos appareils clients.</span><span class="sxs-lookup"><span data-stu-id="4ca93-107">Like Office 2019, Microsoft 365 Apps for enterprise includes all the Office applications, and those applications are installed directly on your client devices.</span></span> <span data-ttu-id="4ca93-108">Contrairement à Office 2019, Microsoft 365 Apps pour entreprise est mis à jour régulièrement avec de nouvelles fonctionnalités et offre un modèle de licence basé sur l’utilisateur qui permet aux utilisateurs d’installer Office sur plusieurs appareils.</span><span class="sxs-lookup"><span data-stu-id="4ca93-108">Unlike Office 2019, Microsoft 365 Apps for enterprise is updated with new features on a regular basis and has a user-based licensing model that allows people to install Office on multiple devices.</span></span> <span data-ttu-id="4ca93-109">Pour plus d’informations, consultez la rubrique [À propos de Microsoft 365 Apps pour entreprise dans l’entreprise](https://docs.microsoft.com/deployoffice/about-office-365-proplus-in-the-enterprise).</span><span class="sxs-lookup"><span data-stu-id="4ca93-109">For more details, see [About Microsoft 365 Apps for enterprise in the enterprise](https://docs.microsoft.com/deployoffice/about-office-365-proplus-in-the-enterprise).</span></span>

<span data-ttu-id="4ca93-p102">Dans cette phase, vous déployez Microsoft 365 Apps pour entreprise sur les appareils clients dans le cadre de Microsoft 365 Entreprise. En plus de ces instructions, nous vous recommandons d’utiliser [Microsoft Fastrack](https://fasttrack.microsoft.com/office) pour vous aider à effectuer votre déploiement.</span><span class="sxs-lookup"><span data-stu-id="4ca93-p102">In this phase, you deploy Microsoft 365 Apps for enterprise to client devices as part of Microsoft 365 Enterprise. In addition to this guidance, we recommend you use [Microsoft Fastrack](https://fasttrack.microsoft.com/office) to help with your deployment.</span></span> 

<span data-ttu-id="4ca93-112">Si vous avez déjà déployé Microsoft 365 Apps pour entreprise, consultez les [critères de sortie](office365proplus-exit-criteria.md) de cette phase pour vous assurer que vous répondez aux conditions requises pour Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="4ca93-112">If you already have Microsoft 365 Apps for enterprise deployed, please see the [exit criteria](office365proplus-exit-criteria.md) for this phase to make sure that it meets the required conditions for Microsoft 365 Enterprise.</span></span>

>[!Note]
><span data-ttu-id="4ca93-113">Pour déployer ensemble Windows 10 Entreprise et Microsoft 365 Apps pour entreprise, voir le [Centre de déploiement de bureau](desktop-deployment-center-home.md).</span><span class="sxs-lookup"><span data-stu-id="4ca93-113">To deploy both Windows 10 Enterprise and Microsoft 365 Apps for enterprise together, see the [Desktop Deployment Center](desktop-deployment-center-home.md).</span></span>
>

## <a name="step-1-assess-your-environment"></a><span data-ttu-id="4ca93-114">Étape 1 : évaluer votre environnement</span><span class="sxs-lookup"><span data-stu-id="4ca93-114">Step 1: Assess your environment</span></span>

<span data-ttu-id="4ca93-p103">Avant de déployer Microsoft 365 Apps pour entreprise, suivez les instructions indiquées dans l’article [Évaluation de votre environnement et de sa configuration requise pour déployer Microsoft 365 Apps pour entreprise](https://docs.microsoft.com/DeployOffice/assess-office-365-proplus). Cette évaluation inclut la configuration requise, les informations des appareils de vos clients (par exemple, les architectures et les langues requises), les conditions de licence, la capacité réseau et la compatibilité des applications. L’exécution de l’évaluation vous aidera à prendre des décisions clés dans le cadre de la planification de votre déploiement.</span><span class="sxs-lookup"><span data-stu-id="4ca93-p103">Before deploying Microsoft 365 Apps for enterprise, follow the guidance in [Assess your environment and requirements for deploying Microsoft 365 Apps for enterprise](https://docs.microsoft.com/DeployOffice/assess-office-365-proplus). This assessment includes system requirements, details of your client devices (such as architectures and required languages), licensing requirements, network capability, and application compatibility. Completing the assessment will help you make key decisions as part of planning your deployment.</span></span>

## <a name="step-2-plan-your-deployment"></a><span data-ttu-id="4ca93-118">Étape 2 : planifier votre déploiement</span><span class="sxs-lookup"><span data-stu-id="4ca93-118">Step 2: Plan your deployment</span></span>

<span data-ttu-id="4ca93-p104">Après avoir évalué votre environnement, suivez les instructions indiquées dans l’article [Planification de votre déploiement de Microsoft 365 Apps pour entreprise](https://docs.microsoft.com/DeployOffice/plan-office-365-proplus) pour créer un plan de déploiement. Ce plan implique les décisions suivantes :</span><span class="sxs-lookup"><span data-stu-id="4ca93-p104">After assessing your environment, follow the guidance in [Plan your deployment of Microsoft 365 Apps for enterprise](https://docs.microsoft.com/DeployOffice/plan-office-365-proplus) to create a deployment plan. This plan includes the following decisions:</span></span> 

- <span data-ttu-id="4ca93-121">Déploiement d’Office, notamment quel outil utiliser (par exemple, Microsoft Endpoint Configuration Manager ou l’outil Déploiement d’Office) et où installer Office</span><span class="sxs-lookup"><span data-stu-id="4ca93-121">How to deploy Office, including what tool to use (such as Microsoft Endpoint Configuration Manager or the Office Deployment Tool) and where to install Office from</span></span>
- <span data-ttu-id="4ca93-122">Comment gérer les mises à jour d’Office</span><span class="sxs-lookup"><span data-stu-id="4ca93-122">How to manage updates to Office</span></span>
- <span data-ttu-id="4ca93-123">Les canaux de mise à jour à utiliser (les canaux de mise à jour pour Office contrôlent la fréquence à laquelle vos utilisateurs reçoivent des mises à jour de fonctionnalités pour leurs applications Office)</span><span class="sxs-lookup"><span data-stu-id="4ca93-123">Which update channels to use (update channels for Office control how frequently your users receive feature updates to their Office applications)</span></span>
- <span data-ttu-id="4ca93-124">Les packages d’installation Office et les groupes de déploiement que vous voulez utiliser, y compris les applications Office et les langues qui doivent être installées pour les utilisateurs</span><span class="sxs-lookup"><span data-stu-id="4ca93-124">The Office installation packages and deployment groups you want to use, including which Office applications and languages should be installed for which users</span></span>

<span data-ttu-id="4ca93-125">L’[article de planification](https://docs.microsoft.com/DeployOffice/plan-office-365-proplus) comporte des recommandations pour toutes ces options, y compris la gestion de votre déploiement, la gestion de vos mises à jour, la définition des packages d’installation et la création de groupes de déploiement.</span><span class="sxs-lookup"><span data-stu-id="4ca93-125">The [planning article](https://docs.microsoft.com/DeployOffice/plan-office-365-proplus) includes best practices for all these options, including managing your deployment, managing your updates, defining installation packages, and creating deployment groups.</span></span> 

## <a name="step-3-deploy"></a><span data-ttu-id="4ca93-126">Étape 3 : déployer</span><span class="sxs-lookup"><span data-stu-id="4ca93-126">Step 3: Deploy</span></span>

<span data-ttu-id="4ca93-127">En fonction de votre plan de déploiement, choisissez le mode de déploiement parmi les possibilités suivantes :</span><span class="sxs-lookup"><span data-stu-id="4ca93-127">Based on your deployment plan, choose how you want to deploy:</span></span>

- <span data-ttu-id="4ca93-128">**[Déployer Microsoft 365 Apps pour entreprise avec le Gestionnaire de configuration](https://docs.microsoft.com/deployoffice/deploy-office-365-proplus-with-system-center-configuration-manager) :** gérez votre déploiement avec le Gestionnaire de configuration, puis téléchargez et déployez Office à partir de points de distribution sur votre réseau.</span><span class="sxs-lookup"><span data-stu-id="4ca93-128">**[Deploy Microsoft 365 Apps for enterprise with Configuration Manager](https://docs.microsoft.com/deployoffice/deploy-office-365-proplus-with-system-center-configuration-manager):** Manage your deployment with Configuration Manager, and download and deploy Office from distribution points on your network</span></span>

- <span data-ttu-id="4ca93-129">**[Déployer Microsoft 365 Apps pour entreprise avec l’outil Déploiement d’Office à partir du cloud](https://docs.microsoft.com/deployoffice/deploy-office-365-proplus-from-the-cloud) :** gérez votre déploiement avec l’outil Déploiement d’Office et installez Office directement sur des appareils clients à partir du CDN d’Office</span><span class="sxs-lookup"><span data-stu-id="4ca93-129">**[Deploy Microsoft 365 Apps for enterprise with the ODT from the cloud](https://docs.microsoft.com/deployoffice/deploy-office-365-proplus-from-the-cloud):** Manage your deployment with the ODT, and install Office on client devices directly from the Office CDN</span></span>
 
- <span data-ttu-id="4ca93-130">**[Installer soi-même Microsoft 365 Apps pour entreprise à partir du portail Office](https://docs.microsoft.com/deployoffice/manage-software-download-settings-office-365) :** gérez votre déploiement à partir du portail Office et demandez à vos utilisateurs d’installer Office directement sur leurs appareils clients à partir du portail</span><span class="sxs-lookup"><span data-stu-id="4ca93-130">**[Self-install Microsoft 365 Apps for enterprise from the Office portal](https://docs.microsoft.com/deployoffice/manage-software-download-settings-office-365):** Manage your deployment from the Office portal and have your users install Office on their client devices directly from the portal</span></span>

<span data-ttu-id="4ca93-p105">De nombreuses organisations utilisent une combinaison de ces options pour différents utilisateurs. Par exemple, une organisation peut utiliser Configuration Manager pour déployer Office pour la plupart de ses utilisateurs, mais activer l’installation autonome pour un petit groupe de collaborateurs qui ne sont pas fréquemment connectés au réseau interne.</span><span class="sxs-lookup"><span data-stu-id="4ca93-p105">Many organizations will use a combination of these options for different users. For example, an organization might use Configuration Manager to deploy Office to most of their users, but enable self-install for a small group of workers who are not frequently connected to the internal network.</span></span> 

<span data-ttu-id="4ca93-p106">Si votre organisation utilise Configuration Manager, nous vous recommandons de procéder à la mise à niveau vers la branche actuelle et de procéder à la mise à jour vers la version actuelle. Pour obtenir plus d’informations, consultez l’article [Quelle branche de Configuration Manager dois-je utiliser ?](https://docs.microsoft.com/configmgr/core/understand/which-branch-should-i-use)</span><span class="sxs-lookup"><span data-stu-id="4ca93-p106">If your organization uses Configuration Manager, we recommend upgrading to the Current Branch and updating to the current release. For more details, see [Which branch of Configuration Manager should I use?](https://docs.microsoft.com/configmgr/core/understand/which-branch-should-i-use)</span></span>

## <a name="how-microsoft-does-microsoft-365-enterprise"></a><span data-ttu-id="4ca93-135">Comment Microsoft gère-t-il Microsoft 365 Entreprise</span><span class="sxs-lookup"><span data-stu-id="4ca93-135">How Microsoft does Microsoft 365 Enterprise</span></span>

<span data-ttu-id="4ca93-136">Découvrez comment les experts Microsoft [déploient et gèrent les mises à jour de Microsoft 365 Apps pour entreprise](https://www.microsoft.com/itshowcase/deploying-and-managing-microsoft-365#primaryR7).</span><span class="sxs-lookup"><span data-stu-id="4ca93-136">Learn how the experts at Microsoft are [deploying and managing updates for Microsoft 365 Apps for enterprise](https://www.microsoft.com/itshowcase/deploying-and-managing-microsoft-365#primaryR7).</span></span>

## <a name="how-contoso-did-microsoft-365-enterprise"></a><span data-ttu-id="4ca93-137">Comment Contoso est-elle passée à Microsoft 365 Entreprise ?</span><span class="sxs-lookup"><span data-stu-id="4ca93-137">How Contoso did Microsoft 365 Enterprise</span></span>

<span data-ttu-id="4ca93-138">Découvrez comment Contoso Corporation, une entreprise multinationale fictive mais représentative, [a déployé Microsoft 365 Apps pour entreprise](contoso-o365pp.md).</span><span class="sxs-lookup"><span data-stu-id="4ca93-138">See how the Contoso Corporation, a fictional but representative multi-national business, [deployed Microsoft 365 Apps for enterprise](contoso-o365pp.md).</span></span>

![Société Contoso](../media/contoso-overview/contoso-icon.png)

## <a name="next-step"></a><span data-ttu-id="4ca93-140">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="4ca93-140">Next step</span></span>

[<span data-ttu-id="4ca93-141">Critères de sortie de l’infrastructure Microsoft 365 Apps pour entreprise</span><span class="sxs-lookup"><span data-stu-id="4ca93-141">Microsoft 365 Apps for enterprise infrastructure exit criteria</span></span>](office365proplus-exit-criteria.md)
