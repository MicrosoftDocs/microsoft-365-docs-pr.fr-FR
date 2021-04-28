---
title: Notes de publication de l'API Microsoft Defender for Endpoint
description: Notes de publication pour les mises à jour de l'ensemble d'API Microsoft Defender for Endpoint.
keywords: Notes de publication de l'API Microsoft Defender pour endpoint, mde, API, API Microsoft Defender pour point de terminaison, mises à jour, notes, publication
search.product: eADQiWindows 10XVcnh
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
ms.topic: article
ms.technology: mde
ms.openlocfilehash: 5093bf64614f30c7daa145484453d7c9000ef2c7
ms.sourcegitcommit: e5b1a900043e2e41650ea1cbf4227043729c6053
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/27/2021
ms.locfileid: "52060884"
---
# <a name="microsoft-defender-for-endpoint-api-release-notes"></a><span data-ttu-id="82ef5-104">Notes de publication de l'API Microsoft Defender for Endpoint</span><span class="sxs-lookup"><span data-stu-id="82ef5-104">Microsoft Defender for Endpoint API release notes</span></span>

<span data-ttu-id="82ef5-105">**S'applique à :** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span><span class="sxs-lookup"><span data-stu-id="82ef5-105">**Applies to:** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span></span>

- <span data-ttu-id="82ef5-106">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="82ef5-106">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="82ef5-107">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="82ef5-107">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink)

<span data-ttu-id="82ef5-108">Les informations suivantes répertorient les mises à jour des API Microsoft Defender for Endpoint et les dates de leur mise à jour.</span><span class="sxs-lookup"><span data-stu-id="82ef5-108">The following information lists the updates made to the Microsoft Defender for Endpoint APIs and the dates they were made.</span></span>

> [!TIP]
> <span data-ttu-id="82ef5-109">Flux RSS : recevez une notification lorsque cette page est mise à jour en copiant et en coller l'URL suivante dans votre lecteur de flux :</span><span class="sxs-lookup"><span data-stu-id="82ef5-109">RSS feed: Get notified when this page is updated by copying and pasting the following URL into your feed reader:</span></span>
>
> ```http
> https://docs.microsoft.com/api/search/rss?search=%22Release+notes+for+updates+made+to+the+Microsoft+Defender+for+Endpoint+set+of+APIs%22&locale=en-us&facet=&%24filter=scopes%2Fany%28t%3A+t+eq+%27Windows+10%27%29
> ```


## <a name="release-notes---newest-to-oldest"></a><span data-ttu-id="82ef5-110">Notes de publication - plus récent à plus ancien</span><span class="sxs-lookup"><span data-stu-id="82ef5-110">Release notes - newest to oldest</span></span>

### <a name="23042021"></a><span data-ttu-id="82ef5-111">23.04.2021</span><span class="sxs-lookup"><span data-stu-id="82ef5-111">23.04.2021</span></span>

- <span data-ttu-id="82ef5-112">Ajout d'une nouvelle API : [méthodes et propriétés d'activité de correction.](get-remediation-methods-properties.md)</span><span class="sxs-lookup"><span data-stu-id="82ef5-112">Added new API: [Remediation activity methods and properties](get-remediation-methods-properties.md).</span></span>

### <a name="10022021"></a><span data-ttu-id="82ef5-113">10.02.2021</span><span class="sxs-lookup"><span data-stu-id="82ef5-113">10.02.2021</span></span>

- <span data-ttu-id="82ef5-114">Ajout d'une nouvelle API : [alertes de mise à jour par lot.](batch-update-alerts.md)</span><span class="sxs-lookup"><span data-stu-id="82ef5-114">Added new API: [Batch update alerts](batch-update-alerts.md).</span></span>

### <a name="25012021"></a><span data-ttu-id="82ef5-115">25.01.2021</span><span class="sxs-lookup"><span data-stu-id="82ef5-115">25.01.2021</span></span>

- <span data-ttu-id="82ef5-116">Limitations de taux mises à jour pour [l'API](run-advanced-query-api.md) de recherche avancée de 15 à 45 demandes par minute.</span><span class="sxs-lookup"><span data-stu-id="82ef5-116">Updated rate limitations for [Advanced Hunting API](run-advanced-query-api.md) from 15 to 45 requests per minute.</span></span>

### <a name="21012021"></a><span data-ttu-id="82ef5-117">21.01.2021</span><span class="sxs-lookup"><span data-stu-id="82ef5-117">21.01.2021</span></span>

- <span data-ttu-id="82ef5-118">Ajout d'une nouvelle API : [rechercher des appareils par balise.](machine-tags.md)</span><span class="sxs-lookup"><span data-stu-id="82ef5-118">Added new API: [Find devices by tag](machine-tags.md).</span></span>
- <span data-ttu-id="82ef5-119">Ajout d'une nouvelle API : [importer des indicateurs.](import-ti-indicators.md)</span><span class="sxs-lookup"><span data-stu-id="82ef5-119">Added new API: [Import Indicators](import-ti-indicators.md).</span></span>

### <a name="03012021"></a><span data-ttu-id="82ef5-120">03.01.2021</span><span class="sxs-lookup"><span data-stu-id="82ef5-120">03.01.2021</span></span>

- <span data-ttu-id="82ef5-121">Preuve d'alerte mise à jour : ajout des propriétés ***detectionStatus** _, _*_parentProcessFilePath_*_ et _ *_parentProcessFileName_** .</span><span class="sxs-lookup"><span data-stu-id="82ef5-121">Updated Alert evidence: added ***detectionStatus** _, _*_parentProcessFilePath_*_ and _ *_parentProcessFileName_** properties.</span></span>
- <span data-ttu-id="82ef5-122">Entité [Alert mise à jour :](alerts.md)ajout de la propriété ***détecteurId.***</span><span class="sxs-lookup"><span data-stu-id="82ef5-122">Updated [Alert entity](alerts.md): added ***detectorId*** property.</span></span>

### <a name="15122020"></a><span data-ttu-id="82ef5-123">15.12.2020</span><span class="sxs-lookup"><span data-stu-id="82ef5-123">15.12.2020</span></span>

- <span data-ttu-id="82ef5-124">Entité [Device](machine.md) mise à jour : liste ***IpInterfaces*** ajoutée.</span><span class="sxs-lookup"><span data-stu-id="82ef5-124">Updated [Device](machine.md) entity: added ***IpInterfaces*** list.</span></span> <span data-ttu-id="82ef5-125">Voir [Les appareils de liste.](get-machines.md)</span><span class="sxs-lookup"><span data-stu-id="82ef5-125">See [List devices](get-machines.md).</span></span>

### <a name="04112020"></a><span data-ttu-id="82ef5-126">04.11.2020</span><span class="sxs-lookup"><span data-stu-id="82ef5-126">04.11.2020</span></span>

- <span data-ttu-id="82ef5-127">Ajout d'une nouvelle API : [définir la valeur de l'appareil.](set-device-value.md)</span><span class="sxs-lookup"><span data-stu-id="82ef5-127">Added new API: [Set device value](set-device-value.md).</span></span>
- <span data-ttu-id="82ef5-128">Entité [Device](machine.md) mise à jour : ajout de ***la propriété deviceValue.***</span><span class="sxs-lookup"><span data-stu-id="82ef5-128">Updated [Device](machine.md) entity: added ***deviceValue*** property.</span></span>

### <a name="01092020"></a><span data-ttu-id="82ef5-129">01.09.2020</span><span class="sxs-lookup"><span data-stu-id="82ef5-129">01.09.2020</span></span>

- <span data-ttu-id="82ef5-130">Ajout d'une option pour développer l'entité Alerte avec sa preuve associée.</span><span class="sxs-lookup"><span data-stu-id="82ef5-130">Added option to expand the Alert entity with its related Evidence.</span></span> <span data-ttu-id="82ef5-131">Voir [Alertes de liste.](get-alerts.md)</span><span class="sxs-lookup"><span data-stu-id="82ef5-131">See [List Alerts](get-alerts.md).</span></span>
