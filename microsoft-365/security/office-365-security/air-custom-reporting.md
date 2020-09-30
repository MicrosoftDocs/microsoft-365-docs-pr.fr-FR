---
title: Utilisation de solutions de création de rapports personnalisées avec une enquête et une réponse automatisées
keywords: SIEM, API, AIR, autoIR, ATP, analyse automatisée, intégration, rapport personnalisé
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
description: Découvrez comment intégrer une enquête et une réponse automatisées à une solution de création de rapports personnalisée ou tierce.
ms.date: 09/29/2020
ms.custom:
- air
ms.openlocfilehash: 08502516ae03dc7c6e7b58aa77939723e7532ef0
ms.sourcegitcommit: 6b1d0bea86ced26cae51695c0077adce8bcff3c4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/30/2020
ms.locfileid: "48308919"
---
# <a name="use-the-management-activity-api-for-custom-or-third-party-reporting-solutions"></a><span data-ttu-id="1151a-104">Utiliser l’API activité de gestion pour les solutions de création de rapports personnalisées ou tierces</span><span class="sxs-lookup"><span data-stu-id="1151a-104">Use the Management Activity API for custom or third-party reporting solutions</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]


<span data-ttu-id="1151a-105">Avec [Microsoft Defender pour Office 365](https://docs.microsoft.com/microsoft-365/security/office-365-security/office-365-atp), vous obtenez des [informations détaillées sur les analyses automatisées](air-view-investigation-results.md).</span><span class="sxs-lookup"><span data-stu-id="1151a-105">With [Microsoft Defender for Office 365](https://docs.microsoft.com/microsoft-365/security/office-365-security/office-365-atp), you get [detailed information about automated investigations](air-view-investigation-results.md).</span></span> <span data-ttu-id="1151a-106">Toutefois, certaines organisations utilisent également une solution de création de rapports personnalisée ou tierce.</span><span class="sxs-lookup"><span data-stu-id="1151a-106">However, some organizations also use a custom or third-party reporting solution.</span></span> <span data-ttu-id="1151a-107">Si votre organisation souhaite intégrer des informations sur des enquêtes automatisées avec une telle solution, vous pouvez utiliser l’API activité de gestion d’Office 365.</span><span class="sxs-lookup"><span data-stu-id="1151a-107">If your organization wants to integrate information about automated investigations with such a solution, you can use the Office 365 Management Activity API.</span></span>

<span data-ttu-id="1151a-108">Pour ce faire, utilisez les ressources suivantes :</span><span class="sxs-lookup"><span data-stu-id="1151a-108">Use the following resources to set this up:</span></span>

****

|<span data-ttu-id="1151a-109">Resource</span><span class="sxs-lookup"><span data-stu-id="1151a-109">Resource</span></span>|<span data-ttu-id="1151a-110">Description</span><span class="sxs-lookup"><span data-stu-id="1151a-110">Description</span></span>|
|---|---|
|[<span data-ttu-id="1151a-111">Vue d’ensemble des API de gestion d’Office 365</span><span class="sxs-lookup"><span data-stu-id="1151a-111">Office 365 Management APIs overview</span></span>](https://docs.microsoft.com/office/office-365-management-api/office-365-management-apis-overview)|<span data-ttu-id="1151a-112">L’API d’activité de gestion d’Office 365 fournit des informations sur les différentes actions et événements d’utilisateur, d’administrateur, de système et de stratégie à partir des journaux d’activité de Microsoft 365 et Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1151a-112">The Office 365 Management Activity API provides information about various user, admin, system, and policy actions and events from Microsoft 365 and Azure Active Directory activity logs.</span></span>|
|[<span data-ttu-id="1151a-113">Prise en main des API de gestion d’Office 365</span><span class="sxs-lookup"><span data-stu-id="1151a-113">Get started with Office 365 Management APIs</span></span>](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis)|<span data-ttu-id="1151a-114">L’API de gestion d’Office 365 utilise Azure AD pour fournir des services d’authentification pour votre application afin d’accéder aux données Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="1151a-114">The Office 365 Management API uses Azure AD to provide authentication services for your application to access Microsoft 365 data.</span></span> <span data-ttu-id="1151a-115">Suivez les étapes décrites dans cet article pour le configurer.</span><span class="sxs-lookup"><span data-stu-id="1151a-115">Follow the steps in this article to set this up.</span></span>|
|[<span data-ttu-id="1151a-116">Référence de l’API Activité de gestion Office 365</span><span class="sxs-lookup"><span data-stu-id="1151a-116">Office 365 Management Activity API reference</span></span>](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference)|<span data-ttu-id="1151a-117">Vous pouvez utiliser l’API activité de gestion d’Office 365 pour récupérer des informations sur les actions et événements d’utilisateur, d’administrateur, de système et de stratégie à partir des journaux d’activité de Microsoft 365 et Azure AD.</span><span class="sxs-lookup"><span data-stu-id="1151a-117">You can use the Office 365 Management Activity API to retrieve information about user, admin, system, and policy actions and events from Microsoft 365 and Azure AD activity logs.</span></span> <span data-ttu-id="1151a-118">Lisez cet article pour en savoir plus sur le fonctionnement de cette procédure.</span><span class="sxs-lookup"><span data-stu-id="1151a-118">Read this article to learn more about how this works.</span></span>|
|[<span data-ttu-id="1151a-119">Schéma de l’API Activité de gestion Office 365</span><span class="sxs-lookup"><span data-stu-id="1151a-119">Office 365 Management Activity API schema</span></span>](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema)|<span data-ttu-id="1151a-120">Pour en savoir plus sur des types de données spécifiques disponibles via l’API activité de gestion Office 365, consultez le schéma [commun](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#common-schema) et le schéma d’enquête et de [réponse aux menaces Office 365](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-investigation-and-response-schema) .</span><span class="sxs-lookup"><span data-stu-id="1151a-120">Get an overview of the [Common schema](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#common-schema) and the [Office 365 ATP and threat investigation and response schema](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-investigation-and-response-schema) to learn about specific kinds of data available through the Office 365 Management Activity API.</span></span>|
|

## <a name="see-also"></a><span data-ttu-id="1151a-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1151a-121">See also</span></span>

- [<span data-ttu-id="1151a-122">Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="1151a-122">Microsoft Defender for Office 365</span></span>](office-365-atp.md)

- [<span data-ttu-id="1151a-123">Recherche et réponse automatisées dans Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="1151a-123">Automated investigation and response in Microsoft 365 Defender</span></span>](https://docs.microsoft.com/microsoft-365/security/mtp/mtp-autoir)
