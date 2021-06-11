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
ms.openlocfilehash: b4c2d586cd23a346db1bcebf891689ff648b639b
ms.sourcegitcommit: 4fb1226d5875bf5b9b29252596855a6562cea9ae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "52844705"
---
# <a name="microsoft-defender-for-endpoint-on-ios"></a><span data-ttu-id="b4ed4-104">Microsoft Defender pour point de terminaison iOS</span><span class="sxs-lookup"><span data-stu-id="b4ed4-104">Microsoft Defender for Endpoint on iOS</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="b4ed4-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="b4ed4-105">**Applies to:**</span></span>
- [<span data-ttu-id="b4ed4-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="b4ed4-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="b4ed4-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="b4ed4-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="b4ed4-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="b4ed4-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="b4ed4-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="b4ed4-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

<span data-ttu-id="b4ed4-110">**Microsoft Defender pour le point de terminaison sur iOS** offre une protection contre le hameçonnage et les connexions réseau non sécurisées à partir de sites web, de courriers électroniques et d’applications.</span><span class="sxs-lookup"><span data-stu-id="b4ed4-110">**Microsoft Defender for Endpoint on iOS** will offer protection against phishing and unsafe network connections from websites, emails, and apps.</span></span> <span data-ttu-id="b4ed4-111">Toutes les alertes sont disponibles via un seul volet de la Centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="b4ed4-111">All alerts will be available through a single pane of glass in the Microsoft Defender Security Center.</span></span> <span data-ttu-id="b4ed4-112">Le portail offre aux équipes de sécurité une vue centralisée des menaces sur les appareils iOS, ainsi que d’autres plateformes.</span><span class="sxs-lookup"><span data-stu-id="b4ed4-112">The portal gives security teams a centralized view of threats on iOS devices along with other platforms.</span></span>

> [!CAUTION]
> <span data-ttu-id="b4ed4-113">L’exécution d’autres produits de protection des points de terminaison tiers avec Defender for Endpoint sur iOS est susceptible de provoquer des problèmes de performances et des erreurs système imprévisibles.</span><span class="sxs-lookup"><span data-stu-id="b4ed4-113">Running other third-party endpoint protection products alongside Defender for Endpoint on iOS is likely to cause performance problems and unpredictable system errors.</span></span>

## <a name="pre-requisites"></a><span data-ttu-id="b4ed4-114">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="b4ed4-114">Pre-requisites</span></span>

<span data-ttu-id="b4ed4-115">**Pour les utilisateurs finaux**</span><span class="sxs-lookup"><span data-stu-id="b4ed4-115">**For End Users**</span></span>

- <span data-ttu-id="b4ed4-116">Licence Microsoft Defender pour point de terminaison attribuée à l’utilisateur final de l’application.</span><span class="sxs-lookup"><span data-stu-id="b4ed4-116">Microsoft Defender for Endpoint license assigned to the end user(s) of the app.</span></span> <span data-ttu-id="b4ed4-117">Consultez [Microsoft Defender pour les conditions requises pour les licences de point de terminaison.](/microsoft-365/security/defender-endpoint/minimum-requirements#licensing-requirements)</span><span class="sxs-lookup"><span data-stu-id="b4ed4-117">See [Microsoft Defender for Endpoint licensing requirements](/microsoft-365/security/defender-endpoint/minimum-requirements#licensing-requirements).</span></span>

- <span data-ttu-id="b4ed4-118">Les appareils sont inscrits [via](/mem/intune/user-help/enroll-your-device-in-intune-ios) l’application Portail d’entreprise Intune pour appliquer les stratégies de conformité des appareils Intune.</span><span class="sxs-lookup"><span data-stu-id="b4ed4-118">Device(s) are [enrolled](/mem/intune/user-help/enroll-your-device-in-intune-ios) via the Intune Company Portal app to enforce Intune device compliance policies.</span></span> <span data-ttu-id="b4ed4-119">Pour ce faire, l’utilisateur final doit se voir attribuer Microsoft Intune licence.</span><span class="sxs-lookup"><span data-stu-id="b4ed4-119">This requires the end user to be assigned a Microsoft Intune license.</span></span>
    - <span data-ttu-id="b4ed4-120">Portail d’entreprise Intune’application peut être téléchargée à partir de [l’App Store d’Apple.](https://apps.apple.com/us/app/intune-company-portal/id719171358)</span><span class="sxs-lookup"><span data-stu-id="b4ed4-120">Intune Company Portal app can be downloaded from the [Apple App Store](https://apps.apple.com/us/app/intune-company-portal/id719171358).</span></span>
    - <span data-ttu-id="b4ed4-121">Notez qu’Apple n’autorise pas la redirection des utilisateurs à télécharger d’autres applications à partir de l’App Store et que cette étape doit donc être effectuée par l’utilisateur avant l’intégration à l’application Microsoft Defender pour endpoint.</span><span class="sxs-lookup"><span data-stu-id="b4ed4-121">Note that Apple does not allow redirecting users to download other apps from the app store and hence this step needs to be done by the user before onboarding to Microsoft Defender for Endpoint app.</span></span>

- <span data-ttu-id="b4ed4-122">Pour plus d’informations sur l’attribution de licences, voir [Attribuer des licences aux utilisateurs.](/azure/active-directory/users-groups-roles/licensing-groups-assign)</span><span class="sxs-lookup"><span data-stu-id="b4ed4-122">For more information on how to assign licenses, see [Assign licenses to users](/azure/active-directory/users-groups-roles/licensing-groups-assign).</span></span>

<span data-ttu-id="b4ed4-123">**Pour les administrateurs**</span><span class="sxs-lookup"><span data-stu-id="b4ed4-123">**For Administrators**</span></span>

- <span data-ttu-id="b4ed4-124">Accès au portail Centre de sécurité Microsoft Defender web.</span><span class="sxs-lookup"><span data-stu-id="b4ed4-124">Access to the Microsoft Defender Security Center portal.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b4ed4-125">Microsoft Intune est la seule solution de gestion des points de terminaison unifiée (UEM) prise en charge pour le déploiement de Microsoft Defender pour Endpoint et l’application de Defender pour les stratégies de conformité des appareils liées aux points de terminaison dans Intune.</span><span class="sxs-lookup"><span data-stu-id="b4ed4-125">Microsoft Intune is the only supported Unified Endpoint Management (UEM) solution for deploying Microsoft Defender for Endpoint and enforcing Defender for Endpoint related device compliance policies in Intune.</span></span>

- <span data-ttu-id="b4ed4-126">Accès à [Microsoft Endpoint Manager centre d’administration,](https://go.microsoft.com/fwlink/?linkid=2109431)pour déployer l’application pour les groupes d’utilisateurs inscrits dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="b4ed4-126">Access to [Microsoft Endpoint Manager admin center](https://go.microsoft.com/fwlink/?linkid=2109431), to deploy the app to enrolled user groups in your organization.</span></span>

<span data-ttu-id="b4ed4-127">**Configuration requise**</span><span class="sxs-lookup"><span data-stu-id="b4ed4-127">**System Requirements**</span></span>

- <span data-ttu-id="b4ed4-128">Appareils iOS exécutant iOS 11.0 et supérieurs.</span><span class="sxs-lookup"><span data-stu-id="b4ed4-128">iOS devices running iOS 11.0 and above.</span></span> <span data-ttu-id="b4ed4-129">iPad sont officiellement pris en charge à partir de la version 1.1.15010101 et versions antérieures.</span><span class="sxs-lookup"><span data-stu-id="b4ed4-129">iPad devices are officially supported from version 1.1.15010101 onward.</span></span>

- <span data-ttu-id="b4ed4-130">L’appareil est inscrit avec [l’application Portail d’entreprise Intune.](https://apps.apple.com/us/app/intune-company-portal/id719171358)</span><span class="sxs-lookup"><span data-stu-id="b4ed4-130">Device is enrolled with the [Intune Company Portal app](https://apps.apple.com/us/app/intune-company-portal/id719171358).</span></span>

## <a name="installation-instructions"></a><span data-ttu-id="b4ed4-131">Instructions d’installation</span><span class="sxs-lookup"><span data-stu-id="b4ed4-131">Installation instructions</span></span>

<span data-ttu-id="b4ed4-132">Le déploiement de Microsoft Defender pour Endpoint sur iOS s’effectue via Microsoft Intune (MDM) et les appareils supervisés et non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="b4ed4-132">Deployment of Microsoft Defender for Endpoint on iOS is via Microsoft Intune (MDM) and both supervised and unsupervised devices are supported.</span></span> <span data-ttu-id="b4ed4-133">Les utilisateurs finaux peuvent également installer directement l’application à partir de [l’App Store d’Apple.](https://aka.ms/mdatpiosappstore)</span><span class="sxs-lookup"><span data-stu-id="b4ed4-133">End-users can also directly install the app from the [Apple app store](https://aka.ms/mdatpiosappstore).</span></span>
<span data-ttu-id="b4ed4-134">Pour plus d’informations, [voir Déployer Microsoft Defender pour endpoint sur iOS.](ios-install.md)</span><span class="sxs-lookup"><span data-stu-id="b4ed4-134">For more information, see [Deploy Microsoft Defender for Endpoint on iOS](ios-install.md).</span></span>

## <a name="resources"></a><span data-ttu-id="b4ed4-135">Ressources</span><span class="sxs-lookup"><span data-stu-id="b4ed4-135">Resources</span></span>

- <span data-ttu-id="b4ed4-136">Restez informé des prochaines publication en visitant les nouveautés de [Microsoft Defender pour Endpoint sur iOS](ios-whatsnew.md) ou notre [blog.](https://techcommunity.microsoft.com/t5/microsoft-defender-atp/bg-p/MicrosoftDefenderATPBlog/label-name/iOS)</span><span class="sxs-lookup"><span data-stu-id="b4ed4-136">Stay informed about upcoming releases by visiting [What's new in Microsoft Defender for Endpoint on iOS](ios-whatsnew.md) or our [blog](https://techcommunity.microsoft.com/t5/microsoft-defender-atp/bg-p/MicrosoftDefenderATPBlog/label-name/iOS).</span></span>

- <span data-ttu-id="b4ed4-137">Fournir des commentaires via le système de commentaires dans l’application ou via [le portail SecOps](https://securitycenter.microsoft.com)</span><span class="sxs-lookup"><span data-stu-id="b4ed4-137">Provide feedback through in-app feedback system or through [SecOps portal](https://securitycenter.microsoft.com)</span></span>

## <a name="next-steps"></a><span data-ttu-id="b4ed4-138">Prochaines étapes</span><span class="sxs-lookup"><span data-stu-id="b4ed4-138">Next steps</span></span>

- [<span data-ttu-id="b4ed4-139">Déployer Microsoft Defender pour le point de terminaison sur iOS</span><span class="sxs-lookup"><span data-stu-id="b4ed4-139">Deploy Microsoft Defender for Endpoint on iOS</span></span>](ios-install.md)
- [<span data-ttu-id="b4ed4-140">Configurer Microsoft Defender pour endpoint sur les fonctionnalités iOS</span><span class="sxs-lookup"><span data-stu-id="b4ed4-140">Configure Microsoft Defender for Endpoint on iOS features</span></span>](ios-configure-features.md)
