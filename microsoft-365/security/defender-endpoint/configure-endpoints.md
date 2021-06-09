---
title: Outils et méthodes d’intégration pour les appareils Windows 10.
description: Intégrer Windows 10 appareils afin qu’ils peuvent envoyer des données de capteur au capteur Microsoft Defender for Endpoint
keywords: Intégrer Windows 10, stratégie de groupe, gestionnaire de configuration de point de terminaison, gestion des appareils mobiles, script local, gp, sccm, mdm, intune
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
ms.collection: M365-security-compliance
ms.topic: conceptual
ms.technology: mde
ms.openlocfilehash: f1ef2670a1ca749e0a2f1ebc96300d4eca043bf8
ms.sourcegitcommit: 55791ddab9ae484f76b30f0470eec8a4cf7b46d1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/20/2021
ms.locfileid: "51892828"
---
# <a name="onboarding-tools-and-methods-for-windows-10-devices"></a><span data-ttu-id="87ad1-104">Outils et méthodes d’intégration pour les appareils Windows 10.</span><span class="sxs-lookup"><span data-stu-id="87ad1-104">Onboarding tools and methods for Windows 10 devices</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="87ad1-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="87ad1-105">**Applies to:**</span></span>
- [<span data-ttu-id="87ad1-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="87ad1-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="87ad1-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="87ad1-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)
- [<span data-ttu-id="87ad1-108">Microsoft 365 Protection contre la perte de données (DLP) de point de terminaison</span><span class="sxs-lookup"><span data-stu-id="87ad1-108">Microsoft 365 Endpoint data loss prevention (DLP)</span></span>](/microsoft-365/compliance/endpoint-dlp-learn-about)
- [<span data-ttu-id="87ad1-109">Microsoft 365 Gestion des risques internes</span><span class="sxs-lookup"><span data-stu-id="87ad1-109">Microsoft 365 Insider risk management</span></span>](/microsoft-365/compliance/insider-risk-management)

><span data-ttu-id="87ad1-110">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="87ad1-110">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="87ad1-111">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="87ad1-111">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-assignaccess-abovefoldlink)

<span data-ttu-id="87ad1-112">Les appareils de votre organisation doivent être configurés pour que le service Defender for Endpoint puisse obtenir des données de capteur de leur part.</span><span class="sxs-lookup"><span data-stu-id="87ad1-112">Devices in your organization must be configured so that the Defender for Endpoint service can get sensor data from them.</span></span> <span data-ttu-id="87ad1-113">Il existe différentes méthodes et outils de déploiement que vous pouvez utiliser pour configurer les appareils de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="87ad1-113">There are various methods and deployment tools that you can use to configure the devices in your organization.</span></span>

<span data-ttu-id="87ad1-114">Les méthodes et outils de déploiement suivants sont pris en charge :</span><span class="sxs-lookup"><span data-stu-id="87ad1-114">The following deployment tools and methods are supported:</span></span>

- <span data-ttu-id="87ad1-115">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="87ad1-115">Group Policy</span></span>
- <span data-ttu-id="87ad1-116">Microsoft Endpoint Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="87ad1-116">Microsoft Endpoint Configuration Manager</span></span>
- <span data-ttu-id="87ad1-117">Gestion des appareils mobiles (y compris Microsoft Intune)</span><span class="sxs-lookup"><span data-stu-id="87ad1-117">Mobile Device Management (including Microsoft Intune)</span></span>
- <span data-ttu-id="87ad1-118">Script local</span><span class="sxs-lookup"><span data-stu-id="87ad1-118">Local script</span></span>

## <a name="in-this-section"></a><span data-ttu-id="87ad1-119">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="87ad1-119">In this section</span></span>
<span data-ttu-id="87ad1-120">Rubrique</span><span class="sxs-lookup"><span data-stu-id="87ad1-120">Topic</span></span> | <span data-ttu-id="87ad1-121">Description</span><span class="sxs-lookup"><span data-stu-id="87ad1-121">Description</span></span>
:---|:---
[<span data-ttu-id="87ad1-122">Intégrer des Windows 10 à l’aide de la stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="87ad1-122">Onboard Windows 10 devices using Group Policy</span></span>](configure-endpoints-gp.md) | <span data-ttu-id="87ad1-123">Utilisez la stratégie de groupe pour déployer le package de configuration sur les appareils.</span><span class="sxs-lookup"><span data-stu-id="87ad1-123">Use Group Policy to deploy the configuration package on devices.</span></span>
[<span data-ttu-id="87ad1-124">Intégrer Windows appareils à l’aide Microsoft Endpoint Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="87ad1-124">Onboard Windows devices using Microsoft Endpoint Configuration Manager</span></span>](configure-endpoints-sccm.md) | <span data-ttu-id="87ad1-125">Vous pouvez utiliser la version Microsoft Endpoint Manager (branche actuelle) 1606 ou la version 1602 de Microsoft Endpoint Manager (branche actuelle) ou une version antérieure pour déployer le package de configuration sur les appareils.</span><span class="sxs-lookup"><span data-stu-id="87ad1-125">You can use either use Microsoft Endpoint Manager (current branch) version 1606 or Microsoft Endpoint Manager (current branch) version 1602 or earlier to deploy the configuration package on devices.</span></span>
[<span data-ttu-id="87ad1-126">Intégrer les appareils Windows 10 à l’aide des outils de gestion des appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="87ad1-126">Onboard Windows 10 devices using Mobile Device Management tools</span></span>](configure-endpoints-mdm.md) | <span data-ttu-id="87ad1-127">Utilisez les outils de gestion des appareils mobiles ou Microsoft Intune pour déployer le package de configuration sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="87ad1-127">Use Mobile Device Management tools or Microsoft Intune to deploy the configuration package on device.</span></span>
[<span data-ttu-id="87ad1-128">Intégrer les appareils Windows 10 utilisant un script local</span><span class="sxs-lookup"><span data-stu-id="87ad1-128">Onboard Windows 10 devices using a local script</span></span>](configure-endpoints-script.md) | <span data-ttu-id="87ad1-129">Découvrez comment utiliser le script local pour déployer le package de configuration sur les points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="87ad1-129">Learn how to use the local script to deploy the configuration package on endpoints.</span></span>
[<span data-ttu-id="87ad1-130">Intégrer les ordinateurs virtuels d’infrastructure de bureau (VDI) non persistants</span><span class="sxs-lookup"><span data-stu-id="87ad1-130">Onboard non-persistent virtual desktop infrastructure (VDI) devices</span></span>](configure-endpoints-vdi.md) | <span data-ttu-id="87ad1-131">Découvrez comment utiliser le package de configuration pour configurer des appareils VDI.</span><span class="sxs-lookup"><span data-stu-id="87ad1-131">Learn how to use the configuration package to configure VDI devices.</span></span>


><span data-ttu-id="87ad1-132">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="87ad1-132">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="87ad1-133">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="87ad1-133">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-configureendpoints-belowfoldlink)
