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
ms.openlocfilehash: fa970b28939ad43bf6a2717e603013277bc9130f
ms.sourcegitcommit: cc3b64a91e16ccdaa9c338b9a9056dbe3963ba9e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/10/2020
ms.locfileid: "42569158"
---
# <a name="turn-on-microsoft-threat-protection"></a><span data-ttu-id="cda99-104">Activer la Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="cda99-104">Turn on Microsoft Threat Protection</span></span>

<span data-ttu-id="cda99-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="cda99-105">**Applies to:**</span></span>
- <span data-ttu-id="cda99-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="cda99-106">Microsoft Threat Protection</span></span>

<span data-ttu-id="cda99-107">La Protection Microsoft contre les menaces unifie votre processus de réponse aux incidents en intégrant les principales fonctionnalités de Microsoft Defender - Protection avancée contre les menaces (ATP), Office 365 - Protection avancée contre les menaces, Microsoft Cloud App Security et Azure ATP.</span><span class="sxs-lookup"><span data-stu-id="cda99-107">Microsoft Threat Protection unifies your incident response process by integrating key capabilities across Microsoft Defender Advanced Threat Protection (ATP), Office 365 ATP, Microsoft Cloud App Security, and Azure ATP.</span></span> <span data-ttu-id="cda99-108">Cette expérience unifiée ajoute des fonctionnalités puissantes auxquelles vous pouvez accéder dans le Centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="cda99-108">This unified experience adds powerful features you can access in the Microsoft 365 security center.</span></span>

<span data-ttu-id="cda99-109">Pour bénéficier de la meilleure protection et optimiser la protection Microsoft contre les menaces, nous vous recommandons de déployer tous les services pris en charge applicables sur votre réseau.</span><span class="sxs-lookup"><span data-stu-id="cda99-109">To get the best protection and optimize Microsoft Threat Protection, we recommend deploying all applicable supported services on your network.</span></span> <span data-ttu-id="cda99-110">Pour plus d’informations, consultez la rubrique [Deploying Supported services](deploy-supported-services.md).</span><span class="sxs-lookup"><span data-stu-id="cda99-110">For more information, [read about deploying supported services](deploy-supported-services.md).</span></span>

## <a name="check-license-eligibility-and-required-permissions"></a><span data-ttu-id="cda99-111">Vérifier l’éligibilité de la licence et les autorisations requises</span><span class="sxs-lookup"><span data-stu-id="cda99-111">Check license eligibility and required permissions</span></span>
<span data-ttu-id="cda99-112">Une licence Microsoft 365 E5, E5 sécurité ou a5 ou une combinaison valide de licences donne accès aux services pris en charge et vous permet d’utiliser la protection Microsoft contre les menaces dans le centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="cda99-112">A Microsoft 365 E5, E5 Security, or A5 license or a valid combination of licenses provides access to supported services and entitles you to use Microsoft Threat Protection in Microsoft 365 security center.</span></span>

<span data-ttu-id="cda99-113">Pour obtenir des informations détaillées sur les licences, [Lisez les conditions relatives aux licences](prerequisites.md#licensing-requirements).</span><span class="sxs-lookup"><span data-stu-id="cda99-113">For detailed licensing information, [read the licensing requirements](prerequisites.md#licensing-requirements).</span></span>

### <a name="check-your-role"></a><span data-ttu-id="cda99-114">Vérifier votre rôle</span><span class="sxs-lookup"><span data-stu-id="cda99-114">Check your role</span></span>
<span data-ttu-id="cda99-115">Vous devez être **administrateur général** ou administrateur de **sécurité** dans Azure Active Directory pour activer Microsoft Threat Protection.</span><span class="sxs-lookup"><span data-stu-id="cda99-115">You must be a **global administrator** or a **security administrator** in Azure Active Directory to turn on Microsoft Threat Protection.</span></span> [<span data-ttu-id="cda99-116">Afficher vos rôles dans Azure AD</span><span class="sxs-lookup"><span data-stu-id="cda99-116">View your roles in Azure AD</span></span>](https://docs.microsoft.com//azure/active-directory/users-groups-roles/directory-manage-roles-portal)

## <a name="start-using-the-service"></a><span data-ttu-id="cda99-117">Commencez à utiliser le service</span><span class="sxs-lookup"><span data-stu-id="cda99-117">Start using the service</span></span>
<span data-ttu-id="cda99-118">Microsoft Threat Protection agrège les données des différents services intégrés.</span><span class="sxs-lookup"><span data-stu-id="cda99-118">Microsoft Threat Protection aggregates data from the various integrated services.</span></span> <span data-ttu-id="cda99-119">Il traitera et stockera les données de manière centralisée afin d’identifier les nouvelles idées et de créer des flux de travail de réponse centralisée.</span><span class="sxs-lookup"><span data-stu-id="cda99-119">It will process and store data centrally to identify new insights and make centralized response workflows possible.</span></span>

<span data-ttu-id="cda99-120">Avant d’activer le service, le centre de sécurité Microsoft 365 ([Security.Microsoft.com](https://security.microsoft.com)) affiche la **page d’accueil** de la protection de Microsoft contre les menaces lorsque vous sélectionnez **incidents**, **Centre de maintenance**ou sélection dans le volet de navigation.</span><span class="sxs-lookup"><span data-stu-id="cda99-120">Before you turn on the service, the Microsoft 365 security center ([security.microsoft.com](https://security.microsoft.com)) shows the Microsoft Threat Protection welcome page when you select **Incidents**, **Action center**, or **Hunting** from the navigation pane.</span></span> <span data-ttu-id="cda99-121">Ces options de navigation ne s’affichent pas si vous n’êtes pas éligible à l’utilisation de la protection contre les menaces Microsoft.</span><span class="sxs-lookup"><span data-stu-id="cda99-121">These navigation options are not shown if you are not eligible to use Microsoft Threat Protection.</span></span>

<span data-ttu-id="cda99-122">![Image de la page d’accueil de la protection de Microsoft contre les menaces affichée si Microsoft Threat](../../media/mtp-welcome.png)
protection n’a pas été activé sur la*page d’accueil de Microsoft Threat Protection dans le centre de sécurité Microsoft 365*</span><span class="sxs-lookup"><span data-stu-id="cda99-122">![Image of the Microsoft Threat Protection welcome page shown if Microsoft Threat Protection has not been turned on](../../media/mtp-welcome.png)
*Microsoft Threat Protection welcome page in Microsoft 365 security center*</span></span>

<span data-ttu-id="cda99-123">Pour activer Microsoft Threat Protection, terminez simplement le processus à partir de la page d’accueil.</span><span class="sxs-lookup"><span data-stu-id="cda99-123">To turn on Microsoft Threat Protection, simply complete the process from the welcome page.</span></span> <span data-ttu-id="cda99-124">Vous pouvez également activer Microsoft Threat Protection en accédant aux **paramètres** ([Security.Microsoft.com/Settings](https://security.microsoft.com/settings)) dans le volet de navigation et en sélectionnant **Microsoft Threat Protection**.</span><span class="sxs-lookup"><span data-stu-id="cda99-124">You can also turn on Microsoft Threat Protection by accessing **Settings** ([security.microsoft.com/settings](https://security.microsoft.com/settings)) in the navigation pane and selecting **Microsoft Threat Protection**.</span></span>

>[!NOTE]
><span data-ttu-id="cda99-125">Si vous ne voyez pas les **paramètres** dans le volet de navigation ou que vous n’avez pas accès à la page, vérifiez vos autorisations et licences.</span><span class="sxs-lookup"><span data-stu-id="cda99-125">If you don't see **Settings** in the navigation pane or couldn't access the page, check your permissions and licenses.</span></span>

### <a name="select-data-center-location"></a><span data-ttu-id="cda99-126">Sélectionner l’emplacement du centre de données</span><span class="sxs-lookup"><span data-stu-id="cda99-126">Select data center location</span></span>
<span data-ttu-id="cda99-127">Si Microsoft Defender - Protection avancée contre les menaces a été configuré pour votre organisation, les données sont stockées et traitées dans le même emplacement de centre de données que celui que vous avez sélectionné pour [vos données Microsoft Defender – Protection avancée contre les menaces](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/data-storage-privacy).</span><span class="sxs-lookup"><span data-stu-id="cda99-127">If Microsoft Defender ATP has been provisioned for your organization, data will be stored and processed in the same data center location you have selected for [your Microsoft Defender ATP data](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/data-storage-privacy).</span></span> <span data-ttu-id="cda99-128">Si vous n’avez pas Microsoft Defender ATP, vous serez invité à choisir un nouvel emplacement de centre de données spécifiquement pour la Protection Microsoft contre les menaces.</span><span class="sxs-lookup"><span data-stu-id="cda99-128">If you don't have Microsoft Defender ATP, you will be asked to choose a new data center location specifically for Microsoft Threat Protection.</span></span> 

<span data-ttu-id="cda99-129">Vous devez fournir le consentement avant le partage des données entre les services et l’agrégation.</span><span class="sxs-lookup"><span data-stu-id="cda99-129">You need to provide consent before data is shared between services and aggregated.</span></span>

### <a name="confirm-that-the-service-is-on"></a><span data-ttu-id="cda99-130">Vérifiez que le service est activé</span><span class="sxs-lookup"><span data-stu-id="cda99-130">Confirm that the service is on</span></span>
<span data-ttu-id="cda99-131">Une fois le service configuré, il ajoute :</span><span class="sxs-lookup"><span data-stu-id="cda99-131">Once the service is provisioned, it adds:</span></span>

- [<span data-ttu-id="cda99-132">Gestion des incidents</span><span class="sxs-lookup"><span data-stu-id="cda99-132">Incidents management</span></span>](incidents-overview.md)
- <span data-ttu-id="cda99-133">Centre de notifications pour la gestion des [examen et réponse automatisés](mtp-autoir.md)</span><span class="sxs-lookup"><span data-stu-id="cda99-133">An action center for managing [automated investigation and response](mtp-autoir.md)</span></span>
- <span data-ttu-id="cda99-134">Fonctionnalités de [chasse avancées](advanced-hunting-overview.md)</span><span class="sxs-lookup"><span data-stu-id="cda99-134">[Advanced hunting](advanced-hunting-overview.md) capabilities</span></span>

<span data-ttu-id="cda99-135">![Image du volet de navigation du centre de sécurité Microsoft 365 avec les](../../media/mtp-on.png)
fonctionnalités de protection de Microsoft Threat*Centre de sécurité Microsoft 365 avec gestion des incidents et autres fonctionnalités de protection contre les menaces Microsoft*</span><span class="sxs-lookup"><span data-stu-id="cda99-135">![Image of Microsoft 365 security center navigation pane with Microsoft Threat Protection features](../../media/mtp-on.png)
*Microsoft 365 security center with incidents management and other Microsoft Threat Protection capabilities*</span></span>

### <a name="getting-azure-atp-data"></a><span data-ttu-id="cda99-136">Obtention de données Azure ATP</span><span class="sxs-lookup"><span data-stu-id="cda99-136">Getting Azure ATP data</span></span>
<span data-ttu-id="cda99-137">Pour partager des données Azure ATP avec la Protection Microsoft contre les menaces, assurez-vous que Microsoft Cloud App Security et l’intégration Azure ATP sont activées.</span><span class="sxs-lookup"><span data-stu-id="cda99-137">To share Azure ATP data with Microsoft Threat Protection, ensure that Microsoft Cloud App Security and Azure ATP integration is turned on.</span></span> [<span data-ttu-id="cda99-138">Découvrez cette intégration</span><span class="sxs-lookup"><span data-stu-id="cda99-138">Learn more about this integration</span></span>](https://docs.microsoft.com/cloud-app-security/aatp-integration)


## <a name="turn-off-microsoft-threat-protection"></a><span data-ttu-id="cda99-139">Désactiver la Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="cda99-139">Turn off Microsoft Threat Protection</span></span>
<span data-ttu-id="cda99-140">Pour cesser d’utiliser la Protection Microsoft contre les menaces, accédez à **Paramètres** > **Protection Microsoft contre les menaces** > **Accepter / Refuser** dans le Centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="cda99-140">To stop using Microsoft Threat Protection, go to **Settings** > **Microsoft Threat Protection** > **Opt-in / Opt-out** in the Microsoft 365 security center.</span></span> <span data-ttu-id="cda99-141">Désélectionnez **Activer la Protection Microsoft contre les menaces** et enregistrez les modifications.</span><span class="sxs-lookup"><span data-stu-id="cda99-141">Unselect **Turn on Microsoft Threat Protection** and save the changes.</span></span>

<span data-ttu-id="cda99-142">Les fonctionnalités correspondantes seront supprimées du centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="cda99-142">Corresponding features will be removed from the Microsoft 365 security center.</span></span>

## <a name="get-assistance"></a><span data-ttu-id="cda99-143">Obtenir de l'aide</span><span class="sxs-lookup"><span data-stu-id="cda99-143">Get assistance</span></span>

<span data-ttu-id="cda99-144">Le personnel du support Microsoft peut vous aider à mettre en service ou à mettre hors service le service et les ressources associées sur votre client.</span><span class="sxs-lookup"><span data-stu-id="cda99-144">Microsoft support staff can help provision or deprovision the service and related resources on your tenant.</span></span> <span data-ttu-id="cda99-145">Pour obtenir de l’aide, sélectionnez **besoin d’aide ?** dans le centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="cda99-145">For assistance, select **Need help?** in the Microsoft 365 security center.</span></span> <span data-ttu-id="cda99-146">Lorsque vous contactez le support technique, mentionnez Microsoft Threat Protection.</span><span class="sxs-lookup"><span data-stu-id="cda99-146">When contacting support, mention Microsoft Threat Protection.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cda99-147">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="cda99-147">Related topics</span></span>

- [<span data-ttu-id="cda99-148">Vue d’ensemble de la Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="cda99-148">Microsoft Threat Protection overview</span></span>](microsoft-threat-protection.md)
- [<span data-ttu-id="cda99-149">Conditions requises et autres conditions préalables relatives aux licences</span><span class="sxs-lookup"><span data-stu-id="cda99-149">Licensing requirements and other prerequisites</span></span>](prerequisites.md)
- [<span data-ttu-id="cda99-150">Déployer les services pris en charge</span><span class="sxs-lookup"><span data-stu-id="cda99-150">Deploy supported services</span></span>](deploy-supported-services.md)
- [<span data-ttu-id="cda99-151">Vue d’ensemble de Microsoft Defender - Protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="cda99-151">Microsoft Defender ATP overview</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection)
- [<span data-ttu-id="cda99-152">Vue d’ensemble d’Office 365 – Protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="cda99-152">Office 365 ATP overview</span></span>](../office-365-security/office-365-atp.md)
- [<span data-ttu-id="cda99-153">Vue d’ensemble de Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="cda99-153">Microsoft Cloud App Security overview</span></span>](https://docs.microsoft.com/cloud-app-security/what-is-cloud-app-security)
- [<span data-ttu-id="cda99-154">Vue d’ensemble d’Azure ATP</span><span class="sxs-lookup"><span data-stu-id="cda99-154">Azure ATP overview</span></span>](https://docs.microsoft.com/azure-advanced-threat-protection/what-is-atp)
- [<span data-ttu-id="cda99-155">Stockage de données Microsoft Defender - Protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="cda99-155">Microsoft Defender ATP data storage</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/data-storage-privacy)
