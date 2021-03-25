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
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: conceptual
search.appverid:
- MOE150
- MET150
ms.technology: m365d
ms.openlocfilehash: 18564b2a5a47b2cf4a8bbd94a3e3a315c8f269ec
ms.sourcegitcommit: dcb97fbfdae52960ae62b6faa707a05358193ed5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2021
ms.locfileid: "51200256"
---
# <a name="turn-on-microsoft-365-defender"></a><span data-ttu-id="25d7e-104">Activer Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="25d7e-104">Turn on Microsoft 365 Defender</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="25d7e-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="25d7e-105">**Applies to:**</span></span>
- <span data-ttu-id="25d7e-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="25d7e-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="25d7e-107">[Microsoft 365 Defender](microsoft-365-defender.md) unifie votre processus de réponse aux incidents en intégrant des fonctionnalités clés dans Microsoft Defender pour le point de terminaison, Microsoft Defender pour Office 365, Microsoft Cloud App Security et Microsoft Defender pour l’identité.</span><span class="sxs-lookup"><span data-stu-id="25d7e-107">[Microsoft 365 Defender](microsoft-365-defender.md) unifies your incident response process by integrating key capabilities across Microsoft Defender for Endpoint, Microsoft Defender for Office 365, Microsoft Cloud App Security, and Microsoft Defender for Identity.</span></span> <span data-ttu-id="25d7e-108">Cette expérience unifiée ajoute des fonctionnalités puissantes auxquelles vous pouvez accéder dans le Centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="25d7e-108">This unified experience adds powerful features you can access in the Microsoft 365 security center.</span></span>

<span data-ttu-id="25d7e-109">Microsoft 365 Defender s’allume automatiquement lorsque les clients éligibles ayant les autorisations requises visitent le Centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="25d7e-109">Microsoft 365 Defender automatically turns on when eligible customers with the required permissions visit Microsoft 365 security center.</span></span> <span data-ttu-id="25d7e-110">Lisez cet article pour comprendre les différents éléments prérequis et la façon dont Microsoft 365 Defender est mise en service.</span><span class="sxs-lookup"><span data-stu-id="25d7e-110">Read this article to understand various prerequisites and how Microsoft 365 Defender is provisioned.</span></span>

## <a name="check-license-eligibility-and-required-permissions"></a><span data-ttu-id="25d7e-111">Vérifier l’éligibilité aux licences et les autorisations requises</span><span class="sxs-lookup"><span data-stu-id="25d7e-111">Check license eligibility and required permissions</span></span>

<span data-ttu-id="25d7e-112">Une licence pour un produit de sécurité Microsoft 365 vous permet généralement d’utiliser Microsoft 365 Defender dans le Centre de sécurité Microsoft 365 sans coût de licence supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="25d7e-112">A license to a Microsoft 365 security product generally entitles you to use Microsoft 365 Defender in Microsoft 365 security center without additional licensing cost.</span></span> <span data-ttu-id="25d7e-113">Nous vous recommandons d’obtenir une licence Microsoft 365 E5, E5 Security, A5 ou A5 Security ou une combinaison valide de licences qui donne accès à tous les services pris en charge.</span><span class="sxs-lookup"><span data-stu-id="25d7e-113">We do recommend getting a Microsoft 365 E5, E5 Security, A5, or A5 Security license or a valid combination of licenses that provides access to all supported services.</span></span>

<span data-ttu-id="25d7e-114">Pour obtenir des informations détaillées sur les licences, [lisez les exigences de licence.](prerequisites.md#licensing-requirements)</span><span class="sxs-lookup"><span data-stu-id="25d7e-114">For detailed licensing information, [read the licensing requirements](prerequisites.md#licensing-requirements).</span></span>

### <a name="check-your-role"></a><span data-ttu-id="25d7e-115">Vérifier votre rôle</span><span class="sxs-lookup"><span data-stu-id="25d7e-115">Check your role</span></span>

<span data-ttu-id="25d7e-116">Vous devez être administrateur **général ou** **administrateur** de sécurité dans Azure Active Directory pour activer Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="25d7e-116">You must be a **global administrator** or a **security administrator** in Azure Active Directory to turn on Microsoft 365 Defender.</span></span> [<span data-ttu-id="25d7e-117">Afficher vos rôles dans Azure AD</span><span class="sxs-lookup"><span data-stu-id="25d7e-117">View your roles in Azure AD</span></span>](/azure/active-directory/users-groups-roles/directory-manage-roles-portal)

## <a name="supported-services"></a><span data-ttu-id="25d7e-118">Services pris en charge</span><span class="sxs-lookup"><span data-stu-id="25d7e-118">Supported services</span></span>

<span data-ttu-id="25d7e-119">Microsoft 365 Defender regroupe les données des différents services pris en charge que vous avez déjà déployés.</span><span class="sxs-lookup"><span data-stu-id="25d7e-119">Microsoft 365 Defender aggregates data from the various supported services that you've already deployed.</span></span> <span data-ttu-id="25d7e-120">Il traitera et stockera les données de manière centralisée pour identifier les nouvelles informations et rendre possibles des flux de travail de réponse centralisés.</span><span class="sxs-lookup"><span data-stu-id="25d7e-120">It will process and store data centrally to identify new insights and make centralized response workflows possible.</span></span> <span data-ttu-id="25d7e-121">Il le fait sans affecter les déploiements, paramètres ou données existants associés aux services intégrés.</span><span class="sxs-lookup"><span data-stu-id="25d7e-121">It does this without affecting existing deployments, settings, or data associated with the integrated services.</span></span>

<span data-ttu-id="25d7e-122">Pour obtenir la meilleure protection et optimiser Microsoft 365 Defender, nous vous recommandons de déployer tous les services pris en charge applicables sur votre réseau.</span><span class="sxs-lookup"><span data-stu-id="25d7e-122">To get the best protection and optimize Microsoft 365 Defender, we recommend deploying all applicable supported services on your network.</span></span> <span data-ttu-id="25d7e-123">Pour plus d’informations, [voir sur le déploiement des services pris en charge.](deploy-supported-services.md)</span><span class="sxs-lookup"><span data-stu-id="25d7e-123">For more information, [read about deploying supported services](deploy-supported-services.md).</span></span>

## <a name="onboard-to-the-service"></a><span data-ttu-id="25d7e-124">Intégrer au service</span><span class="sxs-lookup"><span data-stu-id="25d7e-124">Onboard to the service</span></span>
<span data-ttu-id="25d7e-125">L’intégration à Microsoft 365 Defender est simple.</span><span class="sxs-lookup"><span data-stu-id="25d7e-125">Onboarding to Microsoft 365 Defender is simple.</span></span> <span data-ttu-id="25d7e-126">Dans le menu de navigation, sélectionnez n’importe quel élément sous la section Points de terminaison, par exemple Incidents, Recherche, Centre d’action ou Analyse des menaces pour lancer le processus d’intégration.</span><span class="sxs-lookup"><span data-stu-id="25d7e-126">From the navigation menu, select any item under the Endpoints section, such as Incidents, Hunting, Action center, or Threat analytics to initiate the onboarding process.</span></span> 

### <a name="data-center-location"></a><span data-ttu-id="25d7e-127">Emplacement du centre de données</span><span class="sxs-lookup"><span data-stu-id="25d7e-127">Data center location</span></span>

<span data-ttu-id="25d7e-128">Microsoft 365 Defender stockera et traitera les données au même emplacement que celui utilisé par [Microsoft Defender pour le point de terminaison.](/windows/security/threat-protection/microsoft-defender-atp/data-storage-privacy)</span><span class="sxs-lookup"><span data-stu-id="25d7e-128">Microsoft 365 Defender will store and process data in the [same location used by Microsoft Defender for Endpoint](/windows/security/threat-protection/microsoft-defender-atp/data-storage-privacy).</span></span> <span data-ttu-id="25d7e-129">Si vous n’avez pas Microsoft Defender pour point de terminaison, un nouvel emplacement de centre de données est automatiquement sélectionné en fonction de l’emplacement des services de sécurité Microsoft 365 actifs.</span><span class="sxs-lookup"><span data-stu-id="25d7e-129">If you don't have Microsoft Defender for Endpoint, a new data center location is automatically selected based on the location of active Microsoft 365 security services.</span></span> <span data-ttu-id="25d7e-130">L’emplacement du centre de données sélectionné est affiché à l’écran.</span><span class="sxs-lookup"><span data-stu-id="25d7e-130">The selected data center location is shown in the screen.</span></span>

<span data-ttu-id="25d7e-131">Sélectionnez **Besoin d’aide ?** dans le Centre de sécurité Microsoft 365 pour contacter le support Microsoft concernant la mise en service de Microsoft 365 Defender dans un autre emplacement de centre de données.</span><span class="sxs-lookup"><span data-stu-id="25d7e-131">Select **Need help?** in the Microsoft 365 security center to contact Microsoft support about provisioning Microsoft 365 Defender in a different data center location.</span></span>

> [!NOTE]
> <span data-ttu-id="25d7e-132">Microsoft Defender pour le point de terminaison est automatiquement mis en place dans les centres de données de l’Union européenne (UE) lorsqu’il est allumé par le biais d’Azure Defender.</span><span class="sxs-lookup"><span data-stu-id="25d7e-132">Microsoft Defender for Endpoint automatically provisions in European Union (EU) data centers when turned on through Azure Defender.</span></span> <span data-ttu-id="25d7e-133">Microsoft 365 Defender sera automatiquement mis en service dans le même centre de données de l’UE pour les clients qui ont mis en service Defender pour endpoint de cette manière.</span><span class="sxs-lookup"><span data-stu-id="25d7e-133">Microsoft 365 Defender will automatically provision in the same EU data center for customers who have provisioned Defender for Endpoint in this manner.</span></span>

### <a name="confirm-that-the-service-is-on"></a><span data-ttu-id="25d7e-134">Vérifiez que le service est activé</span><span class="sxs-lookup"><span data-stu-id="25d7e-134">Confirm that the service is on</span></span>

<span data-ttu-id="25d7e-135">Une fois le service configuré, il ajoute :</span><span class="sxs-lookup"><span data-stu-id="25d7e-135">Once the service is provisioned, it adds:</span></span>

- [<span data-ttu-id="25d7e-136">Gestion des incidents</span><span class="sxs-lookup"><span data-stu-id="25d7e-136">Incidents management</span></span>](incidents-overview.md)
- [<span data-ttu-id="25d7e-137">File d’attente des alertes</span><span class="sxs-lookup"><span data-stu-id="25d7e-137">Alerts queue</span></span>](investigate-alerts.md)
- <span data-ttu-id="25d7e-138">Centre de notifications pour la gestion des [examen et réponse automatisés](m365d-autoir.md)</span><span class="sxs-lookup"><span data-stu-id="25d7e-138">An action center for managing [automated investigation and response](m365d-autoir.md)</span></span>
- <span data-ttu-id="25d7e-139">[Fonctionnalités de recherche](advanced-hunting-overview.md) avancées</span><span class="sxs-lookup"><span data-stu-id="25d7e-139">[Advanced hunting](advanced-hunting-overview.md) capabilities</span></span>
- <span data-ttu-id="25d7e-140">Analyses de menaces</span><span class="sxs-lookup"><span data-stu-id="25d7e-140">Threat analytics</span></span>

<span data-ttu-id="25d7e-141">![Image du volet de navigation du Centre de sécurité Microsoft 365 avec Microsoft 365 Defender qui propose le Centre de sécurité Microsoft 365 avec la gestion des incidents et d’autres fonctionnalités de ](../../media/mtp-enable/mtp-on.png)
 *Microsoft 365 Defender*</span><span class="sxs-lookup"><span data-stu-id="25d7e-141">![Image of Microsoft 365 security center navigation pane with Microsoft 365 Defender features](../../media/mtp-enable/mtp-on.png)
*Microsoft 365 security center with incidents management and other Microsoft 365 Defender capabilities*</span></span>

### <a name="getting-microsoft-defender-for-identity-data"></a><span data-ttu-id="25d7e-142">Obtention de données Microsoft Defender pour l’identité</span><span class="sxs-lookup"><span data-stu-id="25d7e-142">Getting Microsoft Defender for Identity data</span></span> 
<span data-ttu-id="25d7e-143">Pour activer l’intégration avec Microsoft Cloud App Security, vous devez vous connecter à Microsoft Cloud App Security au moins une fois.</span><span class="sxs-lookup"><span data-stu-id="25d7e-143">To enable the integration with Microsoft Cloud App Security, you'll need to login to the Microsoft Cloud App Security at least once.</span></span>

## <a name="get-assistance"></a><span data-ttu-id="25d7e-144">Obtenir de l'aide</span><span class="sxs-lookup"><span data-stu-id="25d7e-144">Get assistance</span></span>

<span data-ttu-id="25d7e-145">Pour obtenir des réponses aux questions les plus fréquemment posées sur l’accès à Microsoft 365 Defender, [lisez le FAQ.](m365d-enable-faq.md)</span><span class="sxs-lookup"><span data-stu-id="25d7e-145">To get answers to the most commonly asked questions about turning on Microsoft 365 Defender, [read the FAQ](m365d-enable-faq.md).</span></span>

<span data-ttu-id="25d7e-146">Le personnel du support microsoft peut vous aider à fournir ou à désapprovisioner le service et les ressources associées sur votre client.</span><span class="sxs-lookup"><span data-stu-id="25d7e-146">Microsoft support staff can help provision or deprovision the service and related resources on your tenant.</span></span> <span data-ttu-id="25d7e-147">Pour obtenir de l’aide, **sélectionnez Besoin d’aide ?** dans le Centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="25d7e-147">For assistance, select **Need help?** in the Microsoft 365 security center.</span></span> <span data-ttu-id="25d7e-148">Lorsque vous contactez le support technique, mentionnez Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="25d7e-148">When contacting support, mention Microsoft 365 Defender.</span></span>

## <a name="related-topics"></a><span data-ttu-id="25d7e-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="25d7e-149">Related topics</span></span>

- [<span data-ttu-id="25d7e-150">Forum aux questions</span><span class="sxs-lookup"><span data-stu-id="25d7e-150">Frequently asked questions</span></span>](m365d-enable-faq.md)
- [<span data-ttu-id="25d7e-151">Conditions requises et autres conditions préalables relatives aux licences</span><span class="sxs-lookup"><span data-stu-id="25d7e-151">Licensing requirements and other prerequisites</span></span>](prerequisites.md)
- [<span data-ttu-id="25d7e-152">Déployer les services pris en charge</span><span class="sxs-lookup"><span data-stu-id="25d7e-152">Deploy supported services</span></span>](deploy-supported-services.md)
- [<span data-ttu-id="25d7e-153">Vue d’ensemble de Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="25d7e-153">Microsoft 365 Defender overview</span></span>](microsoft-365-defender.md)
- [<span data-ttu-id="25d7e-154">Vue d’ensemble de Microsoft Defender for Endpoint</span><span class="sxs-lookup"><span data-stu-id="25d7e-154">Microsoft Defender for Endpoint overview</span></span>](../defender-endpoint/microsoft-defender-endpoint.md)
- [<span data-ttu-id="25d7e-155">Vue d’ensemble de Defender pour Office 365</span><span class="sxs-lookup"><span data-stu-id="25d7e-155">Defender for Office 365 overview</span></span>](../office-365-security/defender-for-office-365.md)
- [<span data-ttu-id="25d7e-156">Vue d’ensemble de Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="25d7e-156">Microsoft Cloud App Security overview</span></span>](/cloud-app-security/what-is-cloud-app-security)
- [<span data-ttu-id="25d7e-157">Vue d’ensemble de Microsoft Defender for Identity</span><span class="sxs-lookup"><span data-stu-id="25d7e-157">Microsoft Defender for Identity overview</span></span>](/azure-advanced-threat-protection/what-is-atp)
- [<span data-ttu-id="25d7e-158">Microsoft Defender pour le stockage des données de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="25d7e-158">Microsoft Defender for Endpoint data storage</span></span>](../defender-endpoint/data-storage-privacy.md)
