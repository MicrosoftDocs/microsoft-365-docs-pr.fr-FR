---
title: Critères de sortie de l’infrastructure de protection des informations
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 04/10/2019
ms.audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- M365-security-compliance
- Strat_O365_Enterprise
ms.custom: ''
description: Examinez les critères de l’infrastructure et des services de protection des informations pour vérifier que votre configuration remplit les conditions requises de Microsoft 365 Entreprise.
ms.openlocfilehash: 681b3bb2500680b4f5d5801486347aec1b801714
ms.sourcegitcommit: 81273a9df49647286235b187fa2213c5ec7e8b62
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283694"
---
# <a name="information-protection-infrastructure-exit-criteria"></a><span data-ttu-id="ec25c-103">Critères de sortie de l’infrastructure de protection des informations</span><span class="sxs-lookup"><span data-stu-id="ec25c-103">Information protection infrastructure exit criteria</span></span>

![](./media/deploy-foundation-infrastructure/infoprotection_icon-small.png)

<span data-ttu-id="ec25c-104">Vérifiez que votre infrastructure de protection des informations répond aux critères obligatoires suivants et que vous avez pris en considération les critères facultatifs.</span><span class="sxs-lookup"><span data-stu-id="ec25c-104">Make sure your information protection infrastructure meets the following required criteria and that you've considered those that are optional.</span></span>

<a name="crit-infoprotect-step1"></a>
## <a name="required-security-and-information-protection-levels-for-your-organization-are-defined"></a><span data-ttu-id="ec25c-105">Obligatoire : définition des niveaux de protection des informations et de sécurité pour votre organisation</span><span class="sxs-lookup"><span data-stu-id="ec25c-105">Required: Security and information protection levels for your organization are defined</span></span>

<span data-ttu-id="ec25c-p101">Vous avez planifié et défini les niveaux de sécurité dont votre organisation a besoin. Ces niveaux définissent un niveau minimal de sécurité et des niveaux supplémentaires pour les informations de plus en plus sensibles et la sécurité requise de leurs données.</span><span class="sxs-lookup"><span data-stu-id="ec25c-p101">You've planned for and determined the security levels that your organization needs. These levels define a minimum level of security and additional levels for increasingly sensitive information and their required data security.</span></span>

<span data-ttu-id="ec25c-108">Vous utilisez au moins trois niveaux de sécurité :</span><span class="sxs-lookup"><span data-stu-id="ec25c-108">At a minimum, you are using three security levels:</span></span>

- <span data-ttu-id="ec25c-109">Baseline</span><span class="sxs-lookup"><span data-stu-id="ec25c-109">Baseline</span></span>
- <span data-ttu-id="ec25c-110">Sensible</span><span class="sxs-lookup"><span data-stu-id="ec25c-110">Sensitive</span></span>
- <span data-ttu-id="ec25c-111">Hautement réglementé</span><span class="sxs-lookup"><span data-stu-id="ec25c-111">Highly regulated</span></span>

<span data-ttu-id="ec25c-112">Si nécessaire, l’[Étape 1](infoprotect-define-sec-infoprotect-levels.md) peut vous aider à répondre à cette exigence.</span><span class="sxs-lookup"><span data-stu-id="ec25c-112">If needed, [Step 1](infoprotect-define-sec-infoprotect-levels.md) can help you meet this requirement.</span></span> 

<a name="crit-infoprotect-step4"></a>
## <a name="required-increased-security-for-microsoft-365-is-configured"></a><span data-ttu-id="ec25c-113">Obligatoire : le paramètre Sécurité accrue de Microsoft 365 est configuré</span><span class="sxs-lookup"><span data-stu-id="ec25c-113">Required: Increased security for Office 365 is configured</span></span>

<span data-ttu-id="ec25c-114">Vous avez configuré les paramètres de [Sécurité accrue d’Office 365](https://docs.microsoft.com/office365/securitycompliance/tenant-wide-setup-for-increased-security) suivants :</span><span class="sxs-lookup"><span data-stu-id="ec25c-114">You've configured the following settings for increased security based on the information in [Configure your Office 365 tenant for increased security](https://docs.microsoft.com/office365/securitycompliance/tenant-wide-setup-for-increased-security):</span></span>

- <span data-ttu-id="ec25c-115">Stratégies de gestion des menaces dans le Centre de sécurité Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="ec25c-115">Threat management policies in the Microsoft 365 security Center</span></span>
- <span data-ttu-id="ec25c-116">Autres paramètres à l’échelle du client Exchange Online</span><span class="sxs-lookup"><span data-stu-id="ec25c-116">Additional Exchange Online tenant-wide settings</span></span>
- <span data-ttu-id="ec25c-117">Stratégies de partage à l’échelle du client dans le Centre d’administration SharePoint</span><span class="sxs-lookup"><span data-stu-id="ec25c-117">Tenant-wide sharing policies in SharePoint admin center</span></span>
- <span data-ttu-id="ec25c-118">Paramètres d’Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="ec25c-118">CORS support in Microsoft Azure Active Directory (Azure AD)</span></span>

<span data-ttu-id="ec25c-119">Vous avez également [activé Office 365 - Protection avancée contre les menaces pour SharePoint, OneDrive et Microsoft Teams](https://docs.microsoft.com/fr-FR/office365/securitycompliance/turn-on-atp-for-spo-odb-and-teams).</span><span class="sxs-lookup"><span data-stu-id="ec25c-119">You've also [enabled Office 365 Advanced Threat Protection (ATP) for SharePoint, OneDrive, and Microsoft Teams](https://docs.microsoft.com/fr-FR/office365/securitycompliance/turn-on-atp-for-spo-odb-and-teams).</span></span>

<span data-ttu-id="ec25c-120">Si nécessaire, l’[Étape 3](infoprotect-configure-increased-security-office-365.md) peut vous aider à répondre à cette exigence.</span><span class="sxs-lookup"><span data-stu-id="ec25c-120">If needed, [Step 3](infoprotect-configure-increased-security-office-365.md) can help you meet this requirement.</span></span> 

<a name="crit-infoprotect-step3"></a>
## <a name="optional-classification-is-configured-across-your-environment"></a><span data-ttu-id="ec25c-121">Facultatif : configurer la classification au sein de votre environnement</span><span class="sxs-lookup"><span data-stu-id="ec25c-121">Optional: Classification is configured across your environment</span></span>

<span data-ttu-id="ec25c-122">Vous avez travaillé avec vos équipes juridiques et de conformité afin de développer une classification et un système d’étiquetage appropriés pour les stratégies de sécurité et de gouvernance des données de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="ec25c-122">You've worked with your legal and compliance teams to develop an appropriate classification and labeling scheme for your organization’s data, which include the following:</span></span> 

<span data-ttu-id="ec25c-123">Ces stratégies correspondent à la configuration et au déploiement de ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="ec25c-123">Those policies correspond to the configuration and deployment of:</span></span>

- <span data-ttu-id="ec25c-124">Types de données sensibles</span><span class="sxs-lookup"><span data-stu-id="ec25c-124">Sensitive data types</span></span>
- <span data-ttu-id="ec25c-125">Étiquettes de rétention</span><span class="sxs-lookup"><span data-stu-id="ec25c-125">Retention labels</span></span>
- <span data-ttu-id="ec25c-126">Étiquettes de niveau de confidentialité</span><span class="sxs-lookup"><span data-stu-id="ec25c-126">Sensitivity labels</span></span>
- <span data-ttu-id="ec25c-127">Étiquettes Azure Information Protection</span><span class="sxs-lookup"><span data-stu-id="ec25c-127">Azure Information Protection labels</span></span>

<span data-ttu-id="ec25c-128">Si nécessaire, l’[Étape 2](infoprotect-configure-classification.md) peut vous aider à répondre à cette exigence.</span><span class="sxs-lookup"><span data-stu-id="ec25c-128">If needed, [Step 2](infoprotect-configure-classification.md) can help you meet this requirement.</span></span> 

<a name="crit-infoprotect-step5"></a>
## <a name="optional-configure-privileged-access-management-in-office-365"></a><span data-ttu-id="ec25c-129">Facultatif : configurer la gestion des accès privilégiés pour Office 365</span><span class="sxs-lookup"><span data-stu-id="ec25c-129">Optional: Configure privileged access management in Office 365</span></span>

<span data-ttu-id="ec25c-130">Vous avez utilisé les informations de la rubrique [Configurer la gestion des accès privilégiés dans Office 365](https://docs.microsoft.com/office365/securitycompliance/privileged-access-management-configuration) pour activer l’accès privilégié et créer une ou plusieurs stratégies d’accès privilégié au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="ec25c-130">You've used the information in the [Configure privileged access management in Office 365](https://docs.microsoft.com/office365/securitycompliance/privileged-access-management-configuration) topic to enable privileged access  and create one or more privileged access policies in your Office 365 organization. You've configured these policies and just-in-time access is enabled for access to sensitive data or access to critical configuration settings.</span></span> <span data-ttu-id="ec25c-131">Vous avez configuré ces stratégies et l’accès juste-à-temps est activé pour l’accès aux données sensibles ou aux paramètres de configuration critiques.</span><span class="sxs-lookup"><span data-stu-id="ec25c-131">You've configured these policies and just-in-time access is enabled for access to sensitive data or access to critical configuration settings.</span></span>

<span data-ttu-id="ec25c-132">Si nécessaire, l’[Étape 4](infoprotect-configure-privileged-access-management.md) peut vous aider à répondre à cette exigence.</span><span class="sxs-lookup"><span data-stu-id="ec25c-132">If needed, [Step 4](infoprotect-configure-privileged-access-management.md) can help you meet this requirement.</span></span> 

## <a name="results-and-next-steps"></a><span data-ttu-id="ec25c-133">Résultats et étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="ec25c-133">Validation and next steps</span></span>

<span data-ttu-id="ec25c-134">Votre infrastructure de protection des informations Microsoft 365 Entreprise utilise des niveaux de sécurité définis, une sécurité renforcée pour Office 365, une classification à l’aide d’étiquettes et de types de données sensibles, ainsi qu’une gestion des accès privilégiés.</span><span class="sxs-lookup"><span data-stu-id="ec25c-134">Your information protection infrastructure for Microsoft 365 Enterprise uses defined security levels, increased security for Office 365, classification using sensitive data types and labels, and privileged access management.</span></span>

<span data-ttu-id="ec25c-135">Si vous suivez le déploiement de bout en bout de Microsoft 365 Entreprise, vous êtes maintenant prêt à tirer parti de l’ensemble des fonctionnalités et de la configuration de votre infrastructure de base pour vos [charges de travail et scénarios](deploy-workloads.md).</span><span class="sxs-lookup"><span data-stu-id="ec25c-135">If you're following the end-to-end deployment of Microsoft 365 Enterprise, you're now ready to have your [workloads and scenarios](deploy-workloads.md) take advantage of all the features and configuration of your foundation infrastructure.</span></span>
