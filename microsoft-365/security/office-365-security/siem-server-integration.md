---
title: Intégration de serveur SIEM à Microsoft 365
ms.author: deniseb
author: denisebmsft
manager: dansimp
audience: ITPro
ms.topic: article
ms.date: 06/17/2019
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
ms.custom:
- Ent_Solutions
- SIEM
description: 'Résumé : consultez cet article pour obtenir une vue d’ensemble de l’intégration de serveur SIEM à Microsoft 365.'
ms.openlocfilehash: 97f1c1d1f1862d140e014b4460ac9f40cb1934bb
ms.sourcegitcommit: 1162d676b036449ea4220de8a6642165190e3398
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/20/2019
ms.locfileid: "37080443"
---
# <a name="siem-server-integration-with-microsoft-365-services-and-applications"></a><span data-ttu-id="48999-103">Intégration de serveur SIEM aux services et applications Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="48999-103">SIEM server integration with Microsoft 365 services and applications</span></span>

## <a name="overview"></a><span data-ttu-id="48999-104">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="48999-104">Overview</span></span>

<span data-ttu-id="48999-105">Si votre organisation utilise un serveur de gestion des événements et des informations de sécurité (SIEM), ou si vous envisagez d’obtenir rapidement un serveur SIEM, vous vous demandez peut-être comment l’intégrer à votre Microsoft 365, y compris Office 365 E5.</span><span class="sxs-lookup"><span data-stu-id="48999-105">If your organization is using a Security Information and Event Management (SIEM) server, or if you are planning to get a SIEM server soon, you might be wondering how that'll integrate with your Microsoft 365, including Office 365 E5.</span></span> <span data-ttu-id="48999-106">La nécessité d’un serveur SIEM dépend de nombreux facteurs, tels que les exigences de sécurité de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="48999-106">Whether you need a SIEM server depends on many factors, such as your organization's security requirements.</span></span> <span data-ttu-id="48999-107">Microsoft 365 offre plusieurs fonctionnalités de sécurité ; Toutefois, si votre organisation dispose de contenu et d’applications sur site et dans le Cloud (comme dans le cas d’un déploiement de Cloud hybride), vous pouvez envisager d’ajouter un serveur SIEM pour une protection supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="48999-107">Microsoft 365 offers a variety of security features; however, if your organization has content and applications on premises and in the cloud (as in the case of a hybrid cloud deployment), you might consider adding a SIEM server for extra protection.</span></span> <span data-ttu-id="48999-108">Ou, si votre organisation a des exigences de sécurité particulièrement rigoureuses que vous devez respecter, vous pouvez envisager d’ajouter un serveur SIEM à votre environnement.</span><span class="sxs-lookup"><span data-stu-id="48999-108">Or, if your organization has particularly stringent security requirements you must meet, you might consider adding a SIEM server to your environment.</span></span>

## <a name="siem-server-integration-microsoft-365"></a><span data-ttu-id="48999-109">Intégration de serveur SIEM Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="48999-109">SIEM server integration Microsoft 365</span></span>

<span data-ttu-id="48999-110">Un serveur SIEM peut recevoir des données à partir d’un large éventail de services et d’applications Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="48999-110">A SIEM server can receive data from a wide variety of Microsoft 365 services and applications.</span></span> <span data-ttu-id="48999-111">Le tableau suivant répertorie plusieurs applications et services Microsoft 365, ainsi que des entrées de serveur SIEM et l’endroit où aller pour en savoir plus sur l’intégration de serveur SIEM.</span><span class="sxs-lookup"><span data-stu-id="48999-111">The following table lists several Microsoft 365 services and applications along with SIEM server inputs and where to go to learn more about SIEM server integration.</span></span> 

| <span data-ttu-id="48999-112">Service ou application Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="48999-112">Microsoft 365 Service or Application</span></span> | <span data-ttu-id="48999-113">Entrées de serveur SIEM</span><span class="sxs-lookup"><span data-stu-id="48999-113">SIEM server inputs</span></span> | <span data-ttu-id="48999-114">Ressources pour en savoir plus</span><span class="sxs-lookup"><span data-stu-id="48999-114">Resources to learn more</span></span> |
| --- | --- | --- |
| [<span data-ttu-id="48999-115">Office 365 protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="48999-115">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md) <br/><span data-ttu-id="48999-116">ou</span><span class="sxs-lookup"><span data-stu-id="48999-116">or</span></span><br/>[<span data-ttu-id="48999-117">Office 365 Threat Intelligence</span><span class="sxs-lookup"><span data-stu-id="48999-117">Office 365 Threat Intelligence</span></span>](office-365-ti.md) | <span data-ttu-id="48999-118">Journaux d'audit</span><span class="sxs-lookup"><span data-stu-id="48999-118">Audit logs</span></span> | [<span data-ttu-id="48999-119">Intégration SIEM avec Office 365 protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="48999-119">SIEM integration with Office 365 Advanced Threat Protection</span></span>](siem-integration-with-office-365-ti.md) |
| [<span data-ttu-id="48999-120">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="48999-120">Microsoft Cloud App Security</span></span>](https://docs.microsoft.com/cloud-app-security/what-is-cloud-app-security) | <span data-ttu-id="48999-121">Intégration des journaux</span><span class="sxs-lookup"><span data-stu-id="48999-121">Log integration</span></span> | [<span data-ttu-id="48999-122">Intégration SIEM à la sécurité des applications Cloud Microsoft</span><span class="sxs-lookup"><span data-stu-id="48999-122">SIEM integration with Microsoft Cloud App Security</span></span>](https://docs.microsoft.com/cloud-app-security/siem) |
| [<span data-ttu-id="48999-123">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="48999-123">Microsoft Threat Protection</span></span>](https://docs.microsoft.com/windows/security/threat-protection/) | <span data-ttu-id="48999-124">Intégration des journaux</span><span class="sxs-lookup"><span data-stu-id="48999-124">Log integration</span></span> | [<span data-ttu-id="48999-125">Attirez les alertes sur vos outils SIEM</span><span class="sxs-lookup"><span data-stu-id="48999-125">Pull alerts to your SIEM tools</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/configure-siem) |
| <span data-ttu-id="48999-126">[Centre de sécurité Azure](https://docs.microsoft.com/azure/security-center/security-center-intro) (Protection contre les menaces et détection des menaces)</span><span class="sxs-lookup"><span data-stu-id="48999-126">[Azure Security Center](https://docs.microsoft.com/azure/security-center/security-center-intro) (Threat Protection and Threat Detection)</span></span> | <span data-ttu-id="48999-127">Alertes</span><span class="sxs-lookup"><span data-stu-id="48999-127">Alerts</span></span> | [<span data-ttu-id="48999-128">Exportation de données de sécurité Azure vers la configuration SIEM-pipeline-aperçu</span><span class="sxs-lookup"><span data-stu-id="48999-128">Azure Security data export to SIEM - Pipeline Configuration - Preview</span></span>](https://docs.microsoft.com/azure/security-center/security-center-export-data-to-siem) |
|[<span data-ttu-id="48999-129">Advanced Threat Analytics</span><span class="sxs-lookup"><span data-stu-id="48999-129">Azure Advanced Threat Analytics</span></span>](https://docs.microsoft.com/azure/security/azure-threat-detection) | <span data-ttu-id="48999-130">Moniteur Azure</span><span class="sxs-lookup"><span data-stu-id="48999-130">Azure Monitor</span></span> | [<span data-ttu-id="48999-131">Récents Utiliser Azure Monitor pour intégrer des outils SIEM</span><span class="sxs-lookup"><span data-stu-id="48999-131">(Blog) Use Azure Monitor to integrate with SIEM tools</span></span>](https://azure.microsoft.com/blog/use-azure-monitor-to-integrate-with-siem-tools) |
|[<span data-ttu-id="48999-132">Azure Active Directory Identity Protection</span><span class="sxs-lookup"><span data-stu-id="48999-132">Azure Active Directory Identity Protection</span></span>](https://docs.microsoft.com/azure/active-directory/identity-protection/overview) |<span data-ttu-id="48999-133">Intégration des journaux</span><span class="sxs-lookup"><span data-stu-id="48999-133">Log integration</span></span> |[<span data-ttu-id="48999-134">Intégrer les alertes de l’API de sécurité Microsoft Graph avec des technologies SIEM</span><span class="sxs-lookup"><span data-stu-id="48999-134">Integrate Microsoft Graph Security API alerts with a SIEM</span></span>](https://docs.microsoft.com/graph/security-siemintegration) |


## <a name="audit-logging-must-be-turned-on"></a><span data-ttu-id="48999-135">La journalisation d’audit doit être activée.</span><span class="sxs-lookup"><span data-stu-id="48999-135">Audit logging must be turned on</span></span>

<span data-ttu-id="48999-136">Assurez-vous que la journalisation d’audit est activée avant de configurer l’intégration de serveur SIEM.</span><span class="sxs-lookup"><span data-stu-id="48999-136">Make sure audit logging is turned on before you configure SIEM server integration.</span></span> 

- <span data-ttu-id="48999-137">Pour SharePoint Online, OneDrive entreprise et Azure Active Directory, [la journalisation d’audit est activée dans le centre de sécurité & conformité](https://docs.microsoft.com/office365/securitycompliance/turn-audit-log-search-on-or-off).</span><span class="sxs-lookup"><span data-stu-id="48999-137">For SharePoint Online, OneDrive for Business, and Azure Active Directory, [audit logging is turned on in the Security & Compliance Center](https://docs.microsoft.com/office365/securitycompliance/turn-audit-log-search-on-or-off).</span></span>

- <span data-ttu-id="48999-138">Pour Exchange Online, la [journalisation d’audit est activée avec Windows PowerShell](https://docs.microsoft.com/office365/securitycompliance/enable-mailbox-auditing).</span><span class="sxs-lookup"><span data-stu-id="48999-138">For Exchange Online, [audit logging is turned on with Windows PowerShell](https://docs.microsoft.com/office365/securitycompliance/enable-mailbox-auditing).</span></span>
 
## <a name="see-also"></a><span data-ttu-id="48999-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="48999-139">See Also</span></span>

[<span data-ttu-id="48999-140">Adoption du cloud et solutions hybrides</span><span class="sxs-lookup"><span data-stu-id="48999-140">Cloud adoption and hybrid solutions</span></span>](https://docs.microsoft.com/office365/enterprise/cloud-adoption-and-hybrid-solutions)
  
[<span data-ttu-id="48999-141">Guides de laboratoire de test d’adoption cloud</span><span class="sxs-lookup"><span data-stu-id="48999-141">Cloud adoption Test Lab Guides (TLGs)</span></span>](https://docs.microsoft.com/office365/enterprise/cloud-adoption-test-lab-guides-tlgs)


