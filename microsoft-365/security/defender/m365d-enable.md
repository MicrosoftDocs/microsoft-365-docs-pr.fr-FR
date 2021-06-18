---
title: Activer les Microsoft 365 Defender dans le centre de Microsoft 365 de sécurité
description: Découvrez comment activer Microsoft 365 Defender et commencer à intégrer votre incident de sécurité et votre réponse.
keywords: commencer, activer Microsoft 365 Defender, Microsoft 365 Defender, M365, sécurité, emplacement des données, autorisations requises, éligibilité aux licences, page paramètres
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
f1.keywords:
- NOCSH
ms.author: lomayor
author: lomayor
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: conceptual
search.appverid:
- MOE150
- MET150
ms.technology: m365d
ms.openlocfilehash: 102666834562d0576920c746842582c2870b3738
ms.sourcegitcommit: bbad1938b6661d4a6bca99f235c44e521b1fb662
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/18/2021
ms.locfileid: "53007608"
---
# <a name="turn-on-microsoft-365-defender"></a><span data-ttu-id="deffd-104">Activer Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="deffd-104">Turn on Microsoft 365 Defender</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="deffd-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="deffd-105">**Applies to:**</span></span>
- <span data-ttu-id="deffd-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="deffd-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="deffd-107">[Microsoft 365 Defender](microsoft-365-defender.md) unifie votre processus de réponse aux incidents en intégrant des fonctionnalités clés dans Microsoft Defender pour le point de terminaison, Microsoft Defender pour Office 365, Microsoft Cloud App Security et Microsoft Defender pour l’identité.</span><span class="sxs-lookup"><span data-stu-id="deffd-107">[Microsoft 365 Defender](microsoft-365-defender.md) unifies your incident response process by integrating key capabilities across Microsoft Defender for Endpoint, Microsoft Defender for Office 365, Microsoft Cloud App Security, and Microsoft Defender for Identity.</span></span> <span data-ttu-id="deffd-108">Cette expérience unifiée ajoute des fonctionnalités puissantes auxquelles vous pouvez accéder dans le Centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="deffd-108">This unified experience adds powerful features you can access in the Microsoft 365 security center.</span></span>

<span data-ttu-id="deffd-109">Microsoft 365 Defender s’allume automatiquement lorsque les clients éligibles ayant les autorisations requises visitent Microsoft 365 centre de sécurité.</span><span class="sxs-lookup"><span data-stu-id="deffd-109">Microsoft 365 Defender automatically turns on when eligible customers with the required permissions visit Microsoft 365 security center.</span></span> <span data-ttu-id="deffd-110">Lisez cet article pour comprendre les différents éléments prérequis et la façon Microsoft 365 Defender est mise en service.</span><span class="sxs-lookup"><span data-stu-id="deffd-110">Read this article to understand various prerequisites and how Microsoft 365 Defender is provisioned.</span></span>

## <a name="check-license-eligibility-and-required-permissions"></a><span data-ttu-id="deffd-111">Vérifier l’éligibilité aux licences et les autorisations requises</span><span class="sxs-lookup"><span data-stu-id="deffd-111">Check license eligibility and required permissions</span></span>

<span data-ttu-id="deffd-112">Une licence à un produit de sécurité Microsoft 365 vous permet généralement d’utiliser Microsoft 365 Defender dans Microsoft 365 centre de sécurité sans coût de licence supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="deffd-112">A license to a Microsoft 365 security product generally entitles you to use Microsoft 365 Defender in Microsoft 365 security center without additional licensing cost.</span></span> <span data-ttu-id="deffd-113">Nous vous recommandons d’obtenir une licence Microsoft 365 E5, E5 Security, A5 ou A5 Security ou une combinaison valide de licences qui donne accès à tous les services pris en charge.</span><span class="sxs-lookup"><span data-stu-id="deffd-113">We do recommend getting a Microsoft 365 E5, E5 Security, A5, or A5 Security license or a valid combination of licenses that provides access to all supported services.</span></span>

<span data-ttu-id="deffd-114">Pour obtenir des informations détaillées sur les licences, [lisez les exigences de licence.](prerequisites.md#licensing-requirements)</span><span class="sxs-lookup"><span data-stu-id="deffd-114">For detailed licensing information, [read the licensing requirements](prerequisites.md#licensing-requirements).</span></span>

### <a name="check-your-role"></a><span data-ttu-id="deffd-115">Vérifier votre rôle</span><span class="sxs-lookup"><span data-stu-id="deffd-115">Check your role</span></span>

<span data-ttu-id="deffd-116">Vous devez être administrateur **général ou** **administrateur** de sécurité dans Azure Active Directory pour activer Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="deffd-116">You must be a **global administrator** or a **security administrator** in Azure Active Directory to turn on Microsoft 365 Defender.</span></span> [<span data-ttu-id="deffd-117">Afficher vos rôles dans Azure AD</span><span class="sxs-lookup"><span data-stu-id="deffd-117">View your roles in Azure AD</span></span>](/azure/active-directory/users-groups-roles/directory-manage-roles-portal)

## <a name="supported-services"></a><span data-ttu-id="deffd-118">Services pris en charge</span><span class="sxs-lookup"><span data-stu-id="deffd-118">Supported services</span></span>

<span data-ttu-id="deffd-119">Microsoft 365 Defender regroupe les données des différents services pris en charge que vous avez déjà déployés.</span><span class="sxs-lookup"><span data-stu-id="deffd-119">Microsoft 365 Defender aggregates data from the various supported services that you've already deployed.</span></span> <span data-ttu-id="deffd-120">Il traitera et stockera les données de manière centralisée pour identifier les nouvelles informations et rendre possibles des flux de travail de réponse centralisés.</span><span class="sxs-lookup"><span data-stu-id="deffd-120">It will process and store data centrally to identify new insights and make centralized response workflows possible.</span></span> <span data-ttu-id="deffd-121">Il le fait sans affecter les déploiements, paramètres ou données existants associés aux services intégrés.</span><span class="sxs-lookup"><span data-stu-id="deffd-121">It does this without affecting existing deployments, settings, or data associated with the integrated services.</span></span>

<span data-ttu-id="deffd-122">Pour obtenir la meilleure protection et optimiser les Microsoft 365 Defender, nous vous recommandons de déployer tous les services pris en charge applicables sur votre réseau.</span><span class="sxs-lookup"><span data-stu-id="deffd-122">To get the best protection and optimize Microsoft 365 Defender, we recommend deploying all applicable supported services on your network.</span></span> <span data-ttu-id="deffd-123">Pour plus d’informations, [voir sur le déploiement des services pris en charge.](deploy-supported-services.md)</span><span class="sxs-lookup"><span data-stu-id="deffd-123">For more information, [read about deploying supported services](deploy-supported-services.md).</span></span>

## <a name="onboard-to-the-service"></a><span data-ttu-id="deffd-124">Intégrer au service</span><span class="sxs-lookup"><span data-stu-id="deffd-124">Onboard to the service</span></span>
<span data-ttu-id="deffd-125">L’intégration à Microsoft 365 Defender est simple.</span><span class="sxs-lookup"><span data-stu-id="deffd-125">Onboarding to Microsoft 365 Defender is simple.</span></span> <span data-ttu-id="deffd-126">Dans le menu de navigation, sélectionnez n’importe quel élément, tel que  **incidents & alertes,** de **recherche,** de centre de action ou d’analyse des menaces pour lancer le processus d’intégration.</span><span class="sxs-lookup"><span data-stu-id="deffd-126">From the navigation menu, select any item, such as **Incidents & alerts**, **Hunting**, **Action center**, or **Threat analytics** to initiate the onboarding process.</span></span> 

### <a name="data-center-location"></a><span data-ttu-id="deffd-127">Emplacement du centre de données</span><span class="sxs-lookup"><span data-stu-id="deffd-127">Data center location</span></span>

<span data-ttu-id="deffd-128">Microsoft 365 Defender stockera et traitera les données au même emplacement que celui utilisé [par Microsoft Defender pour endpoint.](/windows/security/threat-protection/microsoft-defender-atp/data-storage-privacy)</span><span class="sxs-lookup"><span data-stu-id="deffd-128">Microsoft 365 Defender will store and process data in the [same location used by Microsoft Defender for Endpoint](/windows/security/threat-protection/microsoft-defender-atp/data-storage-privacy).</span></span> <span data-ttu-id="deffd-129">Si vous n’avez pas Microsoft Defender pour le point de terminaison, un nouvel emplacement de centre de données est automatiquement sélectionné en fonction de l’emplacement des services de sécurité Microsoft 365 actifs.</span><span class="sxs-lookup"><span data-stu-id="deffd-129">If you don't have Microsoft Defender for Endpoint, a new data center location is automatically selected based on the location of active Microsoft 365 security services.</span></span> <span data-ttu-id="deffd-130">L’emplacement du centre de données sélectionné est affiché à l’écran.</span><span class="sxs-lookup"><span data-stu-id="deffd-130">The selected data center location is shown in the screen.</span></span>

<span data-ttu-id="deffd-131">Sélectionnez **Besoin d’aide ?** dans le centre de sécurité Microsoft 365 pour contacter le support Microsoft sur la mise en service Microsoft 365 Defender dans un autre emplacement de centre de données.</span><span class="sxs-lookup"><span data-stu-id="deffd-131">Select **Need help?** in the Microsoft 365 security center to contact Microsoft support about provisioning Microsoft 365 Defender in a different data center location.</span></span>

> [!NOTE]
> <span data-ttu-id="deffd-132">Dans le passé, Microsoft Defender pour point de terminaison était automatiquement mis en service dans les centres de données de l’Union européenne (UE) lorsqu’il était allumé via Azure Defender.</span><span class="sxs-lookup"><span data-stu-id="deffd-132">In the past, Microsoft Defender for Endpoint automatically provisioned in European Union (EU) data centers when turned on through Azure Defender.</span></span> <span data-ttu-id="deffd-133">Microsoft 365 Defender sera automatiquement mis en service dans le même centre de données de l’UE pour les clients qui ont mis en service Defender pour endpoint de cette manière dans le passé.</span><span class="sxs-lookup"><span data-stu-id="deffd-133">Microsoft 365 Defender will automatically provision in the same EU data center for customers who have provisioned Defender for Endpoint in this manner in the past.</span></span>

### <a name="confirm-that-the-service-is-on"></a><span data-ttu-id="deffd-134">Vérifiez que le service est activé</span><span class="sxs-lookup"><span data-stu-id="deffd-134">Confirm that the service is on</span></span>

<span data-ttu-id="deffd-135">Une fois le service configuré, il ajoute :</span><span class="sxs-lookup"><span data-stu-id="deffd-135">Once the service is provisioned, it adds:</span></span>

- [<span data-ttu-id="deffd-136">Gestion des incidents</span><span class="sxs-lookup"><span data-stu-id="deffd-136">Incidents management</span></span>](incidents-overview.md)
- [<span data-ttu-id="deffd-137">File d’attente des alertes</span><span class="sxs-lookup"><span data-stu-id="deffd-137">Alerts queue</span></span>](investigate-alerts.md)
- <span data-ttu-id="deffd-138">Centre de notifications pour la gestion des [examen et réponse automatisés](m365d-autoir.md)</span><span class="sxs-lookup"><span data-stu-id="deffd-138">An action center for managing [automated investigation and response](m365d-autoir.md)</span></span>
- <span data-ttu-id="deffd-139">[Fonctionnalités de recherche](advanced-hunting-overview.md) avancées</span><span class="sxs-lookup"><span data-stu-id="deffd-139">[Advanced hunting](advanced-hunting-overview.md) capabilities</span></span>
- <span data-ttu-id="deffd-140">Analyses de menaces</span><span class="sxs-lookup"><span data-stu-id="deffd-140">Threat analytics</span></span>

<span data-ttu-id="deffd-141">![Image du volet Microsoft 365 de navigation du centre de sécurité avec Microsoft 365 Defender fonctionnalités Microsoft 365 centre de sécurité avec gestion des incidents et autres ](../../media/overview-incident.png)
 *fonctionnalités Microsoft 365 Defender de sécurité*</span><span class="sxs-lookup"><span data-stu-id="deffd-141">![Image of Microsoft 365 security center navigation pane with Microsoft 365 Defender features](../../media/overview-incident.png)
*Microsoft 365 security center with incidents management and other Microsoft 365 Defender capabilities*</span></span>

### <a name="getting-microsoft-defender-for-identity-data"></a><span data-ttu-id="deffd-142">Obtention de données Microsoft Defender pour l’identité</span><span class="sxs-lookup"><span data-stu-id="deffd-142">Getting Microsoft Defender for Identity data</span></span> 
<span data-ttu-id="deffd-143">Pour activer l’intégration avec Microsoft Cloud App Security, vous devez vous connecter au Microsoft Cloud App Security au moins une fois.</span><span class="sxs-lookup"><span data-stu-id="deffd-143">To enable the integration with Microsoft Cloud App Security, you'll need to login to the Microsoft Cloud App Security at least once.</span></span>

## <a name="get-assistance"></a><span data-ttu-id="deffd-144">Obtenir de l'aide</span><span class="sxs-lookup"><span data-stu-id="deffd-144">Get assistance</span></span>

<span data-ttu-id="deffd-145">Pour obtenir des réponses aux questions les plus fréquemment posées sur l’Microsoft 365 Defender, [lisez le FAQ.](m365d-enable-faq.md)</span><span class="sxs-lookup"><span data-stu-id="deffd-145">To get answers to the most commonly asked questions about turning on Microsoft 365 Defender, [read the FAQ](m365d-enable-faq.md).</span></span>

<span data-ttu-id="deffd-146">Le personnel du support microsoft peut vous aider à fournir ou à désapprovisioner le service et les ressources associées sur votre client.</span><span class="sxs-lookup"><span data-stu-id="deffd-146">Microsoft support staff can help provision or deprovision the service and related resources on your tenant.</span></span> <span data-ttu-id="deffd-147">Pour obtenir de l’aide, **sélectionnez Besoin d’aide ?** dans Microsoft 365 de sécurité.</span><span class="sxs-lookup"><span data-stu-id="deffd-147">For assistance, select **Need help?** in the Microsoft 365 security center.</span></span> <span data-ttu-id="deffd-148">Lorsque vous contactez le support technique, Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="deffd-148">When contacting support, mention Microsoft 365 Defender.</span></span>

## <a name="related-topics"></a><span data-ttu-id="deffd-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="deffd-149">Related topics</span></span>

- [<span data-ttu-id="deffd-150">Forum aux questions</span><span class="sxs-lookup"><span data-stu-id="deffd-150">Frequently asked questions</span></span>](m365d-enable-faq.md)
- [<span data-ttu-id="deffd-151">Conditions requises et autres conditions préalables relatives aux licences</span><span class="sxs-lookup"><span data-stu-id="deffd-151">Licensing requirements and other prerequisites</span></span>](prerequisites.md)
- [<span data-ttu-id="deffd-152">Déployer les services pris en charge</span><span class="sxs-lookup"><span data-stu-id="deffd-152">Deploy supported services</span></span>](deploy-supported-services.md)
- [<span data-ttu-id="deffd-153">Microsoft 365 Defender vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="deffd-153">Microsoft 365 Defender overview</span></span>](microsoft-365-defender.md)
- [<span data-ttu-id="deffd-154">Vue d’ensemble de Microsoft Defender for Endpoint</span><span class="sxs-lookup"><span data-stu-id="deffd-154">Microsoft Defender for Endpoint overview</span></span>](../defender-endpoint/microsoft-defender-endpoint.md)
- [<span data-ttu-id="deffd-155">Vue d’ensemble Office 365 Defender for Office 365</span><span class="sxs-lookup"><span data-stu-id="deffd-155">Defender for Office 365 overview</span></span>](../office-365-security/defender-for-office-365.md)
- [<span data-ttu-id="deffd-156">Aperçu de Microsoft Cloud App Security </span><span class="sxs-lookup"><span data-stu-id="deffd-156">Microsoft Cloud App Security overview</span></span>](/cloud-app-security/what-is-cloud-app-security)
- [<span data-ttu-id="deffd-157">Vue d’ensemble de Microsoft Defender for Identity</span><span class="sxs-lookup"><span data-stu-id="deffd-157">Microsoft Defender for Identity overview</span></span>](/azure-advanced-threat-protection/what-is-atp)
- [<span data-ttu-id="deffd-158">Microsoft Defender pour le stockage des données de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="deffd-158">Microsoft Defender for Endpoint data storage</span></span>](../defender-endpoint/data-storage-privacy.md)
