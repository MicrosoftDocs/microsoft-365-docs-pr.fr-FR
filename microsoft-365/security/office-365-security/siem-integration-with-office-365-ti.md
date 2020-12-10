---
title: Intégration SIEM à Microsoft Defender pour Office 365
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
description: Intégrer le serveur SIEM de votre organisation à Microsoft Defender pour Office 365 et aux événements de menace associés dans l’API de gestion des activités Office 365.
ms.custom: seo-marvel-apr2020
ms.openlocfilehash: 93ff1606130c60ceb46087d28bb26f9a6d27d330
ms.sourcegitcommit: ee39faf3507d0edc9497117b3b2854955c959c6c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "49615659"
---
# <a name="siem-integration-with-microsoft-defender-for-office-365"></a><span data-ttu-id="0f10e-103">Intégration SIEM à Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="0f10e-103">SIEM integration with Microsoft Defender for Office 365</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


<span data-ttu-id="0f10e-104">Si votre organisation utilise un serveur de gestion des événements et des informations de sécurité (SIEM), vous pouvez intégrer Microsoft Defender pour Office 365 à votre serveur SIEM.</span><span class="sxs-lookup"><span data-stu-id="0f10e-104">If your organization is using a security information and event management (SIEM) server, you can integrate Microsoft Defender for Office 365 with your SIEM server.</span></span> <span data-ttu-id="0f10e-105">Vous pouvez configurer cette intégration à l’aide de l' [API de gestion des activités Office 365](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference).</span><span class="sxs-lookup"><span data-stu-id="0f10e-105">You can set up this integration by using the [Office 365 Activity Management API](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference).</span></span>

<span data-ttu-id="0f10e-106">L’intégration SIEM vous permet d’afficher des informations, telles que des programmes malveillants ou des hameçons détectés par Microsoft Defender pour Office 365, dans vos rapports de serveur SIEM.</span><span class="sxs-lookup"><span data-stu-id="0f10e-106">SIEM integration enables you to view information, such as malware or phish detected by Microsoft Defender for Office 365, in your SIEM server reports.</span></span>

- <span data-ttu-id="0f10e-107">Pour voir un exemple d’intégration SIEM avec Microsoft Defender pour Office 365, voir blog de la [communauté technique : améliorer l’efficacité de votre SOC avec Defender pour office 365 et l’API de gestion d’Office 365](https://techcommunity.microsoft.com/t5/microsoft-security-and/improve-the-effectiveness-of-your-soc-with-office-365-atp-and/ba-p/1525185).</span><span class="sxs-lookup"><span data-stu-id="0f10e-107">To see an example of SIEM integration with Microsoft Defender for Office 365, see [Tech Community blog: Improve the Effectiveness of your SOC with Defender for Office 365 and the O365 Management API](https://techcommunity.microsoft.com/t5/microsoft-security-and/improve-the-effectiveness-of-your-soc-with-office-365-atp-and/ba-p/1525185).</span></span>

- <span data-ttu-id="0f10e-108">Pour en savoir plus sur les API de gestion d’Office 365, voir [office 365 Management API Overview](https://docs.microsoft.com/office/office-365-management-api/office-365-management-apis-overview).</span><span class="sxs-lookup"><span data-stu-id="0f10e-108">To learn more about the Office 365 Management APIs, see [Office 365 Management APIs overview](https://docs.microsoft.com/office/office-365-management-api/office-365-management-apis-overview).</span></span>

## <a name="how-siem-integration-works"></a><span data-ttu-id="0f10e-109">Fonctionnement de l’intégration SIEM</span><span class="sxs-lookup"><span data-stu-id="0f10e-109">How SIEM integration works</span></span>

<span data-ttu-id="0f10e-110">L’API de gestion des activités Office 365 récupère des informations sur les actions et événements d’utilisateur, d’administrateur, de système et de stratégie à partir des journaux d’activité de Microsoft 365 et Azure Active Directory de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="0f10e-110">The Office 365 Activity Management API retrieves information about user, admin, system, and policy actions and events from your organization's Microsoft 365 and Azure Active Directory activity logs.</span></span> <span data-ttu-id="0f10e-111">Si votre organisation a Microsoft Defender pour Office 365 plan 1 ou 2 ou Office 365 E5, vous pouvez utiliser le [schéma Microsoft Defender pour office 365](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-investigation-and-response-schema).</span><span class="sxs-lookup"><span data-stu-id="0f10e-111">If your organization has Microsoft Defender for Office 365 Plan 1 or 2, or Office 365 E5, you can use the [Microsoft Defender for Office 365 schema](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-investigation-and-response-schema).</span></span>

<span data-ttu-id="0f10e-112">Récemment, les événements des fonctionnalités d’analyse et de réponse automatisées dans [Microsoft Defender pour Office 365 plan 2](office-365-atp.md#microsoft-defender-for-office-365-plan-1-and-plan-2) ont été ajoutés à l’API activité de gestion d’Office 365.</span><span class="sxs-lookup"><span data-stu-id="0f10e-112">Recently, events from automated investigation and response capabilities in [Microsoft Defender for Office 365 Plan 2](office-365-atp.md#microsoft-defender-for-office-365-plan-1-and-plan-2) were added to the Office 365 Management Activity API.</span></span> <span data-ttu-id="0f10e-113">En plus d’inclure des données sur les détails d’enquête de base, tels que l’ID, le nom et l’État, l’API contient également des informations de haut niveau sur les actions et les entités d’enquête.</span><span class="sxs-lookup"><span data-stu-id="0f10e-113">In addition to including data about core investigation details such as ID, name and status, the API also contains high-level information about investigation actions and entities.</span></span>

<span data-ttu-id="0f10e-114">Le serveur SIEM ou un autre système similaire interroge l' **audit.** charge de travail générale pour accéder aux événements de détection.</span><span class="sxs-lookup"><span data-stu-id="0f10e-114">The SIEM server or other similar system polls the **audit.general** workload to access detection events.</span></span> <span data-ttu-id="0f10e-115">Pour plus d’informations, reportez-vous à la rubrique [prise en main des API de gestion d’Office 365](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis).</span><span class="sxs-lookup"><span data-stu-id="0f10e-115">To learn more, see [Get started with Office 365 Management APIs](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis).</span></span>

## <a name="enum-auditlogrecordtype---type-edmint32"></a><span data-ttu-id="0f10e-116">Énumération : AuditLogRecordType - Type : Edm.Int32</span><span class="sxs-lookup"><span data-stu-id="0f10e-116">Enum: AuditLogRecordType - Type: Edm.Int32</span></span>

### <a name="auditlogrecordtype"></a><span data-ttu-id="0f10e-117">AuditLogRecordType</span><span class="sxs-lookup"><span data-stu-id="0f10e-117">AuditLogRecordType</span></span>

<span data-ttu-id="0f10e-118">Le tableau suivant récapitule les valeurs de **AuditLogRecordType** qui sont pertinentes pour les événements Microsoft Defender pour Office 365 :</span><span class="sxs-lookup"><span data-stu-id="0f10e-118">The following table summarizes the values of **AuditLogRecordType** that are relevant for Microsoft Defender for Office 365 events:</span></span>

|<span data-ttu-id="0f10e-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="0f10e-119">Value</span></span>|<span data-ttu-id="0f10e-120">Nom du membre</span><span class="sxs-lookup"><span data-stu-id="0f10e-120">Member name</span></span>|<span data-ttu-id="0f10e-121">Description</span><span class="sxs-lookup"><span data-stu-id="0f10e-121">Description</span></span>|
|---|---|---|
|<span data-ttu-id="0f10e-122">vingt</span><span class="sxs-lookup"><span data-stu-id="0f10e-122">28</span></span>|<span data-ttu-id="0f10e-123">ThreatIntelligence</span><span class="sxs-lookup"><span data-stu-id="0f10e-123">ThreatIntelligence</span></span>|<span data-ttu-id="0f10e-124">Événements de hameçonnage et de programmes malveillants dans Exchange Online Protection et Microsoft Defender pour Office 365.</span><span class="sxs-lookup"><span data-stu-id="0f10e-124">Phishing and malware events from Exchange Online Protection and Microsoft Defender for Office 365.</span></span>|
|<span data-ttu-id="0f10e-125">41</span><span class="sxs-lookup"><span data-stu-id="0f10e-125">41</span></span>|<span data-ttu-id="0f10e-126">ThreatIntelligenceUrl</span><span class="sxs-lookup"><span data-stu-id="0f10e-126">ThreatIntelligenceUrl</span></span>|<span data-ttu-id="0f10e-127">Les liens approuvés de blocage et de blocage des liens de Microsoft Defender pour Office 365.</span><span class="sxs-lookup"><span data-stu-id="0f10e-127">Safe Links time-of-block and block override events from Microsoft Defender for Office 365.</span></span>|
|<span data-ttu-id="0f10e-128">47</span><span class="sxs-lookup"><span data-stu-id="0f10e-128">47</span></span>|<span data-ttu-id="0f10e-129">ThreatIntelligenceAtpContent</span><span class="sxs-lookup"><span data-stu-id="0f10e-129">ThreatIntelligenceAtpContent</span></span>|<span data-ttu-id="0f10e-130">Événements de hameçonnage et de programmes malveillants pour les fichiers dans SharePoint Online, OneDrive entreprise et Microsoft Teams, de Microsoft Defender pour Office 365.</span><span class="sxs-lookup"><span data-stu-id="0f10e-130">Phishing and malware events for files in SharePoint Online, OneDrive for Business, and Microsoft Teams, from Microsoft Defender for Office 365.</span></span>|
|<span data-ttu-id="0f10e-131">64</span><span class="sxs-lookup"><span data-stu-id="0f10e-131">64</span></span>|<span data-ttu-id="0f10e-132">AirInvestigation</span><span class="sxs-lookup"><span data-stu-id="0f10e-132">AirInvestigation</span></span>|<span data-ttu-id="0f10e-133">Des événements d’enquête et de réponse automatisés, tels que des détails d’enquête et des artefacts pertinents, de Microsoft Defender pour Office 365 plan 2.</span><span class="sxs-lookup"><span data-stu-id="0f10e-133">Automated investigation and response events, such as investigation details and relevant artifacts, from Microsoft Defender for Office 365 Plan 2.</span></span>|
|

> [!IMPORTANT]
> <span data-ttu-id="0f10e-134">Vous devez être un administrateur général ou avoir le rôle d’administrateur de sécurité attribué pour le centre de sécurité & conformité afin de configurer l’intégration SIEM avec Microsoft Defender pour Office 365.</span><span class="sxs-lookup"><span data-stu-id="0f10e-134">You must be a global administrator or have the security administrator role assigned for the Security & Compliance Center to set up SIEM integration with Microsoft Defender for Office 365.</span></span>
>
> <span data-ttu-id="0f10e-135">La journalisation d’audit doit être activée pour votre environnement Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="0f10e-135">Audit logging must be turned on for your Microsoft 365 environment.</span></span> <span data-ttu-id="0f10e-136">Pour obtenir de l’aide, consultez la rubrique [activer ou désactiver la recherche dans le journal d’audit](../../compliance/turn-audit-log-search-on-or-off.md).</span><span class="sxs-lookup"><span data-stu-id="0f10e-136">To get help with this, see [Turn audit log search on or off](../../compliance/turn-audit-log-search-on-or-off.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="0f10e-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0f10e-137">See also</span></span>

[<span data-ttu-id="0f10e-138">Examen et réponse contre les menaces Office 365</span><span class="sxs-lookup"><span data-stu-id="0f10e-138">Office 365 threat investigation and response</span></span>](office-365-ti.md)

[<span data-ttu-id="0f10e-139">Recherche et réponse automatiques dans Office 365</span><span class="sxs-lookup"><span data-stu-id="0f10e-139">Automated investigation and response (AIR) in Office 365</span></span>](automated-investigation-response-office.md)

