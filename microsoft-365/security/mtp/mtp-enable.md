---
title: Activer la Protection Microsoft contre les menaces dans le Centre de sécurité Microsoft 365
description: Découvrez comment activer la Protection Microsoft contre les menaces et commencer à intégrer votre incident de sécurité et votre réponse.
keywords: prise en main, activer le MTP, protection Microsoft contre les menaces, M365, sécurité, emplacement des données, autorisations requises, éligibilité des licences, page Paramètres
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
ms.openlocfilehash: 73f76dee8a59229138f906e593a84220c7f70aee
ms.sourcegitcommit: 74bf600424d0cb7b9d16b4f391aeda7875058be1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/24/2020
ms.locfileid: "42235213"
---
# <a name="turn-on-microsoft-threat-protection"></a><span data-ttu-id="cf77f-104">Activer la Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="cf77f-104">Turn on Microsoft Threat Protection</span></span>

<span data-ttu-id="cf77f-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="cf77f-105">**Applies to:**</span></span>
- <span data-ttu-id="cf77f-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="cf77f-106">Microsoft Threat Protection</span></span>



<span data-ttu-id="cf77f-107">La Protection Microsoft contre les menaces unifie votre processus de réponse aux incidents en intégrant les principales fonctionnalités de Microsoft Defender - Protection avancée contre les menaces (ATP), Office 365 - Protection avancée contre les menaces, Microsoft Cloud App Security et Azure ATP.</span><span class="sxs-lookup"><span data-stu-id="cf77f-107">Microsoft Threat Protection unifies your incident response process by integrating key capabilities across Microsoft Defender Advanced Threat Protection (ATP), Office 365 ATP, Microsoft Cloud App Security, and Azure ATP.</span></span> <span data-ttu-id="cf77f-108">Cette expérience unifiée ajoute des fonctionnalités puissantes auxquelles vous pouvez accéder dans le Centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="cf77f-108">This unified experience adds powerful features you can access in the Microsoft 365 security center.</span></span>

## <a name="check-license-eligibility-and-required-permissions"></a><span data-ttu-id="cf77f-109">Vérifier l’éligibilité de la licence et les autorisations requises</span><span class="sxs-lookup"><span data-stu-id="cf77f-109">Check license eligibility and required permissions</span></span>
<span data-ttu-id="cf77f-110">Les clients disposant de Microsoft 365 E5, de Microsoft 365 E5 sécurité ou d’une combinaison équivalente de licences peuvent utiliser Microsoft Threat Protection.</span><span class="sxs-lookup"><span data-stu-id="cf77f-110">Customers with Microsoft 365 E5, Microsoft 365 E5 Security, or an equivalent combination of licenses can use Microsoft Threat Protection.</span></span> <span data-ttu-id="cf77f-111">Pour plus d'informations, [lire les conditions relatives aux licences](prerequisites.md#licensing-requirements).</span><span class="sxs-lookup"><span data-stu-id="cf77f-111">For more information, [read the licensing requirements](prerequisites.md#licensing-requirements).</span></span>

<span data-ttu-id="cf77f-112">Vous devez être **administrateur général** ou administrateur de **sécurité** dans [Azure Active Directory](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles#available-roles) pour activer Microsoft Threat Protection.</span><span class="sxs-lookup"><span data-stu-id="cf77f-112">You must be a **global administrator** or a **security administrator** in [Azure Active Directory](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles#available-roles) to turn on Microsoft Threat Protection.</span></span>

## <a name="start-using-the-service"></a><span data-ttu-id="cf77f-113">Commencez à utiliser le service</span><span class="sxs-lookup"><span data-stu-id="cf77f-113">Start using the service</span></span>
<span data-ttu-id="cf77f-114">Microsoft Threat Protection agrège les données des différents services intégrés.</span><span class="sxs-lookup"><span data-stu-id="cf77f-114">Microsoft Threat Protection aggregates data from the various integrated services.</span></span> <span data-ttu-id="cf77f-115">Il traitera et stockera les données de manière centralisée afin d’identifier les nouvelles idées et de créer des flux de travail de réponse centralisée.</span><span class="sxs-lookup"><span data-stu-id="cf77f-115">It will process and store data centrally to identify new insights and make centralized response workflows possible.</span></span>

<span data-ttu-id="cf77f-116">Avant d’activer le service, le centre de sécurité Microsoft 365 ([Security.Microsoft.com](https://security.microsoft.com)) n’affiche pas les **incidents** ni les options du **Centre de notifications** dans le volet de navigation.</span><span class="sxs-lookup"><span data-stu-id="cf77f-116">Before you turn on the service, the Microsoft 365 security center ([security.microsoft.com](https://security.microsoft.com)) doesn't show the **Incidents** and the **Action center** options in the navigation pane.</span></span>

<span data-ttu-id="cf77f-117">![Image du volet de navigation du centre de sécurité Microsoft 365 sans les](../../media/mtp-off.png)
fonctionnalités Microsoft Threat Protection*Centre de sécurité Microsoft 365 avec la protection Microsoft contre les menaces désactivée*</span><span class="sxs-lookup"><span data-stu-id="cf77f-117">![Image of Microsoft 365 security center navigation pane without Microsoft Threat Protection features](../../media/mtp-off.png)
*Microsoft 365 security center with Microsoft Threat Protection turned off*</span></span>

<span data-ttu-id="cf77f-118">Pour activer Microsoft Threat Protection, sélectionnez **paramètres** dans le volet de navigation.</span><span class="sxs-lookup"><span data-stu-id="cf77f-118">To turn on Microsoft Threat Protection, select **Settings** in the navigation pane.</span></span> <span data-ttu-id="cf77f-119">Dans la **[page Paramètres](https://security.microsoft.com/settings)**, consultez la section**opt-in/opt-out**de la **protection de Microsoft contre** > les menaces.</span><span class="sxs-lookup"><span data-stu-id="cf77f-119">In the **[Settings page](https://security.microsoft.com/settings)**, go to **Microsoft Threat Protection** > **Opt-in / Opt-out**.</span></span>

>[!NOTE]
><span data-ttu-id="cf77f-120">Si vous ne voyez pas les **paramètres** dans le volet de navigation ou que vous n’avez pas accès à la page, vérifiez vos autorisations et licences.</span><span class="sxs-lookup"><span data-stu-id="cf77f-120">If you don't see **Settings** in the navigation pane or couldn't access the page, check your permissions and licenses.</span></span>

### <a name="select-data-center-location"></a><span data-ttu-id="cf77f-121">Sélectionner l’emplacement du centre de données</span><span class="sxs-lookup"><span data-stu-id="cf77f-121">Select data center location</span></span>
<span data-ttu-id="cf77f-122">Si Microsoft Defender - Protection avancée contre les menaces a été configuré pour votre organisation, les données sont stockées et traitées dans le même emplacement de centre de données que celui que vous avez sélectionné pour [vos données Microsoft Defender – Protection avancée contre les menaces](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/data-storage-privacy).</span><span class="sxs-lookup"><span data-stu-id="cf77f-122">If Microsoft Defender ATP has been provisioned for your organization, data will be stored and processed in the same data center location you have selected for [your Microsoft Defender ATP data](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/data-storage-privacy).</span></span> <span data-ttu-id="cf77f-123">Si vous n’avez pas Microsoft Defender ATP, vous serez invité à choisir un nouvel emplacement de centre de données spécifiquement pour la Protection Microsoft contre les menaces.</span><span class="sxs-lookup"><span data-stu-id="cf77f-123">If you don't have Microsoft Defender ATP, you will be asked to choose a new data center location specifically for Microsoft Threat Protection.</span></span> 

<span data-ttu-id="cf77f-124">Vous devez fournir le consentement avant le partage des données entre les services et l’agrégation.</span><span class="sxs-lookup"><span data-stu-id="cf77f-124">You need to provide consent before data is shared between services and aggregated.</span></span>

### <a name="confirm-that-the-service-is-on"></a><span data-ttu-id="cf77f-125">Vérifiez que le service est activé</span><span class="sxs-lookup"><span data-stu-id="cf77f-125">Confirm that the service is on</span></span>
<span data-ttu-id="cf77f-126">Une fois le service configuré, il ajoute :</span><span class="sxs-lookup"><span data-stu-id="cf77f-126">Once the service is provisioned, it adds:</span></span>

- [<span data-ttu-id="cf77f-127">Gestion des incidents</span><span class="sxs-lookup"><span data-stu-id="cf77f-127">Incidents management</span></span>](incidents-overview.md)
- <span data-ttu-id="cf77f-128">Centre de notifications pour la gestion des [examen et réponse automatisés](mtp-autoir.md)</span><span class="sxs-lookup"><span data-stu-id="cf77f-128">An action center for managing [automated investigation and response](mtp-autoir.md)</span></span>
- <span data-ttu-id="cf77f-129">La fonctionnalités de [repérage avancé](advanced-hunting-overview.md) à la page **Repérage**</span><span class="sxs-lookup"><span data-stu-id="cf77f-129">[Advanced hunting](advanced-hunting-overview.md) capabilities to the existing **Hunting** page</span></span>

<span data-ttu-id="cf77f-130">![Image du volet de navigation du centre de sécurité Microsoft 365 avec les](../../media/mtp-on.png)
fonctionnalités de protection de Microsoft Threat*Centre de sécurité Microsoft 365 avec gestion des incidents et autres fonctionnalités de protection contre les menaces Microsoft*</span><span class="sxs-lookup"><span data-stu-id="cf77f-130">![Image of Microsoft 365 security center navigation pane with Microsoft Threat Protection features](../../media/mtp-on.png)
*Microsoft 365 security center with incidents management and other Microsoft Threat Protection capabilities*</span></span>

### <a name="getting-azure-atp-data"></a><span data-ttu-id="cf77f-131">Obtention de données Azure ATP</span><span class="sxs-lookup"><span data-stu-id="cf77f-131">Getting Azure ATP data</span></span>
<span data-ttu-id="cf77f-132">Pour partager des données Azure ATP avec la Protection Microsoft contre les menaces, assurez-vous que Microsoft Cloud App Security et l’intégration Azure ATP sont activées.</span><span class="sxs-lookup"><span data-stu-id="cf77f-132">To share Azure ATP data with Microsoft Threat Protection, ensure that Microsoft Cloud App Security and Azure ATP integration is turned on.</span></span> [<span data-ttu-id="cf77f-133">Découvrez cette intégration</span><span class="sxs-lookup"><span data-stu-id="cf77f-133">Learn more about this integration</span></span>](https://docs.microsoft.com/cloud-app-security/aatp-integration)


## <a name="turn-off-microsoft-threat-protection"></a><span data-ttu-id="cf77f-134">Désactiver la Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="cf77f-134">Turn off Microsoft Threat Protection</span></span>
<span data-ttu-id="cf77f-135">Pour cesser d’utiliser la Protection Microsoft contre les menaces, accédez à **Paramètres** > **Protection Microsoft contre les menaces** > **Accepter / Refuser** dans le Centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="cf77f-135">To stop using Microsoft Threat Protection, go to **Settings** > **Microsoft Threat Protection** > **Opt-in / Opt-out** in the Microsoft 365 security center.</span></span> <span data-ttu-id="cf77f-136">Désélectionnez **Activer la Protection Microsoft contre les menaces** et enregistrez les modifications.</span><span class="sxs-lookup"><span data-stu-id="cf77f-136">Unselect **Turn on Microsoft Threat Protection** and save the changes.</span></span>

<span data-ttu-id="cf77f-137">Les données seront définitivement supprimées et les fonctionnalités correspondantes seront supprimées du centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="cf77f-137">Data will be permanently deleted and corresponding features will be removed from the Microsoft 365 security center.</span></span>

## <a name="get-assistance"></a><span data-ttu-id="cf77f-138">Obtenir de l'aide</span><span class="sxs-lookup"><span data-stu-id="cf77f-138">Get assistance</span></span>

<span data-ttu-id="cf77f-139">Le personnel du support Microsoft peut vous aider à mettre en service ou à mettre hors service le service et les ressources associées sur votre client.</span><span class="sxs-lookup"><span data-stu-id="cf77f-139">Microsoft support staff can help provision or deprovision the service and related resources on your tenant.</span></span> <span data-ttu-id="cf77f-140">Pour obtenir de l’aide, sélectionnez **besoin d’aide ?** dans le centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="cf77f-140">For assistance, select **Need help?** in the Microsoft 365 security center.</span></span> <span data-ttu-id="cf77f-141">Lorsque vous contactez le support technique, mentionnez Microsoft Threat Protection.</span><span class="sxs-lookup"><span data-stu-id="cf77f-141">When contacting support, mention Microsoft Threat Protection.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cf77f-142">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="cf77f-142">Related topics</span></span>

- [<span data-ttu-id="cf77f-143">Vue d’ensemble de la Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="cf77f-143">Microsoft Threat Protection overview</span></span>](microsoft-threat-protection.md)
- [<span data-ttu-id="cf77f-144">Conditions requises et autres conditions préalables relatives aux licences</span><span class="sxs-lookup"><span data-stu-id="cf77f-144">Licensing requirements and other prerequisites</span></span>](prerequisites.md)
- [<span data-ttu-id="cf77f-145">Vue d’ensemble de Microsoft Defender - Protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="cf77f-145">Microsoft Defender ATP overview</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection)
- [<span data-ttu-id="cf77f-146">Vue d’ensemble d’Office 365 – Protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="cf77f-146">Office 365 ATP overview</span></span>](../office-365-security/office-365-atp.md)
- [<span data-ttu-id="cf77f-147">Vue d’ensemble de Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="cf77f-147">Microsoft Cloud App Security overview</span></span>](https://docs.microsoft.com/cloud-app-security/what-is-cloud-app-security)
- [<span data-ttu-id="cf77f-148">Vue d’ensemble d’Azure ATP</span><span class="sxs-lookup"><span data-stu-id="cf77f-148">Azure ATP overview</span></span>](https://docs.microsoft.com/azure-advanced-threat-protection/what-is-atp)
- [<span data-ttu-id="cf77f-149">Stockage de données Microsoft Defender - Protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="cf77f-149">Microsoft Defender ATP data storage</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/data-storage-privacy)
