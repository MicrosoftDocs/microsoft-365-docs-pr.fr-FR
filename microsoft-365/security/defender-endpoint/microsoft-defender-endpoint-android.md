---
title: Microsoft Defender ATP pour Android
ms.reviewer: ''
description: Décrit comment installer et utiliser Microsoft Defender ATP pour Android
keywords: microsoft, defender, atp, android, installation, déployer, désinstallation, intune
search.product: eADQiWindows 10XVcnh
search.appverid: met150
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: dansimp
author: dansimp
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection:
- m365-security-compliance
- m365initiative-defender-endpoint
ms.topic: conceptual
ms.technology: mde
ms.openlocfilehash: e2432dc4aa2c67fadc9112512a080f24c0064df4
ms.sourcegitcommit: 6f2288e0c863496dfd0ee38de754bd43096ab3e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2021
ms.locfileid: "51187612"
---
# <a name="microsoft-defender-for-endpoint-for-android"></a><span data-ttu-id="82d62-104">Microsoft Defender pour le point de terminaison pour Android</span><span class="sxs-lookup"><span data-stu-id="82d62-104">Microsoft Defender for Endpoint for Android</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="82d62-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="82d62-105">**Applies to:**</span></span>
- [<span data-ttu-id="82d62-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="82d62-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="82d62-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="82d62-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="82d62-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="82d62-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="82d62-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="82d62-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

<span data-ttu-id="82d62-110">Cette rubrique décrit comment installer, configurer, mettre à jour et utiliser Defender pour Endpoint pour Android.</span><span class="sxs-lookup"><span data-stu-id="82d62-110">This topic describes how to install, configure, update, and use Defender for Endpoint for Android.</span></span>

> [!CAUTION]
> <span data-ttu-id="82d62-111">L’exécution d’autres produits de protection de point de terminaison tiers avec Defender pour Endpoint pour Android est susceptible de provoquer des problèmes de performances et des erreurs système imprévisibles.</span><span class="sxs-lookup"><span data-stu-id="82d62-111">Running other third-party endpoint protection products alongside Defender for Endpoint for Android is likely to cause performance problems and unpredictable system errors.</span></span>


## <a name="how-to-install-microsoft-defender-for-endpoint-for-android"></a><span data-ttu-id="82d62-112">Comment installer Microsoft Defender pour le point de terminaison pour Android</span><span class="sxs-lookup"><span data-stu-id="82d62-112">How to install Microsoft Defender for Endpoint for Android</span></span>

### <a name="prerequisites"></a><span data-ttu-id="82d62-113">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="82d62-113">Prerequisites</span></span>

-   <span data-ttu-id="82d62-114">**Pour les utilisateurs finaux**</span><span class="sxs-lookup"><span data-stu-id="82d62-114">**For end users**</span></span>

    -   <span data-ttu-id="82d62-115">Licence Microsoft Defender pour point de terminaison attribuée à l’utilisateur final de l’application.</span><span class="sxs-lookup"><span data-stu-id="82d62-115">Microsoft Defender for Endpoint license assigned to the end user(s) of the app.</span></span> <span data-ttu-id="82d62-116">Voir [microsoft Defender pour les conditions requises pour les licences de point de terminaison](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/minimum-requirements#licensing-requirements)</span><span class="sxs-lookup"><span data-stu-id="82d62-116">See [Microsoft Defender for Endpoint licensing requirements](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/minimum-requirements#licensing-requirements)</span></span>

    -   <span data-ttu-id="82d62-117">L’application Portail d’entreprise Intune peut être téléchargée à partir de [Google Play](https://play.google.com/store/apps/details?id=com.microsoft.windowsintune.companyportal) et est disponible sur l’appareil Android.</span><span class="sxs-lookup"><span data-stu-id="82d62-117">Intune Company Portal app can be downloaded from [Google Play](https://play.google.com/store/apps/details?id=com.microsoft.windowsintune.companyportal) and is available on the Android device.</span></span>

        -   <span data-ttu-id="82d62-118">En outre, les appareils peuvent être inscrits [via](https://docs.microsoft.com/mem/intune/user-help/enroll-device-android-company-portal) l’application Portail d’entreprise Intune pour appliquer les stratégies de conformité des appareils Intune.</span><span class="sxs-lookup"><span data-stu-id="82d62-118">Additionally, device(s) can be [enrolled](https://docs.microsoft.com/mem/intune/user-help/enroll-device-android-company-portal) via the Intune Company Portal app to enforce Intune device compliance policies.</span></span> <span data-ttu-id="82d62-119">Pour ce faire, l’utilisateur final doit se voir attribuer une licence Microsoft Intune.</span><span class="sxs-lookup"><span data-stu-id="82d62-119">This requires the end user to be assigned a Microsoft Intune license.</span></span>

    -   <span data-ttu-id="82d62-120">Pour plus d’informations sur l’attribution de licences, voir [Attribuer des licences aux utilisateurs.](https://docs.microsoft.com/azure/active-directory/users-groups-roles/licensing-groups-assign)</span><span class="sxs-lookup"><span data-stu-id="82d62-120">For more information on how to assign licenses, see [Assign licenses to users](https://docs.microsoft.com/azure/active-directory/users-groups-roles/licensing-groups-assign).</span></span>
        

-   <span data-ttu-id="82d62-121">**Pour les administrateurs**</span><span class="sxs-lookup"><span data-stu-id="82d62-121">**For Administrators**</span></span>

    -   <span data-ttu-id="82d62-122">Accès au portail Centre de sécurité Microsoft Defender.</span><span class="sxs-lookup"><span data-stu-id="82d62-122">Access to the Microsoft Defender Security Center portal.</span></span>

        > [!NOTE]
        > <span data-ttu-id="82d62-123">Microsoft Intune est la seule solution de gestion des périphériques mobiles (MDM) prise en charge pour le déploiement de Microsoft Defender pour Endpoint pour Android.</span><span class="sxs-lookup"><span data-stu-id="82d62-123">Microsoft Intune is the only supported Mobile Device Management (MDM) solution for deploying Microsoft Defender for Endpoint for Android.</span></span> <span data-ttu-id="82d62-124">Actuellement, seuls les appareils inscrits sont pris en charge pour l’application de Defender for Endpoint pour les stratégies de conformité des appareils android dans Intune.</span><span class="sxs-lookup"><span data-stu-id="82d62-124">Currently only enrolled devices are supported for enforcing Defender for Endpoint for Android related device compliance policies in Intune.</span></span> 

    -   <span data-ttu-id="82d62-125">Accédez [au Centre d’administration Microsoft Endpoint Manager](https://go.microsoft.com/fwlink/?linkid=2109431)pour déployer l’application sur les groupes d’utilisateurs inscrits dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="82d62-125">Access [Microsoft Endpoint Manager admin center](https://go.microsoft.com/fwlink/?linkid=2109431), to deploy the app to enrolled user groups in your organization.</span></span>

### <a name="system-requirements"></a><span data-ttu-id="82d62-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="82d62-126">System Requirements</span></span>

-   <span data-ttu-id="82d62-127">Appareils Android exécutant Android 6.0 et version supérieure.</span><span class="sxs-lookup"><span data-stu-id="82d62-127">Android devices running Android 6.0 and above.</span></span>
-   <span data-ttu-id="82d62-128">L’application Portail d’entreprise Intune est téléchargée à partir [de Google Play](https://play.google.com/store/apps/details?id=com.microsoft.windowsintune.companyportal) et installée.</span><span class="sxs-lookup"><span data-stu-id="82d62-128">Intune Company Portal app is downloaded from [Google Play](https://play.google.com/store/apps/details?id=com.microsoft.windowsintune.companyportal) and installed.</span></span> <span data-ttu-id="82d62-129">L’inscription des appareils est requise pour que les stratégies de conformité des appareils Intune soient appliquées.</span><span class="sxs-lookup"><span data-stu-id="82d62-129">Device enrollment is required for Intune device compliance policies to be enforced.</span></span>

### <a name="installation-instructions"></a><span data-ttu-id="82d62-130">Instructions d’installation</span><span class="sxs-lookup"><span data-stu-id="82d62-130">Installation instructions</span></span>

<span data-ttu-id="82d62-131">Microsoft Defender pour le point de terminaison pour Android prend en charge l’installation sur les deux modes d’appareils inscrits : les modes Administrateur d’appareil et Android Entreprise hérités.</span><span class="sxs-lookup"><span data-stu-id="82d62-131">Microsoft Defender for Endpoint for Android supports installation on both modes of enrolled devices - the legacy Device Administrator and Android Enterprise modes.</span></span>
<span data-ttu-id="82d62-132">**Actuellement, les appareils personnels avec profil de travail et appareils utilisateur entièrement gérés par l’entreprise sont pris en charge dans Android Entreprise. La prise en charge d’autres modes Android Enterprise sera annoncée lorsque vous serez prêt.**</span><span class="sxs-lookup"><span data-stu-id="82d62-132">**Currently, Personally-owned devices with work profile and Corporate-owned fully managed user device enrolments are supported in Android Enterprise. Support for other Android Enterprise modes will be announced when ready.**</span></span>

<span data-ttu-id="82d62-133">Le déploiement de Microsoft Defender pour Endpoint pour Android est via Microsoft Intune (MDM).</span><span class="sxs-lookup"><span data-stu-id="82d62-133">Deployment of Microsoft Defender for Endpoint for Android is via Microsoft Intune (MDM).</span></span>
<span data-ttu-id="82d62-134">Pour plus d’informations, voir [Déployer Microsoft Defender pour endpoint pour Android avec Microsoft Intune.](android-intune.md)</span><span class="sxs-lookup"><span data-stu-id="82d62-134">For more information, see [Deploy Microsoft Defender for Endpoint for Android with Microsoft Intune](android-intune.md).</span></span>


> [!NOTE]
> <span data-ttu-id="82d62-135">**Microsoft Defender pour le point de terminaison pour Android est désormais disponible [sur Google Play.](https://play.google.com/store/apps/details?id=com.microsoft.scmx)**</span><span class="sxs-lookup"><span data-stu-id="82d62-135">**Microsoft Defender for Endpoint for Android is available on [Google Play](https://play.google.com/store/apps/details?id=com.microsoft.scmx) now.**</span></span> <br> <span data-ttu-id="82d62-136">Vous pouvez vous connecter à Google Play à partir d’Intune pour déployer l’application Microsoft Defender pour endpoint, sur les modes d’inscription Administrateur d’appareil et Android Entreprise.</span><span class="sxs-lookup"><span data-stu-id="82d62-136">You can connect to Google Play from Intune to deploy Microsoft Defender for Endpoint app, across Device Administrator and Android Enterprise entrollment modes.</span></span> 

## <a name="how-to-configure-microsoft-defender-for-endpoint-for-android"></a><span data-ttu-id="82d62-137">Comment configurer Microsoft Defender pour endpoint pour Android</span><span class="sxs-lookup"><span data-stu-id="82d62-137">How to Configure Microsoft Defender for Endpoint for Android</span></span>

<span data-ttu-id="82d62-138">Des instructions sur la configuration de Microsoft Defender pour les fonctionnalités Endpoint pour Android sont disponibles dans Configurer Microsoft Defender pour les fonctionnalités [Endpoint pour Android.](android-configure.md)</span><span class="sxs-lookup"><span data-stu-id="82d62-138">Guidance on how to configure Microsoft Defender for Endpoint for Android features is available in [Configure Microsoft Defender for Endpoint for Android features](android-configure.md).</span></span>



## <a name="related-topics"></a><span data-ttu-id="82d62-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="82d62-139">Related topics</span></span>
- [<span data-ttu-id="82d62-140">Déployer Microsoft Defender pour le point de terminaison avec Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="82d62-140">Deploy Microsoft Defender for Endpoint for with Microsoft Intune</span></span>](android-intune.md)
- [<span data-ttu-id="82d62-141">Configurer Microsoft Defender pour les fonctionnalités Endpoint pour Android</span><span class="sxs-lookup"><span data-stu-id="82d62-141">Configure Microsoft Defender for Endpoint for Android features</span></span>](android-configure.md)

