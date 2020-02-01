---
title: Intégration SIEM avec Office 365 protection avancée contre les menaces
f1.keywords:
- NOCSH
ms.author: deniseb
author: denisebmsft
manager: dansimp
audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
- MOE150
ms.assetid: eb56b69b-3170-4086-82cf-ba40a530fa1b
ms.date: 11/22/2019
ms.collection:
- M365-security-compliance
description: Intégrez le serveur SIEM de votre organisation avec Office 365 protection avancée contre les menaces et les événements de menace associés dans l’API de gestion des activités Office 365.
ms.openlocfilehash: 8a870e02a37ea7f4961d0b8dc42a49cb59d2bace
ms.sourcegitcommit: 1c91b7b24537d0e54d484c3379043db53c1aea65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2020
ms.locfileid: "41598281"
---
# <a name="siem-integration-with-office-365-advanced-threat-protection"></a><span data-ttu-id="f562f-103">Intégration SIEM avec Office 365 protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="f562f-103">SIEM integration with Office 365 Advanced Threat Protection</span></span>

<span data-ttu-id="f562f-104">Si votre organisation utilise un serveur de gestion des événements et des incidents de sécurité (SIEM), vous pouvez intégrer Office 365 Advanced Threat Protection à votre serveur SIEM.</span><span class="sxs-lookup"><span data-stu-id="f562f-104">If your organization is using a security incident and event management (SIEM) server, you can integrate Office 365 Advanced Threat Protection with your SIEM server.</span></span> <span data-ttu-id="f562f-105">L’intégration SIEM vous permet d’afficher des informations, telles que des programmes malveillants ou des hameçons détectés par Office 365 Advanced protection, dans vos rapports de serveur SIEM.</span><span class="sxs-lookup"><span data-stu-id="f562f-105">SIEM integration enables you to view information, such as malware or phish detected by Office 365 Advanced Protection, in your SIEM server reports.</span></span> <span data-ttu-id="f562f-106">Pour configurer l’intégration SIEM, vous utilisez l' [API de gestion des activités Office 365](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference).</span><span class="sxs-lookup"><span data-stu-id="f562f-106">To set up SIEM integration, you use the [Office 365 Activity Management API](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference).</span></span> 

<span data-ttu-id="f562f-107">L’API de gestion des activités Office 365 récupère des informations sur les actions et événements d’utilisateur, d’administrateur, de système et de stratégie à partir des journaux d’activité Office 365 et Azure Active Directory de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="f562f-107">The Office 365 Activity Management API retrieves information about user, admin, system, and policy actions and events from your organization's Office 365 and Azure Active Directory activity logs.</span></span> <span data-ttu-id="f562f-108">Le [schéma de protection avancée contre les menaces office 365](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-investigation-and-response-schema) fonctionne avec la protection avancée contre les menaces, de sorte que si votre organisation a le plan 1 ou plan 2 ou Office 365 E5 Office 365 Advanced Threat Protection, vous pouvez toujours utiliser cette même API pour votre intégration de serveur Siem.</span><span class="sxs-lookup"><span data-stu-id="f562f-108">The [Office 365 Advanced Threat Protection schema](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-investigation-and-response-schema) works with Advanced Threat Protection, so if your organization has the Office 365 Advanced Threat Protection Plan 1 or Plan 2 or Office 365 E5, you can still use that same API for your SIEM server integration.</span></span> 

<span data-ttu-id="f562f-109">Dans le cadre de nos mises à jour récentes, nous avons également ajouté des événements à partir des fonctionnalités d’analyse et de réponse automatisées dans Office 365 DAV plan 2 au sein de l’API activité de gestion d’Office 365.</span><span class="sxs-lookup"><span data-stu-id="f562f-109">As part of our recent updates, we have also added events from automated investigation and response capabilities in Office 365 ATP Plan 2 within the Office 365 Management Activity API.</span></span> <span data-ttu-id="f562f-110">En plus d’inclure des données sur les détails d’enquête de base, tels que l’ID, le nom et l’État, il contient également des informations de haut niveau sur les actions et les entités d’enquête.</span><span class="sxs-lookup"><span data-stu-id="f562f-110">In addition to including data about core investigation details such as ID, name and status, it also contains high-level information about investigation actions and entities.</span></span>   

<span data-ttu-id="f562f-111">Le serveur SIEM ou un autre système similaire doit interroger l' **audit.** charge de travail générale pour accéder aux événements de détection.</span><span class="sxs-lookup"><span data-stu-id="f562f-111">The SIEM server or other similar system should poll the **audit.general** workload to access detection events.</span></span> <span data-ttu-id="f562f-112">Pour plus d’informations, consultez la rubrique [prise en main des API de gestion d’Office 365](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis).</span><span class="sxs-lookup"><span data-stu-id="f562f-112">To learn more see [Get started with Office 365 Management APIs](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis).</span></span> <span data-ttu-id="f562f-113">En outre, les valeurs suivantes de **AuditLogRecordType** sont pertinentes pour les événements ATP Office 365 :</span><span class="sxs-lookup"><span data-stu-id="f562f-113">In addition, the following values of **AuditLogRecordType** are relevant for Office 365 ATP events:</span></span>

### <a name="enum-auditlogrecordtype---type-edmint32"></a><span data-ttu-id="f562f-114">Énumération : AuditLogRecordType - Type : Edm.Int32</span><span class="sxs-lookup"><span data-stu-id="f562f-114">Enum: AuditLogRecordType - Type: Edm.Int32</span></span>

#### <a name="auditlogrecordtype"></a><span data-ttu-id="f562f-115">AuditLogRecordType</span><span class="sxs-lookup"><span data-stu-id="f562f-115">AuditLogRecordType</span></span>

|<span data-ttu-id="f562f-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="f562f-116">Value</span></span>|<span data-ttu-id="f562f-117">Nom du membre</span><span class="sxs-lookup"><span data-stu-id="f562f-117">Member name</span></span>|<span data-ttu-id="f562f-118">Description</span><span class="sxs-lookup"><span data-stu-id="f562f-118">Description</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f562f-119">vingt</span><span class="sxs-lookup"><span data-stu-id="f562f-119">28</span></span>|<span data-ttu-id="f562f-120">ThreatIntelligence</span><span class="sxs-lookup"><span data-stu-id="f562f-120">ThreatIntelligence</span></span>|<span data-ttu-id="f562f-121">Événements d’hameçonnage et de programmes malveillants depuis Exchange Online Protection et Office 365 Advanced Threat Protection.</span><span class="sxs-lookup"><span data-stu-id="f562f-121">Phishing and malware events from Exchange Online Protection and Office 365 Advanced Threat Protection.</span></span>|
|<span data-ttu-id="f562f-122">41</span><span class="sxs-lookup"><span data-stu-id="f562f-122">41</span></span>|<span data-ttu-id="f562f-123">ThreatIntelligenceUrl</span><span class="sxs-lookup"><span data-stu-id="f562f-123">ThreatIntelligenceUrl</span></span>|<span data-ttu-id="f562f-124">Les événements de la protection avancée contre les menaces des liens approuvés ATP (temps de blocage) et de blocage d’Office 365.</span><span class="sxs-lookup"><span data-stu-id="f562f-124">ATP Safe Links time-of-block and block override events from Office 365 Advanced Threat Protection.</span></span>|
|<span data-ttu-id="f562f-125">47</span><span class="sxs-lookup"><span data-stu-id="f562f-125">47</span></span>|<span data-ttu-id="f562f-126">ThreatIntelligenceAtpContent</span><span class="sxs-lookup"><span data-stu-id="f562f-126">ThreatIntelligenceAtpContent</span></span>|<span data-ttu-id="f562f-127">Événements de hameçonnage et de programmes malveillants pour les fichiers dans SharePoint Online, OneDrive entreprise et Microsoft teams à partir d’Office 365 protection avancée contre les menaces.</span><span class="sxs-lookup"><span data-stu-id="f562f-127">Phishing and malware events for files in SharePoint Online, OneDrive for Business, and Microsoft Teams from Office 365 Advanced Threat Protection.</span></span>|
|<span data-ttu-id="f562f-128">64</span><span class="sxs-lookup"><span data-stu-id="f562f-128">64</span></span>|<span data-ttu-id="f562f-129">AirInvestigation</span><span class="sxs-lookup"><span data-stu-id="f562f-129">AirInvestigation</span></span>|<span data-ttu-id="f562f-130">Des événements d’enquête et de réponse automatisés, tels que des détails d’enquête et des artefacts pertinents à partir d’Office 365 Advanced Threat Protection Plan 2.</span><span class="sxs-lookup"><span data-stu-id="f562f-130">Automated investigation and response events, such as investigation details and relevant artifacts from Office 365 Advanced Threat Protection Plan 2.</span></span>|


> [!IMPORTANT]
> <span data-ttu-id="f562f-131">Vous devez être un administrateur général Office 365 ou faire en sorte que le rôle administrateur de sécurité soit affecté au centre de sécurité & conformité afin de configurer l’intégration SIEM avec Office 365 Advanced Threat Protection.</span><span class="sxs-lookup"><span data-stu-id="f562f-131">You must be an Office 365 global administrator or have the security administrator role assigned for the Security & Compliance Center to set up SIEM integration with Office 365 Advanced Threat Protection.</span></span><br/><span data-ttu-id="f562f-132">L’enregistrement d’audit doit être activé pour votre environnement Office 365.</span><span class="sxs-lookup"><span data-stu-id="f562f-132">Audit logging must be turned on for your Office 365 environment.</span></span> <span data-ttu-id="f562f-133">Pour obtenir de l’aide, voir [activer ou désactiver la recherche dans le journal d’audit Office 365](../../compliance/turn-audit-log-search-on-or-off.md).</span><span class="sxs-lookup"><span data-stu-id="f562f-133">To get help with this, see [Turn Office 365 audit log search on or off](../../compliance/turn-audit-log-search-on-or-off.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f562f-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f562f-134">Related topics</span></span>

[<span data-ttu-id="f562f-135">Examen et réponse contre les menaces Office 365</span><span class="sxs-lookup"><span data-stu-id="f562f-135">Office 365 threat investigation and response</span></span>](office-365-ti.md)

[<span data-ttu-id="f562f-136">Recherche et réponse automatiques dans Office 365</span><span class="sxs-lookup"><span data-stu-id="f562f-136">Automated investigation and response (AIR) in Office 365</span></span>](automated-investigation-response-office.md)

[<span data-ttu-id="f562f-137">Protection avancée contre les menaces dans Office 365</span><span class="sxs-lookup"><span data-stu-id="f562f-137">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)

[<span data-ttu-id="f562f-138">Rapports intelligents et Insights dans le centre de sécurité &amp; conformité Office 365</span><span class="sxs-lookup"><span data-stu-id="f562f-138">Smart reports and insights in the Office 365 Security &amp; Compliance Center</span></span>](reports-and-insights-in-security-and-compliance.md)
  
[<span data-ttu-id="f562f-139">Permissions in the Office 365 Security &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="f562f-139">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)
  
