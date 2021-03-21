---
title: Intégration des serveurs SIEM aux applications et services Microsoft 365
f1.keywords:
- NOCSH
ms.author: deniseb
author: denisebmsft
manager: dansimp
audience: ITPro
ms.topic: article
ms.date: 11/18/2019
localization_priority: Normal
ms.collection:
- M365-security-compliance
ms.custom:
- Ent_Solutions
- SIEM
- seo-marvel-apr2020
description: Obtenir une vue d’ensemble de l’intégration du serveur SIEM (Security Information and Event Management) à vos applications et services cloud Microsoft 365
ms.technology: mdo
ms.prod: m365-security
ms.openlocfilehash: 21aaad71f40a01a3bea2f9535d1c3256ae667bae
ms.sourcegitcommit: 27b2b2e5c41934b918cac2c171556c45e36661bf
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/19/2021
ms.locfileid: "50916585"
---
# <a name="security-information-and-event-management-siem-server-integration-with-microsoft-365-services-and-applications"></a><span data-ttu-id="3b4eb-103">Intégration de serveurs SIEM (Security Information and Event Management) aux services et applications Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="3b4eb-103">Security Information and Event Management (SIEM) server integration with Microsoft 365 services and applications</span></span>

<span data-ttu-id="3b4eb-104">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="3b4eb-104">**Applies to**</span></span>
- [<span data-ttu-id="3b4eb-105">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="3b4eb-105">Exchange Online Protection</span></span>](exchange-online-protection-overview.md)
- [<span data-ttu-id="3b4eb-106">Microsoft Defender pour Office 365 Plan 1 et Plan 2</span><span class="sxs-lookup"><span data-stu-id="3b4eb-106">Microsoft Defender for Office 365 plan 1 and plan 2</span></span>](office-365-atp.md)
- [<span data-ttu-id="3b4eb-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="3b4eb-107">Microsoft 365 Defender</span></span>](../mtp/microsoft-threat-protection.md)

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender-for-office.md)]

## <a name="summary"></a><span data-ttu-id="3b4eb-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="3b4eb-108">Summary</span></span>

<span data-ttu-id="3b4eb-109">Votre organisation utilise-t-elle ou prévoit-elle d’obtenir un serveur SIEM (Security Information and Event Management) ?</span><span class="sxs-lookup"><span data-stu-id="3b4eb-109">Is your organization using or planning to get a Security Information and Event Management (SIEM) server?</span></span> <span data-ttu-id="3b4eb-110">Vous vous demandez peut-être comment il s’intègre à Microsoft 365 ou Office 365.</span><span class="sxs-lookup"><span data-stu-id="3b4eb-110">You might be wondering how it integrates with Microsoft 365 or Office 365.</span></span> <span data-ttu-id="3b4eb-111">Cet article fournit la liste des ressources que vous pouvez utiliser pour intégrer votre serveur SIEM aux services et applications Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="3b4eb-111">This article provides a list of resources you can use to integrate your SIEM server with Microsoft 365 services and applications.</span></span>

> [!TIP]
> <span data-ttu-id="3b4eb-112">Si vous n’avez pas encore de serveur SIEM et que vous explorez vos options, envisagez **[Microsoft Azure Sentinel](/azure/sentinel/overview)**.</span><span class="sxs-lookup"><span data-stu-id="3b4eb-112">If you don't have a SIEM server yet and are exploring your options, consider **[Microsoft Azure Sentinel](/azure/sentinel/overview)**.</span></span>

## <a name="do-i-need-a-siem-server"></a><span data-ttu-id="3b4eb-113">Ai-je besoin d’un serveur SIEM ?</span><span class="sxs-lookup"><span data-stu-id="3b4eb-113">Do I need a SIEM server?</span></span>

<span data-ttu-id="3b4eb-114">La nécessité d’un serveur SIEM dépend de nombreux facteurs, tels que les exigences de sécurité de votre organisation et l’emplacement où résident vos données.</span><span class="sxs-lookup"><span data-stu-id="3b4eb-114">Whether you need a SIEM server depends on many factors, such as your organization's security requirements and where your data resides.</span></span> <span data-ttu-id="3b4eb-115">Microsoft 365 inclut un large éventail de fonctionnalités de sécurité qui répondent aux besoins de sécurité de nombreuses organisations sans serveurs supplémentaires, tels qu’un serveur SIEM.</span><span class="sxs-lookup"><span data-stu-id="3b4eb-115">Microsoft 365 includes a wide variety of security features that meet many organizations' security needs without additional servers, such as a SIEM server.</span></span> <span data-ttu-id="3b4eb-116">Certaines organisations ont des circonstances particulières qui nécessitent l’utilisation d’un serveur SIEM.</span><span class="sxs-lookup"><span data-stu-id="3b4eb-116">Some organizations have special circumstances that require the use of a SIEM server.</span></span> <span data-ttu-id="3b4eb-117">Voici quelques exemples :</span><span class="sxs-lookup"><span data-stu-id="3b4eb-117">Here are some examples:</span></span>

- <span data-ttu-id="3b4eb-118">*Fabrikam possède* du contenu et des applications sur site, et d’autres dans le cloud (ils disposent d’un déploiement cloud hybride).</span><span class="sxs-lookup"><span data-stu-id="3b4eb-118">*Fabrikam* has some content and applications on premises, and some in the cloud (they have a hybrid cloud deployment).</span></span> <span data-ttu-id="3b4eb-119">Pour obtenir des rapports de sécurité sur l’ensemble de son contenu et de ses applications, Fabrikam a implémenté un serveur SIEM.</span><span class="sxs-lookup"><span data-stu-id="3b4eb-119">To get security reports across all their content and applications, Fabrikam has implemented a SIEM server.</span></span>

- <span data-ttu-id="3b4eb-120">*Contoso est* une organisation de services financiers qui a des exigences de sécurité particulièrement strictes.</span><span class="sxs-lookup"><span data-stu-id="3b4eb-120">*Contoso* is a financial services organization that has particularly stringent security requirements.</span></span> <span data-ttu-id="3b4eb-121">Ils ont ajouté un serveur SIEM à leur environnement pour tirer parti de la protection de sécurité supplémentaire dont ils ont besoin.</span><span class="sxs-lookup"><span data-stu-id="3b4eb-121">They have added a SIEM server to their environment to take advantage of the extra security protection they require.</span></span>

## <a name="siem-server-integration-with-microsoft-365"></a><span data-ttu-id="3b4eb-122">Intégration de serveur SIEM à Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="3b4eb-122">SIEM server integration with Microsoft 365</span></span>

<span data-ttu-id="3b4eb-123">Un serveur SIEM peut recevoir des données à partir d’un large éventail de services et d’applications Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="3b4eb-123">A SIEM server can receive data from a wide variety of Microsoft 365 services and applications.</span></span> <span data-ttu-id="3b4eb-124">Le tableau suivant répertorie plusieurs services et applications Microsoft 365, ainsi que les entrées serveur SIEM et les ressources pour en savoir plus.</span><span class="sxs-lookup"><span data-stu-id="3b4eb-124">The following table lists several Microsoft 365 services and applications, along with SIEM server inputs and resources to learn more.</span></span>

****

|<span data-ttu-id="3b4eb-125">Service ou application Microsoft 365</span><span class="sxs-lookup"><span data-stu-id="3b4eb-125">Microsoft 365 Service or Application</span></span>|<span data-ttu-id="3b4eb-126">Entrées/méthodes de serveur SIEM</span><span class="sxs-lookup"><span data-stu-id="3b4eb-126">SIEM server inputs/methods</span></span>|<span data-ttu-id="3b4eb-127">Ressources pour en savoir plus</span><span class="sxs-lookup"><span data-stu-id="3b4eb-127">Resources to learn more</span></span>|
|---|---|---|
|[<span data-ttu-id="3b4eb-128">Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="3b4eb-128">Microsoft Defender for Office 365</span></span>](office-365-atp.md)|<span data-ttu-id="3b4eb-129">Journaux d'audit</span><span class="sxs-lookup"><span data-stu-id="3b4eb-129">Audit logs</span></span>|[<span data-ttu-id="3b4eb-130">Intégration DE SIEM à Microsoft Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="3b4eb-130">SIEM integration with Microsoft Defender for Office 365</span></span>](siem-integration-with-office-365-ti.md)|
|[<span data-ttu-id="3b4eb-131">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="3b4eb-131">Microsoft Defender for Endpoint</span></span>](/windows/security/threat-protection/)|<span data-ttu-id="3b4eb-132">Point de terminaison HTTPS hébergé dans Azure</span><span class="sxs-lookup"><span data-stu-id="3b4eb-132">HTTPS endpoint hosted in Azure</span></span> <p> <span data-ttu-id="3b4eb-133">API REST</span><span class="sxs-lookup"><span data-stu-id="3b4eb-133">REST API</span></span>|[<span data-ttu-id="3b4eb-134">Tirer des alertes vers vos outils SIEM</span><span class="sxs-lookup"><span data-stu-id="3b4eb-134">Pull alerts to your SIEM tools</span></span>](/windows/security/threat-protection/microsoft-defender-atp/configure-siem)|
|[<span data-ttu-id="3b4eb-135">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="3b4eb-135">Microsoft Cloud App Security</span></span>](/cloud-app-security/what-is-cloud-app-security)|<span data-ttu-id="3b4eb-136">Intégration des journaux</span><span class="sxs-lookup"><span data-stu-id="3b4eb-136">Log integration</span></span>|[<span data-ttu-id="3b4eb-137">Intégration DE SIEM à Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="3b4eb-137">SIEM integration with Microsoft Cloud App Security</span></span>](/cloud-app-security/siem)|
|

> [!TIP]
> <span data-ttu-id="3b4eb-138">Jetez un œil à [Azure Sentinel](/azure/sentinel/overview).</span><span class="sxs-lookup"><span data-stu-id="3b4eb-138">Take a look at [Azure Sentinel](/azure/sentinel/overview).</span></span> <span data-ttu-id="3b4eb-139">Azure Sentinel est livré avec des connecteurs pour les solutions Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3b4eb-139">Azure Sentinel comes with connectors for Microsoft solutions.</span></span> <span data-ttu-id="3b4eb-140">Ces connecteurs sont disponibles « dès le début » et assurent une intégration en temps réel.</span><span class="sxs-lookup"><span data-stu-id="3b4eb-140">These connectors are available "out of the box" and provide for real-time integration.</span></span> <span data-ttu-id="3b4eb-141">Vous pouvez utiliser Azure Sentinel avec vos solutions Microsoft 365 Defender et vos services Microsoft 365, notamment Office 365, Azure AD, Microsoft Defender pour l’identité, Microsoft Cloud App Security, etc.</span><span class="sxs-lookup"><span data-stu-id="3b4eb-141">You can use Azure Sentinel with your Microsoft 365 Defender solutions and Microsoft 365 services, including Office 365, Azure AD, Microsoft Defender for Identity, Microsoft Cloud App Security, and more.</span></span>

### <a name="audit-logging-must-be-turned-on"></a><span data-ttu-id="3b4eb-142">L’enregistrement d’audit doit être allumé</span><span class="sxs-lookup"><span data-stu-id="3b4eb-142">Audit logging must be turned on</span></span>

<span data-ttu-id="3b4eb-143">Assurez-vous que la journalisation d’audit est allumée avant de configurer l’intégration de serveur SIEM.</span><span class="sxs-lookup"><span data-stu-id="3b4eb-143">Make sure that audit logging is turned on before you configure SIEM server integration.</span></span>

- <span data-ttu-id="3b4eb-144">Pour SharePoint Online, OneDrive Entreprise et Azure Active Directory, la journalisation d’audit est active dans le Centre de sécurité [& conformité.](../../compliance/turn-audit-log-search-on-or-off.md)</span><span class="sxs-lookup"><span data-stu-id="3b4eb-144">For SharePoint Online, OneDrive for Business, and Azure Active Directory, [audit logging is turned on in the Security & Compliance Center](../../compliance/turn-audit-log-search-on-or-off.md).</span></span>

- <span data-ttu-id="3b4eb-145">Pour Exchange Online, voir [Gérer l’audit de boîte aux lettres.](../../compliance/enable-mailbox-auditing.md)</span><span class="sxs-lookup"><span data-stu-id="3b4eb-145">For Exchange Online, see [Manage mailbox auditing](../../compliance/enable-mailbox-auditing.md).</span></span>

## <a name="more-resources"></a><span data-ttu-id="3b4eb-146">Plus de ressources</span><span class="sxs-lookup"><span data-stu-id="3b4eb-146">More resources</span></span>

[<span data-ttu-id="3b4eb-147">Intégrer des solutions de sécurité dans Azure Defender</span><span class="sxs-lookup"><span data-stu-id="3b4eb-147">Integrate security solutions in Azure Defender</span></span>](/azure/security-center/security-center-partner-integration#exporting-data-to-a-siem)

[<span data-ttu-id="3b4eb-148">Intégrer les alertes de l’API de sécurité Microsoft Graph avec des technologies SIEM</span><span class="sxs-lookup"><span data-stu-id="3b4eb-148">Integrate Microsoft Graph Security API alerts with a SIEM</span></span>](/graph/security-integration)