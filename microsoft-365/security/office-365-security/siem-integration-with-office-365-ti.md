---
title: Intégration SIEM avec protection avancée contre les menaces
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
ms.date: 08/21/2020
ms.collection:
- M365-security-compliance
description: Intégrez le serveur SIEM de votre organisation avec Office 365 protection avancée contre les menaces et les événements de menace associés dans l’API de gestion des activités Office 365.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: c4c92fc45546d3d8022a3925baa9c10f9bd0090b
ms.sourcegitcommit: 153f413402f93b79be421741f3b9fed318d6d270
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "48600552"
---
# <a name="siem-integration-with-advanced-threat-protection"></a><span data-ttu-id="04493-103">Intégration SIEM avec protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="04493-103">SIEM integration with Advanced Threat Protection</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


<span data-ttu-id="04493-104">Si votre organisation utilise un serveur de gestion des événements et des informations de sécurité (SIEM), vous pouvez intégrer Office 365 Advanced Threat Protection (Office 365 ATP) à votre serveur SIEM.</span><span class="sxs-lookup"><span data-stu-id="04493-104">If your organization is using a security information and event management (SIEM) server, you can integrate Office 365 Advanced Threat Protection (Office 365 ATP) with your SIEM server.</span></span> <span data-ttu-id="04493-105">Vous pouvez configurer cette intégration à l’aide de l' [API de gestion des activités Office 365](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference).</span><span class="sxs-lookup"><span data-stu-id="04493-105">You can set up this integration by using the [Office 365 Activity Management API](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference).</span></span> 

<span data-ttu-id="04493-106">L’intégration SIEM vous permet d’afficher des informations, telles que des programmes malveillants ou des hameçons détectés par la protection avancée contre les menaces d’Office 365, dans vos rapports de serveur SIEM.</span><span class="sxs-lookup"><span data-stu-id="04493-106">SIEM integration enables you to view information, such as malware or phish detected by Office 365 ATP, in your SIEM server reports.</span></span> 

- <span data-ttu-id="04493-107">Pour voir un exemple d’intégration SIEM avec la protection avancée contre les menaces Office 365, voir blog de la [communauté technique : améliorer l’efficacité de votre SOC avec office 365 ATP et l’API de gestion d’O365](https://techcommunity.microsoft.com/t5/microsoft-security-and/improve-the-effectiveness-of-your-soc-with-office-365-atp-and/ba-p/1525185).</span><span class="sxs-lookup"><span data-stu-id="04493-107">To see an example of SIEM integration with Office 365 ATP, see [Tech Community blog: Improve the Effectiveness of your SOC with Office 365 ATP and the O365 Management API](https://techcommunity.microsoft.com/t5/microsoft-security-and/improve-the-effectiveness-of-your-soc-with-office-365-atp-and/ba-p/1525185).</span></span>

- <span data-ttu-id="04493-108">Pour en savoir plus sur les API de gestion d’Office 365, voir [office 365 Management API Overview](https://docs.microsoft.com/office/office-365-management-api/office-365-management-apis-overview).</span><span class="sxs-lookup"><span data-stu-id="04493-108">To learn more about the Office 365 Management APIs, see [Office 365 Management APIs overview](https://docs.microsoft.com/office/office-365-management-api/office-365-management-apis-overview).</span></span>

## <a name="how-siem-integration-works"></a><span data-ttu-id="04493-109">Fonctionnement de l’intégration SIEM</span><span class="sxs-lookup"><span data-stu-id="04493-109">How SIEM integration works</span></span>

<span data-ttu-id="04493-110">L’API de gestion des activités Office 365 récupère des informations sur les actions et événements d’utilisateur, d’administrateur, de système et de stratégie à partir des journaux d’activité de Microsoft 365 et Azure Active Directory de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="04493-110">The Office 365 Activity Management API retrieves information about user, admin, system, and policy actions and events from your organization's Microsoft 365 and Azure Active Directory activity logs.</span></span> <span data-ttu-id="04493-111">Si votre organisation dispose d’Office 365 ATP plan 1 ou 2, ou Office 365 E5, vous pouvez utiliser le [schéma ATP d’office 365](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-investigation-and-response-schema).</span><span class="sxs-lookup"><span data-stu-id="04493-111">If your organization has Office 365 ATP Plan 1 or 2, or Office 365 E5, you can use the [Office 365 ATP schema](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-investigation-and-response-schema).</span></span>  

<span data-ttu-id="04493-112">Récemment, les événements des fonctionnalités d’analyse et de réponse automatisées dans [office 365 DAV plan 2](office-365-atp.md#office-365-atp-plan-1-and-plan-2) ont été ajoutés à l’API activité de gestion d’Office 365.</span><span class="sxs-lookup"><span data-stu-id="04493-112">Recently, events from automated investigation and response capabilities in [Office 365 ATP Plan 2](office-365-atp.md#office-365-atp-plan-1-and-plan-2) were added to the Office 365 Management Activity API.</span></span> <span data-ttu-id="04493-113">En plus d’inclure des données sur les détails d’enquête de base, tels que l’ID, le nom et l’État, l’API contient également des informations de haut niveau sur les actions et les entités d’enquête.</span><span class="sxs-lookup"><span data-stu-id="04493-113">In addition to including data about core investigation details such as ID, name and status, the API also contains high-level information about investigation actions and entities.</span></span>

<span data-ttu-id="04493-114">Le serveur SIEM ou un autre système similaire interroge l' **audit.** charge de travail générale pour accéder aux événements de détection.</span><span class="sxs-lookup"><span data-stu-id="04493-114">The SIEM server or other similar system polls the **audit.general** workload to access detection events.</span></span> <span data-ttu-id="04493-115">Pour plus d’informations, reportez-vous à la rubrique [prise en main des API de gestion d’Office 365](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis).</span><span class="sxs-lookup"><span data-stu-id="04493-115">To learn more, see [Get started with Office 365 Management APIs](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis).</span></span> 

## <a name="enum-auditlogrecordtype---type-edmint32"></a><span data-ttu-id="04493-116">Énumération : AuditLogRecordType - Type : Edm.Int32</span><span class="sxs-lookup"><span data-stu-id="04493-116">Enum: AuditLogRecordType - Type: Edm.Int32</span></span>

### <a name="auditlogrecordtype"></a><span data-ttu-id="04493-117">AuditLogRecordType</span><span class="sxs-lookup"><span data-stu-id="04493-117">AuditLogRecordType</span></span>

<span data-ttu-id="04493-118">Le tableau suivant récapitule les valeurs de **AuditLogRecordType** qui sont pertinentes pour les événements ATP Office 365 :</span><span class="sxs-lookup"><span data-stu-id="04493-118">The following table summarizes the values of **AuditLogRecordType** that are relevant for Office 365 ATP events:</span></span>

|<span data-ttu-id="04493-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="04493-119">Value</span></span>|<span data-ttu-id="04493-120">Nom du membre</span><span class="sxs-lookup"><span data-stu-id="04493-120">Member name</span></span>|<span data-ttu-id="04493-121">Description</span><span class="sxs-lookup"><span data-stu-id="04493-121">Description</span></span>|
|---|---|---|
|<span data-ttu-id="04493-122">vingt</span><span class="sxs-lookup"><span data-stu-id="04493-122">28</span></span>|<span data-ttu-id="04493-123">ThreatIntelligence</span><span class="sxs-lookup"><span data-stu-id="04493-123">ThreatIntelligence</span></span>|<span data-ttu-id="04493-124">Événements de hameçonnage et de programmes malveillants à partir d’Exchange Online Protection et Office 365 ATP.</span><span class="sxs-lookup"><span data-stu-id="04493-124">Phishing and malware events from Exchange Online Protection and Office 365 ATP.</span></span>|
|<span data-ttu-id="04493-125">41</span><span class="sxs-lookup"><span data-stu-id="04493-125">41</span></span>|<span data-ttu-id="04493-126">ThreatIntelligenceUrl</span><span class="sxs-lookup"><span data-stu-id="04493-126">ThreatIntelligenceUrl</span></span>|<span data-ttu-id="04493-127">Événements de liens approuvés de bloc de temps de bloc et de remplacement de bloc à partir d’Office 365 ATP.</span><span class="sxs-lookup"><span data-stu-id="04493-127">Safe Links time-of-block and block override events from Office 365 ATP.</span></span>|
|<span data-ttu-id="04493-128">47</span><span class="sxs-lookup"><span data-stu-id="04493-128">47</span></span>|<span data-ttu-id="04493-129">ThreatIntelligenceAtpContent</span><span class="sxs-lookup"><span data-stu-id="04493-129">ThreatIntelligenceAtpContent</span></span>|<span data-ttu-id="04493-130">Événements de hameçonnage et de programmes malveillants pour les fichiers dans SharePoint Online, OneDrive entreprise et Microsoft Teams, à partir d’Office 365 ATP.</span><span class="sxs-lookup"><span data-stu-id="04493-130">Phishing and malware events for files in SharePoint Online, OneDrive for Business, and Microsoft Teams, from Office 365 ATP.</span></span>|
|<span data-ttu-id="04493-131">64</span><span class="sxs-lookup"><span data-stu-id="04493-131">64</span></span>|<span data-ttu-id="04493-132">AirInvestigation</span><span class="sxs-lookup"><span data-stu-id="04493-132">AirInvestigation</span></span>|<span data-ttu-id="04493-133">Des événements d’enquête et de réponse automatisés, tels que des détails d’enquête et des artefacts pertinents, à partir d’Office 365 DAV (plan 2).</span><span class="sxs-lookup"><span data-stu-id="04493-133">Automated investigation and response events, such as investigation details and relevant artifacts, from Office 365 ATP Plan 2.</span></span>|
|

> [!IMPORTANT]
> <span data-ttu-id="04493-134">Vous devez être un administrateur général ou avoir le rôle administrateur de sécurité affecté au centre de sécurité & conformité pour configurer l’intégration SIEM avec Office 365 protection avancée contre les menaces.</span><span class="sxs-lookup"><span data-stu-id="04493-134">You must be a global administrator or have the security administrator role assigned for the Security & Compliance Center to set up SIEM integration with Office 365 Advanced Threat Protection.</span></span><br/><span data-ttu-id="04493-135">La journalisation d’audit doit être activée pour votre environnement Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="04493-135">Audit logging must be turned on for your Microsoft 365 environment.</span></span> <span data-ttu-id="04493-136">Pour obtenir de l’aide, consultez la rubrique [activer ou désactiver la recherche dans le journal d’audit](../../compliance/turn-audit-log-search-on-or-off.md).</span><span class="sxs-lookup"><span data-stu-id="04493-136">To get help with this, see [Turn audit log search on or off](../../compliance/turn-audit-log-search-on-or-off.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="04493-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="04493-137">See also</span></span>

[<span data-ttu-id="04493-138">Examen et réponse contre les menaces Office 365</span><span class="sxs-lookup"><span data-stu-id="04493-138">Office 365 threat investigation and response</span></span>](office-365-ti.md)

[<span data-ttu-id="04493-139">Recherche et réponse automatiques dans Office 365</span><span class="sxs-lookup"><span data-stu-id="04493-139">Automated investigation and response (AIR) in Office 365</span></span>](automated-investigation-response-office.md)

