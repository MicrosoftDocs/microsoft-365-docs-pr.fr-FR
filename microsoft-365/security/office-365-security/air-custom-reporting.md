---
title: Solutions de création de rapports personnalisées avec examen et réponse automatisés
keywords: SIEM, API, AIR, autoIR, ATP, examen automatisé, intégration, rapport personnalisé
f1.keywords:
- NOCSH
ms.author: deniseb
author: denisebmsft
manager: dansimp
audience: ITPro
ms.topic: article
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.collection:
- M365-security-compliance
- m365initiative-defender-office365
description: Découvrez comment intégrer un examen et une réponse automatisés à une solution de création de rapports personnalisée ou tierce.
ms.date: 01/29/2021
ms.custom:
- air
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 13782a8e0a8c691a66f214d3f9f03ef9cad4da1f
ms.sourcegitcommit: 786f90a163d34c02b8451d09aa1efb1e1d5f543c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/18/2021
ms.locfileid: "50287136"
---
# <a name="custom-or-third-party-reporting-solutions-for-microsoft-defender-for-office-365"></a><span data-ttu-id="bc8a8-104">Solutions de création de rapports personnalisées ou tierces pour Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="bc8a8-104">Custom or third-party reporting solutions for Microsoft Defender for Office 365</span></span>

<span data-ttu-id="bc8a8-105">Avec [Microsoft Defender pour Office 365,](office-365-atp.md)vous obtenez des informations détaillées sur les [enquêtes automatisées.](air-view-investigation-results.md)</span><span class="sxs-lookup"><span data-stu-id="bc8a8-105">With [Microsoft Defender for Office 365](office-365-atp.md), you get [detailed information about automated investigations](air-view-investigation-results.md).</span></span> <span data-ttu-id="bc8a8-106">Toutefois, certaines organisations utilisent également une solution de création de rapports personnalisée ou tierce.</span><span class="sxs-lookup"><span data-stu-id="bc8a8-106">However, some organizations also use a custom or third-party reporting solution.</span></span> <span data-ttu-id="bc8a8-107">Si votre organisation souhaite intégrer des informations sur les [enquêtes](office-365-air.md) automatisées à une telle solution, vous pouvez utiliser l’API Activité de gestion Office 365.</span><span class="sxs-lookup"><span data-stu-id="bc8a8-107">If your organization wants to integrate information about [automated investigations](office-365-air.md) with such a solution, you can use the Office 365 Management Activity API.</span></span>

<span data-ttu-id="bc8a8-108">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="bc8a8-108">**Applies to**</span></span>
- [<span data-ttu-id="bc8a8-109">Microsoft Defender pour Office 365 Plan 2</span><span class="sxs-lookup"><span data-stu-id="bc8a8-109">Microsoft Defender for Office 365 plan 2</span></span>](office-365-atp.md)
- [<span data-ttu-id="bc8a8-110">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="bc8a8-110">Microsoft 365 Defender</span></span>](../mtp/microsoft-threat-protection.md)

<span data-ttu-id="bc8a8-111">Avec [Microsoft Defender pour Office 365,](office-365-atp.md)vous obtenez des informations détaillées sur les [enquêtes automatisées.](air-view-investigation-results.md)</span><span class="sxs-lookup"><span data-stu-id="bc8a8-111">With [Microsoft Defender for Office 365](office-365-atp.md), you get [detailed information about automated investigations](air-view-investigation-results.md).</span></span> <span data-ttu-id="bc8a8-112">Toutefois, certaines organisations utilisent également une solution de création de rapports personnalisée ou tierce.</span><span class="sxs-lookup"><span data-stu-id="bc8a8-112">However, some organizations also use a custom or third-party reporting solution.</span></span> <span data-ttu-id="bc8a8-113">Si votre organisation souhaite intégrer des informations sur les enquêtes automatisées à une telle solution, vous pouvez utiliser l’API Activité de gestion Office 365.</span><span class="sxs-lookup"><span data-stu-id="bc8a8-113">If your organization wants to integrate information about automated investigations with such a solution, you can use the Office 365 Management Activity API.</span></span>

|<span data-ttu-id="bc8a8-114">Ressource</span><span class="sxs-lookup"><span data-stu-id="bc8a8-114">Resource</span></span>|<span data-ttu-id="bc8a8-115">Description</span><span class="sxs-lookup"><span data-stu-id="bc8a8-115">Description</span></span>|
|:---|:---|
|[<span data-ttu-id="bc8a8-116">Vue d’ensemble des API de gestion d’Office 365</span><span class="sxs-lookup"><span data-stu-id="bc8a8-116">Office 365 Management APIs overview</span></span>](https://docs.microsoft.com/office/office-365-management-api/office-365-management-apis-overview)|<span data-ttu-id="bc8a8-117">L’API Activité de gestion Office 365 fournit des informations sur diverses actions et événements d’utilisateur, d’administrateur, de système et de stratégie à partir des journaux d’activité Microsoft 365 et Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="bc8a8-117">The Office 365 Management Activity API provides information about various user, admin, system, and policy actions and events from Microsoft 365 and Azure Active Directory activity logs.</span></span>|
|[<span data-ttu-id="bc8a8-118">Prise en main des API de gestion d’Office 365</span><span class="sxs-lookup"><span data-stu-id="bc8a8-118">Get started with Office 365 Management APIs</span></span>](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis)|<span data-ttu-id="bc8a8-119">L’API de gestion Office 365 utilise Azure AD pour fournir des services d’authentification pour que votre application accède aux données Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="bc8a8-119">The Office 365 Management API uses Azure AD to provide authentication services for your application to access Microsoft 365 data.</span></span> <span data-ttu-id="bc8a8-120">Suivez les étapes de cet article pour le configurer.</span><span class="sxs-lookup"><span data-stu-id="bc8a8-120">Follow the steps in this article to set this up.</span></span>|
|[<span data-ttu-id="bc8a8-121">Référence de l’API Activité de gestion Office 365</span><span class="sxs-lookup"><span data-stu-id="bc8a8-121">Office 365 Management Activity API reference</span></span>](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference)|<span data-ttu-id="bc8a8-122">Vous pouvez utiliser l’API Activité de gestion Office 365 pour récupérer des informations sur les actions et événements des utilisateurs, des administrateurs, du système et des stratégies à partir des journaux d’activité Microsoft 365 et Azure AD.</span><span class="sxs-lookup"><span data-stu-id="bc8a8-122">You can use the Office 365 Management Activity API to retrieve information about user, admin, system, and policy actions and events from Microsoft 365 and Azure AD activity logs.</span></span> <span data-ttu-id="bc8a8-123">Lisez cet article pour en savoir plus sur son fonctionnement.</span><span class="sxs-lookup"><span data-stu-id="bc8a8-123">Read this article to learn more about how this works.</span></span>|
|[<span data-ttu-id="bc8a8-124">Schéma de l’API Activité de gestion Office 365</span><span class="sxs-lookup"><span data-stu-id="bc8a8-124">Office 365 Management Activity API schema</span></span>](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema)|<span data-ttu-id="bc8a8-125">Obtenez une vue [](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#common-schema) d’ensemble du schéma commun et de Defender pour [Office 365,](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-investigation-and-response-schema) ainsi que du schéma d’examen et de réponse aux menaces pour en savoir plus sur des types spécifiques de données disponibles via l’API Activité de gestion Office 365.</span><span class="sxs-lookup"><span data-stu-id="bc8a8-125">Get an overview of the [Common schema](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#common-schema) and the [Defender for Office 365 and threat investigation and response schema](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-investigation-and-response-schema) to learn about specific kinds of data available through the Office 365 Management Activity API.</span></span>|
|

## <a name="see-also"></a><span data-ttu-id="bc8a8-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bc8a8-126">See also</span></span>

- [<span data-ttu-id="bc8a8-127">Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="bc8a8-127">Microsoft Defender for Office 365</span></span>](office-365-atp.md)
- [<span data-ttu-id="bc8a8-128">Examen et réponse automatisés dans Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="bc8a8-128">Automated investigation and response in Microsoft 365 Defender</span></span>](../mtp/mtp-autoir.md)
