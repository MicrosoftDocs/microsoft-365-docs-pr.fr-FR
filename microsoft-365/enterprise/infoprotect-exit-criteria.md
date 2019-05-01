---
title: Critères de sortie de l’infrastructure de protection des informations
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 04/25/2019
ms.audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- M365-security-compliance
- Strat_O365_Enterprise
ms.custom: ''
description: Examinez les critères de l’infrastructure et des services de protection des informations pour vérifier que votre configuration remplit les conditions requises de Microsoft 365 Entreprise.
ms.openlocfilehash: 9c74a3994a1a404583326f65f1cec579fccbe659
ms.sourcegitcommit: 3b2d3e2b38c4860db977e73dda119a465c669fa4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33400038"
---
# <a name="information-protection-infrastructure-exit-criteria"></a><span data-ttu-id="1a286-103">Critères de sortie de l’infrastructure de protection des informations</span><span class="sxs-lookup"><span data-stu-id="1a286-103">Information protection infrastructure exit criteria</span></span>

![](./media/deploy-foundation-infrastructure/infoprotection_icon-small.png)

<span data-ttu-id="1a286-104">Vérifiez que votre infrastructure de protection des informations répond aux critères obligatoires suivants et que vous avez pris en considération les critères facultatifs.</span><span class="sxs-lookup"><span data-stu-id="1a286-104">Make sure your information protection infrastructure meets the following required criteria and that you've considered those that are optional.</span></span>

<a name="crit-infoprotect-step1"></a>
## <a name="required-security-and-information-protection-levels-for-your-organization-are-defined"></a><span data-ttu-id="1a286-105">Obligatoire : définition des niveaux de protection des informations et de sécurité pour votre organisation</span><span class="sxs-lookup"><span data-stu-id="1a286-105">Required: Security and information protection levels for your organization are defined</span></span>

<span data-ttu-id="1a286-p101">Vous avez planifié et défini les niveaux de sécurité dont votre organisation a besoin. Ces niveaux définissent un niveau minimal de sécurité et des niveaux supplémentaires pour les informations de plus en plus sensibles et la sécurité requise de leurs données.</span><span class="sxs-lookup"><span data-stu-id="1a286-p101">You've planned for and determined the security levels that your organization needs. These levels define a minimum level of security and additional levels for increasingly sensitive information and their required data security.</span></span>

<span data-ttu-id="1a286-108">Vous utilisez au moins trois niveaux de sécurité :</span><span class="sxs-lookup"><span data-stu-id="1a286-108">At a minimum, you are using three security levels:</span></span>

- <span data-ttu-id="1a286-109">Baseline</span><span class="sxs-lookup"><span data-stu-id="1a286-109">Baseline</span></span>
- <span data-ttu-id="1a286-110">Sensible</span><span class="sxs-lookup"><span data-stu-id="1a286-110">Sensitive</span></span>
- <span data-ttu-id="1a286-111">Hautement réglementé</span><span class="sxs-lookup"><span data-stu-id="1a286-111">Highly regulated</span></span>

<span data-ttu-id="1a286-112">Si nécessaire, l’[Étape 1](infoprotect-define-sec-infoprotect-levels.md) peut vous aider à répondre à cette exigence.</span><span class="sxs-lookup"><span data-stu-id="1a286-112">If needed, [Step 1](infoprotect-define-sec-infoprotect-levels.md) can help you meet this requirement.</span></span> 

<a name="crit-infoprotect-step3"></a>
## <a name="required-increased-security-for-microsoft-365-is-configured"></a><span data-ttu-id="1a286-113">Obligatoire : le paramètre Sécurité accrue de Microsoft 365 est configuré</span><span class="sxs-lookup"><span data-stu-id="1a286-113">Required: Increased security for Microsoft 365 is configured</span></span>

<span data-ttu-id="1a286-114">Vous avez configuré les paramètres de [Sécurité accrue d’Office 365](https://docs.microsoft.com/office365/securitycompliance/tenant-wide-setup-for-increased-security) suivants :</span><span class="sxs-lookup"><span data-stu-id="1a286-114">You've configured the following settings for [Office 365 increased security](https://docs.microsoft.com/office365/securitycompliance/tenant-wide-setup-for-increased-security):</span></span>

- <span data-ttu-id="1a286-115">Stratégies de gestion des menaces dans le Centre de sécurité Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="1a286-115">Threat management policies in the Microsoft 365 security Center</span></span>
- <span data-ttu-id="1a286-116">Autres paramètres à l’échelle du client Exchange Online</span><span class="sxs-lookup"><span data-stu-id="1a286-116">Additional Exchange Online tenant-wide settings</span></span>
- <span data-ttu-id="1a286-117">Stratégies de partage à l’échelle du client dans le Centre d’administration SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="1a286-117">Tenant-wide sharing policies in SharePoint admin center</span></span>
- <span data-ttu-id="1a286-118">Paramètres d’Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="1a286-118">Settings in Azure Active Directory (Azure AD)</span></span>

<span data-ttu-id="1a286-119">Vous avez également [activé Office 365 - Protection avancée contre les menaces pour SharePoint, OneDrive et Microsoft Teams](https://docs.microsoft.com/office365/securitycompliance/turn-on-atp-for-spo-odb-and-teams).</span><span class="sxs-lookup"><span data-stu-id="1a286-119">You've also [enabled Office 365 Advanced Threat Protection (ATP) for SharePoint, OneDrive, and Microsoft Teams](https://docs.microsoft.com/office365/securitycompliance/turn-on-atp-for-spo-odb-and-teams).</span></span>

<span data-ttu-id="1a286-120">Si nécessaire, l’[Étape 3](infoprotect-configure-increased-security-office-365.md) peut vous aider à répondre à cette exigence.</span><span class="sxs-lookup"><span data-stu-id="1a286-120">If needed, [Step 3](infoprotect-configure-increased-security-office-365.md) can help you meet this requirement.</span></span> 

<a name="crit-infoprotect-step2"></a>
## <a name="optional-classification-is-configured-across-your-environment"></a><span data-ttu-id="1a286-121">Facultatif : configurer la classification au sein de votre environnement</span><span class="sxs-lookup"><span data-stu-id="1a286-121">Optional: Classification is configured across your environment</span></span>

<span data-ttu-id="1a286-122">Vous avez travaillé avec vos équipes juridiques et de conformité afin de développer une classification et un système d’étiquetage appropriés pour les stratégies de sécurité et de gouvernance des données de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="1a286-122">You've worked with your legal and compliance teams to develop an appropriate classification and labeling scheme for your organization’s data governance and security policies.</span></span> 

<span data-ttu-id="1a286-123">Ces stratégies correspondent à la configuration et au déploiement de ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="1a286-123">Those policies correspond to the configuration and deployment of:</span></span>

- <span data-ttu-id="1a286-124">Types de données sensibles</span><span class="sxs-lookup"><span data-stu-id="1a286-124">Sensitive data types</span></span>
- <span data-ttu-id="1a286-125">Étiquettes de rétention</span><span class="sxs-lookup"><span data-stu-id="1a286-125">Retention labels</span></span>
- <span data-ttu-id="1a286-126">Étiquettes de niveau de confidentialité</span><span class="sxs-lookup"><span data-stu-id="1a286-126">Sensitivity labels</span></span>
- <span data-ttu-id="1a286-127">Étiquettes Azure Information Protection</span><span class="sxs-lookup"><span data-stu-id="1a286-127">Azure Information Protection labels</span></span>

<span data-ttu-id="1a286-128">Si nécessaire, l’[Étape 2](infoprotect-configure-classification.md) peut vous aider à répondre à cette exigence.</span><span class="sxs-lookup"><span data-stu-id="1a286-128">If needed, [Step 2](infoprotect-configure-classification.md) can help you meet this requirement.</span></span> 


<a name="crit-infoprotect-step4"></a>
## <a name="optional-windows-information-protection-is-deployed-across-your-environment"></a><span data-ttu-id="1a286-129">Facultatif : la Protection des informations Windows est déployée dans votre environnement</span><span class="sxs-lookup"><span data-stu-id="1a286-129">Optional: Windows Information Protection is deployed across your environment</span></span>

<span data-ttu-id="1a286-130">Une stratégie Intune est déployée et appliquée sur vos appareils Windows 10 Entreprise inscrits, qui définit les aspects suivants :</span><span class="sxs-lookup"><span data-stu-id="1a286-130">Your enrolled Windows 10 Enterprise devices have an Intune policy deployed and applied that defines:</span></span>

- <span data-ttu-id="1a286-131">Applications à protéger.</span><span class="sxs-lookup"><span data-stu-id="1a286-131">Which apps to protect.</span></span>
- <span data-ttu-id="1a286-132">Niveau de protection.</span><span class="sxs-lookup"><span data-stu-id="1a286-132">The level of protection.</span></span>
- <span data-ttu-id="1a286-133">Étendue de la protection.</span><span class="sxs-lookup"><span data-stu-id="1a286-133">Where the protection extends.</span></span>

<span data-ttu-id="1a286-134">Si nécessaire, l’[Étape 4](infoprotect-deploy-windows-information-protection.md) peut vous aider à respecter cette exigence.</span><span class="sxs-lookup"><span data-stu-id="1a286-134">If needed, [Step 4](infoprotect-deploy-windows-information-protection.md) can help you meet this requirement.</span></span> 

<a name="crit-infoprotect-step5"></a>
## <a name="optional-office-365-data-loss-prevention-dlp-is-deployed"></a><span data-ttu-id="1a286-135">Facultatif : la protection contre la perte de données Office 365 (DLP) est déployée.</span><span class="sxs-lookup"><span data-stu-id="1a286-135">Optional: Office 365 Data Loss Prevention (DLP) is deployed</span></span>

<span data-ttu-id="1a286-136">Vous avez analysé, testé, puis déployé l’ensemble des stratégies DLP (avec des emplacements et des règles assortis de conditions et d’actions) que votre organisation exige pour protéger les données des clients et d’autres types de données privées, ainsi que pour se conformer aux réglementations et exigences sectorielles et régionales.</span><span class="sxs-lookup"><span data-stu-id="1a286-136">You have analyzed, tested, and then rolled out the set of DLP policies—with locations and rules with conditions and actions—that your organization requires to protect customer and other types of private data and to adhere to industry and regional regulations and requirements.</span></span>

<span data-ttu-id="1a286-137">Votre personnel chargé de la conformité et de la sécurité des données utilise le tableau de bord de sécurité et conformité Office 365 pour surveiller les incidents DLP.</span><span class="sxs-lookup"><span data-stu-id="1a286-137">Your data compliance and security staff are using the Office 365 Security & Compliance dashboard to monitor DLP incidents.</span></span>

<span data-ttu-id="1a286-138">Si nécessaire, l’[Étape 5](infoprotect-data-loss-prevention.md) peut vous aider à respecter cette exigence.</span><span class="sxs-lookup"><span data-stu-id="1a286-138">If needed, [Step 3](infoprotect-data-loss-prevention.md) can help you meet this requirement.</span></span> 


<a name="crit-infoprotect-step6"></a>
## <a name="optional-configure-privileged-access-management-in-office-365"></a><span data-ttu-id="1a286-139">Facultatif : configurer la gestion des accès privilégiés pour Office 365</span><span class="sxs-lookup"><span data-stu-id="1a286-139">Optional: Configure privileged access management in Office 365</span></span>

<span data-ttu-id="1a286-140">Vous avez utilisé les informations de la rubrique [Configurer la gestion des accès privilégiés dans Office 365](https://docs.microsoft.com/office365/securitycompliance/privileged-access-management-configuration) pour activer l’accès privilégié et créer une ou plusieurs stratégies d’accès privilégié au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="1a286-140">You've used the information in the [Configure privileged access management in Office 365](https://docs.microsoft.com/office365/securitycompliance/privileged-access-management-configuration) topic to enable privileged access and create one or more privileged access policies in your organization.</span></span> <span data-ttu-id="1a286-141">Vous avez configuré ces stratégies et l’accès juste-à-temps est activé pour l’accès aux données sensibles ou aux paramètres de configuration critiques.</span><span class="sxs-lookup"><span data-stu-id="1a286-141">You've configured these policies and just-in-time access is enabled for access to sensitive data or access to critical configuration settings.</span></span>

<span data-ttu-id="1a286-142">Si nécessaire, l’[Étape 6](infoprotect-configure-privileged-access-management.md) peut vous aider à respecter cette exigence.</span><span class="sxs-lookup"><span data-stu-id="1a286-142">If needed, [Step 4](infoprotect-configure-privileged-access-management.md) can help you meet this requirement.</span></span> 

## <a name="results-and-next-steps"></a><span data-ttu-id="1a286-143">Résultats et étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="1a286-143">Results and next steps</span></span>

<span data-ttu-id="1a286-144">Votre infrastructure de protection des informations pour Microsoft 365 Entreprise utilise des niveaux de sécurité définis, une sécurité renforcée pour Office 365, une classification à l’aide d’étiquettes et de types de données sensibles, la Protection des informations Windows ainsi qu’une gestion des accès privilégiés.</span><span class="sxs-lookup"><span data-stu-id="1a286-144">Your information protection infrastructure for Microsoft 365 Enterprise uses defined security levels, increased security for Office 365, classification using sensitive data types and labels, and privileged access management.</span></span>

<span data-ttu-id="1a286-145">Si vous suivez le déploiement de bout en bout de Microsoft 365 Entreprise, vous êtes maintenant prêt à tirer parti de l’ensemble des fonctionnalités et de la configuration de votre infrastructure de base pour vos [charges de travail et scénarios](deploy-workloads.md).</span><span class="sxs-lookup"><span data-stu-id="1a286-145">If you're following the end-to-end deployment of Microsoft 365 Enterprise, you're now ready to have your [workloads and scenarios](deploy-workloads.md) take advantage of all the features and configuration of your foundation infrastructure.</span></span>
