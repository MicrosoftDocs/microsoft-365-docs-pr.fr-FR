---
title: Activer la Protection Microsoft contre les menaces dans le Centre de sécurité Microsoft 365
description: Découvrez comment activer la Protection Microsoft contre les menaces et commencer à intégrer votre incident de sécurité et votre réponse.
keywords: prise en main, activer le MTP, protection Microsoft contre les menaces, M365, sécurité, emplacement des données, autorisations requises, éligibilité des licences
search.product: eADQiWindows 10XVcnh
ms.prod: microsoft-365-enterprise
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: lomayor
author: lomayor
ms.localizationpriority: medium
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: conceptual
search.appverid:
- MOE150
- MET150
ms.openlocfilehash: 8aeff373b3f5550f7217a5b56aa1dbf994563825
ms.sourcegitcommit: 1c91b7b24537d0e54d484c3379043db53c1aea65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2020
ms.locfileid: "41600061"
---
# <a name="turn-on-microsoft-threat-protection"></a><span data-ttu-id="79bfa-104">Activer la Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="79bfa-104">Turn on Microsoft Threat Protection</span></span>

<span data-ttu-id="79bfa-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="79bfa-105">**Applies to:**</span></span>
- <span data-ttu-id="79bfa-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="79bfa-106">Microsoft Threat Protection</span></span>

[!INCLUDE [Prerelease information](../includes/prerelease.md)]

<span data-ttu-id="79bfa-107">La Protection Microsoft contre les menaces unifie votre processus de réponse aux incidents en intégrant les principales fonctionnalités de Microsoft Defender - Protection avancée contre les menaces (ATP), Office 365 - Protection avancée contre les menaces, Microsoft Cloud App Security et Azure ATP.</span><span class="sxs-lookup"><span data-stu-id="79bfa-107">Microsoft Threat Protection unifies your incident response process by integrating key capabilities across Microsoft Defender Advanced Threat Protection (ATP), Office 365 ATP, Microsoft Cloud App Security, and Azure ATP.</span></span> <span data-ttu-id="79bfa-108">Cette expérience unifiée ajoute des fonctionnalités puissantes auxquelles vous pouvez accéder dans le Centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="79bfa-108">This unified experience adds powerful features you can access in the Microsoft 365 security center.</span></span>

## <a name="check-license-eligibility-and-required-permissions"></a><span data-ttu-id="79bfa-109">Vérifier l’éligibilité de la licence et les autorisations requises</span><span class="sxs-lookup"><span data-stu-id="79bfa-109">Check license eligibility and required permissions</span></span>
<span data-ttu-id="79bfa-110">Les clients disposant d’une licence Microsoft 365 E5 ou équivalente peuvent utiliser la Protection Microsoft contre les menaces.</span><span class="sxs-lookup"><span data-stu-id="79bfa-110">Customers with a Microsoft 365 E5 or equivalent license can use Microsoft Threat Protection.</span></span> <span data-ttu-id="79bfa-111">Pour plus d'informations, [lire les conditions relatives aux licences](prerequisites.md#licensing-requirements).</span><span class="sxs-lookup"><span data-stu-id="79bfa-111">For more information, [read the licensing requirements](prerequisites.md#licensing-requirements).</span></span>

 <span data-ttu-id="79bfa-112">Pour pouvoir activer Microsoft Threat Protection, vous devez être **administrateur général** ou **administrateur de sécurité** dans [Azure Active Directory](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles#available-roles).</span><span class="sxs-lookup"><span data-stu-id="79bfa-112">To be able to turn on Microsoft Threat Protection, you need to be a **global administrator** or a **security administrator** in [Azure Active Directory](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles#available-roles).</span></span>

## <a name="start-using-the-service"></a><span data-ttu-id="79bfa-113">Commencez à utiliser le service</span><span class="sxs-lookup"><span data-stu-id="79bfa-113">Start using the service</span></span>
<span data-ttu-id="79bfa-114">L’activation du service de Protection Microsoft contre les menaces agrège les données des différents services intégrés.</span><span class="sxs-lookup"><span data-stu-id="79bfa-114">Turning on the Microsoft Threat Protection service aggregates data from the various integrated services.</span></span> <span data-ttu-id="79bfa-115">Les données sont traitées et stockées de façon centralisée pour identifier les nouvelles perspectives et rendre possible les flux de travail de réponse centralisée.</span><span class="sxs-lookup"><span data-stu-id="79bfa-115">The data will be processed and stored centrally to identify new insights and to make centralized response workflows possible.</span></span>

<span data-ttu-id="79bfa-116">Avant d’activer le service, le centre de sécurité Microsoft 365 ([Security.Microsoft.com](https://security.microsoft.com)) n’affiche pas les **incidents** ni les options du **Centre de notifications** dans le menu.</span><span class="sxs-lookup"><span data-stu-id="79bfa-116">Before you turn the service on, the Microsoft 365 security center ([security.microsoft.com](https://security.microsoft.com)) does not show the **Incidents** and the **Action center** options on the menu.</span></span>

<span data-ttu-id="79bfa-117">![Image du menu Centre de sécurité Microsoft 365 sans les fonctionnalités de Protection Microsoft contre les menaces](../images/mtp-off.png)
*Centre de sécurité Microsoft 365 avec la protection Microsoft contre les menaces désactivée*</span><span class="sxs-lookup"><span data-stu-id="79bfa-117">![Image of Microsoft 365 security center menu without Microsoft Threat Protection features](../images/mtp-off.png)
*Microsoft 365 security center with Microsoft Threat Protection turned off*</span></span>

<span data-ttu-id="79bfa-118">Pour activer le service de Protection Microsoft contre les menaces, accédez à **Paramètres** > **Protection Microsoft contre les menaces** > **Accepter / Refuser** dans le Centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="79bfa-118">To turn the Microsoft Threat Protection service on, go to **Settings** > **Microsoft Threat Protection** > **Opt-in / Opt-out** in the Microsoft 365 security center.</span></span>

<span data-ttu-id="79bfa-119">Si Microsoft Defender - Protection avancée contre les menaces a été configuré pour votre organisation, les données sont stockées et traitées dans le même emplacement de centre de données que celui que vous avez sélectionné pour [vos données Microsoft Defender – Protection avancée contre les menaces](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/data-storage-privacy).</span><span class="sxs-lookup"><span data-stu-id="79bfa-119">If Microsoft Defender ATP has been provisioned for your organization, data will be stored and processed in the same data center location you have selected for [your Microsoft Defender ATP data](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/data-storage-privacy).</span></span> <span data-ttu-id="79bfa-120">Si vous n’avez pas Microsoft Defender ATP, vous serez invité à choisir un nouvel emplacement de centre de données spécifiquement pour la Protection Microsoft contre les menaces.</span><span class="sxs-lookup"><span data-stu-id="79bfa-120">If you don't have Microsoft Defender ATP, you will be asked to choose a new data center location specifically for Microsoft Threat Protection.</span></span> <span data-ttu-id="79bfa-121">Vous devez fournir un consentement avant que les données soient partagées entre les services et agrégées.</span><span class="sxs-lookup"><span data-stu-id="79bfa-121">You will need to provide consent before data is shared between services and aggregated.</span></span>

### <a name="confirm-that-the-service-is-on"></a><span data-ttu-id="79bfa-122">Vérifiez que le service est activé</span><span class="sxs-lookup"><span data-stu-id="79bfa-122">Confirm that the service is on</span></span>
<span data-ttu-id="79bfa-123">Une fois le service configuré, il ajoute :</span><span class="sxs-lookup"><span data-stu-id="79bfa-123">Once the service is provisioned, it adds:</span></span>

- [<span data-ttu-id="79bfa-124">Gestion des incidents</span><span class="sxs-lookup"><span data-stu-id="79bfa-124">Incidents management</span></span>](incidents-overview.md)
- <span data-ttu-id="79bfa-125">Centre de notifications pour la gestion des [examen et réponse automatisés](mtp-autoir.md)</span><span class="sxs-lookup"><span data-stu-id="79bfa-125">An action center for managing [automated investigation and response](mtp-autoir.md)</span></span>
- <span data-ttu-id="79bfa-126">La fonctionnalités de [repérage avancé](advanced-hunting-overview.md) à la page **Repérage**</span><span class="sxs-lookup"><span data-stu-id="79bfa-126">[Advanced hunting](advanced-hunting-overview.md) capabilities to the existing **Hunting** page</span></span>

<span data-ttu-id="79bfa-127">![Image du menu Centre de sécurité Microsoft 365 avec les fonctionnalités de Protection Microsoft contre les menaces](../images/mtp-on.png)
*Centre de sécurité Microsoft 365 avec la gestion des incidents et d’autres fonctionnalités de Protection Microsoft contre les menaces*</span><span class="sxs-lookup"><span data-stu-id="79bfa-127">![Image of Microsoft 365 security center menu with Microsoft Threat Protection features](../images/mtp-on.png)
*Microsoft 365 security center with incidents management and other Microsoft Threat Protection features*</span></span>

### <a name="getting-azure-atp-data"></a><span data-ttu-id="79bfa-128">Obtention de données Azure ATP</span><span class="sxs-lookup"><span data-stu-id="79bfa-128">Getting Azure ATP data</span></span>
<span data-ttu-id="79bfa-129">Pour partager des données Azure ATP avec la Protection Microsoft contre les menaces, assurez-vous que Microsoft Cloud App Security et l’intégration Azure ATP sont activées.</span><span class="sxs-lookup"><span data-stu-id="79bfa-129">To share Azure ATP data with Microsoft Threat Protection, ensure that Microsoft Cloud App Security and Azure ATP integration is turned on.</span></span> [<span data-ttu-id="79bfa-130">Découvrez cette intégration</span><span class="sxs-lookup"><span data-stu-id="79bfa-130">Learn more about this integration</span></span>](https://docs.microsoft.com/cloud-app-security/aatp-integration)


## <a name="turn-off-microsoft-threat-protection"></a><span data-ttu-id="79bfa-131">Désactiver la Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="79bfa-131">Turn off Microsoft Threat Protection</span></span>
<span data-ttu-id="79bfa-132">Pour cesser d’utiliser la Protection Microsoft contre les menaces, accédez à **Paramètres** > **Protection Microsoft contre les menaces** > **Accepter / Refuser** dans le Centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="79bfa-132">To stop using Microsoft Threat Protection, go to **Settings** > **Microsoft Threat Protection** > **Opt-in / Opt-out** in the Microsoft 365 security center.</span></span> <span data-ttu-id="79bfa-133">Désélectionnez **Activer la Protection Microsoft contre les menaces** et enregistrez les modifications.</span><span class="sxs-lookup"><span data-stu-id="79bfa-133">Unselect **Turn on Microsoft Threat Protection** and save the changes.</span></span>

<span data-ttu-id="79bfa-134">Les données seront définitivement supprimées et les fonctionnalités correspondantes seront supprimées du centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="79bfa-134">Data will be permanently deleted and corresponding features will be removed from the Microsoft 365 security center.</span></span>

## <a name="get-assistance"></a><span data-ttu-id="79bfa-135">Obtenir de l'aide</span><span class="sxs-lookup"><span data-stu-id="79bfa-135">Get assistance</span></span>

<span data-ttu-id="79bfa-136">Le personnel Microsoft peut vous aider à fournir ou à déprovisionner le service et les ressources associées sur votre locataire.</span><span class="sxs-lookup"><span data-stu-id="79bfa-136">Microsoft staff can help provision or deprovision the service and related resources on your tenant.</span></span> <span data-ttu-id="79bfa-137">Pour obtenir de l’aide, sélectionnez **besoin d’aide ?** dans le centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="79bfa-137">For assistance, select **Need help?** in the Microsoft 365 security center.</span></span> <span data-ttu-id="79bfa-138">Lorsque vous décrivez vos préoccupations, mentionnez « protection contre les menaces Microsoft ».</span><span class="sxs-lookup"><span data-stu-id="79bfa-138">When describing your concerns, mention "Microsoft Threat Protection".</span></span>

## <a name="related-topics"></a><span data-ttu-id="79bfa-139">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="79bfa-139">Related topics</span></span>

- [<span data-ttu-id="79bfa-140">Vue d’ensemble de la Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="79bfa-140">Microsoft Threat Protection overview</span></span>](microsoft-threat-protection.md)
- [<span data-ttu-id="79bfa-141">Conditions requises et autres conditions préalables relatives aux licences</span><span class="sxs-lookup"><span data-stu-id="79bfa-141">Licensing requirements and other prerequisites</span></span>](prerequisites.md)
- [<span data-ttu-id="79bfa-142">Vue d’ensemble de Microsoft Defender - Protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="79bfa-142">Microsoft Defender ATP overview</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection)
- [<span data-ttu-id="79bfa-143">Vue d’ensemble d’Office 365 – Protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="79bfa-143">Office 365 ATP overview</span></span>](../office-365-security/office-365-atp.md)
- [<span data-ttu-id="79bfa-144">Vue d’ensemble de Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="79bfa-144">Microsoft Cloud App Security overview</span></span>](https://docs.microsoft.com/cloud-app-security/what-is-cloud-app-security)
- [<span data-ttu-id="79bfa-145">Vue d’ensemble d’Azure ATP</span><span class="sxs-lookup"><span data-stu-id="79bfa-145">Azure ATP overview</span></span>](https://docs.microsoft.com/azure-advanced-threat-protection/what-is-atp)
- [<span data-ttu-id="79bfa-146">Stockage de données Microsoft Defender - Protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="79bfa-146">Microsoft Defender ATP data storage</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/data-storage-privacy)
