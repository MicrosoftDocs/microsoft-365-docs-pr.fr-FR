---
title: Solutions de création de rapports personnalisées avec examen et réponse automatisés
keywords: SIEM, API, AIR, autoIR, Microsoft Defender pour point de terminaison, examen automatisé, intégration, rapport personnalisé
f1.keywords:
- NOCSH
author: JoeDavies-MSFT
ms.author: josephd
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
ms.openlocfilehash: 6ed752f9514f1d2c8cadeb7cbbd1d7b9311b1b5f
ms.sourcegitcommit: 51b316c23e070ab402a687f927e8fa01cb719c74
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2021
ms.locfileid: "52275011"
---
# <a name="custom-or-third-party-reporting-solutions-for-microsoft-defender-for-office-365"></a><span data-ttu-id="ee969-104">Solutions de création de rapports personnalisées ou tierces pour Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="ee969-104">Custom or third-party reporting solutions for Microsoft Defender for Office 365</span></span>

<span data-ttu-id="ee969-105">Avec [Microsoft Defender pour Office 365,](defender-for-office-365.md)vous obtenez des informations détaillées sur les [enquêtes automatisées.](air-view-investigation-results.md)</span><span class="sxs-lookup"><span data-stu-id="ee969-105">With [Microsoft Defender for Office 365](defender-for-office-365.md), you get [detailed information about automated investigations](air-view-investigation-results.md).</span></span> <span data-ttu-id="ee969-106">Toutefois, certaines organisations utilisent également une solution de création de rapports personnalisée ou tierce.</span><span class="sxs-lookup"><span data-stu-id="ee969-106">However, some organizations also use a custom or third-party reporting solution.</span></span> <span data-ttu-id="ee969-107">Si votre organisation souhaite intégrer des informations sur les [enquêtes](office-365-air.md) automatisées à une telle solution, vous pouvez utiliser l’API activité Office 365 gestion.</span><span class="sxs-lookup"><span data-stu-id="ee969-107">If your organization wants to integrate information about [automated investigations](office-365-air.md) with such a solution, you can use the Office 365 Management Activity API.</span></span>

<span data-ttu-id="ee969-108">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="ee969-108">**Applies to**</span></span>
- [<span data-ttu-id="ee969-109">Microsoft Defender pour Office 365 Plan 2</span><span class="sxs-lookup"><span data-stu-id="ee969-109">Microsoft Defender for Office 365 plan 2</span></span>](defender-for-office-365.md)
- [<span data-ttu-id="ee969-110">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="ee969-110">Microsoft 365 Defender</span></span>](../defender/microsoft-365-defender.md)

<span data-ttu-id="ee969-111">Avec [Microsoft Defender pour Office 365,](defender-for-office-365.md)vous obtenez des informations détaillées sur les [enquêtes automatisées.](air-view-investigation-results.md)</span><span class="sxs-lookup"><span data-stu-id="ee969-111">With [Microsoft Defender for Office 365](defender-for-office-365.md), you get [detailed information about automated investigations](air-view-investigation-results.md).</span></span> <span data-ttu-id="ee969-112">Toutefois, certaines organisations utilisent également une solution de création de rapports personnalisée ou tierce.</span><span class="sxs-lookup"><span data-stu-id="ee969-112">However, some organizations also use a custom or third-party reporting solution.</span></span> <span data-ttu-id="ee969-113">Si votre organisation souhaite intégrer des informations sur les enquêtes automatisées à une telle solution, vous pouvez utiliser l’API activité Office 365 gestion.</span><span class="sxs-lookup"><span data-stu-id="ee969-113">If your organization wants to integrate information about automated investigations with such a solution, you can use the Office 365 Management Activity API.</span></span>

|<span data-ttu-id="ee969-114">Resource</span><span class="sxs-lookup"><span data-stu-id="ee969-114">Resource</span></span>|<span data-ttu-id="ee969-115">Description</span><span class="sxs-lookup"><span data-stu-id="ee969-115">Description</span></span>|
|:---|:---|
|[<span data-ttu-id="ee969-116">Vue d’ensemble des API de gestion d’Office 365</span><span class="sxs-lookup"><span data-stu-id="ee969-116">Office 365 Management APIs overview</span></span>](/office/office-365-management-api/office-365-management-apis-overview)|<span data-ttu-id="ee969-117">L’API activité de gestion Office 365 fournit des informations sur diverses actions et événements d’utilisateur, d’administrateur, de système et de stratégie à partir Microsoft 365 et Azure Active Directory journaux d’activité.</span><span class="sxs-lookup"><span data-stu-id="ee969-117">The Office 365 Management Activity API provides information about various user, admin, system, and policy actions and events from Microsoft 365 and Azure Active Directory activity logs.</span></span>|
|[<span data-ttu-id="ee969-118">Prise en main des API de gestion d’Office 365</span><span class="sxs-lookup"><span data-stu-id="ee969-118">Get started with Office 365 Management APIs</span></span>](/office/office-365-management-api/get-started-with-office-365-management-apis)|<span data-ttu-id="ee969-119">L’API Office 365 gestion des données utilise Azure AD pour fournir des services d’authentification permettant à votre application d’accéder Microsoft 365 données.</span><span class="sxs-lookup"><span data-stu-id="ee969-119">The Office 365 Management API uses Azure AD to provide authentication services for your application to access Microsoft 365 data.</span></span> <span data-ttu-id="ee969-120">Suivez les étapes de cet article pour le configurer.</span><span class="sxs-lookup"><span data-stu-id="ee969-120">Follow the steps in this article to set this up.</span></span>|
|[<span data-ttu-id="ee969-121">Référence de l’API Activité de gestion Office 365</span><span class="sxs-lookup"><span data-stu-id="ee969-121">Office 365 Management Activity API reference</span></span>](/office/office-365-management-api/office-365-management-activity-api-reference)|<span data-ttu-id="ee969-122">Vous pouvez utiliser l’API activité de gestion Office 365 pour récupérer des informations sur les actions et événements des utilisateurs, des administrateurs, du système et des stratégies à partir des journaux d’activité Microsoft 365 et Azure AD.</span><span class="sxs-lookup"><span data-stu-id="ee969-122">You can use the Office 365 Management Activity API to retrieve information about user, admin, system, and policy actions and events from Microsoft 365 and Azure AD activity logs.</span></span> <span data-ttu-id="ee969-123">Lisez cet article pour en savoir plus sur son fonctionnement.</span><span class="sxs-lookup"><span data-stu-id="ee969-123">Read this article to learn more about how this works.</span></span>|
|[<span data-ttu-id="ee969-124">Schéma de l’API Activité de gestion Office 365</span><span class="sxs-lookup"><span data-stu-id="ee969-124">Office 365 Management Activity API schema</span></span>](/office/office-365-management-api/office-365-management-activity-api-schema)|<span data-ttu-id="ee969-125">Obtenez une vue [](/office/office-365-management-api/office-365-management-activity-api-schema#common-schema) d’ensemble du schéma commun et du schéma Defender [pour Office 365](/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-investigation-and-response-schema) et de l’examen des menaces et du schéma de réponse pour en savoir plus sur les types de données spécifiques disponibles via l’API activité de gestion Office 365.</span><span class="sxs-lookup"><span data-stu-id="ee969-125">Get an overview of the [Common schema](/office/office-365-management-api/office-365-management-activity-api-schema#common-schema) and the [Defender for Office 365 and threat investigation and response schema](/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-investigation-and-response-schema) to learn about specific kinds of data available through the Office 365 Management Activity API.</span></span>|
|

## <a name="see-also"></a><span data-ttu-id="ee969-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ee969-126">See also</span></span>

- [<span data-ttu-id="ee969-127">Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="ee969-127">Microsoft Defender for Office 365</span></span>](defender-for-office-365.md)
- [<span data-ttu-id="ee969-128">Examen et réponse automatisés dans Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="ee969-128">Automated investigation and response in Microsoft 365 Defender</span></span>](/microsoft-365/security/defender/m365d-autoir)
