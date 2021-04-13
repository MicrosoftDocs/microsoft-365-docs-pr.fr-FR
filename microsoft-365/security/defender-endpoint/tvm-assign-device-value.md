---
title: "Attribuer une valeur d'appareil : gestion des menaces et des vulnérabilités"
description: Découvrez comment affecter une valeur faible, normale ou élevée à un appareil pour vous aider à différencier les priorités des ressources.
keywords: microsoft defender pour la valeur de l'appareil de point de terminaison, la valeur de l'appareil de gestion des menaces et des vulnérabilités, les appareils à valeur élevée, le score d'exposition de la valeur de l'appareil
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
ms.topic: article
ms.technology: mde
ms.openlocfilehash: 1f5d90190418f84795bdd899ea0e48ac25831a96
ms.sourcegitcommit: 3fe7eb32c8d6e01e190b2b782827fbadd73a18e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "51689388"
---
# <a name="assign-device-value---threat-and-vulnerability-management"></a><span data-ttu-id="53b65-104">Attribuer une valeur d'appareil : gestion des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="53b65-104">Assign device value - threat and vulnerability management</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="53b65-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="53b65-105">**Applies to:**</span></span>

- [<span data-ttu-id="53b65-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="53b65-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/?linkid=2154037)
- [<span data-ttu-id="53b65-107">Gestion des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="53b65-107">Threat and vulnerability management</span></span>](next-gen-threat-and-vuln-mgt.md)
- [<span data-ttu-id="53b65-108">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="53b65-108">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="53b65-109">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="53b65-109">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="53b65-110">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="53b65-110">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-portaloverview-abovefoldlink)

[!include[Prerelease information](../../includes/prerelease.md)]

<span data-ttu-id="53b65-111">La définition de la valeur d'un appareil vous permet de différencier les priorités des biens.</span><span class="sxs-lookup"><span data-stu-id="53b65-111">Defining a device’s value helps you differentiate between asset priorities.</span></span> <span data-ttu-id="53b65-112">La valeur de l'appareil est utilisée pour incorporer le risque d'exposition d'un bien individuel dans le calcul du score d'exposition de la gestion des menaces et des vulnérabilités.</span><span class="sxs-lookup"><span data-stu-id="53b65-112">The device value is used to incorporate the risk appetite of an individual asset into the threat and vulnerability management exposure score calculation.</span></span> <span data-ttu-id="53b65-113">Les appareils affectés en tant que « valeur élevée » recevront plus de poids.</span><span class="sxs-lookup"><span data-stu-id="53b65-113">Devices assigned as “high value” will receive more weight.</span></span>

<span data-ttu-id="53b65-114">Vous pouvez également utiliser [l'API définir la valeur de l'appareil.](set-device-value.md)</span><span class="sxs-lookup"><span data-stu-id="53b65-114">You can also use the [set device value API](set-device-value.md).</span></span>

<span data-ttu-id="53b65-115">Options de valeur d'appareil :</span><span class="sxs-lookup"><span data-stu-id="53b65-115">Device value options:</span></span>

- <span data-ttu-id="53b65-116">Faible</span><span class="sxs-lookup"><span data-stu-id="53b65-116">Low</span></span>
- <span data-ttu-id="53b65-117">Normal (valeur par défaut)</span><span class="sxs-lookup"><span data-stu-id="53b65-117">Normal (Default)</span></span>
- <span data-ttu-id="53b65-118">Élevé</span><span class="sxs-lookup"><span data-stu-id="53b65-118">High</span></span>

<span data-ttu-id="53b65-119">Exemples d'appareils à attribuer à une valeur élevée :</span><span class="sxs-lookup"><span data-stu-id="53b65-119">Examples of devices that should be assigned a high value:</span></span>

- <span data-ttu-id="53b65-120">Contrôleurs de domaine, Active Directory</span><span class="sxs-lookup"><span data-stu-id="53b65-120">Domain controllers, Active Directory</span></span>
- <span data-ttu-id="53b65-121">Appareils connectés à Internet</span><span class="sxs-lookup"><span data-stu-id="53b65-121">Internet facing devices</span></span>
- <span data-ttu-id="53b65-122">Périphériques VIP</span><span class="sxs-lookup"><span data-stu-id="53b65-122">VIP devices</span></span>
- <span data-ttu-id="53b65-123">Appareils hébergeant des services de production internes/externes</span><span class="sxs-lookup"><span data-stu-id="53b65-123">Devices hosting internal/external production services</span></span>

## <a name="choose-device-value"></a><span data-ttu-id="53b65-124">Choisir la valeur de l'appareil</span><span class="sxs-lookup"><span data-stu-id="53b65-124">Choose device value</span></span>

1. <span data-ttu-id="53b65-125">Accédez à n'importe quelle page d'appareil. L'endroit le plus simple est de consulter l'inventaire des appareils.</span><span class="sxs-lookup"><span data-stu-id="53b65-125">Navigate to any device page, the easiest place is from the device inventory.</span></span>

2. <span data-ttu-id="53b65-126">Sélectionnez **la valeur de** l'appareil à trois points près de la barre d'actions en haut de la page.</span><span class="sxs-lookup"><span data-stu-id="53b65-126">Select **Device value** from three dots next to the actions bar at the top of the page.</span></span>

    ![Exemple de la valeur de l'appareil.](images/tvm-device-value-dropdown.png)

3. <span data-ttu-id="53b65-128">Un volant s'affiche avec la valeur actuelle de l'appareil et sa valeur.</span><span class="sxs-lookup"><span data-stu-id="53b65-128">A flyout will appear with the current device value and what it means.</span></span> <span data-ttu-id="53b65-129">Examinez la valeur de l'appareil et choisissez celle qui convient le mieux à votre appareil.</span><span class="sxs-lookup"><span data-stu-id="53b65-129">Review the value of the device and choose the one that best fits your device.</span></span>
<span data-ttu-id="53b65-130">![Exemple de volant de valeur d'appareil.](images/tvm-device-value-flyout.png)</span><span class="sxs-lookup"><span data-stu-id="53b65-130">![Example of the device value flyout.](images/tvm-device-value-flyout.png)</span></span>

## <a name="how-device-value-impacts-your-exposure-score"></a><span data-ttu-id="53b65-131">Impact de la valeur de l'appareil sur votre score d'exposition</span><span class="sxs-lookup"><span data-stu-id="53b65-131">How device value impacts your exposure score</span></span>

<span data-ttu-id="53b65-132">Le score d'exposition est une moyenne pondérée sur tous les appareils.</span><span class="sxs-lookup"><span data-stu-id="53b65-132">The exposure score is a weighted average across all devices.</span></span> <span data-ttu-id="53b65-133">Si vous avez des groupes d'appareils, vous pouvez également filtrer le score par groupe d'appareils.</span><span class="sxs-lookup"><span data-stu-id="53b65-133">If you have device groups, you can also filter the score by device group.</span></span>

- <span data-ttu-id="53b65-134">Les appareils normaux ont un poids de 1</span><span class="sxs-lookup"><span data-stu-id="53b65-134">Normal devices have a weight of 1</span></span>
- <span data-ttu-id="53b65-135">Les appareils à faible valeur ont un poids de 0,75</span><span class="sxs-lookup"><span data-stu-id="53b65-135">Low value devices have a weight of 0.75</span></span>
- <span data-ttu-id="53b65-136">Les appareils à valeur élevée ont un poids de NumberOfAssets / 10.</span><span class="sxs-lookup"><span data-stu-id="53b65-136">High value devices have a weight of NumberOfAssets / 10.</span></span>
    - <span data-ttu-id="53b65-137">Si vous avez 100 appareils, chaque appareil à valeur élevée aura un poids de 10 (100/10)</span><span class="sxs-lookup"><span data-stu-id="53b65-137">If you have 100 devices, each high value device will have a weight of 10 (100/10)</span></span>

## <a name="related-topics"></a><span data-ttu-id="53b65-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53b65-138">Related topics</span></span>

- [<span data-ttu-id="53b65-139">Vue d'ensemble de la gestion des menaces et des vulnérabilités</span><span class="sxs-lookup"><span data-stu-id="53b65-139">Threat and vulnerability management overview</span></span>](next-gen-threat-and-vuln-mgt.md)
- [<span data-ttu-id="53b65-140">Score d'exposition</span><span class="sxs-lookup"><span data-stu-id="53b65-140">Exposure Score</span></span>](tvm-exposure-score.md)
- [<span data-ttu-id="53b65-141">API</span><span class="sxs-lookup"><span data-stu-id="53b65-141">APIs</span></span>](next-gen-threat-and-vuln-mgt.md#apis)