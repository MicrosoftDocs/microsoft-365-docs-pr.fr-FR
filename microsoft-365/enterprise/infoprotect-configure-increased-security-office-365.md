---
title: 'Étape 3 : renforcer la sécurité de Microsoft 365'
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
description: Comprendre et renforcer la sécurité de Microsoft 365.
ms.openlocfilehash: eabf0d60f3cfb61b7fffcc688a080ba99f83293e
ms.sourcegitcommit: 3dd9944a6070a7f35c4bc2b57df397f844c3fe79
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2020
ms.locfileid: "42067241"
---
# <a name="step-3-configure-increased-security-for-microsoft-365"></a><span data-ttu-id="3a5b8-103">Étape 3 : renforcer la sécurité de Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="3a5b8-103">Step 3: Configure increased security for Microsoft 365</span></span>

<span data-ttu-id="3a5b8-104">*Cette étape est requise et s’applique aux versions E3 et E5 de Microsoft 365 Entreprise*</span><span class="sxs-lookup"><span data-stu-id="3a5b8-104">*This step is required and applies to both the E3 and E5 versions of Microsoft 365 Enterprise*</span></span>

![Phase 6 : Protection des informations](../media/deploy-foundation-infrastructure/infoprotection_icon-small.png)

<span data-ttu-id="3a5b8-106">Pour vous assurer que votre abonnement Microsoft 365 et ses données démarrent et restent protégés contre des menaces malveillantes, configurez les aspects suivants :</span><span class="sxs-lookup"><span data-stu-id="3a5b8-106">To ensure that your Microsoft 365 subscription and its data start off and remain secure from malicious threats, configure the following:</span></span>

- [<span data-ttu-id="3a5b8-107">Réglage des stratégies de gestion des menaces</span><span class="sxs-lookup"><span data-stu-id="3a5b8-107">Tune threat management policies</span></span>](https://docs.microsoft.com/office365/securitycompliance/tenant-wide-setup-for-increased-security#tune-threat-management-policies-in-the-microsoft-365-security-center)
- [<span data-ttu-id="3a5b8-108">Autres paramètres à l’échelle du client Exchange Online</span><span class="sxs-lookup"><span data-stu-id="3a5b8-108">Additional Exchange Online tenant-wide settings</span></span>](https://docs.microsoft.com/office365/securitycompliance/tenant-wide-setup-for-increased-security#configure-additional-exchange-online-tenant-wide-settings)
- [<span data-ttu-id="3a5b8-109">Stratégies de partage à l’échelle du client dans le Centre d’administration SharePoint</span><span class="sxs-lookup"><span data-stu-id="3a5b8-109">Tenant-wide sharing policies in the SharePoint admin center</span></span>](https://docs.microsoft.com/office365/securitycompliance/tenant-wide-setup-for-increased-security#configure-tenant-wide-sharing-policies-in-sharepoint-admin-center)
- [<span data-ttu-id="3a5b8-110">Paramètres dans Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="3a5b8-110">Settings in Azure Active Directory (Azure AD)</span></span>](https://docs.microsoft.com/office365/securitycompliance/tenant-wide-setup-for-increased-security#configure-settings-in-azure-active-directory)

<span data-ttu-id="3a5b8-111">Une fois la configuration terminée, vous pouvez obtenir des informations concernant votre statut de sécurité à partir de :</span><span class="sxs-lookup"><span data-stu-id="3a5b8-111">Once configured, you can obtain information about your security status from:</span></span>

- [<span data-ttu-id="3a5b8-112">Tableaux de bord et rapports du Centre de sécurité Microsoft</span><span class="sxs-lookup"><span data-stu-id="3a5b8-112">Dashboards and reports in the Microsoft security Center</span></span>](https://docs.microsoft.com/office365/securitycompliance/tenant-wide-setup-for-increased-security#view-dashboards-and-reports-in-the-security-and-compliance-centers)
- [<span data-ttu-id="3a5b8-113">Degré de sécurisation Microsoft</span><span class="sxs-lookup"><span data-stu-id="3a5b8-113">Microsoft Secure Score</span></span>](https://docs.microsoft.com/office365/securitycompliance/microsoft-secure-score)

<span data-ttu-id="3a5b8-114">[Office 365 - Protection avancée contre les menaces](https://docs.microsoft.com/office365/securitycompliance/office-365-atp) est une fonctionnalité de sécurité supplémentaire qui permet à votre organisation de collaborer en toute sécurité comme suit :</span><span class="sxs-lookup"><span data-stu-id="3a5b8-114">An additional security feature is [Office 365 Advanced Threat Protection (ATP)](https://docs.microsoft.com/office365/securitycompliance/office-365-atp), which helps your organization collaborate more securely by:</span></span>

- <span data-ttu-id="3a5b8-115">Protection des [liens](https://docs.microsoft.com/office365/securitycompliance/atp-safe-links) et [pièces jointes](https://docs.microsoft.com/office365/securitycompliance/atp-safe-attachments) dans les e-mails.</span><span class="sxs-lookup"><span data-stu-id="3a5b8-115">Protecting [links](https://docs.microsoft.com/office365/securitycompliance/atp-safe-links) and [attachments](https://docs.microsoft.com/office365/securitycompliance/atp-safe-attachments) in email.</span></span> 
- <span data-ttu-id="3a5b8-116">Fourniture de fonctionnalités de veille contre l’usurpation d’identité et de protection anti-hameçonnage pour les e-mails dans Exchange Online et les [fichiers dans SharePoint Online, OneDrive Entreprise et Microsoft Teams](https://docs.microsoft.com/office365/securitycompliance/atp-for-spo-odb-and-teams).</span><span class="sxs-lookup"><span data-stu-id="3a5b8-116">Providing spoof intelligence and anti-phishing capabilities for email in Exchange Online and [files in SharePoint Online, OneDrive for Business, and Microsoft Teams](https://docs.microsoft.com/office365/securitycompliance/atp-for-spo-odb-and-teams).</span></span> 

<span data-ttu-id="3a5b8-117">Office 365 – Protection avancée contre les menaces est uniquement disponible avec Microsoft 365 E5.</span><span class="sxs-lookup"><span data-stu-id="3a5b8-117">Office 365 ATP is only available with Microsoft 365 E5.</span></span>

|||
|:-------|:-----|
|![Guides de laboratoire de test pour Microsoft Cloud](../media/m365-enterprise-test-lab-guides/cloud-tlg-icon-small.png)| [<span data-ttu-id="3a5b8-119">Guide de laboratoire de test : renforcer la sécurité de Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="3a5b8-119">Test Lab Guide: Configure increased Microsoft 365 security</span></span>](increased-o365-security-microsoft-365-enterprise-dev-test-environment.md) |
|||

<span data-ttu-id="3a5b8-120">Comme point de contrôle intermédiaire, consultez les [critères de sortie](infoprotect-exit-criteria.md#crit-infoprotect-step3) correspondant à cette étape.</span><span class="sxs-lookup"><span data-stu-id="3a5b8-120">As an interim checkpoint, see the [exit criteria](infoprotect-exit-criteria.md#crit-infoprotect-step3) corresponding to this step.</span></span>

## <a name="next-step"></a><span data-ttu-id="3a5b8-121">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="3a5b8-121">Next step</span></span>


|||
|:-------|:-----|
|![Étape 4](../media/stepnumbers/Step4.png)|[<span data-ttu-id="3a5b8-123">Configurer la protection des informations Windows</span><span class="sxs-lookup"><span data-stu-id="3a5b8-123">Configure Windows Information Protection</span></span>](infoprotect-deploy-windows-information-protection.md)|


