---
title: 'Étape 3 : renforcer la sécurité de Microsoft 365'
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
description: Comprendre et renforcer la sécurité de Microsoft 365.
ms.openlocfilehash: a1976a9305c40d721bd56a4b21b8a52552c1a9dc
ms.sourcegitcommit: 81273a9df49647286235b187fa2213c5ec7e8b62
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285076"
---
# <a name="step-3-configure-increased-security-for-microsoft-365"></a><span data-ttu-id="1242a-103">Étape 3 : renforcer la sécurité de Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="1242a-103">Step 3: Configure increased security for Office 365</span></span>

<span data-ttu-id="1242a-104">*Cette étape est requise et s’applique aux versions E3 et E5 de Microsoft 365 Entreprise*</span><span class="sxs-lookup"><span data-stu-id="1242a-104">*This step is required and applies to both the E3 and E5 versions of Microsoft 365 Enterprise*</span></span>

![](./media/deploy-foundation-infrastructure/infoprotection_icon-small.png)

<span data-ttu-id="1242a-105">Pour vous assurer que votre abonnement Microsoft 365 et ses données démarrent et restent protégés contre des menaces malveillantes, configurez les aspects suivants :</span><span class="sxs-lookup"><span data-stu-id="1242a-105">To ensure that your Office 365 subscription and its data start off and remain secure from malicious threats, see Configure your Office 365 tenant for increased security and configure the following additional security:</span></span>

- [<span data-ttu-id="1242a-106">Réglage des stratégies de gestion des menaces</span><span class="sxs-lookup"><span data-stu-id="1242a-106">Tune threat management policies</span></span>](https://docs.microsoft.com/office365/securitycompliance/tenant-wide-setup-for-increased-security#tune-threat-management-policies-in-the-office-365-security--compliance-center)
- [<span data-ttu-id="1242a-107">Autres paramètres à l’échelle du client Exchange Online</span><span class="sxs-lookup"><span data-stu-id="1242a-107">Additional Exchange Online tenant-wide settings</span></span>](https://docs.microsoft.com/office365/securitycompliance/tenant-wide-setup-for-increased-security#configure-additional-exchange-online-tenant-wide-settings)
- [<span data-ttu-id="1242a-108">Stratégies de partage à l’échelle du client dans le Centre d’administration SharePoint</span><span class="sxs-lookup"><span data-stu-id="1242a-108">Tenant-wide sharing policies in the SharePoint admin center</span></span>](https://docs.microsoft.com/office365/securitycompliance/tenant-wide-setup-for-increased-security#configure-tenant-wide-sharing-policies-in-sharepoint-admin-center)
- [<span data-ttu-id="1242a-109">Paramètres dans Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="1242a-109">CORS support in Microsoft Azure Active Directory (Azure AD)</span></span>](https://docs.microsoft.com/office365/securitycompliance/tenant-wide-setup-for-increased-security#configure-settings-in-azure-active-directory)

<span data-ttu-id="1242a-110">Une fois la configuration terminée, vous pouvez obtenir des informations concernant votre statut de sécurité à partir de :</span><span class="sxs-lookup"><span data-stu-id="1242a-110">Once configured, you can obtain information about your security status from:</span></span>

- [<span data-ttu-id="1242a-111">Tableaux de bord et rapports du Centre de sécurité Microsoft</span><span class="sxs-lookup"><span data-stu-id="1242a-111">Dashboards and reports in the Microsoft security Center</span></span>](https://docs.microsoft.com/office365/securitycompliance/tenant-wide-setup-for-increased-security#view-dashboards-and-reports-in-the-security--compliance-center)
- [<span data-ttu-id="1242a-112">Degré de sécurisation Microsoft</span><span class="sxs-lookup"><span data-stu-id="1242a-112">Microsoft Secure Score</span></span>](https://docs.microsoft.com/office365/securitycompliance/microsoft-secure-score)

<span data-ttu-id="1242a-113">[Office 365 - Protection avancée contre les menaces](https://docs.microsoft.com/office365/securitycompliance/office-365-atp) est une fonctionnalité de sécurité supplémentaire qui permet à votre organisation de collaborer en toute sécurité comme suit :</span><span class="sxs-lookup"><span data-stu-id="1242a-113">An additional security feature is Office 365 Advanced Threat Protection (ATP), which helps your organization collaborate more securely by:</span></span>

- <span data-ttu-id="1242a-114">Protection des [liens](https://docs.microsoft.com/office365/securitycompliance/atp-safe-links) et [pièces jointes](https://docs.microsoft.com/office365/securitycompliance/atp-safe-attachments) dans les e-mails.</span><span class="sxs-lookup"><span data-stu-id="1242a-114">Protecting links and attachments in email.</span></span> 
- <span data-ttu-id="1242a-115">Fourniture de fonctionnalités de veille contre l’usurpation d’identité et de protection anti-hameçonnage pour les e-mails dans Exchange Online et les [fichiers dans SharePoint Online, OneDrive Entreprise et Microsoft Teams](https://docs.microsoft.com/office365/securitycompliance/atp-for-spo-odb-and-teams).</span><span class="sxs-lookup"><span data-stu-id="1242a-115">Providing spoof intelligence and anti-phishing capabilities for email in Exchange Online and files in SharePoint Online, OneDrive for Business, and Microsoft Teams.</span></span> 

<span data-ttu-id="1242a-116">Office 365 - Protection avancée contre les menaces est disponible uniquement avec Microsoft 365 Entreprise E5.</span><span class="sxs-lookup"><span data-stu-id="1242a-116">Office 365 ATP is only available with Microsoft 365 Enterprise E5.</span></span>

|||
|:-------|:-----|
|![Guides de Laboratoire de Test pour Microsoft Cloud](media/m365-enterprise-test-lab-guides/cloud-tlg-icon-small.png)| [<span data-ttu-id="1242a-118">Guide de laboratoire de test : renforcer la sécurité de Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="1242a-118">Test Lab Guide: Configure increased Office 365 security</span></span>](increased-o365-security-microsoft-365-enterprise-dev-test-environment.md) |
|||

<span data-ttu-id="1242a-119">Comme point de contrôle intermédiaire, consultez les [critères de sortie](infoprotect-exit-criteria.md#crit-infoprotect-step4) correspondant à cette étape.</span><span class="sxs-lookup"><span data-stu-id="1242a-119">As an interim checkpoint, see the [exit criteria](infoprotect-exit-criteria.md#crit-infoprotect-step4) corresponding to this step.</span></span>

## <a name="next-step"></a><span data-ttu-id="1242a-120">Étape suivante</span><span class="sxs-lookup"><span data-stu-id="1242a-120">Next step</span></span>


|||
|:-------|:-----|
|![](./media/stepnumbers/Step4.png)|[<span data-ttu-id="1242a-121">Configurer la gestion des accès privilégiés</span><span class="sxs-lookup"><span data-stu-id="1242a-121">Configure privileged access management</span></span>](infoprotect-configure-privileged-access-management.md)|


