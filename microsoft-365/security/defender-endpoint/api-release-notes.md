---
title: Notes de publication de l’API Microsoft Defender for Endpoint
description: Notes de publication pour les mises à jour de l’ensemble d’API Microsoft Defender for Endpoint.
keywords: notes de publication de l’api microsoft defender pour le point de terminaison, mde, api, api mdatp, mises à jour, notes, publication
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
ms.openlocfilehash: e37841fa17a5998c431c6a76b878f20ef1b06d10
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51061806"
---
# <a name="microsoft-defender-for-endpoint-api-release-notes"></a><span data-ttu-id="0f433-104">Notes de publication de l’API Microsoft Defender for Endpoint</span><span class="sxs-lookup"><span data-stu-id="0f433-104">Microsoft Defender for Endpoint API release notes</span></span>

<span data-ttu-id="0f433-105">**S’applique à :** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span><span class="sxs-lookup"><span data-stu-id="0f433-105">**Applies to:** [Microsoft Defender for Endpoint](https://go.microsoft.com/fwlink/?linkid=2154037)</span></span>

- <span data-ttu-id="0f433-106">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="0f433-106">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="0f433-107">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="0f433-107">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

<span data-ttu-id="0f433-108">Les informations suivantes répertorient les mises à jour des API Microsoft Defender for Endpoint et les dates de leur mise à jour.</span><span class="sxs-lookup"><span data-stu-id="0f433-108">The following information lists the updates made to the Microsoft Defender for Endpoint APIs and the dates they were made.</span></span>


> [!TIP]
> <span data-ttu-id="0f433-109">Flux RSS : recevez une notification lorsque cette page est mise à jour en copiant et en coller l’URL suivante dans votre lecteur de flux :</span><span class="sxs-lookup"><span data-stu-id="0f433-109">RSS feed: Get notified when this page is updated by copying and pasting the following URL into your feed reader:</span></span> 
>```
>https://docs.microsoft.com/api/search/rss?search=%22Release+notes+for+updates+made+to+the+Microsoft+Defender+for+Endpoint+set+of+APIs%22&locale=en-us&facet=&%24filter=scopes%2Fany%28t%3A+t+eq+%27Windows+10%27%29
>```


### <a name="10022021"></a><span data-ttu-id="0f433-110">10.02.2021</span><span class="sxs-lookup"><span data-stu-id="0f433-110">10.02.2021</span></span>
<hr>

- <span data-ttu-id="0f433-111">Ajout d’une nouvelle API : [alertes de mise à jour par lot.](batch-update-alerts.md)</span><span class="sxs-lookup"><span data-stu-id="0f433-111">Added new API: [Batch update alerts](batch-update-alerts.md).</span></span> 

<br>

### <a name="25012021"></a><span data-ttu-id="0f433-112">25.01.2021</span><span class="sxs-lookup"><span data-stu-id="0f433-112">25.01.2021</span></span>
<hr>

- <span data-ttu-id="0f433-113">Limitations de taux mises à jour pour [l’API](run-advanced-query-api.md) de recherche avancée de 15 à 45 demandes par minute.</span><span class="sxs-lookup"><span data-stu-id="0f433-113">Updated rate limitations for [Advanced Hunting API](run-advanced-query-api.md) from 15 to 45 requests per minute.</span></span> 

<br>

### <a name="21012021"></a><span data-ttu-id="0f433-114">21.01.2021</span><span class="sxs-lookup"><span data-stu-id="0f433-114">21.01.2021</span></span>
<hr>

- <span data-ttu-id="0f433-115">Ajout d’une nouvelle API : [rechercher des appareils par balise.](machine-tags.md)</span><span class="sxs-lookup"><span data-stu-id="0f433-115">Added new API: [Find devices by tag](machine-tags.md).</span></span> 
- <span data-ttu-id="0f433-116">Ajout d’une nouvelle API : [importer des indicateurs.](import-ti-indicators.md)</span><span class="sxs-lookup"><span data-stu-id="0f433-116">Added new API: [Import Indicators](import-ti-indicators.md).</span></span> 

<br>

### <a name="03012021"></a><span data-ttu-id="0f433-117">03.01.2021</span><span class="sxs-lookup"><span data-stu-id="0f433-117">03.01.2021</span></span>
<hr>

- <span data-ttu-id="0f433-118">Preuve d’alerte mise à jour : ajout des propriétés ***detectionStatus** _, _*_parentProcessFilePath_*_ et _ *_parentProcessFileName_** .</span><span class="sxs-lookup"><span data-stu-id="0f433-118">Updated Alert evidence: added ***detectionStatus** _, _*_parentProcessFilePath_*_ and _ *_parentProcessFileName_** properties.</span></span>
- <span data-ttu-id="0f433-119">Entité [Alert mise à jour :](alerts.md)ajout de la propriété ***détecteurId.***</span><span class="sxs-lookup"><span data-stu-id="0f433-119">Updated [Alert entity](alerts.md): added ***detectorId*** property.</span></span>

<br>

### <a name="15122020"></a><span data-ttu-id="0f433-120">15.12.2020</span><span class="sxs-lookup"><span data-stu-id="0f433-120">15.12.2020</span></span>
<hr>

- <span data-ttu-id="0f433-121">Entité [Device](machine.md) mise à jour : liste ***IpInterfaces*** ajoutée.</span><span class="sxs-lookup"><span data-stu-id="0f433-121">Updated [Device](machine.md) entity: added ***IpInterfaces*** list.</span></span> <span data-ttu-id="0f433-122">Voir [Les appareils de liste.](get-machines.md)</span><span class="sxs-lookup"><span data-stu-id="0f433-122">See [List devices](get-machines.md).</span></span>

<br>

### <a name="04112020"></a><span data-ttu-id="0f433-123">04.11.2020</span><span class="sxs-lookup"><span data-stu-id="0f433-123">04.11.2020</span></span>
<hr>

- <span data-ttu-id="0f433-124">Ajout d’une nouvelle API : [définir la valeur de l’appareil.](set-device-value.md)</span><span class="sxs-lookup"><span data-stu-id="0f433-124">Added new API: [Set device value](set-device-value.md).</span></span>
- <span data-ttu-id="0f433-125">Entité [Device](machine.md) mise à jour : ajout de ***la propriété deviceValue.***</span><span class="sxs-lookup"><span data-stu-id="0f433-125">Updated [Device](machine.md) entity: added ***deviceValue*** property.</span></span>

<br>

### <a name="01092020"></a><span data-ttu-id="0f433-126">01.09.2020</span><span class="sxs-lookup"><span data-stu-id="0f433-126">01.09.2020</span></span>
<hr>

- <span data-ttu-id="0f433-127">Ajout d’une option pour développer l’entité Alerte avec sa preuve associée.</span><span class="sxs-lookup"><span data-stu-id="0f433-127">Added option to expand the Alert entity with its related Evidence.</span></span> <span data-ttu-id="0f433-128">Voir [Alertes de liste.](get-alerts.md)</span><span class="sxs-lookup"><span data-stu-id="0f433-128">See [List Alerts](get-alerts.md).</span></span>

<br>
<br>