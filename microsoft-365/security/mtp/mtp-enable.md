---
title: Activer Microsoft 365 Defender dans le Centre de sécurité Microsoft 365
description: Découvrez comment activer Microsoft 365 Defender et commencer à intégrer votre incident de sécurité et votre réponse.
keywords: commencer, activer MTP, Protection Microsoft contre les menaces, M365, sécurité, emplacement des données, autorisations requises, éligibilité aux licences, page paramètres
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
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
ms.technology: m365d
ms.openlocfilehash: 19f035a271626077911b05082a4aba6d67355cdb
ms.sourcegitcommit: 855719ee21017cf87dfa98cbe62806763bcb78ac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/22/2021
ms.locfileid: "49930221"
---
# <a name="turn-on-microsoft-365-defender"></a><span data-ttu-id="763ce-104">Activer Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="763ce-104">Turn on Microsoft 365 Defender</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="763ce-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="763ce-105">**Applies to:**</span></span>
- <span data-ttu-id="763ce-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="763ce-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="763ce-107">[Microsoft 365 Defender](microsoft-threat-protection.md) unifie votre processus de réponse aux incidents en intégrant des fonctionnalités clés dans Microsoft Defender pour le point de terminaison, Microsoft Defender pour Office 365, Microsoft Cloud App Security et Microsoft Defender pour l’identité.</span><span class="sxs-lookup"><span data-stu-id="763ce-107">[Microsoft 365 Defender](microsoft-threat-protection.md) unifies your incident response process by integrating key capabilities across Microsoft Defender for Endpoint, Microsoft Defender for Office 365, Microsoft Cloud App Security, and Microsoft Defender for Identity.</span></span> <span data-ttu-id="763ce-108">Cette expérience unifiée ajoute des fonctionnalités puissantes auxquelles vous pouvez accéder dans le Centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="763ce-108">This unified experience adds powerful features you can access in the Microsoft 365 security center.</span></span>

<span data-ttu-id="763ce-109">Microsoft 365 Defender s’allume automatiquement lorsque les clients éligibles ayant les autorisations requises visitent le Centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="763ce-109">Microsoft 365 Defender automatically turns on when eligible customers with the required permissions visit Microsoft 365 security center.</span></span> <span data-ttu-id="763ce-110">Lisez cet article pour comprendre les différents éléments prérequis et la façon dont Microsoft 365 Defender est mise en service.</span><span class="sxs-lookup"><span data-stu-id="763ce-110">Read this article to understand various prerequisites and how Microsoft 365 Defender is provisioned.</span></span>

## <a name="check-license-eligibility-and-required-permissions"></a><span data-ttu-id="763ce-111">Vérifier l’éligibilité aux licences et les autorisations requises</span><span class="sxs-lookup"><span data-stu-id="763ce-111">Check license eligibility and required permissions</span></span>

<span data-ttu-id="763ce-112">Une licence pour un produit de sécurité Microsoft 365 vous permet généralement d’utiliser Microsoft 365 Defender dans le Centre de sécurité Microsoft 365 sans coût de licence supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="763ce-112">A license to a Microsoft 365 security product generally entitles you to use Microsoft 365 Defender in Microsoft 365 security center without additional licensing cost.</span></span> <span data-ttu-id="763ce-113">Nous vous recommandons d’obtenir une licence Microsoft 365 E5, E5 Security, A5 ou A5 Security ou une combinaison valide de licences qui donne accès à tous les services pris en charge.</span><span class="sxs-lookup"><span data-stu-id="763ce-113">We do recommend getting a Microsoft 365 E5, E5 Security, A5, or A5 Security license or a valid combination of licenses that provides access to all supported services.</span></span>

<span data-ttu-id="763ce-114">Pour obtenir des informations détaillées sur les licences, [lisez les exigences de licence.](prerequisites.md#licensing-requirements)</span><span class="sxs-lookup"><span data-stu-id="763ce-114">For detailed licensing information, [read the licensing requirements](prerequisites.md#licensing-requirements).</span></span>

### <a name="check-your-role"></a><span data-ttu-id="763ce-115">Vérifier votre rôle</span><span class="sxs-lookup"><span data-stu-id="763ce-115">Check your role</span></span>

<span data-ttu-id="763ce-116">Vous devez être administrateur **général ou** **administrateur** de sécurité dans Azure Active Directory pour activer Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="763ce-116">You must be a **global administrator** or a **security administrator** in Azure Active Directory to turn on Microsoft 365 Defender.</span></span> [<span data-ttu-id="763ce-117">Afficher vos rôles dans Azure AD</span><span class="sxs-lookup"><span data-stu-id="763ce-117">View your roles in Azure AD</span></span>](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-manage-roles-portal)

## <a name="supported-services"></a><span data-ttu-id="763ce-118">Services pris en charge</span><span class="sxs-lookup"><span data-stu-id="763ce-118">Supported services</span></span>

<span data-ttu-id="763ce-119">Microsoft 365 Defender regroupe les données des différents services pris en charge que vous avez déjà déployés.</span><span class="sxs-lookup"><span data-stu-id="763ce-119">Microsoft 365 Defender aggregates data from the various supported services that you've already deployed.</span></span> <span data-ttu-id="763ce-120">Il traitera et stockera les données de manière centralisée pour identifier les nouvelles informations et rendre les flux de travail de réponse centralisés possibles.</span><span class="sxs-lookup"><span data-stu-id="763ce-120">It will process and store data centrally to identify new insights and make centralized response workflows possible.</span></span> <span data-ttu-id="763ce-121">Il le fait sans affecter les déploiements, paramètres ou données existants associés aux services intégrés.</span><span class="sxs-lookup"><span data-stu-id="763ce-121">It does this without affecting existing deployments, settings, or data associated with the integrated services.</span></span>

<span data-ttu-id="763ce-122">Pour obtenir la meilleure protection et optimiser Microsoft 365 Defender, nous vous recommandons de déployer tous les services pris en charge applicables sur votre réseau.</span><span class="sxs-lookup"><span data-stu-id="763ce-122">To get the best protection and optimize Microsoft 365 Defender, we recommend deploying all applicable supported services on your network.</span></span> <span data-ttu-id="763ce-123">Pour plus d’informations, [voir sur le déploiement des services pris en charge.](deploy-supported-services.md)</span><span class="sxs-lookup"><span data-stu-id="763ce-123">For more information, [read about deploying supported services](deploy-supported-services.md).</span></span>

## <a name="before-starting-the-service"></a><span data-ttu-id="763ce-124">Avant de démarrer le service</span><span class="sxs-lookup"><span data-stu-id="763ce-124">Before starting the service</span></span>

<span data-ttu-id="763ce-125">Avant d’activer le service, le Centre de sécurité Microsoft 365 ([security.microsoft.com](https://security.microsoft.com)) affiche la page des paramètres  de Microsoft 365 Defender lorsque vous sélectionnez **Incidents,** Centre de sécurité ou Recherche dans le volet de navigation.</span><span class="sxs-lookup"><span data-stu-id="763ce-125">Before you turn on the service, the Microsoft 365 security center ([security.microsoft.com](https://security.microsoft.com)) shows the Microsoft 365 Defender settings page when you select **Incidents**, **Action center**, or **Hunting** from the navigation pane.</span></span> <span data-ttu-id="763ce-126">Ces éléments de navigation ne sont pas affichés si vous n’êtes pas éligible pour utiliser Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="763ce-126">These navigation items are not shown if you are not eligible to use Microsoft 365 Defender.</span></span>

<span data-ttu-id="763ce-127">![Image de la page des paramètres de Microsoft 365 Defender affichée si Microsoft 365 Defender n’a pas été désactivé dans les paramètres de Microsoft 365 Defender dans le Centre de sécurité ](../../media/mtp-enable/mtp-settings.png)
 *Microsoft 365*</span><span class="sxs-lookup"><span data-stu-id="763ce-127">![Image of the Microsoft 365 Defender settings page shown if Microsoft 365 Defender has not been turned on](../../media/mtp-enable/mtp-settings.png)
*Microsoft 365 Defender settings in Microsoft 365 security center*</span></span>

## <a name="starting-the-service"></a><span data-ttu-id="763ce-128">Démarrage du service</span><span class="sxs-lookup"><span data-stu-id="763ce-128">Starting the service</span></span>

<span data-ttu-id="763ce-129">Pour activer Microsoft 365 Defender, sélectionnez simplement Activer **Microsoft 365 Defender** et appliquez la modification.</span><span class="sxs-lookup"><span data-stu-id="763ce-129">To turn on Microsoft 365 Defender, simply select **Turn on Microsoft 365 Defender** and apply the change.</span></span> <span data-ttu-id="763ce-130">Vous pouvez également accéder à cette option en sélectionnant **Paramètres** ([security.microsoft.com/settings](https://security.microsoft.com/settings)) dans le volet de navigation, puis en sélectionnant **Microsoft 365 Defender**.</span><span class="sxs-lookup"><span data-stu-id="763ce-130">You can also access this option by selecting **Settings** ([security.microsoft.com/settings](https://security.microsoft.com/settings)) in the navigation pane and then selecting **Microsoft 365 Defender**.</span></span>

> [!NOTE]
> <span data-ttu-id="763ce-131">Si vous ne voyez pas **Paramètres** dans le volet de navigation ou si vous n’avez pas pu accéder à la page, vérifiez vos autorisations et licences.</span><span class="sxs-lookup"><span data-stu-id="763ce-131">If you don't see **Settings** in the navigation pane or couldn't access the page, check your permissions and licenses.</span></span>

### <a name="data-center-location"></a><span data-ttu-id="763ce-132">Emplacement du centre de données</span><span class="sxs-lookup"><span data-stu-id="763ce-132">Data center location</span></span>

<span data-ttu-id="763ce-133">Microsoft 365 Defender stockera et traitera les données au même emplacement que celui utilisé par [Microsoft Defender pour le point de terminaison.](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/data-storage-privacy)</span><span class="sxs-lookup"><span data-stu-id="763ce-133">Microsoft 365 Defender will store and process data in the [same location used by Microsoft Defender for Endpoint](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/data-storage-privacy).</span></span> <span data-ttu-id="763ce-134">Si vous n’avez pas Microsoft Defender pour point de terminaison, un nouvel emplacement de centre de données est automatiquement sélectionné en fonction de l’emplacement des services de sécurité Microsoft 365 actifs.</span><span class="sxs-lookup"><span data-stu-id="763ce-134">If you don't have Microsoft Defender for Endpoint, a new data center location is automatically selected based on the location of active Microsoft 365 security services.</span></span> <span data-ttu-id="763ce-135">L’emplacement du centre de données sélectionné est affiché à l’écran.</span><span class="sxs-lookup"><span data-stu-id="763ce-135">The selected data center location is shown in the screen.</span></span>

<span data-ttu-id="763ce-136">Sélectionnez **Besoin d’aide ?** dans le Centre de sécurité Microsoft 365 pour contacter le support Microsoft concernant la mise en service de Microsoft 365 Defender dans un autre emplacement de centre de données.</span><span class="sxs-lookup"><span data-stu-id="763ce-136">Select **Need help?** in the Microsoft 365 security center to contact Microsoft support about provisioning Microsoft 365 Defender in a different data center location.</span></span>

> [!NOTE]
> <span data-ttu-id="763ce-137">Microsoft Defender pour le point de terminaison met automatiquement en services les centres de données de l’Union européenne (UE) lorsqu’il est allumé par le biais d’Azure Defender.</span><span class="sxs-lookup"><span data-stu-id="763ce-137">Microsoft Defender for Endpoint automatically provisions in European Union (EU) data centers when turned on through Azure Defender.</span></span> <span data-ttu-id="763ce-138">Microsoft 365 Defender sera automatiquement mis en service dans le même centre de données de l’UE pour les clients qui ont mis en service Defender pour endpoint de cette manière.</span><span class="sxs-lookup"><span data-stu-id="763ce-138">Microsoft 365 Defender will automatically provision in the same EU data center for customers who have provisioned Defender for Endpoint in this manner.</span></span>

### <a name="confirm-that-the-service-is-on"></a><span data-ttu-id="763ce-139">Vérifiez que le service est activé</span><span class="sxs-lookup"><span data-stu-id="763ce-139">Confirm that the service is on</span></span>

<span data-ttu-id="763ce-140">Une fois le service configuré, il ajoute :</span><span class="sxs-lookup"><span data-stu-id="763ce-140">Once the service is provisioned, it adds:</span></span>

- [<span data-ttu-id="763ce-141">Gestion des incidents</span><span class="sxs-lookup"><span data-stu-id="763ce-141">Incidents management</span></span>](incidents-overview.md)
- <span data-ttu-id="763ce-142">Centre de notifications pour la gestion des [examen et réponse automatisés](mtp-autoir.md)</span><span class="sxs-lookup"><span data-stu-id="763ce-142">An action center for managing [automated investigation and response](mtp-autoir.md)</span></span>
- <span data-ttu-id="763ce-143">[Fonctionnalités de recherche](advanced-hunting-overview.md) avancées</span><span class="sxs-lookup"><span data-stu-id="763ce-143">[Advanced hunting](advanced-hunting-overview.md) capabilities</span></span>

<span data-ttu-id="763ce-144">![Image du volet de navigation du Centre de sécurité Microsoft 365 avec Microsoft 365 Defender qui propose le Centre de sécurité Microsoft 365 avec la gestion des incidents et d’autres fonctionnalités de ](../../media/mtp-enable/mtp-on.png)
 *Microsoft 365 Defender*</span><span class="sxs-lookup"><span data-stu-id="763ce-144">![Image of Microsoft 365 security center navigation pane with Microsoft 365 Defender features](../../media/mtp-enable/mtp-on.png)
*Microsoft 365 security center with incidents management and other Microsoft 365 Defender capabilities*</span></span>

### <a name="getting-microsoft-defender-for-identity-data"></a><span data-ttu-id="763ce-145">Obtention de données Microsoft Defender pour l’identité</span><span class="sxs-lookup"><span data-stu-id="763ce-145">Getting Microsoft Defender for Identity data</span></span>

<span data-ttu-id="763ce-146">Pour partager des données Microsoft Defender pour l’identité avec Microsoft 365 Defender, assurez-vous que Microsoft Cloud App Security et l’intégration de Microsoft Defender pour l’identité sont allumés.</span><span class="sxs-lookup"><span data-stu-id="763ce-146">To share Microsoft Defender for Identity data with Microsoft 365 Defender, ensure that Microsoft Cloud App Security and Microsoft Defender for Identity integration is turned on.</span></span> <span data-ttu-id="763ce-147">[En savoir plus sur cette intégration.](https://docs.microsoft.com/cloud-app-security/mdi-integration)</span><span class="sxs-lookup"><span data-stu-id="763ce-147">[Learn more about this integration](https://docs.microsoft.com/cloud-app-security/mdi-integration).</span></span>

## <a name="get-assistance"></a><span data-ttu-id="763ce-148">Obtenir de l'aide</span><span class="sxs-lookup"><span data-stu-id="763ce-148">Get assistance</span></span>

<span data-ttu-id="763ce-149">Pour obtenir des réponses aux questions les plus fréquemment posées sur l’accès à Microsoft 365 Defender, [lisez le FAQ.](mtp-enable-faq.md)</span><span class="sxs-lookup"><span data-stu-id="763ce-149">To get answers to the most commonly asked questions about turning on Microsoft 365 Defender, [read the FAQ](mtp-enable-faq.md).</span></span>

<span data-ttu-id="763ce-150">Le personnel du support microsoft peut vous aider à fournir ou à désapprovisioner le service et les ressources associées sur votre client.</span><span class="sxs-lookup"><span data-stu-id="763ce-150">Microsoft support staff can help provision or deprovision the service and related resources on your tenant.</span></span> <span data-ttu-id="763ce-151">Pour obtenir de l’aide, **sélectionnez Besoin d’aide ?** dans le Centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="763ce-151">For assistance, select **Need help?** in the Microsoft 365 security center.</span></span> <span data-ttu-id="763ce-152">Lorsque vous contactez le support technique, mentionnez Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="763ce-152">When contacting support, mention Microsoft 365 Defender.</span></span>

## <a name="related-topics"></a><span data-ttu-id="763ce-153">Rubriques associées</span><span class="sxs-lookup"><span data-stu-id="763ce-153">Related topics</span></span>

- [<span data-ttu-id="763ce-154">Forum aux questions</span><span class="sxs-lookup"><span data-stu-id="763ce-154">Frequently asked questions</span></span>](mtp-enable-faq.md)
- [<span data-ttu-id="763ce-155">Conditions requises et autres conditions préalables relatives aux licences</span><span class="sxs-lookup"><span data-stu-id="763ce-155">Licensing requirements and other prerequisites</span></span>](prerequisites.md)
- [<span data-ttu-id="763ce-156">Déployer les services pris en charge</span><span class="sxs-lookup"><span data-stu-id="763ce-156">Deploy supported services</span></span>](deploy-supported-services.md)
- [<span data-ttu-id="763ce-157">Vue d’ensemble de Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="763ce-157">Microsoft 365 Defender overview</span></span>](microsoft-threat-protection.md)
- [<span data-ttu-id="763ce-158">Vue d’ensemble de Microsoft Defender for Endpoint</span><span class="sxs-lookup"><span data-stu-id="763ce-158">Microsoft Defender for Endpoint overview</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection)
- [<span data-ttu-id="763ce-159">Vue d’ensemble de Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="763ce-159">Defender for Office 365 overview</span></span>](../office-365-security/office-365-atp.md)
- [<span data-ttu-id="763ce-160">Vue d’ensemble de Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="763ce-160">Microsoft Cloud App Security overview</span></span>](https://docs.microsoft.com/cloud-app-security/what-is-cloud-app-security)
- [<span data-ttu-id="763ce-161">Vue d’ensemble de Microsoft Defender for Identity</span><span class="sxs-lookup"><span data-stu-id="763ce-161">Microsoft Defender for Identity overview</span></span>](https://docs.microsoft.com/azure-advanced-threat-protection/what-is-atp)
- [<span data-ttu-id="763ce-162">Microsoft Defender pour le stockage des données de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="763ce-162">Microsoft Defender for Endpoint data storage</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/data-storage-privacy)
