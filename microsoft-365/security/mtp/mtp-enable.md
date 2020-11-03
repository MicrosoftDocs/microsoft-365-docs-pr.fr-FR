---
title: Activer Microsoft 365 Defender dans le centre de sécurité Microsoft 365
description: Découvrez comment activer Microsoft 365 Defender et commencer à intégrer votre incident de sécurité et votre réponse.
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
ms.openlocfilehash: b5bb99ed4b8cee7ea920679e20f69c7a0e002d26
ms.sourcegitcommit: 815229e39a0f905d9f06717f00dc82e2a028fa7c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2020
ms.locfileid: "48843635"
---
# <a name="turn-on-microsoft-365-defender"></a><span data-ttu-id="a3bce-104">Activer Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="a3bce-104">Turn on Microsoft 365 Defender</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../includes/microsoft-defender.md)]


<span data-ttu-id="a3bce-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="a3bce-105">**Applies to:**</span></span>
- <span data-ttu-id="a3bce-106">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="a3bce-106">Microsoft 365 Defender</span></span>

<span data-ttu-id="a3bce-107">[Microsoft 365 Defender](microsoft-threat-protection.md) unifie votre processus de réponse aux incidents en intégrant les fonctionnalités clés de Microsoft Defender pour le point de terminaison, Microsoft Defender pour Office 365, Microsoft Cloud App Security et Microsoft Defender for Identity.</span><span class="sxs-lookup"><span data-stu-id="a3bce-107">[Microsoft 365 Defender](microsoft-threat-protection.md) unifies your incident response process by integrating key capabilities across Microsoft Defender for Endpoint, Microsoft Defender for Office 365, Microsoft Cloud App Security, and Microsoft Defender for Identity.</span></span> <span data-ttu-id="a3bce-108">Cette expérience unifiée ajoute des fonctionnalités puissantes auxquelles vous pouvez accéder dans le Centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="a3bce-108">This unified experience adds powerful features you can access in the Microsoft 365 security center.</span></span>

<span data-ttu-id="a3bce-109">Microsoft 365 Defender s’active automatiquement lorsque les clients éligibles disposant des autorisations requises sont le centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="a3bce-109">Microsoft 365 Defender automatically turns on when eligible customers with the required permissions visit Microsoft 365 security center.</span></span> <span data-ttu-id="a3bce-110">Lisez cet article pour comprendre les différentes conditions préalables et la configuration de Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="a3bce-110">Read this article to understand various prerequisites and how Microsoft 365 Defender is provisioned.</span></span>

## <a name="check-license-eligibility-and-required-permissions"></a><span data-ttu-id="a3bce-111">Vérifier l’éligibilité de la licence et les autorisations requises</span><span class="sxs-lookup"><span data-stu-id="a3bce-111">Check license eligibility and required permissions</span></span>
<span data-ttu-id="a3bce-112">Une licence pour un produit de sécurité Microsoft 365 vous permet généralement d’utiliser Microsoft 365 Defender dans le centre de sécurité Microsoft 365 sans coût de licence supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="a3bce-112">A license to a Microsoft 365 security product generally entitles you to use Microsoft 365 Defender in Microsoft 365 security center without additional licensing cost.</span></span> <span data-ttu-id="a3bce-113">Nous vous recommandons d’obtenir une licence de sécurité Microsoft 365 E5, E5 sécurité, a5 ou a5 ou une combinaison valide de licences qui donne accès à tous les services pris en charge.</span><span class="sxs-lookup"><span data-stu-id="a3bce-113">We do recommend getting a Microsoft 365 E5, E5 Security, A5, or A5 Security license or a valid combination of licenses that provides access to all supported services.</span></span>

<span data-ttu-id="a3bce-114">Pour obtenir des informations détaillées sur les licences, [Lisez les conditions relatives aux licences](prerequisites.md#licensing-requirements).</span><span class="sxs-lookup"><span data-stu-id="a3bce-114">For detailed licensing information, [read the licensing requirements](prerequisites.md#licensing-requirements).</span></span>

### <a name="check-your-role"></a><span data-ttu-id="a3bce-115">Vérifier votre rôle</span><span class="sxs-lookup"><span data-stu-id="a3bce-115">Check your role</span></span>
<span data-ttu-id="a3bce-116">Vous devez être **administrateur général** ou administrateur de **sécurité** dans Azure Active Directory pour activer Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="a3bce-116">You must be a **global administrator** or a **security administrator** in Azure Active Directory to turn on Microsoft 365 Defender.</span></span> [<span data-ttu-id="a3bce-117">Afficher vos rôles dans Azure AD</span><span class="sxs-lookup"><span data-stu-id="a3bce-117">View your roles in Azure AD</span></span>](https://docs.microsoft.com//azure/active-directory/users-groups-roles/directory-manage-roles-portal)

## <a name="supported-services"></a><span data-ttu-id="a3bce-118">Services pris en charge</span><span class="sxs-lookup"><span data-stu-id="a3bce-118">Supported services</span></span>
<span data-ttu-id="a3bce-119">Microsoft 365 Defender agrège les données à partir des différents services pris en charge que vous avez déjà déployés.</span><span class="sxs-lookup"><span data-stu-id="a3bce-119">Microsoft 365 Defender aggregates data from the various supported services that you've already deployed.</span></span> <span data-ttu-id="a3bce-120">Il traitera et stockera les données de manière centralisée afin d’identifier les nouvelles idées et de créer des flux de travail de réponse centralisée.</span><span class="sxs-lookup"><span data-stu-id="a3bce-120">It will process and store data centrally to identify new insights and make centralized response workflows possible.</span></span> <span data-ttu-id="a3bce-121">Il effectue cette opération sans affecter les déploiements, paramètres ou données existants associés aux services intégrés.</span><span class="sxs-lookup"><span data-stu-id="a3bce-121">It does this without affecting existing deployments, settings, or data associated with the integrated services.</span></span>

<span data-ttu-id="a3bce-122">Pour bénéficier de la meilleure protection et optimiser Microsoft 365 Defender, nous vous recommandons de déployer tous les services pris en charge applicables sur votre réseau.</span><span class="sxs-lookup"><span data-stu-id="a3bce-122">To get the best protection and optimize Microsoft 365 Defender, we recommend deploying all applicable supported services on your network.</span></span> <span data-ttu-id="a3bce-123">Pour plus d’informations, consultez la rubrique [Deploying Supported services](deploy-supported-services.md).</span><span class="sxs-lookup"><span data-stu-id="a3bce-123">For more information, [read about deploying supported services](deploy-supported-services.md).</span></span>

## <a name="before-starting-the-service"></a><span data-ttu-id="a3bce-124">Avant de démarrer le service</span><span class="sxs-lookup"><span data-stu-id="a3bce-124">Before starting the service</span></span>
<span data-ttu-id="a3bce-125">Avant d’activer le service, le centre de sécurité Microsoft 365 ( [Security.Microsoft.com](https://security.microsoft.com)) affiche la page Paramètres de Microsoft 365 Defender lorsque vous sélectionnez **incidents** , **Centre de maintenance** ou **sélection** dans le volet de navigation.</span><span class="sxs-lookup"><span data-stu-id="a3bce-125">Before you turn on the service, the Microsoft 365 security center ( [security.microsoft.com](https://security.microsoft.com)) shows the Microsoft 365 Defender settings page when you select **Incidents** , **Action center** , or **Hunting** from the navigation pane.</span></span> <span data-ttu-id="a3bce-126">Ces éléments de navigation ne s’affichent pas si vous n’êtes pas éligible à l’utilisation de Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="a3bce-126">These navigation items are not shown if you are not eligible to use Microsoft 365 Defender.</span></span>

<span data-ttu-id="a3bce-127">![Image de la page Paramètres de Microsoft 365 Defender affichée si Microsoft 365 Defender n’a pas été activé pour les ](../../media/mtp-enable/mtp-settings.png)
 *paramètres de Microsoft 365 Defender dans le centre de sécurité Microsoft 365*</span><span class="sxs-lookup"><span data-stu-id="a3bce-127">![Image of the Microsoft 365 Defender settings page shown if Microsoft 365 Defender has not been turned on](../../media/mtp-enable/mtp-settings.png)
*Microsoft 365 Defender settings in Microsoft 365 security center*</span></span>

## <a name="starting-the-service"></a><span data-ttu-id="a3bce-128">Démarrage du service</span><span class="sxs-lookup"><span data-stu-id="a3bce-128">Starting the service</span></span>
<span data-ttu-id="a3bce-129">Pour activer Microsoft 365 Defender, il vous suffit de sélectionner **activer microsoft 365 Defender** et d’appliquer la modification.</span><span class="sxs-lookup"><span data-stu-id="a3bce-129">To turn on Microsoft 365 Defender, simply select **Turn on Microsoft 365 Defender** and apply the change.</span></span> <span data-ttu-id="a3bce-130">Vous pouvez également accéder à cette option en sélectionnant **paramètres** ( [Security.Microsoft.com/Settings](https://security.microsoft.com/settings)) dans le volet de navigation, puis en sélectionnant **Microsoft 365 Defender**.</span><span class="sxs-lookup"><span data-stu-id="a3bce-130">You can also access this option by selecting **Settings** ( [security.microsoft.com/settings](https://security.microsoft.com/settings)) in the navigation pane and then selecting **Microsoft 365 Defender**.</span></span>

>[!NOTE]
><span data-ttu-id="a3bce-131">Si vous ne voyez pas les **paramètres** dans le volet de navigation ou que vous n’avez pas accès à la page, vérifiez vos autorisations et licences.</span><span class="sxs-lookup"><span data-stu-id="a3bce-131">If you don't see **Settings** in the navigation pane or couldn't access the page, check your permissions and licenses.</span></span>

### <a name="data-center-location"></a><span data-ttu-id="a3bce-132">Emplacement du centre de données</span><span class="sxs-lookup"><span data-stu-id="a3bce-132">Data center location</span></span>
<span data-ttu-id="a3bce-133">Microsoft 365 Defender stockera et traite les données dans le [même emplacement que celui utilisé par Microsoft Defender pour le point de terminaison](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/data-storage-privacy).</span><span class="sxs-lookup"><span data-stu-id="a3bce-133">Microsoft 365 Defender will store and process data in the [same location used by Microsoft Defender for Endpoint](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/data-storage-privacy).</span></span> <span data-ttu-id="a3bce-134">Si vous ne disposez pas de Microsoft Defender for Endpoint, un nouvel emplacement de centre de données est automatiquement sélectionné en fonction de l’emplacement des services de sécurité Microsoft 365 actifs.</span><span class="sxs-lookup"><span data-stu-id="a3bce-134">If you don't have Microsoft Defender for Endpoint, a new data center location is automatically selected based on the location of active Microsoft 365 security services.</span></span> <span data-ttu-id="a3bce-135">L’emplacement du centre de données sélectionné est affiché à l’écran.</span><span class="sxs-lookup"><span data-stu-id="a3bce-135">The selected data center location is shown in the screen.</span></span> 

<span data-ttu-id="a3bce-136">Sélectionnez **besoin d’aide ?** dans le centre de sécurité Microsoft 365 pour contacter le support Microsoft concernant la mise en service de Microsoft 365 Defender dans un autre emplacement de centre de données.</span><span class="sxs-lookup"><span data-stu-id="a3bce-136">Select **Need help?** in the Microsoft 365 security center to contact Microsoft support about provisioning Microsoft 365 Defender in a different data center location.</span></span> 

>[!NOTE]
><span data-ttu-id="a3bce-137">Microsoft Defender for Endpoint provisions automatiques dans les centres de données de l’Union européenne (UE) lors de l’activation via Azure Defender \*.</span><span class="sxs-lookup"><span data-stu-id="a3bce-137">Microsoft Defender for Endpoint automatically provisions in European Union (EU) data centers when turned on through Azure Defender\*.</span></span> <span data-ttu-id="a3bce-138">Microsoft 365 Defender est automatiquement mis en service dans le même centre de données UE pour les clients qui ont configuré Defender pour le système d’extrémité de cette manière.</span><span class="sxs-lookup"><span data-stu-id="a3bce-138">Microsoft 365 Defender will automatically provision in the same EU data center for customers who have provisioned Defender for Endpoint in this manner.</span></span> 

### <a name="confirm-that-the-service-is-on"></a><span data-ttu-id="a3bce-139">Vérifiez que le service est activé</span><span class="sxs-lookup"><span data-stu-id="a3bce-139">Confirm that the service is on</span></span>
<span data-ttu-id="a3bce-140">Une fois le service configuré, il ajoute :</span><span class="sxs-lookup"><span data-stu-id="a3bce-140">Once the service is provisioned, it adds:</span></span>

- [<span data-ttu-id="a3bce-141">Gestion des incidents</span><span class="sxs-lookup"><span data-stu-id="a3bce-141">Incidents management</span></span>](incidents-overview.md)
- <span data-ttu-id="a3bce-142">Centre de notifications pour la gestion des [examen et réponse automatisés](mtp-autoir.md)</span><span class="sxs-lookup"><span data-stu-id="a3bce-142">An action center for managing [automated investigation and response](mtp-autoir.md)</span></span>
- <span data-ttu-id="a3bce-143">Fonctionnalités de [chasse avancées](advanced-hunting-overview.md)</span><span class="sxs-lookup"><span data-stu-id="a3bce-143">[Advanced hunting](advanced-hunting-overview.md) capabilities</span></span>

<span data-ttu-id="a3bce-144">![Image du volet de navigation du centre de sécurité Microsoft 365 avec les fonctionnalités Microsoft 365 Defender ](../../media/mtp-enable/mtp-on.png)
 *Microsoft 365 Centre de sécurité avec gestion des incidents et autres fonctionnalités Microsoft 365 Defender*</span><span class="sxs-lookup"><span data-stu-id="a3bce-144">![Image of Microsoft 365 security center navigation pane with Microsoft 365 Defender features](../../media/mtp-enable/mtp-on.png)
*Microsoft 365 security center with incidents management and other Microsoft 365 Defender capabilities*</span></span>

### <a name="getting-microsoft-defender-for-identity-data"></a><span data-ttu-id="a3bce-145">Obtention de Microsoft Defender pour les données d’identité</span><span class="sxs-lookup"><span data-stu-id="a3bce-145">Getting Microsoft Defender for Identity data</span></span>
<span data-ttu-id="a3bce-146">Pour partager Microsoft Defender pour les données d’identité avec Microsoft 365 Defender, assurez-vous que Microsoft Cloud App Security et Microsoft Defender for Identity Integration sont activés.</span><span class="sxs-lookup"><span data-stu-id="a3bce-146">To share Microsoft Defender for Identity data with Microsoft 365 Defender, ensure that Microsoft Cloud App Security and Microsoft Defender for Identity integration is turned on.</span></span> [<span data-ttu-id="a3bce-147">Découvrez cette intégration</span><span class="sxs-lookup"><span data-stu-id="a3bce-147">Learn more about this integration</span></span>](https://docs.microsoft.com/cloud-app-security/aatp-integration)


## <a name="turn-off-microsoft-365-defender"></a><span data-ttu-id="a3bce-148">Désactiver Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="a3bce-148">Turn off Microsoft 365 Defender</span></span>
<span data-ttu-id="a3bce-149">Pour cesser d’utiliser Microsoft 365 Defender, accédez à **paramètres**  >  **Microsoft 365 Defender**  >  **opt-in/opt-out** dans le centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="a3bce-149">To stop using Microsoft 365 Defender, go to **Settings** > **Microsoft 365 Defender** > **Opt-in / Opt-out** in the Microsoft 365 security center.</span></span> <span data-ttu-id="a3bce-150">Désélectionnez **activer Microsoft 365 Defender** et appliquer les modifications.</span><span class="sxs-lookup"><span data-stu-id="a3bce-150">Unselect **Turn on Microsoft 365 Defender** and apply the changes.</span></span>

<span data-ttu-id="a3bce-151">Les fonctionnalités correspondantes seront supprimées du centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="a3bce-151">Corresponding features will be removed from the Microsoft 365 security center.</span></span>

## <a name="get-assistance"></a><span data-ttu-id="a3bce-152">Obtenir de l'aide</span><span class="sxs-lookup"><span data-stu-id="a3bce-152">Get assistance</span></span>

<span data-ttu-id="a3bce-153">Pour obtenir des réponses aux questions les plus fréquemment posées sur l’activation de Microsoft 365 Defender, [Lisez le Forum aux](mtp-enable-faq.md)questions.</span><span class="sxs-lookup"><span data-stu-id="a3bce-153">To get answers to the most commonly asked questions about turning on Microsoft 365 Defender, [read the FAQ](mtp-enable-faq.md).</span></span>

<span data-ttu-id="a3bce-154">Le personnel du support Microsoft peut vous aider à mettre en service ou à mettre hors service le service et les ressources associées sur votre client.</span><span class="sxs-lookup"><span data-stu-id="a3bce-154">Microsoft support staff can help provision or deprovision the service and related resources on your tenant.</span></span> <span data-ttu-id="a3bce-155">Pour obtenir de l’aide, sélectionnez **besoin d’aide ?** dans le centre de sécurité Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="a3bce-155">For assistance, select **Need help?** in the Microsoft 365 security center.</span></span> <span data-ttu-id="a3bce-156">Lorsque vous contactez le support technique, mentionnez Microsoft 365 Defender.</span><span class="sxs-lookup"><span data-stu-id="a3bce-156">When contacting support, mention Microsoft 365 Defender.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a3bce-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a3bce-157">Related topics</span></span>

- [<span data-ttu-id="a3bce-158">Foire aux questions</span><span class="sxs-lookup"><span data-stu-id="a3bce-158">Frequently asked questions</span></span>](mtp-enable-faq.md)
- [<span data-ttu-id="a3bce-159">Conditions requises et autres conditions préalables relatives aux licences</span><span class="sxs-lookup"><span data-stu-id="a3bce-159">Licensing requirements and other prerequisites</span></span>](prerequisites.md)
- [<span data-ttu-id="a3bce-160">Déployer les services pris en charge</span><span class="sxs-lookup"><span data-stu-id="a3bce-160">Deploy supported services</span></span>](deploy-supported-services.md)
- [<span data-ttu-id="a3bce-161">Vue d’ensemble de Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="a3bce-161">Microsoft 365 Defender overview</span></span>](microsoft-threat-protection.md)
- [<span data-ttu-id="a3bce-162">Vue d’ensemble de Microsoft Defender pour les points de terminaison</span><span class="sxs-lookup"><span data-stu-id="a3bce-162">Microsoft Defender for Endpoint overview</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/microsoft-defender-advanced-threat-protection)
- [<span data-ttu-id="a3bce-163">Vue d’ensemble de Defender for Office 365</span><span class="sxs-lookup"><span data-stu-id="a3bce-163">Defender for Office 365 overview</span></span>](../office-365-security/office-365-atp.md)
- [<span data-ttu-id="a3bce-164">Vue d’ensemble de Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="a3bce-164">Microsoft Cloud App Security overview</span></span>](https://docs.microsoft.com/cloud-app-security/what-is-cloud-app-security)
- [<span data-ttu-id="a3bce-165">Vue d’ensemble de Microsoft Defender for Identity</span><span class="sxs-lookup"><span data-stu-id="a3bce-165">Microsoft Defender for Identity overview</span></span>](https://docs.microsoft.com/azure-advanced-threat-protection/what-is-atp)
- [<span data-ttu-id="a3bce-166">Microsoft Defender pour le stockage des données de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="a3bce-166">Microsoft Defender for Endpoint data storage</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/data-storage-privacy)
