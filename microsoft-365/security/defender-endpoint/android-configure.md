---
title: Configurer Microsoft Defender pour point de terminaison pour des fonctionnalités Android
description: Décrit comment configurer Microsoft Defender pour endpoint sur Android
keywords: microsoft, defender, Microsoft Defender pour le point de terminaison, mde, android, configuration
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
ms.topic: conceptual
ms.technology: mde
ms.openlocfilehash: 264ebbe0ceb6d6b83c006dbd1dd071a78ae219c3
ms.sourcegitcommit: 4fb1226d5875bf5b9b29252596855a6562cea9ae
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2021
ms.locfileid: "52841349"
---
# <a name="configure-defender-for-endpoint-on-android-features"></a><span data-ttu-id="60437-104">Configurer Defender pour le point de terminaison sur les fonctionnalités Android</span><span class="sxs-lookup"><span data-stu-id="60437-104">Configure Defender for Endpoint on Android features</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="60437-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="60437-105">**Applies to:**</span></span>
- [<span data-ttu-id="60437-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="60437-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="60437-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="60437-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

## <a name="conditional-access-with-defender-for-endpoint-on-android"></a><span data-ttu-id="60437-108">Accès conditionnel avec Defender pour point de terminaison sur Android</span><span class="sxs-lookup"><span data-stu-id="60437-108">Conditional Access with Defender for Endpoint on Android</span></span>  
<span data-ttu-id="60437-109">Microsoft Defender pour le point de terminaison sur Android, ainsi que Microsoft Intune et Azure Active Directory permet d’appliquer la conformité des appareils et des stratégies d’accès conditionnel en fonction des niveaux de risque de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="60437-109">Microsoft Defender for Endpoint on Android along with Microsoft Intune and Azure Active Directory enables enforcing Device compliance and Conditional Access policies based on device risk levels.</span></span> <span data-ttu-id="60437-110">Defender pour point de terminaison est une solution de défense contre les menaces mobiles (MTD) que vous pouvez déployer pour tirer parti de cette fonctionnalité via Intune.</span><span class="sxs-lookup"><span data-stu-id="60437-110">Defender for Endpoint is a Mobile Threat Defense (MTD) solution that you can deploy to leverage this capability via Intune.</span></span>

<span data-ttu-id="60437-111">Pour plus d’informations sur la façon de configurer Defender pour Endpoint sur Android et l’accès conditionnel, voir [Defender pour Endpoint et Intune.](/mem/intune/protect/advanced-threat-protection)</span><span class="sxs-lookup"><span data-stu-id="60437-111">For more information about how to set up Defender for Endpoint on Android and Conditional Access, see [Defender for Endpoint and Intune](/mem/intune/protect/advanced-threat-protection).</span></span>

## <a name="configure-custom-indicators"></a><span data-ttu-id="60437-112">Configurer des indicateurs personnalisés</span><span class="sxs-lookup"><span data-stu-id="60437-112">Configure custom indicators</span></span>  

> [!NOTE]
> <span data-ttu-id="60437-113">Defender pour le point de terminaison sur Android prend uniquement en charge la création d’indicateurs personnalisés pour les adresses IP et les URL/domaines.</span><span class="sxs-lookup"><span data-stu-id="60437-113">Defender for Endpoint on Android only supports creating custom indicators for IP addresses and URLs/domains.</span></span>

<span data-ttu-id="60437-114">Defender pour le point de terminaison sur Android permet aux administrateurs de configurer des indicateurs personnalisés pour prendre en charge également les appareils Android.</span><span class="sxs-lookup"><span data-stu-id="60437-114">Defender for Endpoint on Android enables admins to configure custom indicators to support Android devices as well.</span></span> <span data-ttu-id="60437-115">Pour plus d’informations sur la configuration des indicateurs personnalisés, voir [Gérer les indicateurs.](manage-indicators.md)</span><span class="sxs-lookup"><span data-stu-id="60437-115">For more information on how to configure custom indicators, see [Manage indicators](manage-indicators.md).</span></span>

## <a name="configure-web-protection"></a><span data-ttu-id="60437-116">Configurer la protection web</span><span class="sxs-lookup"><span data-stu-id="60437-116">Configure web protection</span></span>
<span data-ttu-id="60437-117">Defender pour le point de terminaison sur Android permet aux administrateurs informatiques de configurer la fonctionnalité de protection web.</span><span class="sxs-lookup"><span data-stu-id="60437-117">Defender for Endpoint on Android allows IT Administrators the ability to configure the web protection feature.</span></span> <span data-ttu-id="60437-118">Cette fonctionnalité est disponible dans le centre d Microsoft Endpoint Manager’administration.</span><span class="sxs-lookup"><span data-stu-id="60437-118">This capability is available within the Microsoft Endpoint Manager Admin center.</span></span>

> [!NOTE]
> <span data-ttu-id="60437-119">Defender pour le point de terminaison sur Android utiliserait un VPN pour fournir la fonctionnalité de protection web.</span><span class="sxs-lookup"><span data-stu-id="60437-119">Defender for Endpoint on Android would use a VPN in order to provide the Web Protection feature.</span></span> <span data-ttu-id="60437-120">Il ne s’agit pas d’un VPN normal et d’un VPN local/en boucle autonome qui ne prend pas le trafic en dehors de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="60437-120">This is not a regular VPN and is a local/self-looping VPN that does not take traffic outside the device.</span></span> <span data-ttu-id="60437-121">Pour plus d’informations, voir [Configurer la protection web sur les appareils qui exécutent Android.](/mem/intune/protect/advanced-threat-protection-manage-android)</span><span class="sxs-lookup"><span data-stu-id="60437-121">For more information, see [Configure web protection on devices that run Android](/mem/intune/protect/advanced-threat-protection-manage-android).</span></span>

## <a name="related-topics"></a><span data-ttu-id="60437-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="60437-122">Related topics</span></span>
- [<span data-ttu-id="60437-123">Vue d’ensemble de Microsoft Defender pour point de terminaison Android</span><span class="sxs-lookup"><span data-stu-id="60437-123">Overview of Microsoft Defender for Endpoint on Android</span></span>](microsoft-defender-endpoint-android.md)
- [<span data-ttu-id="60437-124">Déployer Microsoft Defender pour point de terminaison Android via Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="60437-124">Deploy Microsoft Defender for Endpoint on Android with Microsoft Intune</span></span>](android-intune.md)
