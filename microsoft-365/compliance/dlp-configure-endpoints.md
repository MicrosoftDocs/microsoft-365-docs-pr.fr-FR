---
title: Outils et méthodes d’intégration pour les appareils Windows 10 (aperçu)
f1.keywords: NOCSH
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: ''
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
search.appverid:
- MET150
description: Périphériques Windows 10 embarqués afin qu’ils puissent envoyer des données de capteur aux solutions de conformité de Microsoft 365
ms.openlocfilehash: 5f5a777d11dda900116b6095166ffffed6efa31b
ms.sourcegitcommit: bd36c88e731e3fee2a3a5cb3564fdc94f11bab94
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/27/2020
ms.locfileid: "48769641"
---
# <a name="onboarding-tools-and-methods-for-windows-10-devices-preview"></a><span data-ttu-id="02d99-103">Outils et méthodes d’intégration pour les appareils Windows 10 (aperçu)</span><span class="sxs-lookup"><span data-stu-id="02d99-103">Onboarding tools and methods for Windows 10 devices (preview)</span></span>

<span data-ttu-id="02d99-104">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="02d99-104">**Applies to:**</span></span>
- [<span data-ttu-id="02d99-105">Microsoft 365 protection contre la perte de données (DLP)</span><span class="sxs-lookup"><span data-stu-id="02d99-105">Microsoft 365 Endpoint data loss prevention (DLP)</span></span>](/microsoft-365/compliance/endpoint-dlp-learn-about)

<span data-ttu-id="02d99-106">Les appareils de votre organisation doivent être configurés de manière à ce que le service de protection contre la perte de données du point de terminaison de Microsoft 365 puisse obtenir des données de capteur.</span><span class="sxs-lookup"><span data-stu-id="02d99-106">Devices in your organization must be configured so that the Microsoft 365 Endpoint data loss prevention service can get sensor data from them.</span></span> <span data-ttu-id="02d99-107">Il existe plusieurs méthodes et outils de déploiement que vous pouvez utiliser pour configurer les appareils dans votre organisation.</span><span class="sxs-lookup"><span data-stu-id="02d99-107">There are various methods and deployment tools that you can use to configure the devices in your organization.</span></span>

<span data-ttu-id="02d99-108">Les méthodes et les outils de déploiement suivants sont pris en charge :</span><span class="sxs-lookup"><span data-stu-id="02d99-108">The following deployment tools and methods are supported:</span></span>

- <span data-ttu-id="02d99-109">stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="02d99-109">group policy</span></span>
- <span data-ttu-id="02d99-110">Microsoft Endpoint Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="02d99-110">Microsoft Endpoint Configuration Manager</span></span>
- <span data-ttu-id="02d99-111">Gestion des appareils mobiles (y compris Microsoft Intune)</span><span class="sxs-lookup"><span data-stu-id="02d99-111">Mobile Device Management (including Microsoft Intune)</span></span>
- <span data-ttu-id="02d99-112">script local</span><span class="sxs-lookup"><span data-stu-id="02d99-112">local script</span></span>

## <a name="in-this-section"></a><span data-ttu-id="02d99-113">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="02d99-113">In this section</span></span>
<span data-ttu-id="02d99-114">Rubrique</span><span class="sxs-lookup"><span data-stu-id="02d99-114">Topic</span></span> | <span data-ttu-id="02d99-115">Description</span><span class="sxs-lookup"><span data-stu-id="02d99-115">Description</span></span>
:---|:---
[<span data-ttu-id="02d99-116">Périphériques Windows 10 embarqués à l’aide de la stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="02d99-116">Onboard Windows 10 devices using Group Policy</span></span>](dlp-configure-endpoints-gp.md) | <span data-ttu-id="02d99-117">Utilisez la stratégie de groupe pour déployer le package de configuration sur les appareils.</span><span class="sxs-lookup"><span data-stu-id="02d99-117">Use Group Policy to deploy the configuration package on devices.</span></span>
[<span data-ttu-id="02d99-118">Appareils Windows intégrés utilisant le gestionnaire de configuration de point de terminaison Microsoft</span><span class="sxs-lookup"><span data-stu-id="02d99-118">Onboard Windows devices using Microsoft Endpoint Configuration Manager</span></span>](dlp-configure-endpoints-sccm.md) | <span data-ttu-id="02d99-119">Vous pouvez utiliser Microsoft Endpoint Configuration Manager (branchy) version 1606 ou Microsoft Endpoint Configuration Manager (branchy) version 1602 ou antérieure pour déployer le package de configuration sur les appareils.</span><span class="sxs-lookup"><span data-stu-id="02d99-119">You can use either use Microsoft Endpoint Configuration Manager (current branch) version 1606 or Microsoft Endpoint Configuration Manager (current branch) version 1602 or earlier to deploy the configuration package on devices.</span></span>
[<span data-ttu-id="02d99-120">Périphériques Windows 10 intégrés à l’aide des outils de gestion des appareils mobiles</span><span class="sxs-lookup"><span data-stu-id="02d99-120">Onboard Windows 10 devices using Mobile Device Management tools</span></span>](dlp-configure-endpoints-mdm.md) | <span data-ttu-id="02d99-121">Utilisez les outils de gestion des appareils mobiles ou Microsoft Intune pour déployer le package de configuration sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="02d99-121">Use Mobile Device Management tools or Microsoft Intune to deploy the configuration package on device.</span></span>
[<span data-ttu-id="02d99-122">Périphériques Windows 10 embarqués à l’aide d’un script local</span><span class="sxs-lookup"><span data-stu-id="02d99-122">Onboard Windows 10 devices using a local script</span></span>](dlp-configure-endpoints-script.md) | <span data-ttu-id="02d99-123">Découvrez comment utiliser le script local pour déployer le package de configuration sur des points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="02d99-123">Learn how to use the local script to deploy the configuration package on endpoints.</span></span>
[<span data-ttu-id="02d99-124">Périphériques VDI (Virtual Desktop Infrastructure) non persistants</span><span class="sxs-lookup"><span data-stu-id="02d99-124">Onboard non-persistent virtual desktop infrastructure (VDI) devices</span></span>](dlp-configure-endpoints-vdi.md) | <span data-ttu-id="02d99-125">Découvrez comment utiliser le package de configuration pour configurer des appareils VDI.</span><span class="sxs-lookup"><span data-stu-id="02d99-125">Learn how to use the configuration package to configure VDI devices.</span></span>
