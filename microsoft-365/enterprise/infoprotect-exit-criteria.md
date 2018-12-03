---
title: Critères de sortie de l’infrastructure de protection des informations
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
description: Examinez les critères de l’infrastructure et des services de protection des informations pour vérifier que votre configuration remplit les conditions requises de Microsoft 365 Entreprise.
ms.openlocfilehash: 10d7b3b888999b65e5faff81e9a2d32e595294cf
ms.sourcegitcommit: eb1a77e4cc4e8f564a1c78d2ef53d7245fe4517a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/28/2018
ms.locfileid: "26867367"
---
# <a name="information-protection-infrastructure-exit-criteria"></a><span data-ttu-id="164ec-103">Critères de sortie de l’infrastructure de protection des informations</span><span class="sxs-lookup"><span data-stu-id="164ec-103">Information protection infrastructure exit criteria</span></span>

![](./media/deploy-foundation-infrastructure/infoprotection_icon-small.png)

<span data-ttu-id="164ec-104">Avant de terminer votre infrastructure de base, assurez-vous que votre infrastructure de protection des informations remplit les conditions suivantes.</span><span class="sxs-lookup"><span data-stu-id="164ec-104">Before you are complete with your foundation infrastructure, make sure that your information protection infrastructure meets these conditions.</span></span> 

<a name="crit-infoprotect-step1"></a>
## <a name="required-security-and-information-protection-levels-for-your-organization-are-defined"></a><span data-ttu-id="164ec-105">Obligatoire : définition des niveaux de protection des informations et de sécurité pour votre organisation</span><span class="sxs-lookup"><span data-stu-id="164ec-105">Required: Security and information protection levels for your organization are defined</span></span>

<span data-ttu-id="164ec-p101">Vous avez planifié et défini les niveaux de sécurité dont votre organisation a besoin. Ces niveaux définissent un niveau minimal de sécurité et des niveaux supplémentaires pour les informations de plus en plus sensibles et la sécurité requise de leurs données.</span><span class="sxs-lookup"><span data-stu-id="164ec-p101">You've planned for and determined the security levels that your organization needs. These levels define a minimum level of security and additional levels for increasingly sensitive information and their required data security.</span></span>

<span data-ttu-id="164ec-108">Vous utilisez au moins trois niveaux de sécurité :</span><span class="sxs-lookup"><span data-stu-id="164ec-108">At a minimum, you are using three security levels:</span></span>

- <span data-ttu-id="164ec-109">Baseline</span><span class="sxs-lookup"><span data-stu-id="164ec-109">Baseline</span></span>
- <span data-ttu-id="164ec-110">Sensible</span><span class="sxs-lookup"><span data-stu-id="164ec-110">Sensitive</span></span>
- <span data-ttu-id="164ec-111">Hautement réglementé</span><span class="sxs-lookup"><span data-stu-id="164ec-111">Highly regulated</span></span>

<span data-ttu-id="164ec-112">Si nécessaire, l’[Étape 1](infoprotect-define-sec-infoprotect-levels.md) peut vous aider à répondre à cette exigence.</span><span class="sxs-lookup"><span data-stu-id="164ec-112">If needed, [Step 1](infoprotect-define-sec-infoprotect-levels.md) can help you meet this requirement.</span></span> 

<a name="crit-infoprotect-step4"></a>
## <a name="required-increased-security-for-office-365-is-configured"></a><span data-ttu-id="164ec-113">Obligatoire : renforcer la sécurité d’Office 365</span><span class="sxs-lookup"><span data-stu-id="164ec-113">Required: Increased security for Office 365 is configured</span></span>

<span data-ttu-id="164ec-114">Vous avez configuré les paramètres suivants afin de renforcer la sécurité en fonction des informations figurant dans l’article [Configurer votre client Office 365 pour renforcer la sécurité](https://support.office.com/article/Configure-your-Office-365-tenant-for-increased-security-8d274fe3-db51-4107-ba64-865e7155b355) :</span><span class="sxs-lookup"><span data-stu-id="164ec-114">You've configured the following settings for increased security based on the information in [Configure your Office 365 tenant for increased security](https://support.office.com/article/Configure-your-Office-365-tenant-for-increased-security-8d274fe3-db51-4107-ba64-865e7155b355):</span></span>

- <span data-ttu-id="164ec-115">Stratégies de gestion des menaces dans le Centre de sécurité et conformité Office 365</span><span class="sxs-lookup"><span data-stu-id="164ec-115">Threat management policies in the Office 365 Security & Compliance Center</span></span>
- <span data-ttu-id="164ec-116">Autres paramètres à l’échelle du client Exchange Online</span><span class="sxs-lookup"><span data-stu-id="164ec-116">Additional Exchange Online tenant-wide settings</span></span>
- <span data-ttu-id="164ec-117">Stratégies de partage à l’échelle du client dans le Centre d’administration SharePoint</span><span class="sxs-lookup"><span data-stu-id="164ec-117">Tenant-wide sharing policies in SharePoint admin center</span></span>
- <span data-ttu-id="164ec-118">Paramètres dans Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="164ec-118">Settings in Azure Active Directory</span></span>

<span data-ttu-id="164ec-119">Vous avez également [activé Office 365 – Protection avancée contre les menaces (ATP)](https://support.office.com/article/Office-365-ATP-for-SharePoint-OneDrive-and-Microsoft-Teams-26261670-db33-4c53-b125-af0662c34607#turniton).</span><span class="sxs-lookup"><span data-stu-id="164ec-119">You've also [enabled Office 365 Advanced Threat Protection (ATP)](https://support.office.com/article/Office-365-ATP-for-SharePoint-OneDrive-and-Microsoft-Teams-26261670-db33-4c53-b125-af0662c34607#turniton).</span></span>

<span data-ttu-id="164ec-120">Si nécessaire, l’[Étape 3](infoprotect-configure-increased-security-office-365.md) peut vous aider à répondre à cette exigence.</span><span class="sxs-lookup"><span data-stu-id="164ec-120">If needed, [Step 3](infoprotect-configure-increased-security-office-365.md) can help you meet this requirement.</span></span> 

<a name="crit-infoprotect-step3"></a>
## <a name="optional-classification-is-configured-across-your-environment"></a><span data-ttu-id="164ec-121">Facultatif : configurer la classification au sein de votre environnement</span><span class="sxs-lookup"><span data-stu-id="164ec-121">Optional: Classification is configured across your environment</span></span>

<span data-ttu-id="164ec-122">Vous avez travaillé avec vos équipes juridiques et de conformité afin de développer une classification et un système d’étiquetage appropriés pour les données de votre organisation, comme suit :</span><span class="sxs-lookup"><span data-stu-id="164ec-122">You've worked with your legal and compliance teams to develop an appropriate classification and labeling scheme for your organization’s data, which include the following:</span></span>

- <span data-ttu-id="164ec-123">Types de données sensibles</span><span class="sxs-lookup"><span data-stu-id="164ec-123">Sensitive data types</span></span>
- <span data-ttu-id="164ec-124">Étiquettes Office 365</span><span class="sxs-lookup"><span data-stu-id="164ec-124">Office 365 labels</span></span>
- <span data-ttu-id="164ec-125">Étiquettes Azure Information Protection</span><span class="sxs-lookup"><span data-stu-id="164ec-125">Azure Information Protection labels</span></span>

<span data-ttu-id="164ec-126">Si nécessaire, l’[Étape 2](infoprotect-configure-classification.md) peut vous aider à répondre à cette exigence.</span><span class="sxs-lookup"><span data-stu-id="164ec-126">If needed, [Step 2](infoprotect-configure-classification.md) can help you meet this requirement.</span></span> 

<a name="crit-infoprotect-step5"></a>
## <a name="optional-configure-privileged-access-management-in-office-365"></a><span data-ttu-id="164ec-127">Facultatif : configurer la gestion des accès privilégiés pour Office 365</span><span class="sxs-lookup"><span data-stu-id="164ec-127">Optional: Configure privileged access management in Office 365</span></span>

<span data-ttu-id="164ec-p102">Vous avez utilisé les informations contenues dans la rubrique [Configurer la gestion des accès privilégié dans Office 365](https://docs.microsoft.com/office365/securitycompliance/privileged-access-management-configuration) pour activer l’accès privilégié et créer une ou plusieurs stratégies d’accès privilégiés dans votre organisation Office 365. Ces stratégies sont configurés, et l’accès juste-à-temps est activé pour l’accès aux paramètres de configuration critiques et aux données sensibles.</span><span class="sxs-lookup"><span data-stu-id="164ec-p102">You've used the information in the [Configure privileged access management in Office 365](https://docs.microsoft.com/office365/securitycompliance/privileged-access-management-configuration) topic to enable privileged access  and create one or more privileged access policies in your Office 365 organization. You've configured these policies and just-in-time access is enabled for access to sensitive data or access to critical configuration settings.</span></span>

<span data-ttu-id="164ec-130">Si nécessaire, l’[Étape 4](infoprotect-configure-privileged-access-management.md) peut vous aider à répondre à cette exigence.</span><span class="sxs-lookup"><span data-stu-id="164ec-130">If needed, [Step 4](infoprotect-configure-privileged-access-management.md) can help you meet this requirement.</span></span> 

## <a name="next-step"></a><span data-ttu-id="164ec-131">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="164ec-131">Next Step</span></span>

<span data-ttu-id="164ec-132">Vous êtes maintenant prêt à déployer des [charges de travail et scénarios](deploy-workloads.md), tels que Microsoft Teams et Exchange Online, qui s’exécutent sur votre infrastructure de base Microsoft 365 Entreprise.</span><span class="sxs-lookup"><span data-stu-id="164ec-132">You're now ready to deploy [workloads and scenarios](deploy-workloads.md), such as Microsoft Teams and Exchange Online, that run on top of your Microsoft 365 Enterprise foundation infrastructure.</span></span>
