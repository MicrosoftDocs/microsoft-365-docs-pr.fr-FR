---
title: Configurer Microsoft Defender pour le point de terminaison pour les fonctionnalités iOS
description: Décrit comment déployer Microsoft Defender ATP pour les fonctionnalités iOS
keywords: microsoft, defender, atp, ios, configurer, fonctionnalités, ios
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
ms.openlocfilehash: 8f74d4799bcb02051cddd09b80ed6ab50258302b
ms.sourcegitcommit: 987f70e44e406ab6b1dd35f336a9d0c228032794
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/05/2021
ms.locfileid: "51587226"
---
# <a name="configure-microsoft-defender-for-endpoint-for-ios-features"></a><span data-ttu-id="3002a-104">Configurer Microsoft Defender pour le point de terminaison pour les fonctionnalités iOS</span><span class="sxs-lookup"><span data-stu-id="3002a-104">Configure Microsoft Defender for Endpoint for iOS features</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="3002a-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="3002a-105">**Applies to:**</span></span>
- [<span data-ttu-id="3002a-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="3002a-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="3002a-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="3002a-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="3002a-108">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="3002a-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="3002a-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="3002a-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

> [!NOTE]
> <span data-ttu-id="3002a-110">Defender pour le point de terminaison pour iOS utiliserait un VPN pour fournir la fonctionnalité de protection web.</span><span class="sxs-lookup"><span data-stu-id="3002a-110">Defender for Endpoint for iOS would use a VPN in order to provide the Web Protection feature.</span></span> <span data-ttu-id="3002a-111">Il ne s’agit pas d’un VPN normal et d’un VPN local/en boucle autonome qui ne prend pas le trafic en dehors de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="3002a-111">This is not a regular VPN and is a local/self-looping VPN that does not take traffic outside the device.</span></span>

## <a name="conditional-access-with-defender-for-endpoint-for-ios"></a><span data-ttu-id="3002a-112">Accès conditionnel avec Defender pour point de terminaison pour iOS</span><span class="sxs-lookup"><span data-stu-id="3002a-112">Conditional Access with Defender for Endpoint for iOS</span></span>  
<span data-ttu-id="3002a-113">Microsoft Defender pour le point de terminaison pour iOS, ainsi que Microsoft Intune et Azure Active Directory permettent d’appliquer des stratégies de conformité des appareils et d’accès conditionnel en fonction des niveaux de risque des appareils.</span><span class="sxs-lookup"><span data-stu-id="3002a-113">Microsoft Defender for Endpoint for iOS along with Microsoft Intune and Azure Active Directory enables enforcing Device compliance and Conditional Access policies based on device risk levels.</span></span> <span data-ttu-id="3002a-114">Defender pour point de terminaison est une solution de défense contre les menaces mobiles que vous pouvez déployer pour tirer parti de cette fonctionnalité via Intune.</span><span class="sxs-lookup"><span data-stu-id="3002a-114">Defender for Endpoint is a Mobile Threat Defense (MTD) solution that you can deploy to leverage this capability via Intune.</span></span>

<span data-ttu-id="3002a-115">Pour plus d’informations sur la façon de configurer l’accès conditionnel avec Defender pour Endpoint pour iOS, voir [Defender pour Endpoint et Intune.](https://docs.microsoft.com/mem/intune/protect/advanced-threat-protection)</span><span class="sxs-lookup"><span data-stu-id="3002a-115">For more information about how to set up Conditional Access with Defender for Endpoint for iOS, see [Defender for Endpoint and Intune](https://docs.microsoft.com/mem/intune/protect/advanced-threat-protection).</span></span>

## <a name="web-protection-and-vpn"></a><span data-ttu-id="3002a-116">Protection web et VPN</span><span class="sxs-lookup"><span data-stu-id="3002a-116">Web Protection and VPN</span></span>

<span data-ttu-id="3002a-117">Par défaut, Defender pour le point de terminaison pour iOS inclut et active la fonctionnalité de protection web.</span><span class="sxs-lookup"><span data-stu-id="3002a-117">By default, Defender for Endpoint for iOS includes and enables the web protection feature.</span></span> <span data-ttu-id="3002a-118">[La protection web permet](web-protection-overview.md) de sécuriser les appareils contre les menaces web et de protéger les utilisateurs contre les attaques par hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="3002a-118">[Web protection](web-protection-overview.md) helps to secure devices against web threats and protect users from phishing attacks.</span></span> <span data-ttu-id="3002a-119">Defender pour le point de terminaison pour iOS utilise un VPN pour fournir cette protection.</span><span class="sxs-lookup"><span data-stu-id="3002a-119">Defender for Endpoint for iOS uses a VPN in order to provide this protection.</span></span> <span data-ttu-id="3002a-120">Notez qu’il s’agit d’un VPN local et, contrairement au VPN traditionnel, le trafic réseau n’est pas envoyé à l’extérieur de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="3002a-120">Please note this is a local VPN and unlike traditional VPN, network traffic is not sent outside the device.</span></span>

<span data-ttu-id="3002a-121">Bien qu’il soit activé par défaut, il se peut que vous de soyez dans certains cas dans l’obligation de désactiver le VPN.</span><span class="sxs-lookup"><span data-stu-id="3002a-121">While enabled by default, there might be some cases that require you to disable VPN.</span></span> <span data-ttu-id="3002a-122">Par exemple, vous souhaitez exécuter certaines applications qui ne fonctionnent pas lorsqu’un VPN est configuré.</span><span class="sxs-lookup"><span data-stu-id="3002a-122">For example, you want to run some apps that do not work when a VPN is configured.</span></span> <span data-ttu-id="3002a-123">Dans ce cas, vous pouvez choisir de désactiver le VPN de l’application sur l’appareil en suivant les étapes ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="3002a-123">In such cases, you can choose to disable VPN from the app on the device by following the steps below:</span></span>

1. <span data-ttu-id="3002a-124">Sur votre appareil iOS, ouvrez l’application **Paramètres,** cliquez ou appuyez sur **Général,** puis **sur VPN.**</span><span class="sxs-lookup"><span data-stu-id="3002a-124">On your iOS device, open the **Settings** app, click or tap **General** and then **VPN**.</span></span>
1. <span data-ttu-id="3002a-125">Cliquez ou appuyez sur le bouton « i » de Microsoft Defender ATP.</span><span class="sxs-lookup"><span data-stu-id="3002a-125">Click or tap the "i" button for Microsoft Defender ATP.</span></span>
1. <span data-ttu-id="3002a-126">Désactivez la connexion **à la demande** pour désactiver le VPN.</span><span class="sxs-lookup"><span data-stu-id="3002a-126">Toggle off **Connect On Demand** to disable VPN.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="3002a-127">![Connexion de la connexion VPN à la demande](images/ios-vpn-config.png)</span><span class="sxs-lookup"><span data-stu-id="3002a-127">![VPN config connect on demand](images/ios-vpn-config.png)</span></span>

> [!NOTE]
> <span data-ttu-id="3002a-128">La protection web n’est pas disponible lorsque le VPN est désactivé.</span><span class="sxs-lookup"><span data-stu-id="3002a-128">Web Protection will not be available when VPN is disabled.</span></span> <span data-ttu-id="3002a-129">Pour activer à nouveau la Protection Web, ouvrez l’application Microsoft Defender pour point de terminaison sur l’appareil, puis cliquez ou appuyez sur **Démarrer le VPN.**</span><span class="sxs-lookup"><span data-stu-id="3002a-129">To re-enable Web Protection, open the Microsoft Defender for Endpoint app on the device and click or tap **Start VPN**.</span></span>

## <a name="co-existence-of-multiple-vpn-profiles"></a><span data-ttu-id="3002a-130">Coexistence de plusieurs profils VPN</span><span class="sxs-lookup"><span data-stu-id="3002a-130">Co-existence of multiple VPN profiles</span></span>

<span data-ttu-id="3002a-131">Apple iOS ne prend pas en charge plusieurs VPN à l’échelle de l’appareil pour être actifs simultanément.</span><span class="sxs-lookup"><span data-stu-id="3002a-131">Apple iOS does not support multiple device-wide VPNs to be active simultaneously.</span></span> <span data-ttu-id="3002a-132">Alors que plusieurs profils VPN peuvent exister sur l’appareil, un seul VPN peut être actif à la fois.</span><span class="sxs-lookup"><span data-stu-id="3002a-132">While multiple VPN profiles can exist on the device, only one VPN can be active at a time.</span></span>


## <a name="configure-compliance-policy-against-jailbroken-devices"></a><span data-ttu-id="3002a-133">Configurer la stratégie de conformité contre les appareils jailbreakés</span><span class="sxs-lookup"><span data-stu-id="3002a-133">Configure compliance policy against jailbroken devices</span></span>

<span data-ttu-id="3002a-134">Pour protéger les données d’entreprise contre l’accès sur les appareils iOS jailbreakés, nous vous recommandons de configurer la stratégie de conformité suivante sur Intune.</span><span class="sxs-lookup"><span data-stu-id="3002a-134">To protect corporate data from being accessed on jailbroken iOS devices, we recommend that you set up the following compliance policy on Intune.</span></span>

> [!NOTE]
> <span data-ttu-id="3002a-135">Pour l’instant, Microsoft Defender pour endpoint pour iOS ne fournit pas de protection contre les scénarios de jailbreak.</span><span class="sxs-lookup"><span data-stu-id="3002a-135">At this time Microsoft Defender for Endpoint for iOS does not provide protection against jailbreak scenarios.</span></span> <span data-ttu-id="3002a-136">S’il est utilisé sur un appareil jailbreaké, dans des scénarios spécifiques, les données utilisées par l’application telles que votre ID de messagerie d’entreprise et votre image de profil d’entreprise (si disponible) peuvent être exposées localement.</span><span class="sxs-lookup"><span data-stu-id="3002a-136">If used on a jailbroken device, then in specific scenarios data that is used by the application like your corporate email id and corporate profile picture (if available) can be exposed locally</span></span>

<span data-ttu-id="3002a-137">Suivez les étapes ci-dessous pour créer une stratégie de conformité contre les appareils jailbreakés.</span><span class="sxs-lookup"><span data-stu-id="3002a-137">Follow the steps below to create a compliance policy against jailbroken devices.</span></span>

1. <span data-ttu-id="3002a-138">Dans [le Centre d’administration Microsoft Endpoint Manager,](https://go.microsoft.com/fwlink/?linkid=2109431)allez **aux** stratégies de conformité  ->  **des appareils**  ->  **Créer une stratégie.**</span><span class="sxs-lookup"><span data-stu-id="3002a-138">In [Microsoft Endpoint Manager admin center](https://go.microsoft.com/fwlink/?linkid=2109431), go to **Devices** -> **Compliance policies** -> **Create Policy**.</span></span> <span data-ttu-id="3002a-139">Sélectionnez « iOS/iPadOS » comme plateforme, puis cliquez sur **Créer.**</span><span class="sxs-lookup"><span data-stu-id="3002a-139">Select "iOS/iPadOS" as platform and click **Create**.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="3002a-140">![Créer une stratégie](images/ios-jb-policy.png)</span><span class="sxs-lookup"><span data-stu-id="3002a-140">![Create Policy](images/ios-jb-policy.png)</span></span>

2. <span data-ttu-id="3002a-141">Spécifiez un nom de stratégie, par exemple « Stratégie de conformité pour jailbreak ».</span><span class="sxs-lookup"><span data-stu-id="3002a-141">Specify a name of the policy, for example "Compliance Policy for Jailbreak".</span></span>
3. <span data-ttu-id="3002a-142">Dans la page paramètres de conformité, cliquez  pour développer la **section** État de l’appareil, puis cliquez sur Bloquer pour les **appareils jailbreakés.**</span><span class="sxs-lookup"><span data-stu-id="3002a-142">In the compliance settings page, click to expand **Device Health** section and click **Block** for **Jailbroken devices** field.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="3002a-143">![Paramètres de stratégie](images/ios-jb-settings.png)</span><span class="sxs-lookup"><span data-stu-id="3002a-143">![Policy Settings](images/ios-jb-settings.png)</span></span>

4. <span data-ttu-id="3002a-144">Dans la *section Action pour non-conformité,* sélectionnez les actions en conformité avec vos besoins, puis sélectionnez **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="3002a-144">In the *Action for noncompliance* section, select the actions as per your requirements and select **Next**.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="3002a-145">![Actions de stratégie](images/ios-jb-actions.png)</span><span class="sxs-lookup"><span data-stu-id="3002a-145">![Policy Actions](images/ios-jb-actions.png)</span></span>

5. <span data-ttu-id="3002a-146">Dans la section *Affectations,* sélectionnez les groupes d’utilisateurs que vous souhaitez inclure pour cette stratégie, puis sélectionnez **Suivant.**</span><span class="sxs-lookup"><span data-stu-id="3002a-146">In the *Assignments* section, select the user groups that you want to include for this policy and then select **Next**.</span></span>
6. <span data-ttu-id="3002a-147">Dans la section **Révision+Créer,** vérifiez que toutes les informations entrées sont correctes, puis sélectionnez **Créer.**</span><span class="sxs-lookup"><span data-stu-id="3002a-147">In the **Review+Create** section, verify that all the information entered is correct and then select **Create**.</span></span>

## <a name="configure-custom-indicators"></a><span data-ttu-id="3002a-148">Configurer des indicateurs personnalisés</span><span class="sxs-lookup"><span data-stu-id="3002a-148">Configure custom indicators</span></span>

<span data-ttu-id="3002a-149">Defender pour le point de terminaison pour iOS permet aux administrateurs de configurer également des indicateurs personnalisés sur les appareils iOS.</span><span class="sxs-lookup"><span data-stu-id="3002a-149">Defender for Endpoint for iOS enables admins to configure custom indicators on iOS devices as well.</span></span> <span data-ttu-id="3002a-150">Pour plus d’informations sur la configuration des indicateurs personnalisés, voir [Gérer les indicateurs.](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/manage-indicators)</span><span class="sxs-lookup"><span data-stu-id="3002a-150">For more information on how to configure custom indicators, see [Manage indicators](https://docs.microsoft.com/microsoft-365/security/defender-endpoint/manage-indicators).</span></span>

> [!NOTE]
> <span data-ttu-id="3002a-151">Defender pour le point de terminaison pour iOS prend en charge la création d’indicateurs personnalisés uniquement pour les adresses IP et les URL/domaines.</span><span class="sxs-lookup"><span data-stu-id="3002a-151">Defender for Endpoint for iOS supports creating custom indicators only for IP addresses and URLs/domains.</span></span>

## <a name="report-unsafe-site"></a><span data-ttu-id="3002a-152">Signaler un site non sécurisé</span><span class="sxs-lookup"><span data-stu-id="3002a-152">Report unsafe site</span></span>

<span data-ttu-id="3002a-153">Les sites web de hameçonnage usurpent l’identité de sites web dignes de confiance dans le but d’obtenir vos informations personnelles ou financières.</span><span class="sxs-lookup"><span data-stu-id="3002a-153">Phishing websites impersonate trustworthy websites for the purpose of obtaining your personal or financial information.</span></span> <span data-ttu-id="3002a-154">Consultez la page [Fournir des commentaires sur la protection](https://www.microsoft.com/wdsi/filesubmission/exploitguard/networkprotection) du réseau si vous souhaitez signaler un site web qui pourrait être un site de hameçonnage.</span><span class="sxs-lookup"><span data-stu-id="3002a-154">Visit the [Provide feedback about network protection](https://www.microsoft.com/wdsi/filesubmission/exploitguard/networkprotection) page if you want to report a website that could be a phishing site.</span></span>

## <a name="battery-consumption-issues-on-ios-when-microsoft-defender-for-endpoint-is-installed"></a><span data-ttu-id="3002a-155">Problèmes de consommation de batterie sur iOS lors de l’installation de Microsoft Defender for Endpoint</span><span class="sxs-lookup"><span data-stu-id="3002a-155">Battery Consumption issues on iOS when Microsoft Defender for Endpoint is installed</span></span>

<span data-ttu-id="3002a-156">L’utilisation de la batterie par une application est calculée par Apple en fonction d’une multitude de facteurs, notamment l’utilisation du processeur et du réseau.</span><span class="sxs-lookup"><span data-stu-id="3002a-156">The battery usage by an app is computed by Apple based on a multitude of factors including CPU and Network usage.</span></span> <span data-ttu-id="3002a-157">Microsoft Defender pour le point de terminaison utilise un VPN local/de bouc-back en arrière-plan pour vérifier le trafic web des sites web ou connexions malveillants.</span><span class="sxs-lookup"><span data-stu-id="3002a-157">Microsoft Defender for Endpoint uses a local/loop-back VPN in the background to check web traffic for any malicious websites or connections.</span></span> <span data-ttu-id="3002a-158">Les paquets réseau de n’importe quelle application sont vérifiés et l’utilisation de la batterie de Microsoft Defender for Endpoint est calculée de manière incorrecte.</span><span class="sxs-lookup"><span data-stu-id="3002a-158">Network packets from any app go through this check and that causes the battery usage of Microsoft Defender for Endpoint to be computed inaccurately.</span></span> <span data-ttu-id="3002a-159">Cela donne une fausse impression à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3002a-159">This gives a false impression to the user.</span></span> <span data-ttu-id="3002a-160">La consommation réelle de batterie de Microsoft Defender pour le point de terminaison est inférieure à ce qui est affiché dans la page Paramètres de la batterie sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="3002a-160">The actual battery consumption of Microsoft Defender for Endpoint is lesser than what is shown on the Battery Settings page on the device.</span></span> <span data-ttu-id="3002a-161">Cette opération est basée sur des tests effectués sur l’application Microsoft Defender for Endpoint pour comprendre la consommation de batterie.</span><span class="sxs-lookup"><span data-stu-id="3002a-161">This is based on conducted tests done on the Microsoft Defender for Endpoint app to understand battery consumption.</span></span>

<span data-ttu-id="3002a-162">En outre, le VPN utilisé est un VPN local et contrairement aux VPN traditionnels, le trafic réseau n’est pas envoyé en dehors de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="3002a-162">Also the VPN used is a local VPN and unlike traditional VPNs, network traffic is not sent outside the device.</span></span>
