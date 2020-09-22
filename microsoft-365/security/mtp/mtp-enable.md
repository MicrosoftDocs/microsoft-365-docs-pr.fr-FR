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
ms.openlocfilehash: 65e3a2609bc41ddeda95134874e5873e184a2a54
ms.sourcegitcommit: c083602dda3cdcb5b58cb8aa070d77019075f765
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/22/2020
ms.locfileid: "48201158"
---
# <a name="turn-on-microsoft-threat-protection"></a><span data-ttu-id="99379-104">Activer la Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="99379-104">Turn on Microsoft Threat Protection</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="99379-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="99379-105">**Applies to:**</span></span>
- <span data-ttu-id="99379-106">Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="99379-106">Microsoft Threat Protection</span></span>

<span data-ttu-id="99379-107">La [protection de Microsoft contre les menaces](microsoft-threat-protection.md) unifie votre processus de réponse aux incidents en intégrant des fonctionnalités clés dans la protection avancée contre les menaces Microsoft Defender, Office 365 ATP, la sécurité des applications Cloud Microsoft et Azure ATP.</span><span class="sxs-lookup"><span data-stu-id="99379-107">[Microsoft Threat Protection](microsoft-threat-protection.md) unifies your incident response process by integrating key capabilities across Microsoft Defender Advanced Threat Protection (ATP), Office 365 ATP, Microsoft Cloud App Security, and Azure ATP.</span></span> <span data-ttu-id="99379-108">Cette expérience unifiée ajoute des fonctionnalités puissantes auxquelles vous pouvez accéder dans le Centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="99379-108">This unified experience adds powerful features you can access in the Microsoft 365 security center.</span></span>

<span data-ttu-id="99379-109">La protection contre les menaces Microsoft s’active automatiquement lorsque les clients éligibles disposant des autorisations requises se reporter au centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="99379-109">Microsoft Threat Protection automatically turns on when eligible customers with the required permissions visit Microsoft 365 security center.</span></span> <span data-ttu-id="99379-110">Lisez cet article pour comprendre les différentes conditions préalables et la configuration de la protection contre les menaces Microsoft.</span><span class="sxs-lookup"><span data-stu-id="99379-110">Read this article to understand various prerequisites and how Microsoft Threat Protection is provisioned.</span></span>

## <a name="check-license-eligibility-and-required-permissions"></a><span data-ttu-id="99379-111">Vérifier l’éligibilité de la licence et les autorisations requises</span><span class="sxs-lookup"><span data-stu-id="99379-111">Check license eligibility and required permissions</span></span>
<span data-ttu-id="99379-112">Une licence pour un produit de sécurité Microsoft 365 vous permet généralement d’utiliser la protection Microsoft contre les menaces dans le centre de sécurité Microsoft 365 sans coût de licence supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="99379-112">A license to a Microsoft 365 security product generally entitles you to use Microsoft Threat Protection in Microsoft 365 security center without additional licensing cost.</span></span> <span data-ttu-id="99379-113">Nous vous recommandons d’obtenir une licence de sécurité Microsoft 365 E5, E5 sécurité, a5 ou a5 ou une combinaison valide de licences qui donne accès à tous les services pris en charge.</span><span class="sxs-lookup"><span data-stu-id="99379-113">We do recommend getting a Microsoft 365 E5, E5 Security, A5, or A5 Security license or a valid combination of licenses that provides access to all supported services.</span></span>

<span data-ttu-id="99379-114">Pour obtenir des informations détaillées sur les licences, [Lisez les conditions relatives aux licences](prerequisites.md#licensing-requirements).</span><span class="sxs-lookup"><span data-stu-id="99379-114">For detailed licensing information, [read the licensing requirements](prerequisites.md#licensing-requirements).</span></span>

### <a name="check-your-role"></a><span data-ttu-id="99379-115">Vérifier votre rôle</span><span class="sxs-lookup"><span data-stu-id="99379-115">Check your role</span></span>
<span data-ttu-id="99379-116">Vous devez être **administrateur général** ou administrateur de **sécurité** dans Azure Active Directory pour activer Microsoft Threat Protection.</span><span class="sxs-lookup"><span data-stu-id="99379-116">You must be a **global administrator** or a **security administrator** in Azure Active Directory to turn on Microsoft Threat Protection.</span></span> [<span data-ttu-id="99379-117">Afficher vos rôles dans Azure AD</span><span class="sxs-lookup"><span data-stu-id="99379-117">View your roles in Azure AD</span></span>](https://docs.microsoft.com//azure/active-directory/users-groups-roles/directory-manage-roles-portal)

## <a name="supported-services"></a><span data-ttu-id="99379-118">Services pris en charge</span><span class="sxs-lookup"><span data-stu-id="99379-118">Supported services</span></span>
<span data-ttu-id="99379-119">Microsoft Threat Protection agrège les données à partir des différents services pris en charge que vous avez déjà déployés.</span><span class="sxs-lookup"><span data-stu-id="99379-119">Microsoft Threat Protection aggregates data from the various supported services that you've already deployed.</span></span> <span data-ttu-id="99379-120">Il traitera et stockera les données de manière centralisée afin d’identifier les nouvelles idées et de créer des flux de travail de réponse centralisée.</span><span class="sxs-lookup"><span data-stu-id="99379-120">It will process and store data centrally to identify new insights and make centralized response workflows possible.</span></span> <span data-ttu-id="99379-121">Il effectue cette opération sans affecter les déploiements, paramètres ou données existants associés aux services intégrés.</span><span class="sxs-lookup"><span data-stu-id="99379-121">It does this without affecting existing deployments, settings, or data associated with the integrated services.</span></span>

<span data-ttu-id="99379-122">Pour bénéficier de la meilleure protection et optimiser la protection Microsoft contre les menaces, nous vous recommandons de déployer tous les services pris en charge applicables sur votre réseau.</span><span class="sxs-lookup"><span data-stu-id="99379-122">To get the best protection and optimize Microsoft Threat Protection, we recommend deploying all applicable supported services on your network.</span></span> <span data-ttu-id="99379-123">Pour plus d’informations, consultez la rubrique [Deploying Supported services](deploy-supported-services.md).</span><span class="sxs-lookup"><span data-stu-id="99379-123">For more information, [read about deploying supported services](deploy-supported-services.md).</span></span>

## <a name="before-starting-the-service"></a><span data-ttu-id="99379-124">Avant de démarrer le service</span><span class="sxs-lookup"><span data-stu-id="99379-124">Before starting the service</span></span>
<span data-ttu-id="99379-125">Avant d’activer le service, le centre de sécurité Microsoft 365 ([Security.Microsoft.com](https://security.microsoft.com)) affiche la page Paramètres de protection de Microsoft contre les menaces lorsque vous sélectionnez **incidents**, **Centre de maintenance** **ou sélection** dans le volet de navigation.</span><span class="sxs-lookup"><span data-stu-id="99379-125">Before you turn on the service, the Microsoft 365 security center ([security.microsoft.com](https://security.microsoft.com)) shows the Microsoft Threat Protection settings page when you select **Incidents**, **Action center**, or **Hunting** from the navigation pane.</span></span> <span data-ttu-id="99379-126">Ces éléments de navigation ne s’affichent pas si vous n’êtes pas éligible à l’utilisation de la protection contre les menaces Microsoft.</span><span class="sxs-lookup"><span data-stu-id="99379-126">These navigation items are not shown if you are not eligible to use Microsoft Threat Protection.</span></span>

<span data-ttu-id="99379-127">![Image de la page des paramètres de protection contre les menaces Microsoft affichée si Microsoft Threat Protection n’a pas été activé sur les ](../../media/mtp-enable/mtp-settings.png)
 *paramètres de protection contre les menaces Microsoft dans le centre de sécurité Microsoft 365*</span><span class="sxs-lookup"><span data-stu-id="99379-127">![Image of the Microsoft Threat Protection settings page shown if Microsoft Threat Protection has not been turned on](../../media/mtp-enable/mtp-settings.png)
*Microsoft Threat Protection settings in Microsoft 365 security center*</span></span>

## <a name="starting-the-service"></a><span data-ttu-id="99379-128">Démarrage du service</span><span class="sxs-lookup"><span data-stu-id="99379-128">Starting the service</span></span>
<span data-ttu-id="99379-129">Pour activer Microsoft Threat Protection, sélectionnez simplement **activer la protection contre Microsoft Threat** et appliquer la modification.</span><span class="sxs-lookup"><span data-stu-id="99379-129">To turn on Microsoft Threat Protection, simply select **Turn on Microsoft Threat Protection** and apply the change.</span></span> <span data-ttu-id="99379-130">Vous pouvez également accéder à cette option en sélectionnant **paramètres** ([Security.Microsoft.com/Settings](https://security.microsoft.com/settings)) dans le volet de navigation, puis en sélectionnant **protection Microsoft contre les menaces**.</span><span class="sxs-lookup"><span data-stu-id="99379-130">You can also access this option by selecting **Settings** ([security.microsoft.com/settings](https://security.microsoft.com/settings)) in the navigation pane and then selecting **Microsoft Threat Protection**.</span></span>

>[!NOTE]
><span data-ttu-id="99379-131">Si vous ne voyez pas les **paramètres** dans le volet de navigation ou que vous n’avez pas accès à la page, vérifiez vos autorisations et licences.</span><span class="sxs-lookup"><span data-stu-id="99379-131">If you don't see **Settings** in the navigation pane or couldn't access the page, check your permissions and licenses.</span></span>

### <a name="data-center-location"></a><span data-ttu-id="99379-132">Emplacement du centre de données</span><span class="sxs-lookup"><span data-stu-id="99379-132">Data center location</span></span>
<span data-ttu-id="99379-133">Microsoft Threat Protection stocke et traite les données au [même emplacement que celui utilisé par Microsoft Defender ATP](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/data-storage-privacy).</span><span class="sxs-lookup"><span data-stu-id="99379-133">Microsoft Threat Protection will store and process data in the [same location used by Microsoft Defender ATP](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/data-storage-privacy).</span></span> <span data-ttu-id="99379-134">Si vous ne disposez pas de Microsoft Defender ATP, un nouvel emplacement de centre de données est automatiquement sélectionné en fonction de l’emplacement des services de sécurité Microsoft 365 actifs.</span><span class="sxs-lookup"><span data-stu-id="99379-134">If you don't have Microsoft Defender ATP, a new data center location is automatically selected based on the location of active Microsoft 365 security services.</span></span> <span data-ttu-id="99379-135">L’emplacement du centre de données sélectionné est affiché à l’écran.</span><span class="sxs-lookup"><span data-stu-id="99379-135">The selected data center location is shown in the screen.</span></span> 

<span data-ttu-id="99379-136">Sélectionnez **besoin d’aide ?** dans le centre de sécurité Microsoft 365 pour contacter le support Microsoft sur la mise en service de la protection contre les menaces Microsoft dans un autre emplacement de centre de données.</span><span class="sxs-lookup"><span data-stu-id="99379-136">Select **Need help?** in the Microsoft 365 security center to contact Microsoft support about provisioning Microsoft Threat Protection in a different data center location.</span></span> 

>[!NOTE]
><span data-ttu-id="99379-137">Microsoft Defender s’approvisionne automatiquement dans les centres de données de l’Union européenne (UE) lors de l’activation via le centre de sécurité Azure.</span><span class="sxs-lookup"><span data-stu-id="99379-137">Microsoft Defender ATP automatically provisions in European Union (EU) data centers when turned on through Azure Security Center.</span></span> <span data-ttu-id="99379-138">La protection Microsoft contre les menaces est automatiquement mise en service dans le centre de données de l’UE pour les clients qui ont configuré Microsoft Defender ATP de cette manière.</span><span class="sxs-lookup"><span data-stu-id="99379-138">Microsoft Threat Protection will automatically provision in the same EU data center for customers who have provisioned Microsoft Defender ATP in this manner.</span></span> 

### <a name="confirm-that-the-service-is-on"></a><span data-ttu-id="99379-139">Vérifiez que le service est activé</span><span class="sxs-lookup"><span data-stu-id="99379-139">Confirm that the service is on</span></span>
<span data-ttu-id="99379-140">Une fois le service configuré, il ajoute :</span><span class="sxs-lookup"><span data-stu-id="99379-140">Once the service is provisioned, it adds:</span></span>

- [<span data-ttu-id="99379-141">Gestion des incidents</span><span class="sxs-lookup"><span data-stu-id="99379-141">Incidents management</span></span>](incidents-overview.md)
- <span data-ttu-id="99379-142">Centre de notifications pour la gestion des [examen et réponse automatisés](mtp-autoir.md)</span><span class="sxs-lookup"><span data-stu-id="99379-142">An action center for managing [automated investigation and response](mtp-autoir.md)</span></span>
- <span data-ttu-id="99379-143">Fonctionnalités de [chasse avancées](advanced-hunting-overview.md)</span><span class="sxs-lookup"><span data-stu-id="99379-143">[Advanced hunting](advanced-hunting-overview.md) capabilities</span></span>

<span data-ttu-id="99379-144">![Image du volet de navigation du centre de sécurité Microsoft 365 avec les fonctionnalités de protection de Microsoft Threat ](../../media/mtp-enable/mtp-on.png)
 *Centre de sécurité Microsoft 365 avec gestion des incidents et autres fonctionnalités de protection contre les menaces Microsoft*</span><span class="sxs-lookup"><span data-stu-id="99379-144">![Image of Microsoft 365 security center navigation pane with Microsoft Threat Protection features](../../media/mtp-enable/mtp-on.png)
*Microsoft 365 security center with incidents management and other Microsoft Threat Protection capabilities*</span></span>

### <a name="getting-azure-atp-data"></a><span data-ttu-id="99379-145">Obtention de données Azure ATP</span><span class="sxs-lookup"><span data-stu-id="99379-145">Getting Azure ATP data</span></span>
<span data-ttu-id="99379-146">Pour partager des données Azure ATP avec la Protection Microsoft contre les menaces, assurez-vous que Microsoft Cloud App Security et l’intégration Azure ATP sont activées.</span><span class="sxs-lookup"><span data-stu-id="99379-146">To share Azure ATP data with Microsoft Threat Protection, ensure that Microsoft Cloud App Security and Azure ATP integration is turned on.</span></span> [<span data-ttu-id="99379-147">Découvrez cette intégration</span><span class="sxs-lookup"><span data-stu-id="99379-147">Learn more about this integration</span></span>](https://docs.microsoft.com/cloud-app-security/aatp-integration)


## <a name="turn-off-microsoft-threat-protection"></a><span data-ttu-id="99379-148">Désactiver la Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="99379-148">Turn off Microsoft Threat Protection</span></span>
<span data-ttu-id="99379-149">Pour cesser d’utiliser la Protection Microsoft contre les menaces, accédez à **Paramètres** > **Protection Microsoft contre les menaces** > **Accepter / Refuser** dans le Centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="99379-149">To stop using Microsoft Threat Protection, go to **Settings** > **Microsoft Threat Protection** > **Opt-in / Opt-out** in the Microsoft 365 security center.</span></span> <span data-ttu-id="99379-150">Désélectionnez **activer la protection de Microsoft contre les menaces** et appliquer les modifications.</span><span class="sxs-lookup"><span data-stu-id="99379-150">Unselect **Turn on Microsoft Threat Protection** and apply the changes.</span></span>

<span data-ttu-id="99379-151">Les fonctionnalités correspondantes seront supprimées du centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="99379-151">Corresponding features will be removed from the Microsoft 365 security center.</span></span>

## <a name="get-assistance"></a><span data-ttu-id="99379-152">Obtenir de l'aide</span><span class="sxs-lookup"><span data-stu-id="99379-152">Get assistance</span></span>

<span data-ttu-id="99379-153">Pour obtenir des réponses aux questions les plus fréquemment posées sur l’activation de Microsoft Threat Protection, [Lisez le Forum aux](mtp-enable-faq.md)questions.</span><span class="sxs-lookup"><span data-stu-id="99379-153">To get answers to the most commonly asked questions about turning on Microsoft Threat Protection, [read the FAQ](mtp-enable-faq.md).</span></span>

<span data-ttu-id="99379-154">Le personnel du support Microsoft peut vous aider à mettre en service ou à mettre hors service le service et les ressources associées sur votre client.</span><span class="sxs-lookup"><span data-stu-id="99379-154">Microsoft support staff can help provision or deprovision the service and related resources on your tenant.</span></span> <span data-ttu-id="99379-155">Pour obtenir de l’aide, sélectionnez **besoin d’aide ?** dans le centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="99379-155">For assistance, select **Need help?** in the Microsoft 365 security center.</span></span> <span data-ttu-id="99379-156">Lorsque vous contactez le support technique, mentionnez Microsoft Threat Protection.</span><span class="sxs-lookup"><span data-stu-id="99379-156">When contacting support, mention Microsoft Threat Protection.</span></span>

## <a name="related-topics"></a><span data-ttu-id="99379-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="99379-157">Related topics</span></span>

- [<span data-ttu-id="99379-158">Foire aux questions</span><span class="sxs-lookup"><span data-stu-id="99379-158">Frequently asked questions</span></span>](mtp-enable-faq.md)
- [<span data-ttu-id="99379-159">Conditions requises et autres conditions préalables relatives aux licences</span><span class="sxs-lookup"><span data-stu-id="99379-159">Licensing requirements and other prerequisites</span></span>](prerequisites.md)
- [<span data-ttu-id="99379-160">Déployer les services pris en charge</span><span class="sxs-lookup"><span data-stu-id="99379-160">Deploy supported services</span></span>](deploy-supported-services.md)
- [<span data-ttu-id="99379-161">Vue d’ensemble de la Protection Microsoft contre les menaces</span><span class="sxs-lookup"><span data-stu-id="99379-161">Microsoft Threat Protection overview</span></span>](microsoft-threat-protection.md)
- [<span data-ttu-id="99379-162">Vue d’ensemble de Microsoft Defender - Protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="99379-162">Microsoft Defender ATP overview</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection)
- [<span data-ttu-id="99379-163">Vue d’ensemble d’Office 365 – Protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="99379-163">Office 365 ATP overview</span></span>](../office-365-security/office-365-atp.md)
- [<span data-ttu-id="99379-164">Vue d’ensemble de Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="99379-164">Microsoft Cloud App Security overview</span></span>](https://docs.microsoft.com/cloud-app-security/what-is-cloud-app-security)
- [<span data-ttu-id="99379-165">Vue d’ensemble d’Azure ATP</span><span class="sxs-lookup"><span data-stu-id="99379-165">Azure ATP overview</span></span>](https://docs.microsoft.com/azure-advanced-threat-protection/what-is-atp)
- [<span data-ttu-id="99379-166">Stockage de données Microsoft Defender - Protection avancée contre les menaces</span><span class="sxs-lookup"><span data-stu-id="99379-166">Microsoft Defender ATP data storage</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/data-storage-privacy)
