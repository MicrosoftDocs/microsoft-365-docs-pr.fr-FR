---
title: Critères de sortie de l’infrastructure de protection des informations
f1.keywords:
- NOCSH
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 09/19/2019
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- M365-security-compliance
- Strat_O365_Enterprise
ms.custom: ''
description: Examinez les critères de l’infrastructure et des services de protection des informations pour vérifier que votre configuration remplit les conditions requises de Microsoft 365 Entreprise.
ms.openlocfilehash: 28eff02ea870dcfca7e2e32580ed6a3a9e8a9484
ms.sourcegitcommit: 6c8edbc54b193e964cf93aec48c51cb79231f1d9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2020
ms.locfileid: "42544163"
---
# <a name="information-protection-infrastructure-exit-criteria"></a><span data-ttu-id="50036-103">Critères de sortie de l’infrastructure de protection des informations</span><span class="sxs-lookup"><span data-stu-id="50036-103">Information protection infrastructure exit criteria</span></span>

![Phase 6 : Protection des informations](../media/deploy-foundation-infrastructure/infoprotection_icon-small.png)

<span data-ttu-id="50036-105">Vérifiez que votre infrastructure de protection des informations répond aux critères obligatoires suivants et que vous avez pris en considération les critères facultatifs.</span><span class="sxs-lookup"><span data-stu-id="50036-105">Make sure your information protection infrastructure meets the following required criteria and that you've considered those that are optional.</span></span>

<a name="crit-infoprotect-step1"></a>
## <a name="required-security-and-information-protection-levels-for-your-organization-are-defined"></a><span data-ttu-id="50036-106">Obligatoire : définition des niveaux de protection des informations et de sécurité pour votre organisation</span><span class="sxs-lookup"><span data-stu-id="50036-106">Required: Security and information protection levels for your organization are defined</span></span>

<span data-ttu-id="50036-p101">Vous avez planifié et défini les niveaux de sécurité dont votre organisation a besoin. Ces niveaux définissent un niveau minimal de sécurité et des niveaux supplémentaires pour les informations de plus en plus sensibles et la sécurité requise de leurs données.</span><span class="sxs-lookup"><span data-stu-id="50036-p101">You've planned for and determined the security levels that your organization needs. These levels define a minimum level of security and additional levels for increasingly sensitive information and their required data security.</span></span>

<span data-ttu-id="50036-109">Vous utilisez au moins trois niveaux de sécurité :</span><span class="sxs-lookup"><span data-stu-id="50036-109">At a minimum, you are using three security levels:</span></span>

- <span data-ttu-id="50036-110">Baseline</span><span class="sxs-lookup"><span data-stu-id="50036-110">Baseline</span></span>
- <span data-ttu-id="50036-111">Sensible</span><span class="sxs-lookup"><span data-stu-id="50036-111">Sensitive</span></span>
- <span data-ttu-id="50036-112">Hautement réglementé</span><span class="sxs-lookup"><span data-stu-id="50036-112">Highly regulated</span></span>

<span data-ttu-id="50036-113">Si nécessaire, l’[Étape 1](infoprotect-define-sec-infoprotect-levels.md) peut vous aider à répondre à cette exigence.</span><span class="sxs-lookup"><span data-stu-id="50036-113">If needed, [Step 1](infoprotect-define-sec-infoprotect-levels.md) can help you meet this requirement.</span></span> 

<a name="crit-infoprotect-step3"></a>
## <a name="required-increased-security-for-microsoft-365-is-configured"></a><span data-ttu-id="50036-114">Obligatoire : le paramètre Sécurité accrue de Microsoft 365 est configuré</span><span class="sxs-lookup"><span data-stu-id="50036-114">Required: Increased security for Microsoft 365 is configured</span></span>

<span data-ttu-id="50036-115">Vous avez configuré les paramètres de [Sécurité accrue d’Office 365](https://docs.microsoft.com/office365/securitycompliance/tenant-wide-setup-for-increased-security) suivants :</span><span class="sxs-lookup"><span data-stu-id="50036-115">You've configured the following settings for [Office 365 increased security](https://docs.microsoft.com/office365/securitycompliance/tenant-wide-setup-for-increased-security):</span></span>

- <span data-ttu-id="50036-116">Stratégies de gestion des menaces dans le Centre de sécurité Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="50036-116">Threat management policies in the Microsoft 365 security Center</span></span>
- <span data-ttu-id="50036-117">Autres paramètres à l’échelle du client Exchange Online</span><span class="sxs-lookup"><span data-stu-id="50036-117">Additional Exchange Online tenant-wide settings</span></span>
- <span data-ttu-id="50036-118">Stratégies de partage à l’échelle du client dans le Centre d’administration SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="50036-118">Tenant-wide sharing policies in SharePoint Online admin center</span></span>
- <span data-ttu-id="50036-119">Paramètres d’Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="50036-119">Settings in Azure Active Directory (Azure AD)</span></span>

<span data-ttu-id="50036-120">Vous avez également [activé Office 365 - Protection avancée contre les menaces pour SharePoint, OneDrive et Microsoft Teams](https://docs.microsoft.com/office365/securitycompliance/turn-on-atp-for-spo-odb-and-teams).</span><span class="sxs-lookup"><span data-stu-id="50036-120">You've also [enabled Office 365 Advanced Threat Protection (ATP) for SharePoint, OneDrive, and Microsoft Teams](https://docs.microsoft.com/office365/securitycompliance/turn-on-atp-for-spo-odb-and-teams).</span></span>

<span data-ttu-id="50036-121">Si nécessaire, l’[Étape 3](infoprotect-configure-increased-security-office-365.md) peut vous aider à répondre à cette exigence.</span><span class="sxs-lookup"><span data-stu-id="50036-121">If needed, [Step 3](infoprotect-configure-increased-security-office-365.md) can help you meet this requirement.</span></span> 

<a name="crit-infoprotect-step2"></a>
## <a name="optional-classification-is-configured-across-your-environment"></a><span data-ttu-id="50036-122">Facultatif : configurer la classification au sein de votre environnement</span><span class="sxs-lookup"><span data-stu-id="50036-122">Optional: Classification is configured across your environment</span></span>

<span data-ttu-id="50036-123">Vous avez travaillé avec vos équipes juridiques et de conformité afin de développer une classification et un système d’étiquetage appropriés pour les stratégies de sécurité et de gouvernance des données de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="50036-123">You've worked with your legal and compliance teams to develop an appropriate classification and labeling scheme for your organization’s data governance and security policies.</span></span> 

<span data-ttu-id="50036-124">Ces stratégies correspondent à la configuration et au déploiement de ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="50036-124">Those policies correspond to the configuration and deployment of:</span></span>

- <span data-ttu-id="50036-125">Types de données sensibles</span><span class="sxs-lookup"><span data-stu-id="50036-125">Sensitive data types</span></span>
- <span data-ttu-id="50036-126">Étiquettes de rétention</span><span class="sxs-lookup"><span data-stu-id="50036-126">Retention labels</span></span>
- <span data-ttu-id="50036-127">Étiquettes de niveau de confidentialité</span><span class="sxs-lookup"><span data-stu-id="50036-127">Sensitivity labels</span></span>
- <span data-ttu-id="50036-128">Étiquettes Azure Information Protection</span><span class="sxs-lookup"><span data-stu-id="50036-128">Azure Information Protection labels</span></span>

<span data-ttu-id="50036-129">Si nécessaire, l’[Étape 2](infoprotect-configure-classification.md) peut vous aider à répondre à cette exigence.</span><span class="sxs-lookup"><span data-stu-id="50036-129">If needed, [Step 2](infoprotect-configure-classification.md) can help you meet this requirement.</span></span> 


<a name="crit-infoprotect-step4"></a>
## <a name="optional-windows-information-protection-is-deployed-across-your-environment"></a><span data-ttu-id="50036-130">Facultatif : la Protection des informations Windows est déployée dans votre environnement</span><span class="sxs-lookup"><span data-stu-id="50036-130">Optional: Windows Information Protection is deployed across your environment</span></span>

<span data-ttu-id="50036-131">Une stratégie Intune est déployée et appliquée sur vos appareils Windows 10 Entreprise inscrits, qui définit les aspects suivants :</span><span class="sxs-lookup"><span data-stu-id="50036-131">Your enrolled Windows 10 Enterprise devices have an Intune policy deployed and applied that defines:</span></span>

- <span data-ttu-id="50036-132">Applications à protéger.</span><span class="sxs-lookup"><span data-stu-id="50036-132">Which apps to protect.</span></span>
- <span data-ttu-id="50036-133">Niveau de protection.</span><span class="sxs-lookup"><span data-stu-id="50036-133">The level of protection.</span></span>
- <span data-ttu-id="50036-134">Étendue de la protection.</span><span class="sxs-lookup"><span data-stu-id="50036-134">Where the protection extends.</span></span>

<span data-ttu-id="50036-135">Si nécessaire, l’[Étape 4](infoprotect-deploy-windows-information-protection.md) peut vous aider à respecter cette exigence.</span><span class="sxs-lookup"><span data-stu-id="50036-135">If needed, [Step 4](infoprotect-deploy-windows-information-protection.md) can help you meet this requirement.</span></span> 

<a name="crit-infoprotect-step5"></a>
## <a name="optional-office-365-data-loss-prevention-dlp-is-deployed"></a><span data-ttu-id="50036-136">Facultatif : la protection contre la perte de données Office 365 (DLP) est déployée.</span><span class="sxs-lookup"><span data-stu-id="50036-136">Optional: Office 365 Data Loss Prevention (DLP) is deployed</span></span>

<span data-ttu-id="50036-137">Vous avez analysé, testé, puis déployé l’ensemble des stratégies DLP (avec des emplacements et des règles assortis de conditions et d’actions) que votre organisation exige pour protéger les données des clients et d’autres types de données privées, ainsi que pour se conformer aux réglementations et exigences sectorielles et régionales.</span><span class="sxs-lookup"><span data-stu-id="50036-137">You have analyzed, tested, and then rolled out the set of DLP policies—with locations and rules with conditions and actions—that your organization requires to protect customer and other types of private data and to adhere to industry and regional regulations and requirements.</span></span>

<span data-ttu-id="50036-138">Votre personnel chargé de la conformité et de la sécurité des données utilise le tableau de bord de sécurité et conformité Office 365 pour surveiller les incidents DLP.</span><span class="sxs-lookup"><span data-stu-id="50036-138">Your data compliance and security staff are using the Office 365 Security & Compliance dashboard to monitor DLP incidents.</span></span>

<span data-ttu-id="50036-139">Si nécessaire, l’[Étape 5](infoprotect-data-loss-prevention.md) peut vous aider à respecter cette exigence.</span><span class="sxs-lookup"><span data-stu-id="50036-139">If needed, [Step 5](infoprotect-data-loss-prevention.md) can help you meet this requirement.</span></span> 

<a name="crit-infoprotect-step6"></a>
## <a name="optional-email-encryption-is-configured"></a><span data-ttu-id="50036-140">Facultatif : le chiffrement d’e-mail est configuré</span><span class="sxs-lookup"><span data-stu-id="50036-140">Optional: Email encryption is configured</span></span>

<span data-ttu-id="50036-141">Vous avez configuré le chiffrement d’e-mail suivant en fonction des besoins de votre organisation :</span><span class="sxs-lookup"><span data-stu-id="50036-141">You've configured the following email encryption as needed for your organization:</span></span>

|||
|:-------|:-----|
| <span data-ttu-id="50036-142">**Méthode de chiffrement**</span><span class="sxs-lookup"><span data-stu-id="50036-142">**Encryption method**</span></span> | <span data-ttu-id="50036-143">**Pour les e-mails envoyés**</span><span class="sxs-lookup"><span data-stu-id="50036-143">**For email sent**</span></span> |
| [<span data-ttu-id="50036-144">Chiffrement de messages Office 365 (OME)</span><span class="sxs-lookup"><span data-stu-id="50036-144">Office 365 Message Encryption (OME)</span></span>](https://docs.microsoft.com/Office365/SecurityCompliance/ome)  | <span data-ttu-id="50036-145">Hors de votre organisation avec chiffrement</span><span class="sxs-lookup"><span data-stu-id="50036-145">Outside your organization with encryption</span></span> |
| [<span data-ttu-id="50036-146">Gestion des droits relatifs à l’information (IRM)</span><span class="sxs-lookup"><span data-stu-id="50036-146">Information Rights Management (IRM)</span></span>](https://docs.microsoft.com/office365/SecurityCompliance/information-rights-management-in-exchange-online) | <span data-ttu-id="50036-147">Avec autorisations et chiffrement</span><span class="sxs-lookup"><span data-stu-id="50036-147">With both encryption and permissions</span></span> |
| [<span data-ttu-id="50036-148">S/MIME (Secure/Multipurpose Internet Mail Extension)</span><span class="sxs-lookup"><span data-stu-id="50036-148">Secure/Multipurpose Internet Mail Extensions (S/MIME)</span></span>](https://docs.microsoft.com/Exchange/policy-and-compliance/smime) | <span data-ttu-id="50036-149">Avec chiffrement et signatures numériques à l’aide du chiffrement à clé publique</span><span class="sxs-lookup"><span data-stu-id="50036-149">With both encryption and digital signatures using public key cryptography</span></span> |
|||

<span data-ttu-id="50036-150">Si nécessaire, l’[étape 6](infoprotect-email-encryption.md) peut vous aider à respecter cette exigence.</span><span class="sxs-lookup"><span data-stu-id="50036-150">If needed, [Step 6](infoprotect-email-encryption.md) can help you meet this requirement.</span></span>

<a name="crit-infoprotect-step7"></a>
## <a name="optional-configure-privileged-access-management-in-office-365"></a><span data-ttu-id="50036-151">Facultatif : configurer la gestion des accès privilégiés pour Office 365</span><span class="sxs-lookup"><span data-stu-id="50036-151">Optional: Configure privileged access management in Office 365</span></span>

<span data-ttu-id="50036-152">Vous avez utilisé les informations de la rubrique [Configurer la gestion des accès privilégiés dans Office 365](https://docs.microsoft.com/office365/securitycompliance/privileged-access-management-configuration) pour activer l’accès privilégié et créer une ou plusieurs stratégies d’accès privilégié au sein de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="50036-152">You've used the information in the [Configure privileged access management in Office 365](https://docs.microsoft.com/office365/securitycompliance/privileged-access-management-configuration) topic to enable privileged access and create one or more privileged access policies in your organization.</span></span> <span data-ttu-id="50036-153">Vous avez configuré ces stratégies et l’accès juste-à-temps est activé pour l’accès aux données sensibles ou aux paramètres de configuration critiques.</span><span class="sxs-lookup"><span data-stu-id="50036-153">You've configured these policies and just-in-time access is enabled for access to sensitive data or access to critical configuration settings.</span></span>

<span data-ttu-id="50036-154">Si nécessaire, l’[Étape 7](infoprotect-configure-privileged-access-management.md) peut vous aider à respecter cette exigence.</span><span class="sxs-lookup"><span data-stu-id="50036-154">If needed, [Step 7](infoprotect-configure-privileged-access-management.md) can help you meet this requirement.</span></span> 

## <a name="results-and-next-steps"></a><span data-ttu-id="50036-155">Résultats et étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="50036-155">Results and next steps</span></span>

<span data-ttu-id="50036-156">Votre infrastructure de protection des informations pour Microsoft 365 Entreprise utilise des niveaux de sécurité définis, une sécurité renforcée pour Office 365, une classification à l’aide d’étiquettes et de types de données sensibles, la Protection des informations Windows, la protection contre la perte de données, le chiffrement de courrier ainsi qu’une gestion des accès privilégiés.</span><span class="sxs-lookup"><span data-stu-id="50036-156">Your information protection infrastructure for Microsoft 365 Enterprise uses defined security levels, increased security for Office 365, classification using sensitive data types and labels, Windows Information Protection, Data Loss Prevention, email encryption, and privileged access management.</span></span>

<span data-ttu-id="50036-157">Si vous suivez le déploiement de bout en bout de Microsoft 365 Entreprise, vous êtes maintenant prêt à tirer parti de l’ensemble des fonctionnalités et de la configuration de votre infrastructure de base pour vos [charges de travail et scénarios](deploy-workloads.md).</span><span class="sxs-lookup"><span data-stu-id="50036-157">If you're following the end-to-end deployment of Microsoft 365 Enterprise, you're now ready to have your [workloads and scenarios](deploy-workloads.md) take advantage of all the features and configuration of your foundation infrastructure.</span></span>
