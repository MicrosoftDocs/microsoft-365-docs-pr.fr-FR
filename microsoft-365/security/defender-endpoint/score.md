---
title: Méthodes et propriétés du score
description: Récupère le score d’exposition de votre organisation, le score de sécurisation de l’appareil et le score d’exposition par groupe d’appareils
keywords: api, api de graphique, api pris en charge, score, score d’exposition, score de sécurité de l’appareil, score d’exposition par groupe d’appareils
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: dansimp
author: dansimp
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
MS.technology: mde
ms.custom: api
ms.openlocfilehash: 89012dce4aa5b74d09f071b23f7709b4bd0bf03c
ms.sourcegitcommit: 5d8de3e9ee5f52a3eb4206f690365bb108a3247b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "52771428"
---
# <a name="score-resource-type"></a><span data-ttu-id="1640b-104">Type de ressource Score</span><span class="sxs-lookup"><span data-stu-id="1640b-104">Score resource type</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="1640b-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="1640b-105">**Applies to:**</span></span>
- [<span data-ttu-id="1640b-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="1640b-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/?linkid=2154037)
- [<span data-ttu-id="1640b-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="1640b-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="1640b-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="1640b-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="1640b-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="1640b-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]


[!include[Prerelease information](../../includes/prerelease.md)]

## <a name="methods"></a><span data-ttu-id="1640b-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="1640b-110">Methods</span></span>

<span data-ttu-id="1640b-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="1640b-111">Method</span></span> |<span data-ttu-id="1640b-112">Type renvoyé</span><span class="sxs-lookup"><span data-stu-id="1640b-112">Return Type</span></span> |<span data-ttu-id="1640b-113">Description</span><span class="sxs-lookup"><span data-stu-id="1640b-113">Description</span></span>
:---|:---|:---
[<span data-ttu-id="1640b-114">Obtenir un score d'exposition</span><span class="sxs-lookup"><span data-stu-id="1640b-114">Get exposure score</span></span>](get-exposure-score.md) | [<span data-ttu-id="1640b-115">Score</span><span class="sxs-lookup"><span data-stu-id="1640b-115">Score</span></span>](score.md) | <span data-ttu-id="1640b-116">Obtenir le score d’exposition de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="1640b-116">Get the organizational exposure score.</span></span>
[<span data-ttu-id="1640b-117">Obtenir un score sécurisé d’appareil</span><span class="sxs-lookup"><span data-stu-id="1640b-117">Get device secure score</span></span>](get-device-secure-score.md) | [<span data-ttu-id="1640b-118">Score</span><span class="sxs-lookup"><span data-stu-id="1640b-118">Score</span></span>](score.md) | <span data-ttu-id="1640b-119">Obtenez le score de sécurité de l’appareil de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="1640b-119">Get the organizational device secure score.</span></span>
[<span data-ttu-id="1640b-120">Liste du score d’exposition par groupe d’appareils</span><span class="sxs-lookup"><span data-stu-id="1640b-120">List exposure score by device group</span></span>](get-machine-group-exposure-score.md)| [<span data-ttu-id="1640b-121">Score</span><span class="sxs-lookup"><span data-stu-id="1640b-121">Score</span></span>](score.md) | <span data-ttu-id="1640b-122">Liste des scores par groupe d’appareils.</span><span class="sxs-lookup"><span data-stu-id="1640b-122">List scores by device group.</span></span>

## <a name="properties"></a><span data-ttu-id="1640b-123">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1640b-123">Properties</span></span>

<span data-ttu-id="1640b-124">Propriété</span><span class="sxs-lookup"><span data-stu-id="1640b-124">Property</span></span> |  <span data-ttu-id="1640b-125">Type</span><span class="sxs-lookup"><span data-stu-id="1640b-125">Type</span></span>    |   <span data-ttu-id="1640b-126">Description</span><span class="sxs-lookup"><span data-stu-id="1640b-126">Description</span></span>
:---|:---|:---
<span data-ttu-id="1640b-127">Niveau</span><span class="sxs-lookup"><span data-stu-id="1640b-127">Score</span></span> | <span data-ttu-id="1640b-128">Double</span><span class="sxs-lookup"><span data-stu-id="1640b-128">Double</span></span> | <span data-ttu-id="1640b-129">Score actuel.</span><span class="sxs-lookup"><span data-stu-id="1640b-129">The current score.</span></span>
<span data-ttu-id="1640b-130">Temps</span><span class="sxs-lookup"><span data-stu-id="1640b-130">Time</span></span> | <span data-ttu-id="1640b-131">Date/heure</span><span class="sxs-lookup"><span data-stu-id="1640b-131">DateTime</span></span> | <span data-ttu-id="1640b-132">Date et heure à laquelle l’appel de cette API a été effectué.</span><span class="sxs-lookup"><span data-stu-id="1640b-132">The date and time in which the call for this API was made.</span></span>
<span data-ttu-id="1640b-133">RbacGroupName</span><span class="sxs-lookup"><span data-stu-id="1640b-133">RbacGroupName</span></span> | <span data-ttu-id="1640b-134">String</span><span class="sxs-lookup"><span data-stu-id="1640b-134">String</span></span> | <span data-ttu-id="1640b-135">Nom du groupe d’appareils.</span><span class="sxs-lookup"><span data-stu-id="1640b-135">The device group name.</span></span>
