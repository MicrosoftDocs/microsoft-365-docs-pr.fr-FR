---
title: Intégration DE SIEM à Microsoft Defender pour Office 365
f1.keywords:
- NOCSH
ms.author: deniseb
author: denisebmsft
manager: dansimp
audience: ITPro
ms.topic: article
localization_priority: None
search.appverid:
- MET150
- MOE150
ms.assetid: eb56b69b-3170-4086-82cf-ba40a530fa1b
ms.date: 08/21/2020
ms.collection:
- M365-security-compliance
description: Intégrez le serveur SIEM de votre organisation à Microsoft Defender pour Office 365 et les événements de menace associés dans l’API de gestion des activités Office 365.
ms.custom: seo-marvel-apr2020
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: ca8f86c831df16568ae569e7b21c7e0a33475948
ms.sourcegitcommit: dcb97fbfdae52960ae62b6faa707a05358193ed5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2021
ms.locfileid: "51204064"
---
# <a name="siem-integration-with-microsoft-defender-for-office-365"></a><span data-ttu-id="69ee4-103">Intégration de SIEM à Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="69ee4-103">SIEM integration with Microsoft Defender for Office 365</span></span>

<span data-ttu-id="69ee4-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="69ee4-104">**Applies to**</span></span>
- [<span data-ttu-id="69ee4-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="69ee4-105">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="69ee4-106">Microsoft Defender pour Office 365 : offre 1 et offre 2</span><span class="sxs-lookup"><span data-stu-id="69ee4-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](defender-for-office-365.md)
- [<span data-ttu-id="69ee4-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="69ee4-107">Microsoft 365 Defender</span></span>](../defender/microsoft-365-defender.md)

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


<span data-ttu-id="69ee4-108">Si votre organisation utilise un serveur SIEM (Security Information and Event Management), vous pouvez intégrer Microsoft Defender pour Office 365 à votre serveur SIEM.</span><span class="sxs-lookup"><span data-stu-id="69ee4-108">If your organization is using a security information and event management (SIEM) server, you can integrate Microsoft Defender for Office 365 with your SIEM server.</span></span> <span data-ttu-id="69ee4-109">Vous pouvez configurer cette intégration à l’aide de l’API de gestion des activités [Office 365.](/office/office-365-management-api/office-365-management-activity-api-reference)</span><span class="sxs-lookup"><span data-stu-id="69ee4-109">You can set up this integration by using the [Office 365 Activity Management API](/office/office-365-management-api/office-365-management-activity-api-reference).</span></span>

<span data-ttu-id="69ee4-110">L’intégration SIEM vous permet d’afficher des informations, telles que des programmes malveillants ou des hameçonnages détectés par Microsoft Defender pour Office 365, dans vos rapports de serveur SIEM.</span><span class="sxs-lookup"><span data-stu-id="69ee4-110">SIEM integration enables you to view information, such as malware or phish detected by Microsoft Defender for Office 365, in your SIEM server reports.</span></span>

- <span data-ttu-id="69ee4-111">Pour voir un exemple d’intégration SIEM avec Microsoft Defender pour Office 365, consultez le blog de la communauté technique : Améliorer l’efficacité de votre SOC avec Defender pour Office 365 et l’API de gestion [O365.](https://techcommunity.microsoft.com/t5/microsoft-security-and/improve-the-effectiveness-of-your-soc-with-office-365-atp-and/ba-p/1525185)</span><span class="sxs-lookup"><span data-stu-id="69ee4-111">To see an example of SIEM integration with Microsoft Defender for Office 365, see [Tech Community blog: Improve the Effectiveness of your SOC with Defender for Office 365 and the O365 Management API](https://techcommunity.microsoft.com/t5/microsoft-security-and/improve-the-effectiveness-of-your-soc-with-office-365-atp-and/ba-p/1525185).</span></span>

- <span data-ttu-id="69ee4-112">Pour en savoir plus sur les API de gestion Office 365, consultez la vue d’ensemble des API de [gestion d’Office 365.](/office/office-365-management-api/office-365-management-apis-overview)</span><span class="sxs-lookup"><span data-stu-id="69ee4-112">To learn more about the Office 365 Management APIs, see [Office 365 Management APIs overview](/office/office-365-management-api/office-365-management-apis-overview).</span></span>

## <a name="how-siem-integration-works"></a><span data-ttu-id="69ee4-113">Fonctionnement de l’intégration SIEM</span><span class="sxs-lookup"><span data-stu-id="69ee4-113">How SIEM integration works</span></span>

<span data-ttu-id="69ee4-114">L’API de gestion des activités Office 365 récupère des informations sur les actions et événements des utilisateurs, des administrateurs, du système et des stratégies à partir des journaux d’activité Microsoft 365 et Azure Active Directory de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="69ee4-114">The Office 365 Activity Management API retrieves information about user, admin, system, and policy actions and events from your organization's Microsoft 365 and Azure Active Directory activity logs.</span></span> <span data-ttu-id="69ee4-115">Si votre organisation dispose de Microsoft Defender pour Office 365 Plan 1 ou 2 ou Office 365 E5, vous pouvez utiliser le schéma Microsoft Defender pour [Office 365.](/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-investigation-and-response-schema)</span><span class="sxs-lookup"><span data-stu-id="69ee4-115">If your organization has Microsoft Defender for Office 365 Plan 1 or 2, or Office 365 E5, you can use the [Microsoft Defender for Office 365 schema](/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-investigation-and-response-schema).</span></span>

<span data-ttu-id="69ee4-116">Récemment, les événements des fonctionnalités d’investigation et de réponse automatisées dans Microsoft Defender pour [Office 365 Plan 2](defender-for-office-365.md#microsoft-defender-for-office-365-plan-1-and-plan-2) ont été ajoutés à l’API Activité de gestion Office 365.</span><span class="sxs-lookup"><span data-stu-id="69ee4-116">Recently, events from automated investigation and response capabilities in [Microsoft Defender for Office 365 Plan 2](defender-for-office-365.md#microsoft-defender-for-office-365-plan-1-and-plan-2) were added to the Office 365 Management Activity API.</span></span> <span data-ttu-id="69ee4-117">En plus d’inclure des données sur les détails d’investigation principaux tels que l’ID, le nom et l’état, l’API contient également des informations de haut niveau sur les actions d’investigation et les entités.</span><span class="sxs-lookup"><span data-stu-id="69ee4-117">In addition to including data about core investigation details such as ID, name and status, the API also contains high-level information about investigation actions and entities.</span></span>

<span data-ttu-id="69ee4-118">Le serveur SIEM ou un autre système similaire sonde la charge de travail **audit.general** pour accéder aux événements de détection.</span><span class="sxs-lookup"><span data-stu-id="69ee4-118">The SIEM server or other similar system polls the **audit.general** workload to access detection events.</span></span> <span data-ttu-id="69ee4-119">Pour en savoir plus, consultez La prise en charge des API de gestion [d’Office 365.](/office/office-365-management-api/get-started-with-office-365-management-apis)</span><span class="sxs-lookup"><span data-stu-id="69ee4-119">To learn more, see [Get started with Office 365 Management APIs](/office/office-365-management-api/get-started-with-office-365-management-apis).</span></span>

## <a name="enum-auditlogrecordtype---type-edmint32"></a><span data-ttu-id="69ee4-120">Énumération : AuditLogRecordType - Type : Edm.Int32</span><span class="sxs-lookup"><span data-stu-id="69ee4-120">Enum: AuditLogRecordType - Type: Edm.Int32</span></span>

### <a name="auditlogrecordtype"></a><span data-ttu-id="69ee4-121">AuditLogRecordType</span><span class="sxs-lookup"><span data-stu-id="69ee4-121">AuditLogRecordType</span></span>

<span data-ttu-id="69ee4-122">Le tableau suivant récapitule les valeurs **d’AuditLogRecordType** pertinentes pour les événements Microsoft Defender pour Office 365 :</span><span class="sxs-lookup"><span data-stu-id="69ee4-122">The following table summarizes the values of **AuditLogRecordType** that are relevant for Microsoft Defender for Office 365 events:</span></span>

|<span data-ttu-id="69ee4-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="69ee4-123">Value</span></span>|<span data-ttu-id="69ee4-124">Nom du membre</span><span class="sxs-lookup"><span data-stu-id="69ee4-124">Member name</span></span>|<span data-ttu-id="69ee4-125">Description</span><span class="sxs-lookup"><span data-stu-id="69ee4-125">Description</span></span>|
|---|---|---|
|<span data-ttu-id="69ee4-126">28</span><span class="sxs-lookup"><span data-stu-id="69ee4-126">28</span></span>|<span data-ttu-id="69ee4-127">ThreatIntelligence</span><span class="sxs-lookup"><span data-stu-id="69ee4-127">ThreatIntelligence</span></span>|<span data-ttu-id="69ee4-128">Événements de hameçonnage et de programmes malveillants depuis Exchange Online Protection et Microsoft Defender pour Office 365.</span><span class="sxs-lookup"><span data-stu-id="69ee4-128">Phishing and malware events from Exchange Online Protection and Microsoft Defender for Office 365.</span></span>|
|<span data-ttu-id="69ee4-129">41</span><span class="sxs-lookup"><span data-stu-id="69ee4-129">41</span></span>|<span data-ttu-id="69ee4-130">ThreatIntelligenceUrl</span><span class="sxs-lookup"><span data-stu-id="69ee4-130">ThreatIntelligenceUrl</span></span>|<span data-ttu-id="69ee4-131">Événements de remplacement de la durée de blocage et du blocage des liens sécurisés à partir de Microsoft Defender pour Office 365.</span><span class="sxs-lookup"><span data-stu-id="69ee4-131">Safe Links time-of-block and block override events from Microsoft Defender for Office 365.</span></span>|
|<span data-ttu-id="69ee4-132">47</span><span class="sxs-lookup"><span data-stu-id="69ee4-132">47</span></span>|<span data-ttu-id="69ee4-133">ThreatIntelligenceAtpContent</span><span class="sxs-lookup"><span data-stu-id="69ee4-133">ThreatIntelligenceAtpContent</span></span>|<span data-ttu-id="69ee4-134">Événements de hameçonnage et de programmes malveillants pour les fichiers dans SharePoint Online, OneDrive Entreprise et Microsoft Teams, à partir de Microsoft Defender pour Office 365.</span><span class="sxs-lookup"><span data-stu-id="69ee4-134">Phishing and malware events for files in SharePoint Online, OneDrive for Business, and Microsoft Teams, from Microsoft Defender for Office 365.</span></span>|
|<span data-ttu-id="69ee4-135">64</span><span class="sxs-lookup"><span data-stu-id="69ee4-135">64</span></span>|<span data-ttu-id="69ee4-136">AirInvestigation</span><span class="sxs-lookup"><span data-stu-id="69ee4-136">AirInvestigation</span></span>|<span data-ttu-id="69ee4-137">Événements d’investigation et de réponse automatisés, tels que les détails de l’enquête et les artefacts pertinents, de Microsoft Defender pour Office 365 Plan 2.</span><span class="sxs-lookup"><span data-stu-id="69ee4-137">Automated investigation and response events, such as investigation details and relevant artifacts, from Microsoft Defender for Office 365 Plan 2.</span></span>|
|

> [!IMPORTANT]
> <span data-ttu-id="69ee4-138">Vous devez être un administrateur général ou avoir le rôle d’administrateur de la sécurité attribué au Centre de sécurité & conformité pour configurer l’intégration SIEM avec Microsoft Defender pour Office 365.</span><span class="sxs-lookup"><span data-stu-id="69ee4-138">You must be a global administrator or have the security administrator role assigned for the Security & Compliance Center to set up SIEM integration with Microsoft Defender for Office 365.</span></span>
>
> <span data-ttu-id="69ee4-139">La journalisation d’audit doit être allumée pour votre environnement Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="69ee4-139">Audit logging must be turned on for your Microsoft 365 environment.</span></span> <span data-ttu-id="69ee4-140">Pour obtenir de l’aide, voir Activer ou désactiver la recherche dans le journal [d’audit.](../../compliance/turn-audit-log-search-on-or-off.md)</span><span class="sxs-lookup"><span data-stu-id="69ee4-140">To get help with this, see [Turn audit log search on or off](../../compliance/turn-audit-log-search-on-or-off.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="69ee4-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="69ee4-141">See also</span></span>

[<span data-ttu-id="69ee4-142">Examen et réponse contre les menaces Office 365</span><span class="sxs-lookup"><span data-stu-id="69ee4-142">Office 365 threat investigation and response</span></span>](office-365-ti.md)

[<span data-ttu-id="69ee4-143">Examen et réponse automatisés (AIR) dans Office 365</span><span class="sxs-lookup"><span data-stu-id="69ee4-143">Automated investigation and response (AIR) in Office 365</span></span>](automated-investigation-response-office.md)