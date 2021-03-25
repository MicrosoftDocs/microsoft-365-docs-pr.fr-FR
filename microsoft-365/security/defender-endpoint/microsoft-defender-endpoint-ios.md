---
title: Vue d’ensemble de Microsoft Defender ATP pour iOS
ms.reviewer: ''
description: Décrit comment installer et utiliser Microsoft Defender ATP pour iOS
keywords: microsoft, defender, atp, ios, vue d’ensemble, installation, déployer, désinstallation, intune
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
ms.openlocfilehash: 6e5aae9dcb361caf9133c1270a16711fc43033bb
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51066286"
---
# <a name="microsoft-defender-for-endpoint-for-ios"></a><span data-ttu-id="31319-104">Microsoft Defender pour point de terminaison iOS</span><span class="sxs-lookup"><span data-stu-id="31319-104">Microsoft Defender for Endpoint for iOS</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="31319-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="31319-105">**Applies to:**</span></span>
- [<span data-ttu-id="31319-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="31319-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2146631)
- [<span data-ttu-id="31319-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="31319-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="31319-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="31319-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="31319-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="31319-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

<span data-ttu-id="31319-110">**Microsoft Defender pour le point de terminaison pour iOS** offre une protection contre le hameçonnage et les connexions réseau non sécurisées à partir de sites web, de courriers électroniques et d’applications.</span><span class="sxs-lookup"><span data-stu-id="31319-110">**Microsoft Defender for Endpoint for iOS** will offer protection against phishing and unsafe network connections from websites, emails, and apps.</span></span> <span data-ttu-id="31319-111">Toutes les alertes seront disponibles via un seul volet de verre dans le Centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="31319-111">All alerts will be available through a single pane of glass in the Microsoft Defender Security Center.</span></span> <span data-ttu-id="31319-112">Le portail offre aux équipes de sécurité une vue centralisée des menaces sur les appareils iOS, ainsi que d’autres plateformes.</span><span class="sxs-lookup"><span data-stu-id="31319-112">The portal gives security teams a centralized view of threats on iOS devices along with other platforms.</span></span>

> [!CAUTION]
> <span data-ttu-id="31319-113">L’exécution d’autres produits de protection de point de terminaison tiers avec Defender for Endpoint pour iOS est susceptible de provoquer des problèmes de performances et des erreurs système imprévisibles.</span><span class="sxs-lookup"><span data-stu-id="31319-113">Running other third-party endpoint protection products alongside Defender for Endpoint for iOS is likely to cause performance problems and unpredictable system errors.</span></span>

## <a name="pre-requisites"></a><span data-ttu-id="31319-114">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="31319-114">Pre-requisites</span></span>

<span data-ttu-id="31319-115">**Pour les utilisateurs finaux**</span><span class="sxs-lookup"><span data-stu-id="31319-115">**For End Users**</span></span>

- <span data-ttu-id="31319-116">Licence Microsoft Defender pour point de terminaison attribuée à l’utilisateur final de l’application.</span><span class="sxs-lookup"><span data-stu-id="31319-116">Microsoft Defender for Endpoint license assigned to the end user(s) of the app.</span></span> <span data-ttu-id="31319-117">Consultez [Microsoft Defender pour les conditions requises pour les licences de point de terminaison.](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/minimum-requirements#licensing-requirements)</span><span class="sxs-lookup"><span data-stu-id="31319-117">See [Microsoft Defender for Endpoint licensing requirements](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/minimum-requirements#licensing-requirements).</span></span>

- <span data-ttu-id="31319-118">Les appareils sont inscrits [via](https://docs.microsoft.com/mem/intune/user-help/enroll-your-device-in-intune-ios) l’application Portail d’entreprise Intune pour appliquer les stratégies de conformité des appareils Intune.</span><span class="sxs-lookup"><span data-stu-id="31319-118">Device(s) are [enrolled](https://docs.microsoft.com/mem/intune/user-help/enroll-your-device-in-intune-ios) via the Intune Company Portal app to enforce Intune device compliance policies.</span></span> <span data-ttu-id="31319-119">Pour ce faire, l’utilisateur final doit se voir attribuer une licence Microsoft Intune.</span><span class="sxs-lookup"><span data-stu-id="31319-119">This requires the end user to be assigned a Microsoft Intune license.</span></span>
    - <span data-ttu-id="31319-120">L’application Portail d’entreprise Intune peut être téléchargée à partir de [l’App Store d’Apple.](https://apps.apple.com/us/app/intune-company-portal/id719171358)</span><span class="sxs-lookup"><span data-stu-id="31319-120">Intune Company Portal app can be downloaded from the [Apple App Store](https://apps.apple.com/us/app/intune-company-portal/id719171358).</span></span>
    - <span data-ttu-id="31319-121">Notez qu’Apple n’autorise pas la redirection des utilisateurs à télécharger d’autres applications à partir de l’App Store et que cette étape doit donc être effectuée par l’utilisateur avant l’intégration à l’application Microsoft Defender pour endpoint.</span><span class="sxs-lookup"><span data-stu-id="31319-121">Note that Apple does not allow redirecting users to download other apps from the app store and hence this step needs to be done by the user before onboarding to Microsoft Defender for Endpoint app.</span></span>

- <span data-ttu-id="31319-122">Pour plus d’informations sur l’attribution de licences, voir [Attribuer des licences aux utilisateurs.](https://docs.microsoft.com/azure/active-directory/users-groups-roles/licensing-groups-assign)</span><span class="sxs-lookup"><span data-stu-id="31319-122">For more information on how to assign licenses, see [Assign licenses to users](https://docs.microsoft.com/azure/active-directory/users-groups-roles/licensing-groups-assign).</span></span>

<span data-ttu-id="31319-123">**Pour les administrateurs**</span><span class="sxs-lookup"><span data-stu-id="31319-123">**For Administrators**</span></span>

- <span data-ttu-id="31319-124">Accès au portail Centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="31319-124">Access to the Microsoft Defender Security Center portal.</span></span>

    > [!NOTE]
    > <span data-ttu-id="31319-125">Microsoft Intune est la seule solution de gestion des périphériques mobiles (MDM) prise en charge pour le déploiement de Microsoft Defender pour Endpoint pour iOS.</span><span class="sxs-lookup"><span data-stu-id="31319-125">Microsoft Intune is the only supported Mobile Device Management (MDM) solution for deploying Microsoft Defender for Endpoint for iOS.</span></span> <span data-ttu-id="31319-126">Actuellement, seuls les appareils inscrits sont pris en charge pour l’application de Defender for Endpoint pour les stratégies de conformité des appareils liées à iOS dans Intune.</span><span class="sxs-lookup"><span data-stu-id="31319-126">Currently only enrolled devices are supported for enforcing Defender for Endpoint for iOS related device compliance policies in Intune.</span></span>

- <span data-ttu-id="31319-127">Accès au [Centre d’administration Microsoft Endpoint Manager](https://go.microsoft.com/fwlink/?linkid=2109431), pour déployer l’application pour les groupes d’utilisateurs inscrits dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="31319-127">Access to [Microsoft Endpoint Manager admin center](https://go.microsoft.com/fwlink/?linkid=2109431), to deploy the app to enrolled user groups in your organization.</span></span>

<span data-ttu-id="31319-128">**Configuration requise**</span><span class="sxs-lookup"><span data-stu-id="31319-128">**System Requirements**</span></span>

- <span data-ttu-id="31319-129">Appareils iOS exécutant iOS 11.0 et supérieurs.</span><span class="sxs-lookup"><span data-stu-id="31319-129">iOS devices running iOS 11.0 and above.</span></span> <span data-ttu-id="31319-130">Les appareils iPad sont officiellement pris en charge à partir de la version 1.1.15010101 et versions antérieures.</span><span class="sxs-lookup"><span data-stu-id="31319-130">iPad devices are officially supported from version 1.1.15010101 onward.</span></span>

- <span data-ttu-id="31319-131">L’appareil est inscrit avec [l’application Portail d’entreprise Intune.](https://apps.apple.com/us/app/intune-company-portal/id719171358)</span><span class="sxs-lookup"><span data-stu-id="31319-131">Device is enrolled with the [Intune Company Portal app](https://apps.apple.com/us/app/intune-company-portal/id719171358).</span></span>

> [!NOTE]
> <span data-ttu-id="31319-132">**Microsoft Defender ATP (Microsoft Defender for Endpoint) pour iOS est désormais disponible sur [l’App Store d’Apple.](https://aka.ms/mdatpiosappstore)**</span><span class="sxs-lookup"><span data-stu-id="31319-132">**Microsoft Defender ATP (Microsoft Defender for Endpoint) for iOS is now available on [Apple App Store](https://aka.ms/mdatpiosappstore).**</span></span>

## <a name="installation-instructions"></a><span data-ttu-id="31319-133">Instructions d’installation</span><span class="sxs-lookup"><span data-stu-id="31319-133">Installation instructions</span></span>

<span data-ttu-id="31319-134">Le déploiement de Microsoft Defender pour endpoint pour iOS est réalisé via Microsoft Intune (MDM) et les appareils supervisés et non pris en charge sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="31319-134">Deployment of Microsoft Defender for Endpoint for iOS is via Microsoft Intune (MDM) and both supervised and unsupervised devices are supported.</span></span>
<span data-ttu-id="31319-135">Pour plus d’informations, [voir Déployer Microsoft Defender pour endpoint pour iOS.](ios-install.md)</span><span class="sxs-lookup"><span data-stu-id="31319-135">For more information, see [Deploy Microsoft Defender for Endpoint for iOS](ios-install.md).</span></span>

## <a name="resources"></a><span data-ttu-id="31319-136">Ressources</span><span class="sxs-lookup"><span data-stu-id="31319-136">Resources</span></span>

- <span data-ttu-id="31319-137">Restez informé des prochaines publication en visitant notre [blog.](https://techcommunity.microsoft.com/t5/microsoft-defender-atp/bg-p/MicrosoftDefenderATPBlog/label-name/iOS)</span><span class="sxs-lookup"><span data-stu-id="31319-137">Stay informed about upcoming releases by visiting our [blog](https://techcommunity.microsoft.com/t5/microsoft-defender-atp/bg-p/MicrosoftDefenderATPBlog/label-name/iOS).</span></span>

- <span data-ttu-id="31319-138">Fournir des commentaires via le système de commentaires dans l’application ou via [le portail SecOps](https://securitycenter.microsoft.com)</span><span class="sxs-lookup"><span data-stu-id="31319-138">Provide feedback through in-app feedback system or through [SecOps portal](https://securitycenter.microsoft.com)</span></span>

## <a name="next-steps"></a><span data-ttu-id="31319-139">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="31319-139">Next steps</span></span>

- [<span data-ttu-id="31319-140">Déployer Microsoft Defender pour le point de terminaison pour iOS</span><span class="sxs-lookup"><span data-stu-id="31319-140">Deploy Microsoft Defender for Endpoint for iOS</span></span>](ios-install.md)
- [<span data-ttu-id="31319-141">Configurer Microsoft Defender pour le point de terminaison pour les fonctionnalités iOS</span><span class="sxs-lookup"><span data-stu-id="31319-141">Configure Microsoft Defender for Endpoint for iOS features</span></span>](ios-configure-features.md)
