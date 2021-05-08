---
title: Microsoft Defender pour point de terminaison iOS
ms.reviewer: ''
description: Décrit comment installer et utiliser Microsoft Defender pour endpoint sur iOS
keywords: microsoft, defender, Microsoft Defender for Endpoint, ios, overview, installation, deploy, uninstallation, intune
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: macapara
author: mjcaparas
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- m365-security-compliance
- m365initiative-defender-endpoint
ms.topic: conceptual
ms.technology: mde
ms.openlocfilehash: 3d9dd871edba29ec6119329f98ada990abad6e8d
ms.sourcegitcommit: ff20f5b4e3268c7c98a84fb1cbe7db7151596b6d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/06/2021
ms.locfileid: "52246415"
---
# <a name="microsoft-defender-for-endpoint-on-ios"></a><span data-ttu-id="345f6-104">Microsoft Defender pour point de terminaison iOS</span><span class="sxs-lookup"><span data-stu-id="345f6-104">Microsoft Defender for Endpoint on iOS</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="345f6-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="345f6-105">**Applies to:**</span></span>
- [<span data-ttu-id="345f6-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="345f6-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="345f6-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="345f6-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="345f6-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="345f6-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="345f6-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="345f6-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

<span data-ttu-id="345f6-110">**Microsoft Defender pour le point de terminaison sur iOS** offre une protection contre le hameçonnage et les connexions réseau non sécurisées à partir de sites web, de courriers électroniques et d’applications.</span><span class="sxs-lookup"><span data-stu-id="345f6-110">**Microsoft Defender for Endpoint on iOS** will offer protection against phishing and unsafe network connections from websites, emails, and apps.</span></span> <span data-ttu-id="345f6-111">Toutes les alertes seront disponibles par le biais d’un seul volet de la Centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="345f6-111">All alerts will be available through a single pane of glass in the Microsoft Defender Security Center.</span></span> <span data-ttu-id="345f6-112">Le portail offre aux équipes de sécurité une vue centralisée des menaces sur les appareils iOS, ainsi que d’autres plateformes.</span><span class="sxs-lookup"><span data-stu-id="345f6-112">The portal gives security teams a centralized view of threats on iOS devices along with other platforms.</span></span>

> [!CAUTION]
> <span data-ttu-id="345f6-113">L’exécution d’autres produits de protection des points de terminaison tiers avec Defender for Endpoint sur iOS est susceptible de provoquer des problèmes de performances et des erreurs système imprévisibles.</span><span class="sxs-lookup"><span data-stu-id="345f6-113">Running other third-party endpoint protection products alongside Defender for Endpoint on iOS is likely to cause performance problems and unpredictable system errors.</span></span>

## <a name="pre-requisites"></a><span data-ttu-id="345f6-114">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="345f6-114">Pre-requisites</span></span>

<span data-ttu-id="345f6-115">**Pour les utilisateurs finaux**</span><span class="sxs-lookup"><span data-stu-id="345f6-115">**For End Users**</span></span>

- <span data-ttu-id="345f6-116">Licence Microsoft Defender pour point de terminaison attribuée à l’utilisateur final de l’application.</span><span class="sxs-lookup"><span data-stu-id="345f6-116">Microsoft Defender for Endpoint license assigned to the end user(s) of the app.</span></span> <span data-ttu-id="345f6-117">Consultez [Microsoft Defender pour les conditions requises pour les licences de point de terminaison.](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/minimum-requirements#licensing-requirements)</span><span class="sxs-lookup"><span data-stu-id="345f6-117">See [Microsoft Defender for Endpoint licensing requirements](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/minimum-requirements#licensing-requirements).</span></span>

- <span data-ttu-id="345f6-118">Les appareils sont inscrits [via](https://docs.microsoft.com/mem/intune/user-help/enroll-your-device-in-intune-ios) l’application Portail d’entreprise Intune pour appliquer les stratégies de conformité des appareils Intune.</span><span class="sxs-lookup"><span data-stu-id="345f6-118">Device(s) are [enrolled](https://docs.microsoft.com/mem/intune/user-help/enroll-your-device-in-intune-ios) via the Intune Company Portal app to enforce Intune device compliance policies.</span></span> <span data-ttu-id="345f6-119">Pour ce faire, l’utilisateur final doit se voir attribuer Microsoft Intune licence.</span><span class="sxs-lookup"><span data-stu-id="345f6-119">This requires the end user to be assigned a Microsoft Intune license.</span></span>
    - <span data-ttu-id="345f6-120">Portail d’entreprise Intune’application peut être téléchargée à partir de [l’App Store d’Apple.](https://apps.apple.com/us/app/intune-company-portal/id719171358)</span><span class="sxs-lookup"><span data-stu-id="345f6-120">Intune Company Portal app can be downloaded from the [Apple App Store](https://apps.apple.com/us/app/intune-company-portal/id719171358).</span></span>
    - <span data-ttu-id="345f6-121">Notez qu’Apple n’autorise pas la redirection des utilisateurs à télécharger d’autres applications à partir de l’App Store et que cette étape doit donc être effectuée par l’utilisateur avant l’intégration à l’application Microsoft Defender pour endpoint.</span><span class="sxs-lookup"><span data-stu-id="345f6-121">Note that Apple does not allow redirecting users to download other apps from the app store and hence this step needs to be done by the user before onboarding to Microsoft Defender for Endpoint app.</span></span>

- <span data-ttu-id="345f6-122">Pour plus d’informations sur l’attribution de licences, voir [Attribuer des licences aux utilisateurs.](https://docs.microsoft.com/azure/active-directory/users-groups-roles/licensing-groups-assign)</span><span class="sxs-lookup"><span data-stu-id="345f6-122">For more information on how to assign licenses, see [Assign licenses to users](https://docs.microsoft.com/azure/active-directory/users-groups-roles/licensing-groups-assign).</span></span>

<span data-ttu-id="345f6-123">**Pour les administrateurs**</span><span class="sxs-lookup"><span data-stu-id="345f6-123">**For Administrators**</span></span>

- <span data-ttu-id="345f6-124">Accès au portail Centre de sécurité Microsoft Defender web.</span><span class="sxs-lookup"><span data-stu-id="345f6-124">Access to the Microsoft Defender Security Center portal.</span></span>

    > [!NOTE]
    > <span data-ttu-id="345f6-125">Microsoft Intune est la seule solution de gestion des périphériques mobiles (MDM) prise en charge pour le déploiement de Microsoft Defender pour Endpoint sur iOS.</span><span class="sxs-lookup"><span data-stu-id="345f6-125">Microsoft Intune is the only supported Mobile Device Management (MDM) solution for deploying Microsoft Defender for Endpoint on iOS.</span></span> <span data-ttu-id="345f6-126">Actuellement, seuls les appareils inscrits sont pris en charge pour l’application de Defender for Endpoint sur les stratégies de conformité des appareils liées à iOS dans Intune.</span><span class="sxs-lookup"><span data-stu-id="345f6-126">Currently only enrolled devices are supported for enforcing Defender for Endpoint on iOS related device compliance policies in Intune.</span></span>

- <span data-ttu-id="345f6-127">Accès à [Microsoft Endpoint Manager centre d’administration,](https://go.microsoft.com/fwlink/?linkid=2109431)pour déployer l’application pour les groupes d’utilisateurs inscrits dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="345f6-127">Access to [Microsoft Endpoint Manager admin center](https://go.microsoft.com/fwlink/?linkid=2109431), to deploy the app to enrolled user groups in your organization.</span></span>

<span data-ttu-id="345f6-128">**Conditions requises pour le réseau**</span><span class="sxs-lookup"><span data-stu-id="345f6-128">**Network Requirements**</span></span>
- <span data-ttu-id="345f6-129">Pour que Microsoft Defender pour le point de terminaison sur iOS fonctionne lorsqu’il est connecté à un réseau, le pare-feu/proxy doit être configuré pour permettre l’accès aux URL du service Microsoft Defender pour les points de [terminaison](configure-proxy-internet.md#enable-access-to-microsoft-defender-for-endpoint-service-urls-in-the-proxy-server)</span><span class="sxs-lookup"><span data-stu-id="345f6-129">For Microsoft Defender for Endpoint on iOS to function when connected to a network the firewall/proxy will need to be configured to [enable access to Microsoft Defender for Endpoint service URLs](configure-proxy-internet.md#enable-access-to-microsoft-defender-for-endpoint-service-urls-in-the-proxy-server)</span></span>

<span data-ttu-id="345f6-130">**Configuration requise**</span><span class="sxs-lookup"><span data-stu-id="345f6-130">**System Requirements**</span></span>

- <span data-ttu-id="345f6-131">Appareils iOS exécutant iOS 11.0 et supérieurs.</span><span class="sxs-lookup"><span data-stu-id="345f6-131">iOS devices running iOS 11.0 and above.</span></span> <span data-ttu-id="345f6-132">iPad sont officiellement pris en charge à partir de la version 1.1.15010101 et versions antérieures.</span><span class="sxs-lookup"><span data-stu-id="345f6-132">iPad devices are officially supported from version 1.1.15010101 onward.</span></span>

- <span data-ttu-id="345f6-133">L’appareil est inscrit avec [l’application Portail d’entreprise Intune.](https://apps.apple.com/us/app/intune-company-portal/id719171358)</span><span class="sxs-lookup"><span data-stu-id="345f6-133">Device is enrolled with the [Intune Company Portal app](https://apps.apple.com/us/app/intune-company-portal/id719171358).</span></span>

> [!NOTE]
> <span data-ttu-id="345f6-134">**Microsoft Defender ATP (Microsoft Defender pour point de terminaison) sur iOS est désormais disponible sur [l’App Store d’Apple.](https://aka.ms/mdatpiosappstore)**</span><span class="sxs-lookup"><span data-stu-id="345f6-134">**Microsoft Defender ATP (Microsoft Defender for Endpoint) on iOS is now available on [Apple App Store](https://aka.ms/mdatpiosappstore).**</span></span>

## <a name="installation-instructions"></a><span data-ttu-id="345f6-135">Instructions d’installation</span><span class="sxs-lookup"><span data-stu-id="345f6-135">Installation instructions</span></span>

<span data-ttu-id="345f6-136">Le déploiement de Microsoft Defender pour Endpoint sur iOS s’effectue via Microsoft Intune (MDM) et les appareils supervisés et non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="345f6-136">Deployment of Microsoft Defender for Endpoint on iOS is via Microsoft Intune (MDM) and both supervised and unsupervised devices are supported.</span></span>
<span data-ttu-id="345f6-137">Pour plus d’informations, [voir Déployer Microsoft Defender pour endpoint sur iOS.](ios-install.md)</span><span class="sxs-lookup"><span data-stu-id="345f6-137">For more information, see [Deploy Microsoft Defender for Endpoint on iOS](ios-install.md).</span></span>

## <a name="resources"></a><span data-ttu-id="345f6-138">Ressources</span><span class="sxs-lookup"><span data-stu-id="345f6-138">Resources</span></span>

- <span data-ttu-id="345f6-139">Restez informé des prochaines publication en visitant les nouveautés de [Microsoft Defender pour Endpoint sur iOS](ios-whatsnew.md) ou notre [blog.](https://techcommunity.microsoft.com/t5/microsoft-defender-atp/bg-p/MicrosoftDefenderATPBlog/label-name/iOS)</span><span class="sxs-lookup"><span data-stu-id="345f6-139">Stay informed about upcoming releases by visiting [What's new in Microsoft Defender for Endpoint on iOS](ios-whatsnew.md) or our [blog](https://techcommunity.microsoft.com/t5/microsoft-defender-atp/bg-p/MicrosoftDefenderATPBlog/label-name/iOS).</span></span>

- <span data-ttu-id="345f6-140">Fournir des commentaires via le système de commentaires dans l’application ou via [le portail SecOps](https://securitycenter.microsoft.com)</span><span class="sxs-lookup"><span data-stu-id="345f6-140">Provide feedback through in-app feedback system or through [SecOps portal](https://securitycenter.microsoft.com)</span></span>

## <a name="next-steps"></a><span data-ttu-id="345f6-141">Prochaines étapes</span><span class="sxs-lookup"><span data-stu-id="345f6-141">Next steps</span></span>

- [<span data-ttu-id="345f6-142">Déployer Microsoft Defender pour le point de terminaison sur iOS</span><span class="sxs-lookup"><span data-stu-id="345f6-142">Deploy Microsoft Defender for Endpoint on iOS</span></span>](ios-install.md)
- [<span data-ttu-id="345f6-143">Configurer Microsoft Defender pour endpoint sur les fonctionnalités iOS</span><span class="sxs-lookup"><span data-stu-id="345f6-143">Configure Microsoft Defender for Endpoint on iOS features</span></span>](ios-configure-features.md)
