---
title: Microsoft Defender pour point de terminaison Android
ms.reviewer: ''
description: Décrit comment installer et utiliser Microsoft Defender pour endpoint sur Android
keywords: microsoft, defender, Microsoft Defender pour le point de terminaison, android, installation, déployer, désinstaller, intune
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
ms.openlocfilehash: 3f8a8c04f608096e5c226d6899fbbd983bd8d8c1
ms.sourcegitcommit: ff20f5b4e3268c7c98a84fb1cbe7db7151596b6d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/06/2021
ms.locfileid: "52246427"
---
# <a name="microsoft-defender-for-endpoint-on-android"></a><span data-ttu-id="3c260-104">Microsoft Defender pour point de terminaison Android</span><span class="sxs-lookup"><span data-stu-id="3c260-104">Microsoft Defender for Endpoint on Android</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="3c260-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="3c260-105">**Applies to:**</span></span>
- [<span data-ttu-id="3c260-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="3c260-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="3c260-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="3c260-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="3c260-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="3c260-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="3c260-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="3c260-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

<span data-ttu-id="3c260-110">Cette rubrique décrit comment installer, configurer, mettre à jour et utiliser Defender pour Endpoint sur Android.</span><span class="sxs-lookup"><span data-stu-id="3c260-110">This topic describes how to install, configure, update, and use Defender for Endpoint on Android.</span></span>

> [!CAUTION]
> <span data-ttu-id="3c260-111">L’exécution d’autres produits de protection des points de terminaison tiers avec Defender for Endpoint sur Android est susceptible de provoquer des problèmes de performances et des erreurs système imprévisibles.</span><span class="sxs-lookup"><span data-stu-id="3c260-111">Running other third-party endpoint protection products alongside Defender for Endpoint on Android is likely to cause performance problems and unpredictable system errors.</span></span>


## <a name="how-to-install-microsoft-defender-for-endpoint-on-android"></a><span data-ttu-id="3c260-112">Comment installer Microsoft Defender pour le point de terminaison sur Android</span><span class="sxs-lookup"><span data-stu-id="3c260-112">How to install Microsoft Defender for Endpoint on Android</span></span>

### <a name="prerequisites"></a><span data-ttu-id="3c260-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3c260-113">Prerequisites</span></span>

-   <span data-ttu-id="3c260-114">**Pour les utilisateurs finaux**</span><span class="sxs-lookup"><span data-stu-id="3c260-114">**For end users**</span></span>

    -   <span data-ttu-id="3c260-115">Licence Microsoft Defender pour point de terminaison attribuée à l’utilisateur final de l’application.</span><span class="sxs-lookup"><span data-stu-id="3c260-115">Microsoft Defender for Endpoint license assigned to the end user(s) of the app.</span></span> <span data-ttu-id="3c260-116">Voir [microsoft Defender pour les conditions requises pour les licences de point de terminaison](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/minimum-requirements#licensing-requirements)</span><span class="sxs-lookup"><span data-stu-id="3c260-116">See [Microsoft Defender for Endpoint licensing requirements](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/minimum-requirements#licensing-requirements)</span></span>

    -   <span data-ttu-id="3c260-117">Portail d’entreprise Intune’application peut être téléchargée à partir [de Google Play](https://play.google.com/store/apps/details?id=com.microsoft.windowsintune.companyportal) et est disponible sur l’appareil Android.</span><span class="sxs-lookup"><span data-stu-id="3c260-117">Intune Company Portal app can be downloaded from [Google Play](https://play.google.com/store/apps/details?id=com.microsoft.windowsintune.companyportal) and is available on the Android device.</span></span>

        -   <span data-ttu-id="3c260-118">En outre, les appareils peuvent être inscrits [via](https://docs.microsoft.com/mem/intune/user-help/enroll-device-android-company-portal) l’application Portail d’entreprise Intune pour appliquer des stratégies de conformité des appareils Intune.</span><span class="sxs-lookup"><span data-stu-id="3c260-118">Additionally, device(s) can be [enrolled](https://docs.microsoft.com/mem/intune/user-help/enroll-device-android-company-portal) via the Intune Company Portal app to enforce Intune device compliance policies.</span></span> <span data-ttu-id="3c260-119">Pour ce faire, l’utilisateur final doit se voir attribuer Microsoft Intune licence.</span><span class="sxs-lookup"><span data-stu-id="3c260-119">This requires the end user to be assigned a Microsoft Intune license.</span></span>

    -   <span data-ttu-id="3c260-120">Pour plus d’informations sur l’attribution de licences, voir [Attribuer des licences aux utilisateurs.](https://docs.microsoft.com/azure/active-directory/users-groups-roles/licensing-groups-assign)</span><span class="sxs-lookup"><span data-stu-id="3c260-120">For more information on how to assign licenses, see [Assign licenses to users](https://docs.microsoft.com/azure/active-directory/users-groups-roles/licensing-groups-assign).</span></span>
        

-   <span data-ttu-id="3c260-121">**Pour les administrateurs**</span><span class="sxs-lookup"><span data-stu-id="3c260-121">**For Administrators**</span></span>

    -   <span data-ttu-id="3c260-122">Accès au portail Centre de sécurité Microsoft Defender web.</span><span class="sxs-lookup"><span data-stu-id="3c260-122">Access to the Microsoft Defender Security Center portal.</span></span>

        > [!NOTE]
        > <span data-ttu-id="3c260-123">Microsoft Intune est la seule solution de gestion des périphériques mobiles (MDM) prise en charge pour le déploiement de Microsoft Defender pour Endpoint sur Android.</span><span class="sxs-lookup"><span data-stu-id="3c260-123">Microsoft Intune is the only supported Mobile Device Management (MDM) solution for deploying Microsoft Defender for Endpoint on Android.</span></span> <span data-ttu-id="3c260-124">Actuellement, seuls les appareils inscrits sont pris en charge pour l’application de Defender for Endpoint sur les stratégies de conformité des appareils android dans Intune.</span><span class="sxs-lookup"><span data-stu-id="3c260-124">Currently only enrolled devices are supported for enforcing Defender for Endpoint on Android related device compliance policies in Intune.</span></span> 

    -   <span data-ttu-id="3c260-125">Accédez [Microsoft Endpoint Manager centre d’administration,](https://go.microsoft.com/fwlink/?linkid=2109431)pour déployer l’application pour les groupes d’utilisateurs inscrits dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="3c260-125">Access [Microsoft Endpoint Manager admin center](https://go.microsoft.com/fwlink/?linkid=2109431), to deploy the app to enrolled user groups in your organization.</span></span>
        
### <a name="network-requirements"></a><span data-ttu-id="3c260-126">Configuration réseau requise</span><span class="sxs-lookup"><span data-stu-id="3c260-126">Network Requirements</span></span>

- <span data-ttu-id="3c260-127">Pour que Microsoft Defender pour le point de terminaison sur Android fonctionne lorsqu’il est connecté à un réseau, le pare-feu/proxy doit être configuré pour permettre l’accès aux URL du service Microsoft Defender pour les points de [terminaison.](configure-proxy-internet.md#enable-access-to-microsoft-defender-for-endpoint-service-urls-in-the-proxy-server)</span><span class="sxs-lookup"><span data-stu-id="3c260-127">For Microsoft Defender for Endpoint on Android to function when connected to a network the firewall/proxy will need to be configured to [enable access to Microsoft Defender for Endpoint service URLs](configure-proxy-internet.md#enable-access-to-microsoft-defender-for-endpoint-service-urls-in-the-proxy-server).</span></span>

### <a name="system-requirements"></a><span data-ttu-id="3c260-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3c260-128">System Requirements</span></span>

-   <span data-ttu-id="3c260-129">Appareils Android exécutant Android 6.0 et version supérieure.</span><span class="sxs-lookup"><span data-stu-id="3c260-129">Android devices running Android 6.0 and above.</span></span>
-   <span data-ttu-id="3c260-130">Portail d’entreprise Intune’application est téléchargée à partir [de Google Play](https://play.google.com/store/apps/details?id=com.microsoft.windowsintune.companyportal) et installée.</span><span class="sxs-lookup"><span data-stu-id="3c260-130">Intune Company Portal app is downloaded from [Google Play](https://play.google.com/store/apps/details?id=com.microsoft.windowsintune.companyportal) and installed.</span></span> <span data-ttu-id="3c260-131">L’inscription des appareils est requise pour que les stratégies de conformité des appareils Intune soient appliquées.</span><span class="sxs-lookup"><span data-stu-id="3c260-131">Device enrollment is required for Intune device compliance policies to be enforced.</span></span>

### <a name="installation-instructions"></a><span data-ttu-id="3c260-132">Instructions d’installation</span><span class="sxs-lookup"><span data-stu-id="3c260-132">Installation instructions</span></span>

<span data-ttu-id="3c260-133">Microsoft Defender pour Endpoint sur Android prend en charge l’installation sur les deux modes d’appareils inscrits : l’administrateur d’appareil hérité et les modes Enterprise Android.</span><span class="sxs-lookup"><span data-stu-id="3c260-133">Microsoft Defender for Endpoint on Android supports installation on both modes of enrolled devices - the legacy Device Administrator and Android Enterprise modes.</span></span>
<span data-ttu-id="3c260-134">**Actuellement, les appareils personnels avec profil de travail et les inscriptions d’appareils utilisateur entièrement gérées par l’entreprise sont pris en charge dans Android Enterprise. La prise en charge des autres modes Enterprise Android sera annoncée lorsque vous serez prêt.**</span><span class="sxs-lookup"><span data-stu-id="3c260-134">**Currently, Personally-owned devices with work profile and Corporate-owned fully managed user device enrollments are supported in Android Enterprise. Support for other Android Enterprise modes will be announced when ready.**</span></span>

<span data-ttu-id="3c260-135">Le déploiement de Microsoft Defender pour Endpoint sur Android s’effectue via Microsoft Intune (MDM).</span><span class="sxs-lookup"><span data-stu-id="3c260-135">Deployment of Microsoft Defender for Endpoint on Android is via Microsoft Intune (MDM).</span></span>
<span data-ttu-id="3c260-136">Pour plus d’informations, voir [Déployer Microsoft Defender pour endpoint sur Android avec Microsoft Intune](android-intune.md).</span><span class="sxs-lookup"><span data-stu-id="3c260-136">For more information, see [Deploy Microsoft Defender for Endpoint on Android with Microsoft Intune](android-intune.md).</span></span>


> [!NOTE]
> <span data-ttu-id="3c260-137">**Microsoft Defender pour le point de terminaison sur Android est désormais disponible [sur Google Play.](https://play.google.com/store/apps/details?id=com.microsoft.scmx)**</span><span class="sxs-lookup"><span data-stu-id="3c260-137">**Microsoft Defender for Endpoint on Android is available on [Google Play](https://play.google.com/store/apps/details?id=com.microsoft.scmx) now.**</span></span> <br> <span data-ttu-id="3c260-138">Vous pouvez vous connecter à Google Play à partir d’Intune pour déployer l’application Microsoft Defender pour Endpoint, sur les modes d’inscription de l’administrateur d’appareil et Enterprise Android.</span><span class="sxs-lookup"><span data-stu-id="3c260-138">You can connect to Google Play from Intune to deploy Microsoft Defender for Endpoint app, across Device Administrator and Android Enterprise entrollment modes.</span></span> 

## <a name="how-to-configure-microsoft-defender-for-endpoint-on-android"></a><span data-ttu-id="3c260-139">Comment configurer Microsoft Defender pour endpoint sur Android</span><span class="sxs-lookup"><span data-stu-id="3c260-139">How to Configure Microsoft Defender for Endpoint on Android</span></span>

<span data-ttu-id="3c260-140">Des instructions sur la configuration de Microsoft Defender pour le point de terminaison sur les fonctionnalités Android sont disponibles dans Configurer Microsoft Defender pour le point de terminaison [sur les fonctionnalités Android.](android-configure.md)</span><span class="sxs-lookup"><span data-stu-id="3c260-140">Guidance on how to configure Microsoft Defender for Endpoint on Android features is available in [Configure Microsoft Defender for Endpoint on Android features](android-configure.md).</span></span>



## <a name="related-topics"></a><span data-ttu-id="3c260-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3c260-141">Related topics</span></span>
- [<span data-ttu-id="3c260-142">Déployer Microsoft Defender pour point de terminaison Android via Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="3c260-142">Deploy Microsoft Defender for Endpoint on Android with Microsoft Intune</span></span>](android-intune.md)
- [<span data-ttu-id="3c260-143">Configurer Microsoft Defender pour point de terminaison pour des fonctionnalités Android</span><span class="sxs-lookup"><span data-stu-id="3c260-143">Configure Microsoft Defender for Endpoint on Android features</span></span>](android-configure.md)

