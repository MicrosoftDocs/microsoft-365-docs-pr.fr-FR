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
description: Découvrez comment intégrer des enquêtes et des réponses automatisées à une solution de création de rapports personnalisée ou tierce.
ms.date: 01/29/2021
ms.custom:
- air
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 82f3b38e5b6e31313c94f5ac389e883f6b076540
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51065633"
---
# <a name="custom-or-third-party-reporting-solutions-for-microsoft-defender-for-office-365"></a><span data-ttu-id="37852-104">Solutions de création de rapports personnalisées ou tierces pour Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="37852-104">Custom or third-party reporting solutions for Microsoft Defender for Office 365</span></span>

<span data-ttu-id="37852-105">Avec [Microsoft Defender pour Office 365,](defender-for-office-365.md)vous obtenez des informations détaillées sur les [enquêtes automatisées.](air-view-investigation-results.md)</span><span class="sxs-lookup"><span data-stu-id="37852-105">With [Microsoft Defender for Office 365](defender-for-office-365.md), you get [detailed information about automated investigations](air-view-investigation-results.md).</span></span> <span data-ttu-id="37852-106">Toutefois, certaines organisations utilisent également une solution de création de rapports personnalisée ou tierce.</span><span class="sxs-lookup"><span data-stu-id="37852-106">However, some organizations also use a custom or third-party reporting solution.</span></span> <span data-ttu-id="37852-107">Si votre organisation souhaite intégrer des informations sur les [enquêtes](office-365-air.md) automatisées à une telle solution, vous pouvez utiliser l’API Activité de gestion Office 365.</span><span class="sxs-lookup"><span data-stu-id="37852-107">If your organization wants to integrate information about [automated investigations](office-365-air.md) with such a solution, you can use the Office 365 Management Activity API.</span></span>

<span data-ttu-id="37852-108">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="37852-108">**Applies to**</span></span>
- [<span data-ttu-id="37852-109">Microsoft Defender pour Office 365 Plan 2</span><span class="sxs-lookup"><span data-stu-id="37852-109">Microsoft Defender for Office 365 plan 2</span></span>](defender-for-office-365.md)
- [<span data-ttu-id="37852-110">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="37852-110">Microsoft 365 Defender</span></span>](../defender/microsoft-365-defender.md)

<span data-ttu-id="37852-111">Avec [Microsoft Defender pour Office 365,](defender-for-office-365.md)vous obtenez des informations détaillées sur les [enquêtes automatisées.](air-view-investigation-results.md)</span><span class="sxs-lookup"><span data-stu-id="37852-111">With [Microsoft Defender for Office 365](defender-for-office-365.md), you get [detailed information about automated investigations](air-view-investigation-results.md).</span></span> <span data-ttu-id="37852-112">Toutefois, certaines organisations utilisent également une solution de création de rapports personnalisée ou tierce.</span><span class="sxs-lookup"><span data-stu-id="37852-112">However, some organizations also use a custom or third-party reporting solution.</span></span> <span data-ttu-id="37852-113">Si votre organisation souhaite intégrer des informations sur les enquêtes automatisées à une telle solution, vous pouvez utiliser l’API Activité de gestion Office 365.</span><span class="sxs-lookup"><span data-stu-id="37852-113">If your organization wants to integrate information about automated investigations with such a solution, you can use the Office 365 Management Activity API.</span></span>

|<span data-ttu-id="37852-114">Resource</span><span class="sxs-lookup"><span data-stu-id="37852-114">Resource</span></span>|<span data-ttu-id="37852-115">Description</span><span class="sxs-lookup"><span data-stu-id="37852-115">Description</span></span>|
|:---|:---|
|[<span data-ttu-id="37852-116">Vue d’ensemble des API de gestion d’Office 365</span><span class="sxs-lookup"><span data-stu-id="37852-116">Office 365 Management APIs overview</span></span>](/office/office-365-management-api/office-365-management-apis-overview)|<span data-ttu-id="37852-117">L’API Activité de gestion Office 365 fournit des informations sur diverses actions et événements d’utilisateur, d’administrateur, de système et de stratégie à partir des journaux d’activité Microsoft 365 et Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="37852-117">The Office 365 Management Activity API provides information about various user, admin, system, and policy actions and events from Microsoft 365 and Azure Active Directory activity logs.</span></span>|
|[<span data-ttu-id="37852-118">Prise en main des API de gestion d’Office 365</span><span class="sxs-lookup"><span data-stu-id="37852-118">Get started with Office 365 Management APIs</span></span>](/office/office-365-management-api/get-started-with-office-365-management-apis)|<span data-ttu-id="37852-119">L’API de gestion Office 365 utilise Azure AD pour fournir des services d’authentification pour que votre application accède aux données Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="37852-119">The Office 365 Management API uses Azure AD to provide authentication services for your application to access Microsoft 365 data.</span></span> <span data-ttu-id="37852-120">Suivez les étapes de cet article pour le configurer.</span><span class="sxs-lookup"><span data-stu-id="37852-120">Follow the steps in this article to set this up.</span></span>|
|[<span data-ttu-id="37852-121">Référence de l’API Activité de gestion Office 365</span><span class="sxs-lookup"><span data-stu-id="37852-121">Office 365 Management Activity API reference</span></span>](/office/office-365-management-api/office-365-management-activity-api-reference)|<span data-ttu-id="37852-122">Vous pouvez utiliser l’API Activité de gestion Office 365 pour récupérer des informations sur les actions et événements des utilisateurs, des administrateurs, du système et des stratégies à partir des journaux d’activité Microsoft 365 et Azure AD.</span><span class="sxs-lookup"><span data-stu-id="37852-122">You can use the Office 365 Management Activity API to retrieve information about user, admin, system, and policy actions and events from Microsoft 365 and Azure AD activity logs.</span></span> <span data-ttu-id="37852-123">Lisez cet article pour en savoir plus sur son fonctionnement.</span><span class="sxs-lookup"><span data-stu-id="37852-123">Read this article to learn more about how this works.</span></span>|
|[<span data-ttu-id="37852-124">Schéma de l’API Activité de gestion Office 365</span><span class="sxs-lookup"><span data-stu-id="37852-124">Office 365 Management Activity API schema</span></span>](/office/office-365-management-api/office-365-management-activity-api-schema)|<span data-ttu-id="37852-125">Obtenez une vue [](/office/office-365-management-api/office-365-management-activity-api-schema#common-schema) d’ensemble du schéma commun et de Defender pour [Office 365,](/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-investigation-and-response-schema) ainsi que du schéma d’examen et de réponse aux menaces pour en savoir plus sur les types de données spécifiques disponibles via l’API Activité de gestion Office 365.</span><span class="sxs-lookup"><span data-stu-id="37852-125">Get an overview of the [Common schema](/office/office-365-management-api/office-365-management-activity-api-schema#common-schema) and the [Defender for Office 365 and threat investigation and response schema](/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-investigation-and-response-schema) to learn about specific kinds of data available through the Office 365 Management Activity API.</span></span>|
|

## <a name="see-also"></a><span data-ttu-id="37852-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="37852-126">See also</span></span>

- [<span data-ttu-id="37852-127">Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="37852-127">Microsoft Defender for Office 365</span></span>](defender-for-office-365.md)
- [<span data-ttu-id="37852-128">Examen et réponse automatisés dans Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="37852-128">Automated investigation and response in Microsoft 365 Defender</span></span>](/microsoft-365/security/defender/m365d-autoir)
