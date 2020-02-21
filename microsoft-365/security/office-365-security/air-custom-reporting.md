---
title: Utilisation de solutions de création de rapports personnalisées avec une enquête et une réponse automatiques dans Office 365
keywords: AIR, autoIR, ATP, automatisation, analyse, réponse, correction, menaces, avancé, menace, protection
f1.keywords:
- NOCSH
ms.author: deniseb
author: denisebmsft
manager: dansimp
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.collection: M365-security-compliance
description: Découvrez comment intégrer une enquête et une réponse automatisées Office 365 avec une solution de création de rapports personnalisée ou tierce.
ms.openlocfilehash: 3df69c9118b3170924a99a1787761b1bb07aadfa
ms.sourcegitcommit: 2f117a6fd27a097ca25afa933dd088b69d483974
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "42175920"
---
# <a name="use-the-office-365-management-activity-api-for-custom-or-third-party-reporting-solutions"></a><span data-ttu-id="de827-104">Utiliser l’API activité de gestion d’Office 365 pour des solutions de création de rapports personnalisées ou tierces</span><span class="sxs-lookup"><span data-stu-id="de827-104">Use the Office 365 Management Activity API for custom or third-party reporting solutions</span></span>

<span data-ttu-id="de827-105">Avec [Office 365 Advanced Threat Protection](https://docs.microsoft.com/microsoft-365/security/office-365-security/office-365-atp), vous obtenez des [informations détaillées sur les analyses automatisées](air-view-investigation-results.md).</span><span class="sxs-lookup"><span data-stu-id="de827-105">With [Office 365 Advanced Threat Protection](https://docs.microsoft.com/microsoft-365/security/office-365-security/office-365-atp), you get [detailed information about automated investigations](air-view-investigation-results.md).</span></span> <span data-ttu-id="de827-106">Toutefois, certaines organisations utilisent également une solution de création de rapports personnalisée ou tierce.</span><span class="sxs-lookup"><span data-stu-id="de827-106">However, some organizations also use a custom or third-party reporting solution.</span></span> <span data-ttu-id="de827-107">Si votre organisation souhaite intégrer des informations sur des enquêtes automatisées avec une telle solution, vous pouvez utiliser l’API activité de gestion d’Office 365.</span><span class="sxs-lookup"><span data-stu-id="de827-107">If your organization wants to integrate information about automated investigations with such a solution, you can use the Office 365 Management Activity API.</span></span>

<span data-ttu-id="de827-108">Pour ce faire, utilisez les ressources suivantes :</span><span class="sxs-lookup"><span data-stu-id="de827-108">Use the following resources to set this up:</span></span>

|<span data-ttu-id="de827-109">Resource</span><span class="sxs-lookup"><span data-stu-id="de827-109">Resource</span></span>  |<span data-ttu-id="de827-110">Description</span><span class="sxs-lookup"><span data-stu-id="de827-110">Description</span></span>  |
|---------|---------|
|[<span data-ttu-id="de827-111">Vue d’ensemble des API de gestion d’Office 365</span><span class="sxs-lookup"><span data-stu-id="de827-111">Office 365 Management APIs overview</span></span>](https://docs.microsoft.com/office/office-365-management-api/office-365-management-apis-overview)     |<span data-ttu-id="de827-112">L’API Activité de gestion Office 365 fournit des informations sur diverses actions et événements d’utilisateur, d’administrateur, de système et de stratégie à partir des journaux d’activité Office 365 et Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="de827-112">The Office 365 Management Activity API provides information about various user, admin, system, and policy actions and events from Office 365 and Azure Active Directory activity logs.</span></span>         |
|[<span data-ttu-id="de827-113">Prise en main des API de gestion d’Office 365</span><span class="sxs-lookup"><span data-stu-id="de827-113">Get started with Office 365 Management APIs</span></span>](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis)     |<span data-ttu-id="de827-114">L’API de gestion d’Office 365 utilise Azure AD pour fournir des services d’authentification à votre application pour accéder aux données d’Office 365.</span><span class="sxs-lookup"><span data-stu-id="de827-114">The Office 365 Management API uses Azure AD to provide authentication services for your application to access Office 365 data.</span></span> <span data-ttu-id="de827-115">Suivez les étapes décrites dans cet article pour le configurer.</span><span class="sxs-lookup"><span data-stu-id="de827-115">Follow the steps in this article to set this up.</span></span>          |
|[<span data-ttu-id="de827-116">Référence de l’API Activité de gestion Office 365</span><span class="sxs-lookup"><span data-stu-id="de827-116">Office 365 Management Activity API reference</span></span>](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference)     |<span data-ttu-id="de827-117">Vous pouvez utiliser l’API activité de gestion d’Office 365 pour récupérer des informations sur les actions et événements d’utilisateur, d’administrateur, de système et de stratégie à partir des journaux d’activité Office 365 et Azure AD.</span><span class="sxs-lookup"><span data-stu-id="de827-117">You can use the Office 365 Management Activity API to retrieve information about user, admin, system, and policy actions and events from Office 365 and Azure AD activity logs.</span></span> <span data-ttu-id="de827-118">Lisez cet article pour en savoir plus sur le fonctionnement de cette procédure.</span><span class="sxs-lookup"><span data-stu-id="de827-118">Read this article to learn more about how this works.</span></span>        |
|[<span data-ttu-id="de827-119">Schéma de l’API Activité de gestion Office 365</span><span class="sxs-lookup"><span data-stu-id="de827-119">Office 365 Management Activity API schema</span></span>](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema)     |<span data-ttu-id="de827-120">Pour en savoir plus sur des types de données spécifiques disponibles via l’API activité de gestion Office 365, consultez le schéma [commun](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#common-schema) et le schéma d’enquête et de [réponse aux menaces Office 365](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-investigation-and-response-schema) .</span><span class="sxs-lookup"><span data-stu-id="de827-120">Get an overview of the [Common schema](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#common-schema) and the [Office 365 ATP and threat investigation and response schema](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-investigation-and-response-schema) to learn about specific kinds of data available through the Office 365 Management Activity API.</span></span>         |

## <a name="related-articles"></a><span data-ttu-id="de827-121">Articles connexes</span><span class="sxs-lookup"><span data-stu-id="de827-121">Related articles</span></span>

- [<span data-ttu-id="de827-122">Protection avancée contre les menaces dans Office 365</span><span class="sxs-lookup"><span data-stu-id="de827-122">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)

- [<span data-ttu-id="de827-123">En savoir plus sur l’analyse et la réponse automatisées dans Microsoft Threat Protection</span><span class="sxs-lookup"><span data-stu-id="de827-123">Learn about automated investigation and response in Microsoft Threat Protection</span></span>](https://docs.microsoft.com/microsoft-365/security/mtp/mtp-autoir)