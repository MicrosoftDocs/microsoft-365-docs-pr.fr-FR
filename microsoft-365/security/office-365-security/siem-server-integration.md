---
title: Intégration de serveur SIEM aux services et applications Microsoft 365
f1.keywords:
- NOCSH
ms.author: deniseb
author: denisebmsft
manager: dansimp
audience: ITPro
ms.topic: article
ms.date: 11/18/2019
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
ms.custom:
- Ent_Solutions
- SIEM
- seo-marvel-apr2020
description: Obtenir une vue d’ensemble de l’intégration du serveur des informations de sécurité et de la gestion des événements (SIEM) à vos applications et services Cloud Microsoft 365
ms.openlocfilehash: d2be5e0127adf25b3884e3717caccf60d4db1d28
ms.sourcegitcommit: 6a1a8aa024fd685d04da97bfcbc8eadacc488534
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/12/2020
ms.locfileid: "46653570"
---
# <a name="security-information-and-event-management-siem-server-integration-with-microsoft-365-services-and-applications"></a><span data-ttu-id="f9f77-103">Intégration du serveur de gestion des événements et des informations de sécurité (SIEM) aux services et applications Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="f9f77-103">Security Information and Event Management (SIEM) server integration with Microsoft 365 services and applications</span></span>

## <a name="summary"></a><span data-ttu-id="f9f77-104">Résumé</span><span class="sxs-lookup"><span data-stu-id="f9f77-104">Summary</span></span>

<span data-ttu-id="f9f77-105">Votre organisation utilise-t-elle ou envisage-t-elle un serveur de gestion des événements et des informations de sécurité (SIEM) ?</span><span class="sxs-lookup"><span data-stu-id="f9f77-105">Is your organization using or planning to get a Security Information and Event Management (SIEM) server?</span></span> <span data-ttu-id="f9f77-106">Vous vous demandez peut-être comment il s’intègre à Microsoft 365 ou Office 365.</span><span class="sxs-lookup"><span data-stu-id="f9f77-106">You might be wondering how it integrates with Microsoft 365 or Office 365.</span></span> <span data-ttu-id="f9f77-107">Cet article fournit une liste de ressources que vous pouvez utiliser pour intégrer votre serveur SIEM aux services et applications Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="f9f77-107">This article provides a list of resources you can use to integrate your SIEM server with Microsoft 365 services and applications.</span></span>

> [!TIP]
> <span data-ttu-id="f9f77-108">Si vous n’avez pas encore de serveur SIEM et que vous Explorez vos options, envisagez **[Microsoft Azure Sentinel](https://docs.microsoft.com/azure/sentinel/overview)**.</span><span class="sxs-lookup"><span data-stu-id="f9f77-108">If you don't have a SIEM server yet and are exploring your options, consider **[Microsoft Azure Sentinel](https://docs.microsoft.com/azure/sentinel/overview)**.</span></span>

## <a name="do-i-need-a-siem-server"></a><span data-ttu-id="f9f77-109">Ai-je besoin d’un serveur SIEM ?</span><span class="sxs-lookup"><span data-stu-id="f9f77-109">Do I need a SIEM server?</span></span>

<span data-ttu-id="f9f77-110">La nécessité d’un serveur SIEM dépend de nombreux facteurs, tels que les exigences de sécurité de votre organisation et l’emplacement de stockage de vos données.</span><span class="sxs-lookup"><span data-stu-id="f9f77-110">Whether you need a SIEM server depends on many factors, such as your organization's security requirements and where your data resides.</span></span> <span data-ttu-id="f9f77-111">Microsoft 365 inclut un large éventail de fonctionnalités de sécurité qui répondent aux besoins de sécurité de plusieurs organisations sans serveurs supplémentaires, tels qu’un serveur SIEM.</span><span class="sxs-lookup"><span data-stu-id="f9f77-111">Microsoft 365 includes a wide variety of security features that meet many organizations' security needs without additional servers, such as a SIEM server.</span></span> <span data-ttu-id="f9f77-112">Certaines organisations ont des circonstances spéciales qui nécessitent l’utilisation d’un serveur SIEM.</span><span class="sxs-lookup"><span data-stu-id="f9f77-112">Some organizations have special circumstances that require the use of a SIEM server.</span></span> <span data-ttu-id="f9f77-113">Voici quelques exemples :</span><span class="sxs-lookup"><span data-stu-id="f9f77-113">Here are some examples:</span></span>

- <span data-ttu-id="f9f77-114">*Fabrikam* dispose de contenu et d’applications sur site, et d’autres dans le Cloud (ils ont un déploiement Cloud hybride).</span><span class="sxs-lookup"><span data-stu-id="f9f77-114">*Fabrikam* has some content and applications on premises, and some in the cloud (they have a hybrid cloud deployment).</span></span> <span data-ttu-id="f9f77-115">Pour obtenir des rapports de sécurité sur tous les contenus et applications, Fabrikam a implémenté un serveur SIEM.</span><span class="sxs-lookup"><span data-stu-id="f9f77-115">To get security reports across all their content and applications, Fabrikam has implemented a SIEM server.</span></span>

- <span data-ttu-id="f9f77-116">*Contoso* est une organisation de services financiers présentant des exigences de sécurité particulièrement strictes.</span><span class="sxs-lookup"><span data-stu-id="f9f77-116">*Contoso* is a financial services organization that has particularly stringent security requirements.</span></span> <span data-ttu-id="f9f77-117">Ils ont ajouté un serveur SIEM à leur environnement pour tirer parti de la protection de sécurité supplémentaire dont ils ont besoin.</span><span class="sxs-lookup"><span data-stu-id="f9f77-117">They have added a SIEM server to their environment to take advantage of the extra security protection they require.</span></span>

## <a name="siem-server-integration-with-microsoft-365"></a><span data-ttu-id="f9f77-118">Intégration de serveur SIEM à Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="f9f77-118">SIEM server integration with Microsoft 365</span></span>

<span data-ttu-id="f9f77-119">Un serveur SIEM peut recevoir des données à partir d’un large éventail de services et d’applications Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="f9f77-119">A SIEM server can receive data from a wide variety of Microsoft 365 services and applications.</span></span> <span data-ttu-id="f9f77-120">Le tableau suivant répertorie plusieurs applications et services Microsoft 365, ainsi que des ressources et des entrées de serveur SIEM pour en savoir plus.</span><span class="sxs-lookup"><span data-stu-id="f9f77-120">The following table lists several Microsoft 365 services and applications, along with SIEM server inputs and resources to learn more.</span></span>

****

|<span data-ttu-id="f9f77-121">Service ou application Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="f9f77-121">Microsoft 365 Service or Application</span></span>|<span data-ttu-id="f9f77-122">Entrées/méthodes du serveur SIEM</span><span class="sxs-lookup"><span data-stu-id="f9f77-122">SIEM server inputs/methods</span></span>|<span data-ttu-id="f9f77-123">Ressources pour en savoir plus</span><span class="sxs-lookup"><span data-stu-id="f9f77-123">Resources to learn more</span></span>|
|---|---|---|
|[<span data-ttu-id="f9f77-124">Protection avancée contre les menaces dans Office 365</span><span class="sxs-lookup"><span data-stu-id="f9f77-124">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)|<span data-ttu-id="f9f77-125">Journaux d'audit</span><span class="sxs-lookup"><span data-stu-id="f9f77-125">Audit logs</span></span>|[<span data-ttu-id="f9f77-126">Intégration SIEM avec Office 365 protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="f9f77-126">SIEM integration with Office 365 Advanced Threat Protection</span></span>](siem-integration-with-office-365-ti.md)|
|[<span data-ttu-id="f9f77-127">Microsoft Defender – Protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="f9f77-127">Microsoft Defender Advanced Threat Protection</span></span>](https://docs.microsoft.com/windows/security/threat-protection/)|<span data-ttu-id="f9f77-128">Point de terminaison HTTPs hébergé dans Azure</span><span class="sxs-lookup"><span data-stu-id="f9f77-128">HTTPS endpoint hosted in Azure</span></span> <br/><span data-ttu-id="f9f77-129">API REST</span><span class="sxs-lookup"><span data-stu-id="f9f77-129">REST API</span></span>|[<span data-ttu-id="f9f77-130">Attirez les alertes sur vos outils SIEM</span><span class="sxs-lookup"><span data-stu-id="f9f77-130">Pull alerts to your SIEM tools</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/configure-siem)|
|[<span data-ttu-id="f9f77-131">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="f9f77-131">Microsoft Cloud App Security</span></span>](https://docs.microsoft.com/cloud-app-security/what-is-cloud-app-security)|<span data-ttu-id="f9f77-132">Intégration des journaux</span><span class="sxs-lookup"><span data-stu-id="f9f77-132">Log integration</span></span>|[<span data-ttu-id="f9f77-133">Intégration SIEM à la sécurité des applications Cloud Microsoft</span><span class="sxs-lookup"><span data-stu-id="f9f77-133">SIEM integration with Microsoft Cloud App Security</span></span>](https://docs.microsoft.com/cloud-app-security/siem)|
|

> [!TIP]
> <span data-ttu-id="f9f77-134">Jetez un œil à [Azure Sentinel](https://docs.microsoft.com/azure/sentinel/overview).</span><span class="sxs-lookup"><span data-stu-id="f9f77-134">Take a look at [Azure Sentinel](https://docs.microsoft.com/azure/sentinel/overview).</span></span> <span data-ttu-id="f9f77-135">Azure sentinelle inclut des connecteurs pour les solutions Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f9f77-135">Azure Sentinel comes with connectors for Microsoft solutions.</span></span> <span data-ttu-id="f9f77-136">Ces connecteurs sont disponibles « en l’absence de » et permettent une intégration en temps réel.</span><span class="sxs-lookup"><span data-stu-id="f9f77-136">These connectors are available "out of the box" and provide for real-time integration.</span></span> <span data-ttu-id="f9f77-137">Vous pouvez utiliser Azure Sentinel avec vos solutions de protection contre les menaces Microsoft et les services Microsoft 365, notamment Office 365, Azure AD, Azure ATP, sécurité des applications Cloud Microsoft, et bien plus encore.</span><span class="sxs-lookup"><span data-stu-id="f9f77-137">You can use Azure Sentinel with your Microsoft Threat Protection solutions and Microsoft 365 services, including Office 365, Azure AD, Azure ATP, Microsoft Cloud App Security, and more.</span></span>

### <a name="audit-logging-must-be-turned-on"></a><span data-ttu-id="f9f77-138">La journalisation d’audit doit être activée.</span><span class="sxs-lookup"><span data-stu-id="f9f77-138">Audit logging must be turned on</span></span>

<span data-ttu-id="f9f77-139">Assurez-vous que la journalisation d’audit est activée avant de configurer l’intégration de serveur SIEM.</span><span class="sxs-lookup"><span data-stu-id="f9f77-139">Make sure that audit logging is turned on before you configure SIEM server integration.</span></span>

- <span data-ttu-id="f9f77-140">Pour SharePoint Online, OneDrive entreprise et Azure Active Directory, [la journalisation d’audit est activée dans le centre de sécurité & conformité](../../compliance/turn-audit-log-search-on-or-off.md).</span><span class="sxs-lookup"><span data-stu-id="f9f77-140">For SharePoint Online, OneDrive for Business, and Azure Active Directory, [audit logging is turned on in the Security & Compliance Center](../../compliance/turn-audit-log-search-on-or-off.md).</span></span>

- <span data-ttu-id="f9f77-141">Pour Exchange Online, consultez la rubrique [Manage Mailbox Auditing](../../compliance/enable-mailbox-auditing.md).</span><span class="sxs-lookup"><span data-stu-id="f9f77-141">For Exchange Online, see [Manage mailbox auditing](../../compliance/enable-mailbox-auditing.md).</span></span>

## <a name="more-resources"></a><span data-ttu-id="f9f77-142">Autres ressources</span><span class="sxs-lookup"><span data-stu-id="f9f77-142">More resources</span></span>

[<span data-ttu-id="f9f77-143">Intégrer des solutions de sécurité dans Azure Security Center</span><span class="sxs-lookup"><span data-stu-id="f9f77-143">Integrate security solutions in Azure Security Center</span></span>](https://docs.microsoft.com/azure/security-center/security-center-partner-integration#exporting-data-to-a-siem)

[<span data-ttu-id="f9f77-144">Intégrer les alertes de l’API de sécurité Microsoft Graph avec des technologies SIEM</span><span class="sxs-lookup"><span data-stu-id="f9f77-144">Integrate Microsoft Graph Security API alerts with a SIEM</span></span>](https://docs.microsoft.com/graph/security-integration)
