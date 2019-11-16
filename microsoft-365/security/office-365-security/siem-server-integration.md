---
title: Intégration de serveur SIEM aux services et applications Microsoft 365
ms.author: deniseb
author: denisebmsft
manager: dansimp
audience: ITPro
ms.topic: article
ms.date: 11/15/2019
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
ms.custom:
- Ent_Solutions
- SIEM
description: Lisez cet article pour obtenir une vue d’ensemble de l’intégration de serveur SIEM à Microsoft 365.
ms.openlocfilehash: bea6141022fef1275a7e291217f698f52613f170
ms.sourcegitcommit: d8d001c03c28c10bea005d1c9b5f4a8f393af706
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/16/2019
ms.locfileid: "38677507"
---
# <a name="siem-server-integration-with-microsoft-365-services-and-applications"></a><span data-ttu-id="00ffa-103">Intégration de serveur SIEM aux services et applications Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="00ffa-103">SIEM server integration with Microsoft 365 services and applications</span></span>

## <a name="summary"></a><span data-ttu-id="00ffa-104">Résumé</span><span class="sxs-lookup"><span data-stu-id="00ffa-104">Summary</span></span>

<span data-ttu-id="00ffa-105">Si votre organisation utilise un serveur de gestion des événements et des informations de sécurité (SIEM), ou si vous envisagez d’obtenir rapidement un serveur SIEM, vous vous demandez peut-être comment l’intégrer à Microsoft 365 ou Office 365.</span><span class="sxs-lookup"><span data-stu-id="00ffa-105">If your organization is using a Security Information and Event Management (SIEM) server, or if you are planning to get a SIEM server soon, you might be wondering how that'll integrate with Microsoft 365 or Office 365.</span></span> <span data-ttu-id="00ffa-106">Cet article fournit une liste de ressources que vous pouvez utiliser pour configurer l’intégration de serveur SIEM à vos applications et services Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="00ffa-106">This article provides a list of resources you can use to set up SIEM server integration with your Microsoft 365 services and applications.</span></span>

> [!TIP]
> <span data-ttu-id="00ffa-107">Si vous n’avez pas encore de serveur SIEM et que vous Explorez vos options, envisagez **[Microsoft Azure Sentinel](https://docs.microsoft.com/azure/sentinel/overview)**.</span><span class="sxs-lookup"><span data-stu-id="00ffa-107">If you don't have a SIEM server yet and are exploring your options, consider **[Microsoft Azure Sentinel](https://docs.microsoft.com/azure/sentinel/overview)**.</span></span>

## <a name="do-i-need-a-siem-server"></a><span data-ttu-id="00ffa-108">Ai-je besoin d’un serveur SIEM ?</span><span class="sxs-lookup"><span data-stu-id="00ffa-108">Do I need a SIEM server?</span></span>

<span data-ttu-id="00ffa-109">La nécessité d’un serveur SIEM dépend de nombreux facteurs, tels que les exigences de sécurité de votre organisation et l’emplacement de stockage de vos données.</span><span class="sxs-lookup"><span data-stu-id="00ffa-109">Whether you need a SIEM server depends on many factors, such as your organization's security requirements and where your data resides.</span></span> <span data-ttu-id="00ffa-110">Microsoft 365 inclut un large éventail de fonctionnalités de sécurité qui répondent aux besoins de sécurité de plusieurs organisations sans serveurs supplémentaires, tels qu’un serveur SIEM.</span><span class="sxs-lookup"><span data-stu-id="00ffa-110">Microsoft 365 includes a wide variety of security features that meet many organizations' security needs without additional servers, such as a SIEM server.</span></span> <span data-ttu-id="00ffa-111">Certaines organisations ont des circonstances spéciales qui nécessitent l’utilisation d’un serveur SIEM.</span><span class="sxs-lookup"><span data-stu-id="00ffa-111">Some organizations have special circumstances that require the use of a SIEM server.</span></span> <span data-ttu-id="00ffa-112">Voici quelques exemples :</span><span class="sxs-lookup"><span data-stu-id="00ffa-112">Here are some examples:</span></span>

- <span data-ttu-id="00ffa-113">*Fabrikam* dispose de contenu et d’applications sur site, et d’autres dans le Cloud (ils ont un déploiement Cloud hybride).</span><span class="sxs-lookup"><span data-stu-id="00ffa-113">*Fabrikam* has some content and applications on premises, and some in the cloud (they have a hybrid cloud deployment).</span></span> <span data-ttu-id="00ffa-114">Pour obtenir des rapports de sécurité sur tous les contenus et applications, Fabrikam a implémenté un serveur SIEM.</span><span class="sxs-lookup"><span data-stu-id="00ffa-114">To get security reports across all their content and applications, Fabrikam has implemented a SIEM server.</span></span> 

- <span data-ttu-id="00ffa-115">*Contoso* est une organisation de services financiers présentant des exigences de sécurité particulièrement strictes.</span><span class="sxs-lookup"><span data-stu-id="00ffa-115">*Contoso* is a financial services organization that has particularly stringent security requirements.</span></span> <span data-ttu-id="00ffa-116">Ils ont ajouté un serveur SIEM à leur environnement pour tirer parti de la protection de sécurité supplémentaire dont ils ont besoin.</span><span class="sxs-lookup"><span data-stu-id="00ffa-116">They have added a SIEM server to their environment to take advantage of the extra security protection they require.</span></span>

## <a name="siem-server-integration-with-microsoft-365"></a><span data-ttu-id="00ffa-117">Intégration de serveur SIEM à Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="00ffa-117">SIEM server integration with Microsoft 365</span></span>

<span data-ttu-id="00ffa-118">Un serveur SIEM peut recevoir des données à partir d’un large éventail de services et d’applications Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="00ffa-118">A SIEM server can receive data from a wide variety of Microsoft 365 services and applications.</span></span> <span data-ttu-id="00ffa-119">Le tableau suivant répertorie plusieurs services et applications Microsoft 365 avec des entrées de serveur SIEM, ainsi que des ressources pour en savoir plus sur l’intégration de serveur SIEM.</span><span class="sxs-lookup"><span data-stu-id="00ffa-119">The following table lists several Microsoft 365 services and applications along with SIEM server inputs, and resources to learn more about SIEM server integration.</span></span> 

| <span data-ttu-id="00ffa-120">Service ou application Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="00ffa-120">Microsoft 365 Service or Application</span></span> | <span data-ttu-id="00ffa-121">Entrées de serveur SIEM</span><span class="sxs-lookup"><span data-stu-id="00ffa-121">SIEM server inputs</span></span> | <span data-ttu-id="00ffa-122">Ressources pour en savoir plus</span><span class="sxs-lookup"><span data-stu-id="00ffa-122">Resources to learn more</span></span> |
| --- | --- | --- |
| [<span data-ttu-id="00ffa-123">Office 365 Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="00ffa-123">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)  | <span data-ttu-id="00ffa-124">Journaux d'audit</span><span class="sxs-lookup"><span data-stu-id="00ffa-124">Audit logs</span></span> | [<span data-ttu-id="00ffa-125">Intégration SIEM avec Office 365 protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="00ffa-125">SIEM integration with Office 365 Advanced Threat Protection</span></span>](siem-integration-with-office-365-ti.md) |
| [<span data-ttu-id="00ffa-126">Microsoft Defender – Protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="00ffa-126">Microsoft Defender Advanced Threat Protection</span></span>](https://docs.microsoft.com/windows/security/threat-protection/) | <span data-ttu-id="00ffa-127">Point de terminaison HTTPs hébergé dans Azure</span><span class="sxs-lookup"><span data-stu-id="00ffa-127">HTTPS endpoint hosted in Azure</span></span> <br/><span data-ttu-id="00ffa-128">API REST</span><span class="sxs-lookup"><span data-stu-id="00ffa-128">REST API</span></span>| [<span data-ttu-id="00ffa-129">Attirez les alertes sur vos outils SIEM</span><span class="sxs-lookup"><span data-stu-id="00ffa-129">Pull alerts to your SIEM tools</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/configure-siem) |
| [<span data-ttu-id="00ffa-130">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="00ffa-130">Microsoft Cloud App Security</span></span>](https://docs.microsoft.com/cloud-app-security/what-is-cloud-app-security) | <span data-ttu-id="00ffa-131">Intégration des journaux</span><span class="sxs-lookup"><span data-stu-id="00ffa-131">Log integration</span></span> | [<span data-ttu-id="00ffa-132">Intégration SIEM à la sécurité des applications Cloud Microsoft</span><span class="sxs-lookup"><span data-stu-id="00ffa-132">SIEM integration with Microsoft Cloud App Security</span></span>](https://docs.microsoft.com/cloud-app-security/siem) |

> [!TIP]
> <span data-ttu-id="00ffa-133">Jetez un coup d’œil à [Azure Sentinel](https://docs.microsoft.com/azure/sentinel/overview), qui est fourni avec un certain nombre de connecteurs pour les solutions Microsoft, disponible dès à présent et offrant une intégration en temps réel, y compris des solutions de protection contre les menaces Microsoft, ainsi que des sources Microsoft 365, notamment Office 365, Azure ad, Azure ATP et Microsoft Cloud App Security, et bien plus encore.</span><span class="sxs-lookup"><span data-stu-id="00ffa-133">Take a look at [Azure Sentinel](https://docs.microsoft.com/azure/sentinel/overview), which comes with a number of connectors for Microsoft solutions, available out of the box and providing real-time integration, including Microsoft Threat Protection solutions, and Microsoft 365 sources, including Office 365, Azure AD, Azure ATP, and Microsoft Cloud App Security, and more.</span></span>

### <a name="audit-logging-must-be-turned-on"></a><span data-ttu-id="00ffa-134">La journalisation d’audit doit être activée.</span><span class="sxs-lookup"><span data-stu-id="00ffa-134">Audit logging must be turned on</span></span>

<span data-ttu-id="00ffa-135">Assurez-vous que la journalisation d’audit est activée avant de configurer l’intégration de serveur SIEM.</span><span class="sxs-lookup"><span data-stu-id="00ffa-135">Make sure audit logging is turned on before you configure SIEM server integration.</span></span> 

- <span data-ttu-id="00ffa-136">Pour SharePoint Online, OneDrive entreprise et Azure Active Directory, [la journalisation d’audit est activée dans le centre de sécurité & conformité](https://docs.microsoft.com/office365/securitycompliance/turn-audit-log-search-on-or-off).</span><span class="sxs-lookup"><span data-stu-id="00ffa-136">For SharePoint Online, OneDrive for Business, and Azure Active Directory, [audit logging is turned on in the Security & Compliance Center](https://docs.microsoft.com/office365/securitycompliance/turn-audit-log-search-on-or-off).</span></span>

- <span data-ttu-id="00ffa-137">Pour Exchange Online, la [journalisation d’audit est activée avec Windows PowerShell](https://docs.microsoft.com/office365/securitycompliance/enable-mailbox-auditing).</span><span class="sxs-lookup"><span data-stu-id="00ffa-137">For Exchange Online, [audit logging is turned on with Windows PowerShell](https://docs.microsoft.com/office365/securitycompliance/enable-mailbox-auditing).</span></span>
 
## <a name="additional-resources"></a><span data-ttu-id="00ffa-138">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="00ffa-138">Additional resources</span></span>

[<span data-ttu-id="00ffa-139">Intégrer des solutions de sécurité dans Azure Security Center</span><span class="sxs-lookup"><span data-stu-id="00ffa-139">Integrate security solutions in Azure Security Center</span></span>](https://docs.microsoft.com/azure/security-center/security-center-partner-integration#exporting-data-to-a-siem)

[<span data-ttu-id="00ffa-140">Intégrer les alertes de l’API de sécurité Microsoft Graph avec des technologies SIEM</span><span class="sxs-lookup"><span data-stu-id="00ffa-140">Integrate Microsoft Graph Security API alerts with a SIEM</span></span>](https://docs.microsoft.com/graph/security-integration)