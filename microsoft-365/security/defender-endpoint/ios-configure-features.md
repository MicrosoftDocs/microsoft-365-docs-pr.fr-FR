---
title: Configurer Microsoft Defender pour endpoint sur les fonctionnalités iOS
description: Décrit comment déployer Microsoft Defender pour endpoint sur les fonctionnalités iOS
keywords: microsoft, defender, Microsoft Defender for Endpoint, ios, configure, features, ios
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
ms.topic: conceptual
ms.technology: mde
ms.openlocfilehash: dab72da02927c3fff6025eb2d0fa9ed0fdf1d0d7
ms.sourcegitcommit: ff20f5b4e3268c7c98a84fb1cbe7db7151596b6d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/06/2021
ms.locfileid: "52245275"
---
# <a name="configure-microsoft-defender-for-endpoint-on-ios-features"></a><span data-ttu-id="ae9c1-104">Configurer Microsoft Defender pour endpoint sur les fonctionnalités iOS</span><span class="sxs-lookup"><span data-stu-id="ae9c1-104">Configure Microsoft Defender for Endpoint on iOS features</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="ae9c1-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="ae9c1-105">**Applies to:**</span></span>
- [<span data-ttu-id="ae9c1-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="ae9c1-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="ae9c1-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="ae9c1-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="ae9c1-108">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="ae9c1-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="ae9c1-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="ae9c1-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

> [!NOTE]
> <span data-ttu-id="ae9c1-110">Defender pour le point de terminaison sur iOS utiliserait un VPN pour fournir la fonctionnalité de protection web.</span><span class="sxs-lookup"><span data-stu-id="ae9c1-110">Defender for Endpoint on iOS would use a VPN in order to provide the Web Protection feature.</span></span> <span data-ttu-id="ae9c1-111">Il ne s’agit pas d’un VPN normal et d’un VPN local/en boucle autonome qui ne prend pas le trafic en dehors de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ae9c1-111">This is not a regular VPN and is a local/self-looping VPN that does not take traffic outside the device.</span></span>

## <a name="conditional-access-with-defender-for-endpoint-on-ios"></a><span data-ttu-id="ae9c1-112">Accès conditionnel avec Defender pour point de terminaison sur iOS</span><span class="sxs-lookup"><span data-stu-id="ae9c1-112">Conditional Access with Defender for Endpoint on iOS</span></span>  
<span data-ttu-id="ae9c1-113">Microsoft Defender pour endpoint sur iOS, ainsi que Microsoft Intune et Azure Active Directory permet d’appliquer la conformité des appareils et les stratégies d’accès conditionnel en fonction du score de risque de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ae9c1-113">Microsoft Defender for Endpoint on iOS along with Microsoft Intune and Azure Active Directory enables enforcing Device compliance and Conditional Access policies based on device risk score.</span></span> <span data-ttu-id="ae9c1-114">Defender pour point de terminaison est une solution de défense contre les menaces mobiles (MTD) que vous pouvez déployer pour tirer parti de cette fonctionnalité via Intune.</span><span class="sxs-lookup"><span data-stu-id="ae9c1-114">Defender for Endpoint is a Mobile Threat Defense (MTD) solution that you can deploy to leverage this capability via Intune.</span></span>

<span data-ttu-id="ae9c1-115">Pour plus d’informations sur la façon de configurer l’accès conditionnel avec Defender pour Endpoint sur iOS, voir [Defender pour Endpoint et Intune.](https://docs.microsoft.com/mem/intune/protect/advanced-threat-protection)</span><span class="sxs-lookup"><span data-stu-id="ae9c1-115">For more information about how to set up Conditional Access with Defender for Endpoint on iOS, see [Defender for Endpoint and Intune](https://docs.microsoft.com/mem/intune/protect/advanced-threat-protection).</span></span>

> [!NOTE]
> <span data-ttu-id="ae9c1-116">**La détection de jailbreak par Microsoft Defender pour point de terminaison sur iOS est actuellement en prévisualisation.**</span><span class="sxs-lookup"><span data-stu-id="ae9c1-116">**Jailbreak detection by Microsoft Defender for Endpoint on iOS is currently in preview**.</span></span> <span data-ttu-id="ae9c1-117">Si un appareil est détecté comme jailbreaké par Microsoft Defender pour endpoint, une alerte à risque élevé est signalée au Centre de sécurité et si l’accès conditionnel est configuré en fonction du score de risque de l’appareil, l’appareil ne pourra pas accéder aux données d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="ae9c1-117">If a device is detected to be jailbroken by Microsoft Defender for Endpoint, a **High**-risk alert will be reported to Security Center and if Conditional Access is setup based on device risk score, then the device will be blocked from accessing corporate data.</span></span>

## <a name="web-protection-and-vpn"></a><span data-ttu-id="ae9c1-118">Protection web et VPN</span><span class="sxs-lookup"><span data-stu-id="ae9c1-118">Web Protection and VPN</span></span>

<span data-ttu-id="ae9c1-119">Par défaut, Defender pour le point de terminaison sur iOS inclut et active la fonctionnalité de protection web.</span><span class="sxs-lookup"><span data-stu-id="ae9c1-119">By default, Defender for Endpoint on iOS includes and enables the web protection feature.</span></span> <span data-ttu-id="ae9c1-120">[La protection web permet](web-protection-overview.md) de sécuriser les appareils contre les menaces web et de protéger les utilisateurs contre les attaques par hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="ae9c1-120">[Web protection](web-protection-overview.md) helps to secure devices against web threats and protect users from phishing attacks.</span></span> <span data-ttu-id="ae9c1-121">Defender pour le point de terminaison sur iOS utilise un VPN pour fournir cette protection.</span><span class="sxs-lookup"><span data-stu-id="ae9c1-121">Defender for Endpoint on iOS uses a VPN in order to provide this protection.</span></span> <span data-ttu-id="ae9c1-122">Notez qu’il s’agit d’un VPN local et, contrairement au VPN traditionnel, le trafic réseau n’est pas envoyé en dehors de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ae9c1-122">Please note this is a local VPN and unlike traditional VPN, network traffic is not sent outside the device.</span></span>

<span data-ttu-id="ae9c1-123">Bien qu’il soit activé par défaut, il se peut que vous de soyez dans certains cas dans l’obligation de désactiver le VPN.</span><span class="sxs-lookup"><span data-stu-id="ae9c1-123">While enabled by default, there might be some cases that require you to disable VPN.</span></span> <span data-ttu-id="ae9c1-124">Par exemple, vous souhaitez exécuter certaines applications qui ne fonctionnent pas lorsqu’un VPN est configuré.</span><span class="sxs-lookup"><span data-stu-id="ae9c1-124">For example, you want to run some apps that do not work when a VPN is configured.</span></span> <span data-ttu-id="ae9c1-125">Dans ce cas, vous pouvez choisir de désactiver le VPN de l’application sur l’appareil en suivant les étapes ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="ae9c1-125">In such cases, you can choose to disable VPN from the app on the device by following the steps below:</span></span>

1. <span data-ttu-id="ae9c1-126">Sur votre appareil iOS, ouvrez **l’application Paramètres,** cliquez ou appuyez sur **Général,** puis **sur VPN.**</span><span class="sxs-lookup"><span data-stu-id="ae9c1-126">On your iOS device, open the **Settings** app, click or tap **General** and then **VPN**.</span></span>
1. <span data-ttu-id="ae9c1-127">Cliquez ou appuyez sur le bouton « i » de Microsoft Defender pour le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="ae9c1-127">Click or tap the "i" button for Microsoft Defender for Endpoint.</span></span>
1. <span data-ttu-id="ae9c1-128">Désactivez la **Connecter à la demande** pour désactiver le VPN.</span><span class="sxs-lookup"><span data-stu-id="ae9c1-128">Toggle off **Connect On Demand** to disable VPN.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="ae9c1-129">![Connexion de la connexion VPN à la demande](images/ios-vpn-config.png)</span><span class="sxs-lookup"><span data-stu-id="ae9c1-129">![VPN config connect on demand](images/ios-vpn-config.png)</span></span>

> [!NOTE]
> <span data-ttu-id="ae9c1-130">La protection web n’est pas disponible lorsque le VPN est désactivé.</span><span class="sxs-lookup"><span data-stu-id="ae9c1-130">Web Protection will not be available when VPN is disabled.</span></span> <span data-ttu-id="ae9c1-131">Pour activer à nouveau la Protection Web, ouvrez l’application Microsoft Defender pour point de terminaison sur l’appareil, puis cliquez ou appuyez sur **Démarrer le VPN.**</span><span class="sxs-lookup"><span data-stu-id="ae9c1-131">To re-enable Web Protection, open the Microsoft Defender for Endpoint app on the device and click or tap **Start VPN**.</span></span>

## <a name="co-existence-of-multiple-vpn-profiles"></a><span data-ttu-id="ae9c1-132">Coexistence de plusieurs profils VPN</span><span class="sxs-lookup"><span data-stu-id="ae9c1-132">Co-existence of multiple VPN profiles</span></span>

<span data-ttu-id="ae9c1-133">Apple iOS ne prend pas en charge plusieurs VPN à l’échelle de l’appareil pour être actifs simultanément.</span><span class="sxs-lookup"><span data-stu-id="ae9c1-133">Apple iOS does not support multiple device-wide VPNs to be active simultaneously.</span></span> <span data-ttu-id="ae9c1-134">Même si plusieurs profils VPN peuvent exister sur l’appareil, un seul VPN peut être actif à la fois.</span><span class="sxs-lookup"><span data-stu-id="ae9c1-134">While multiple VPN profiles can exist on the device, only one VPN can be active at a time.</span></span>


## <a name="configure-compliance-policy-against-jailbroken-devices"></a><span data-ttu-id="ae9c1-135">Configurer la stratégie de conformité contre les appareils jailbreakés</span><span class="sxs-lookup"><span data-stu-id="ae9c1-135">Configure compliance policy against jailbroken devices</span></span>

<span data-ttu-id="ae9c1-136">Pour protéger les données d’entreprise contre l’accès sur les appareils iOS jailbreakés, nous vous recommandons de configurer la stratégie de conformité suivante sur Intune.</span><span class="sxs-lookup"><span data-stu-id="ae9c1-136">To protect corporate data from being accessed on jailbroken iOS devices, we recommend that you set up the following compliance policy on Intune.</span></span>

> [!NOTE]
> <span data-ttu-id="ae9c1-137">Pour l’instant, la détection des jailbreaks par Microsoft Defender for Endpoint sur iOS est en prévisualisation.</span><span class="sxs-lookup"><span data-stu-id="ae9c1-137">At this time jailbreak detection by Microsoft Defender for Endpoint on iOS is in preview.</span></span> <span data-ttu-id="ae9c1-138">Nous vous recommandons de configurer cette stratégie en tant que couche supplémentaire de défense contre les scénarios de jailbreak.</span><span class="sxs-lookup"><span data-stu-id="ae9c1-138">We recommend that you setup this policy as an additional layer of defense against jailbreak scenarios.</span></span>

<span data-ttu-id="ae9c1-139">Suivez les étapes ci-dessous pour créer une stratégie de conformité contre les appareils jailbreakés.</span><span class="sxs-lookup"><span data-stu-id="ae9c1-139">Follow the steps below to create a compliance policy against jailbroken devices.</span></span>

1. <span data-ttu-id="ae9c1-140">In [Microsoft Endpoint Manager admin center](https://go.microsoft.com/fwlink/?linkid=2109431), go to **Devices**  ->  **Compliance policies** Create  ->  **Policy**.</span><span class="sxs-lookup"><span data-stu-id="ae9c1-140">In [Microsoft Endpoint Manager admin center](https://go.microsoft.com/fwlink/?linkid=2109431), go to **Devices** -> **Compliance policies** -> **Create Policy**.</span></span> <span data-ttu-id="ae9c1-141">Sélectionnez « iOS/iPadOS » comme plateforme, puis cliquez sur **Créer.**</span><span class="sxs-lookup"><span data-stu-id="ae9c1-141">Select "iOS/iPadOS" as platform and click **Create**.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="ae9c1-142">![Créer une stratégie](images/ios-jb-policy.png)</span><span class="sxs-lookup"><span data-stu-id="ae9c1-142">![Create Policy](images/ios-jb-policy.png)</span></span>

2. <span data-ttu-id="ae9c1-143">Spécifiez un nom de stratégie, par exemple « Stratégie de conformité pour jailbreak ».</span><span class="sxs-lookup"><span data-stu-id="ae9c1-143">Specify a name of the policy, for example "Compliance Policy for Jailbreak".</span></span>
3. <span data-ttu-id="ae9c1-144">Dans la page paramètres de conformité, cliquez  pour développer la **section** État de l’appareil, puis cliquez sur Bloquer pour les **appareils jailbreakés.**</span><span class="sxs-lookup"><span data-stu-id="ae9c1-144">In the compliance settings page, click to expand **Device Health** section and click **Block** for **Jailbroken devices** field.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="ae9c1-145">![Stratégie Paramètres](images/ios-jb-settings.png)</span><span class="sxs-lookup"><span data-stu-id="ae9c1-145">![Policy Settings](images/ios-jb-settings.png)</span></span>

4. <span data-ttu-id="ae9c1-146">Dans la *section Action pour non-conformité,* sélectionnez les actions en conformité avec vos besoins, puis sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="ae9c1-146">In the *Action for noncompliance* section, select the actions as per your requirements and select **Next**.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="ae9c1-147">![Actions de stratégie](images/ios-jb-actions.png)</span><span class="sxs-lookup"><span data-stu-id="ae9c1-147">![Policy Actions](images/ios-jb-actions.png)</span></span>

5. <span data-ttu-id="ae9c1-148">Dans la section *Affectations,* sélectionnez les groupes d’utilisateurs que vous souhaitez inclure pour cette stratégie, puis sélectionnez **Suivant.**</span><span class="sxs-lookup"><span data-stu-id="ae9c1-148">In the *Assignments* section, select the user groups that you want to include for this policy and then select **Next**.</span></span>
6. <span data-ttu-id="ae9c1-149">Dans la section **Révision+Créer,** vérifiez que toutes les informations entrées sont correctes, puis sélectionnez **Créer.**</span><span class="sxs-lookup"><span data-stu-id="ae9c1-149">In the **Review+Create** section, verify that all the information entered is correct and then select **Create**.</span></span>

## <a name="configure-custom-indicators"></a><span data-ttu-id="ae9c1-150">Configurer des indicateurs personnalisés</span><span class="sxs-lookup"><span data-stu-id="ae9c1-150">Configure custom indicators</span></span>

<span data-ttu-id="ae9c1-151">Defender pour le point de terminaison sur iOS permet aux administrateurs de configurer également des indicateurs personnalisés sur les appareils iOS.</span><span class="sxs-lookup"><span data-stu-id="ae9c1-151">Defender for Endpoint on iOS enables admins to configure custom indicators on iOS devices as well.</span></span> <span data-ttu-id="ae9c1-152">Pour plus d’informations sur la configuration des indicateurs personnalisés, voir [Gérer les indicateurs.](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/manage-indicators)</span><span class="sxs-lookup"><span data-stu-id="ae9c1-152">For more information on how to configure custom indicators, see [Manage indicators](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/manage-indicators).</span></span>

> [!NOTE]
> <span data-ttu-id="ae9c1-153">Defender pour le point de terminaison sur iOS prend en charge la création d’indicateurs personnalisés uniquement pour les adresses IP et les URL/domaines.</span><span class="sxs-lookup"><span data-stu-id="ae9c1-153">Defender for Endpoint on iOS supports creating custom indicators only for IP addresses and URLs/domains.</span></span>

## <a name="report-unsafe-site"></a><span data-ttu-id="ae9c1-154">Signaler un site non sécurisé</span><span class="sxs-lookup"><span data-stu-id="ae9c1-154">Report unsafe site</span></span>

<span data-ttu-id="ae9c1-155">Les sites web de hameçonnage usurpent l’identité de sites web dignes de confiance dans le but d’obtenir vos informations personnelles ou financières.</span><span class="sxs-lookup"><span data-stu-id="ae9c1-155">Phishing websites impersonate trustworthy websites for the purpose of obtaining your personal or financial information.</span></span> <span data-ttu-id="ae9c1-156">Consultez la page [Fournir des commentaires sur la protection](https://www.microsoft.com/wdsi/filesubmission/exploitguard/networkprotection) du réseau si vous souhaitez signaler un site web qui pourrait être un site de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="ae9c1-156">Visit the [Provide feedback about network protection](https://www.microsoft.com/wdsi/filesubmission/exploitguard/networkprotection) page if you want to report a website that could be a phishing site.</span></span>

## <a name="battery-consumption-issues-on-ios-when-microsoft-defender-for-endpoint-is-installed"></a><span data-ttu-id="ae9c1-157">Problèmes de consommation de batterie sur iOS lors de l’installation de Microsoft Defender for Endpoint</span><span class="sxs-lookup"><span data-stu-id="ae9c1-157">Battery Consumption issues on iOS when Microsoft Defender for Endpoint is installed</span></span>

<span data-ttu-id="ae9c1-158">L’utilisation de la batterie par une application est calculée par Apple en fonction d’une multitude de facteurs, notamment l’utilisation du processeur et du réseau.</span><span class="sxs-lookup"><span data-stu-id="ae9c1-158">The battery usage by an app is computed by Apple based on a multitude of factors including CPU and Network usage.</span></span> <span data-ttu-id="ae9c1-159">Microsoft Defender pour le point de terminaison utilise un VPN local/loop-back en arrière-plan pour vérifier le trafic web des sites web ou connexions malveillants.</span><span class="sxs-lookup"><span data-stu-id="ae9c1-159">Microsoft Defender for Endpoint uses a local/loop-back VPN in the background to check web traffic for any malicious websites or connections.</span></span> <span data-ttu-id="ae9c1-160">Les paquets réseau de n’importe quelle application sont vérifiés et l’utilisation de la batterie de Microsoft Defender for Endpoint est calculée de manière incorrecte.</span><span class="sxs-lookup"><span data-stu-id="ae9c1-160">Network packets from any app go through this check and that causes the battery usage of Microsoft Defender for Endpoint to be computed inaccurately.</span></span> <span data-ttu-id="ae9c1-161">Cela donne une fausse impression à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ae9c1-161">This gives a false impression to the user.</span></span> <span data-ttu-id="ae9c1-162">La consommation réelle de batterie de Microsoft Defender pour le point de terminaison est inférieure à ce qui est affiché sur la page Paramètres batterie sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ae9c1-162">The actual battery consumption of Microsoft Defender for Endpoint is lesser than what is shown on the Battery Settings page on the device.</span></span> <span data-ttu-id="ae9c1-163">Cette opération est basée sur des tests effectués sur l’application Microsoft Defender for Endpoint pour comprendre la consommation de batterie.</span><span class="sxs-lookup"><span data-stu-id="ae9c1-163">This is based on conducted tests done on the Microsoft Defender for Endpoint app to understand battery consumption.</span></span>

<span data-ttu-id="ae9c1-164">En outre, le VPN utilisé est un VPN local et contrairement aux VPN traditionnels, le trafic réseau n’est pas envoyé en dehors de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ae9c1-164">Also the VPN used is a local VPN and unlike traditional VPNs, network traffic is not sent outside the device.</span></span>
