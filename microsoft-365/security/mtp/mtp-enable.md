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
ms.openlocfilehash: 0bb91f226a29fe6b175cf1ca4866316d1457291e
ms.sourcegitcommit: bd8d55f82ca008af1b93a9bb4d1545f68e8188ad
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2020
ms.locfileid: "44011862"
---
# <a name="turn-on-microsoft-threat-protection"></a><span data-ttu-id="ade4e-104">Activer la Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="ade4e-104">Turn on Microsoft Threat Protection</span></span>

<span data-ttu-id="ade4e-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="ade4e-105">**Applies to:**</span></span>
- <span data-ttu-id="ade4e-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="ade4e-106">Microsoft Threat Protection</span></span>

<span data-ttu-id="ade4e-107">La Protection Microsoft contre les menaces unifie votre processus de réponse aux incidents en intégrant les principales fonctionnalités de Microsoft Defender - Protection avancée contre les menaces (ATP), Office 365 - Protection avancée contre les menaces, Microsoft Cloud App Security et Azure ATP.</span><span class="sxs-lookup"><span data-stu-id="ade4e-107">Microsoft Threat Protection unifies your incident response process by integrating key capabilities across Microsoft Defender Advanced Threat Protection (ATP), Office 365 ATP, Microsoft Cloud App Security, and Azure ATP.</span></span> <span data-ttu-id="ade4e-108">Cette expérience unifiée ajoute des fonctionnalités puissantes auxquelles vous pouvez accéder dans le Centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="ade4e-108">This unified experience adds powerful features you can access in the Microsoft 365 security center.</span></span>

<span data-ttu-id="ade4e-109">Pour bénéficier de la meilleure protection et optimiser la protection Microsoft contre les menaces, nous vous recommandons de déployer tous les services pris en charge applicables sur votre réseau.</span><span class="sxs-lookup"><span data-stu-id="ade4e-109">To get the best protection and optimize Microsoft Threat Protection, we recommend deploying all applicable supported services on your network.</span></span> <span data-ttu-id="ade4e-110">Pour plus d’informations, consultez la rubrique [Deploying Supported services](deploy-supported-services.md).</span><span class="sxs-lookup"><span data-stu-id="ade4e-110">For more information, [read about deploying supported services](deploy-supported-services.md).</span></span>

## <a name="check-license-eligibility-and-required-permissions"></a><span data-ttu-id="ade4e-111">Vérifier l’éligibilité de la licence et les autorisations requises</span><span class="sxs-lookup"><span data-stu-id="ade4e-111">Check license eligibility and required permissions</span></span>
<span data-ttu-id="ade4e-112">Une licence Microsoft 365 E5, E5 Security, a5 ou a5 ou une combinaison valide de licences donne accès aux services pris en charge et vous permet d’utiliser la protection Microsoft contre les menaces dans le centre de sécurité Microsoft 365 sans coût de licence supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="ade4e-112">A Microsoft 365 E5, E5 Security, A5, or A5 Security license or a valid combination of licenses provides access to supported services and entitles you to use Microsoft Threat Protection in Microsoft 365 security center without additional licensing cost.</span></span>

<span data-ttu-id="ade4e-113">Pour obtenir des informations détaillées sur les licences, [Lisez les conditions relatives aux licences](prerequisites.md#licensing-requirements).</span><span class="sxs-lookup"><span data-stu-id="ade4e-113">For detailed licensing information, [read the licensing requirements](prerequisites.md#licensing-requirements).</span></span>

### <a name="check-your-role"></a><span data-ttu-id="ade4e-114">Vérifier votre rôle</span><span class="sxs-lookup"><span data-stu-id="ade4e-114">Check your role</span></span>
<span data-ttu-id="ade4e-115">Vous devez être **administrateur général** ou administrateur de **sécurité** dans Azure Active Directory pour activer Microsoft Threat Protection.</span><span class="sxs-lookup"><span data-stu-id="ade4e-115">You must be a **global administrator** or a **security administrator** in Azure Active Directory to turn on Microsoft Threat Protection.</span></span> [<span data-ttu-id="ade4e-116">Afficher vos rôles dans Azure AD</span><span class="sxs-lookup"><span data-stu-id="ade4e-116">View your roles in Azure AD</span></span>](https://docs.microsoft.com//azure/active-directory/users-groups-roles/directory-manage-roles-portal)

## <a name="start-using-the-service"></a><span data-ttu-id="ade4e-117">Commencez à utiliser le service</span><span class="sxs-lookup"><span data-stu-id="ade4e-117">Start using the service</span></span>

>[!IMPORTANT]
><span data-ttu-id="ade4e-118">À partir du 3 mai 2020, Microsoft mettra progressivement en place de nouvelles expériences optimisées en [matière de licences](prerequisites.md#licensing-requirements) et d’activation de la protection contre les menaces Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ade4e-118">Starting May 3, 2020, Microsoft will gradually roll out new, optimized experiences around [licensing requirements](prerequisites.md#licensing-requirements) and turning on Microsoft Threat Protection.</span></span> <span data-ttu-id="ade4e-119">Pendant plusieurs semaines pendant cette période, certains clients commencent à voir les modifications apportées à leurs expériences de portail.</span><span class="sxs-lookup"><span data-stu-id="ade4e-119">For several weeks during this period, some customers will start to see changes to their portal experiences.</span></span> <span data-ttu-id="ade4e-120">Les informations sur les nouvelles expériences sont marquées **nouvelle expérience** dans cet article.</span><span class="sxs-lookup"><span data-stu-id="ade4e-120">Information about the new experiences are marked **New experience** in this article.</span></span>

<span data-ttu-id="ade4e-121">Microsoft Threat Protection agrège les données des différents services intégrés.</span><span class="sxs-lookup"><span data-stu-id="ade4e-121">Microsoft Threat Protection aggregates data from the various integrated services.</span></span> <span data-ttu-id="ade4e-122">Il traitera et stockera les données de manière centralisée afin d’identifier les nouvelles idées et de créer des flux de travail de réponse centralisée.</span><span class="sxs-lookup"><span data-stu-id="ade4e-122">It will process and store data centrally to identify new insights and make centralized response workflows possible.</span></span> <span data-ttu-id="ade4e-123">Il effectue cette opération sans affecter les déploiements, paramètres ou données existants associés aux services intégrés.</span><span class="sxs-lookup"><span data-stu-id="ade4e-123">It does this without affecting existing deployments, settings, or data associated with the integrated services.</span></span>

<span data-ttu-id="ade4e-124">Avant d’activer le service, le centre de sécurité Microsoft 365 ([Security.Microsoft.com](https://security.microsoft.com)) affiche la **page d’accueil** de la protection de Microsoft contre les menaces lorsque vous sélectionnez **incidents**, **Centre de maintenance**ou sélection dans le volet de navigation.</span><span class="sxs-lookup"><span data-stu-id="ade4e-124">Before you turn on the service, the Microsoft 365 security center ([security.microsoft.com](https://security.microsoft.com)) shows the Microsoft Threat Protection welcome page when you select **Incidents**, **Action center**, or **Hunting** from the navigation pane.</span></span> <span data-ttu-id="ade4e-125">Ces options de navigation ne s’affichent pas si vous n’êtes pas éligible à l’utilisation de la protection contre les menaces Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ade4e-125">These navigation options are not shown if you are not eligible to use Microsoft Threat Protection.</span></span>

<span data-ttu-id="ade4e-126">![Image de la page d’accueil de la protection de Microsoft contre les menaces affichée si Microsoft Threat](../../media/mtp-welcome.png)
protection n’a pas été activé sur la*page d’accueil de Microsoft Threat Protection dans le centre de sécurité Microsoft 365*</span><span class="sxs-lookup"><span data-stu-id="ade4e-126">![Image of the Microsoft Threat Protection welcome page shown if Microsoft Threat Protection has not been turned on](../../media/mtp-welcome.png)
*Microsoft Threat Protection welcome page in Microsoft 365 security center*</span></span>

<span data-ttu-id="ade4e-127">Pour activer Microsoft Threat Protection, terminez simplement le processus à partir de la page d’accueil.</span><span class="sxs-lookup"><span data-stu-id="ade4e-127">To turn on Microsoft Threat Protection, simply complete the process from the welcome page.</span></span> <span data-ttu-id="ade4e-128">Vous pouvez également activer Microsoft Threat Protection en accédant aux **paramètres** ([Security.Microsoft.com/Settings](https://security.microsoft.com/settings)) dans le volet de navigation et en sélectionnant **Microsoft Threat Protection**.</span><span class="sxs-lookup"><span data-stu-id="ade4e-128">You can also turn on Microsoft Threat Protection by accessing **Settings** ([security.microsoft.com/settings](https://security.microsoft.com/settings)) in the navigation pane and selecting **Microsoft Threat Protection**.</span></span>

>[!NOTE]
><span data-ttu-id="ade4e-129">Si vous ne voyez pas les **paramètres** dans le volet de navigation ou que vous n’avez pas accès à la page, vérifiez vos autorisations et licences.</span><span class="sxs-lookup"><span data-stu-id="ade4e-129">If you don't see **Settings** in the navigation pane or couldn't access the page, check your permissions and licenses.</span></span>       

### <a name="select-data-center-location"></a><span data-ttu-id="ade4e-130">Sélectionner l’emplacement du centre de données</span><span class="sxs-lookup"><span data-stu-id="ade4e-130">Select data center location</span></span>
<span data-ttu-id="ade4e-131">Si Microsoft Defender - Protection avancée contre les menaces a été configuré pour votre organisation, les données sont stockées et traitées dans le même emplacement de centre de données que celui que vous avez sélectionné pour [vos données Microsoft Defender – Protection avancée contre les menaces](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/data-storage-privacy).</span><span class="sxs-lookup"><span data-stu-id="ade4e-131">If Microsoft Defender ATP has been provisioned for your organization, data will be stored and processed in the same data center location you have selected for [your Microsoft Defender ATP data](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/data-storage-privacy).</span></span> <span data-ttu-id="ade4e-132">Si vous n’avez pas Microsoft Defender ATP, vous serez invité à choisir un nouvel emplacement de centre de données spécifiquement pour la Protection Microsoft contre les menaces.</span><span class="sxs-lookup"><span data-stu-id="ade4e-132">If you don't have Microsoft Defender ATP, you will be asked to choose a new data center location specifically for Microsoft Threat Protection.</span></span> 
 
<span data-ttu-id="ade4e-133">Vous devez fournir le consentement avant le partage des données entre les services et l’agrégation.</span><span class="sxs-lookup"><span data-stu-id="ade4e-133">You need to provide consent before data is shared between services and aggregated.</span></span>

<span data-ttu-id="ade4e-134">**Nouvelle expérience :** À partir du 3 mai, 2020, les clients recevront progressivement les modifications apportées à cette expérience.</span><span class="sxs-lookup"><span data-stu-id="ade4e-134">**New experience:** Starting May 3, 2020, customers will gradually receive changes to this experience.</span></span> <span data-ttu-id="ade4e-135">Pour les personnes ayant la nouvelle expérience, le service sélectionne automatiquement l’emplacement de centre de données optimal pour vos données agrégées en fonction de vos services de sécurité Microsoft 365 existants.</span><span class="sxs-lookup"><span data-stu-id="ade4e-135">For those with the new experience, the service automatically selects the optimal data center location for your aggregated data based on your existing Microsoft 365 security services.</span></span> <span data-ttu-id="ade4e-136">L’emplacement du centre de données sélectionné est affiché à l’écran.</span><span class="sxs-lookup"><span data-stu-id="ade4e-136">The selected data center location is shown in the screen.</span></span>

### <a name="confirm-that-the-service-is-on"></a><span data-ttu-id="ade4e-137">Vérifiez que le service est activé</span><span class="sxs-lookup"><span data-stu-id="ade4e-137">Confirm that the service is on</span></span>
<span data-ttu-id="ade4e-138">Une fois le service configuré, il ajoute :</span><span class="sxs-lookup"><span data-stu-id="ade4e-138">Once the service is provisioned, it adds:</span></span>

- [<span data-ttu-id="ade4e-139">Gestion des incidents</span><span class="sxs-lookup"><span data-stu-id="ade4e-139">Incidents management</span></span>](incidents-overview.md)
- <span data-ttu-id="ade4e-140">Centre de notifications pour la gestion des [examen et réponse automatisés](mtp-autoir.md)</span><span class="sxs-lookup"><span data-stu-id="ade4e-140">An action center for managing [automated investigation and response](mtp-autoir.md)</span></span>
- <span data-ttu-id="ade4e-141">Fonctionnalités de [chasse avancées](advanced-hunting-overview.md)</span><span class="sxs-lookup"><span data-stu-id="ade4e-141">[Advanced hunting](advanced-hunting-overview.md) capabilities</span></span>

<span data-ttu-id="ade4e-142">![Image du volet de navigation du centre de sécurité Microsoft 365 avec les](../../media/mtp-on.png)
fonctionnalités de protection de Microsoft Threat*Centre de sécurité Microsoft 365 avec gestion des incidents et autres fonctionnalités de protection contre les menaces Microsoft*</span><span class="sxs-lookup"><span data-stu-id="ade4e-142">![Image of Microsoft 365 security center navigation pane with Microsoft Threat Protection features](../../media/mtp-on.png)
*Microsoft 365 security center with incidents management and other Microsoft Threat Protection capabilities*</span></span>

### <a name="getting-azure-atp-data"></a><span data-ttu-id="ade4e-143">Obtention de données Azure ATP</span><span class="sxs-lookup"><span data-stu-id="ade4e-143">Getting Azure ATP data</span></span>
<span data-ttu-id="ade4e-144">Pour partager des données Azure ATP avec la Protection Microsoft contre les menaces, assurez-vous que Microsoft Cloud App Security et l’intégration Azure ATP sont activées.</span><span class="sxs-lookup"><span data-stu-id="ade4e-144">To share Azure ATP data with Microsoft Threat Protection, ensure that Microsoft Cloud App Security and Azure ATP integration is turned on.</span></span> [<span data-ttu-id="ade4e-145">Découvrez cette intégration</span><span class="sxs-lookup"><span data-stu-id="ade4e-145">Learn more about this integration</span></span>](https://docs.microsoft.com/cloud-app-security/aatp-integration)


## <a name="turn-off-microsoft-threat-protection"></a><span data-ttu-id="ade4e-146">Désactiver la Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="ade4e-146">Turn off Microsoft Threat Protection</span></span>
<span data-ttu-id="ade4e-147">Pour cesser d’utiliser la Protection Microsoft contre les menaces, accédez à **Paramètres** > **Protection Microsoft contre les menaces** > **Accepter / Refuser** dans le Centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="ade4e-147">To stop using Microsoft Threat Protection, go to **Settings** > **Microsoft Threat Protection** > **Opt-in / Opt-out** in the Microsoft 365 security center.</span></span> <span data-ttu-id="ade4e-148">Désélectionnez **Activer la Protection Microsoft contre les menaces** et enregistrez les modifications.</span><span class="sxs-lookup"><span data-stu-id="ade4e-148">Unselect **Turn on Microsoft Threat Protection** and save the changes.</span></span>

<span data-ttu-id="ade4e-149">Les fonctionnalités correspondantes seront supprimées du centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="ade4e-149">Corresponding features will be removed from the Microsoft 365 security center.</span></span>

## <a name="get-assistance"></a><span data-ttu-id="ade4e-150">Obtenir de l'aide</span><span class="sxs-lookup"><span data-stu-id="ade4e-150">Get assistance</span></span>

<span data-ttu-id="ade4e-151">Le personnel du support Microsoft peut vous aider à mettre en service ou à mettre hors service le service et les ressources associées sur votre client.</span><span class="sxs-lookup"><span data-stu-id="ade4e-151">Microsoft support staff can help provision or deprovision the service and related resources on your tenant.</span></span> <span data-ttu-id="ade4e-152">Pour obtenir de l’aide, sélectionnez **besoin d’aide ?** dans le centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="ade4e-152">For assistance, select **Need help?** in the Microsoft 365 security center.</span></span> <span data-ttu-id="ade4e-153">Lorsque vous contactez le support technique, mentionnez Microsoft Threat Protection.</span><span class="sxs-lookup"><span data-stu-id="ade4e-153">When contacting support, mention Microsoft Threat Protection.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ade4e-154">Sujets associés</span><span class="sxs-lookup"><span data-stu-id="ade4e-154">Related topics</span></span>

- [<span data-ttu-id="ade4e-155">Vue d’ensemble de la Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="ade4e-155">Microsoft Threat Protection overview</span></span>](microsoft-threat-protection.md)
- [<span data-ttu-id="ade4e-156">Conditions requises et autres conditions préalables relatives aux licences</span><span class="sxs-lookup"><span data-stu-id="ade4e-156">Licensing requirements and other prerequisites</span></span>](prerequisites.md)
- [<span data-ttu-id="ade4e-157">Déployer les services pris en charge</span><span class="sxs-lookup"><span data-stu-id="ade4e-157">Deploy supported services</span></span>](deploy-supported-services.md)
- [<span data-ttu-id="ade4e-158">Vue d’ensemble de Microsoft Defender - Protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="ade4e-158">Microsoft Defender ATP overview</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection)
- [<span data-ttu-id="ade4e-159">Vue d’ensemble d’Office 365 – Protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="ade4e-159">Office 365 ATP overview</span></span>](../office-365-security/office-365-atp.md)
- [<span data-ttu-id="ade4e-160">Vue d’ensemble de Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="ade4e-160">Microsoft Cloud App Security overview</span></span>](https://docs.microsoft.com/cloud-app-security/what-is-cloud-app-security)
- [<span data-ttu-id="ade4e-161">Vue d’ensemble d’Azure ATP</span><span class="sxs-lookup"><span data-stu-id="ade4e-161">Azure ATP overview</span></span>](https://docs.microsoft.com/azure-advanced-threat-protection/what-is-atp)
- [<span data-ttu-id="ade4e-162">Stockage de données Microsoft Defender - Protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="ade4e-162">Microsoft Defender ATP data storage</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/data-storage-privacy)
