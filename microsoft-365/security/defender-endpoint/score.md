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
ms.technology: mde
ms.openlocfilehash: 1c287a72318cfb2e6e4e3860ac90a90e561040fe
ms.sourcegitcommit: 582555d2b4ef5f2e2494ffdeab2c1d49e5d6b724
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/01/2021
ms.locfileid: "51500954"
---
# <a name="score-resource-type"></a><span data-ttu-id="d29ba-104">Type de ressource Score</span><span class="sxs-lookup"><span data-stu-id="d29ba-104">Score resource type</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="d29ba-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="d29ba-105">**Applies to:**</span></span>
- [<span data-ttu-id="d29ba-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="d29ba-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/?linkid=2154037)
- [<span data-ttu-id="d29ba-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="d29ba-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="d29ba-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="d29ba-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="d29ba-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="d29ba-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]


[!include[Prerelease information](../../includes/prerelease.md)]

## <a name="methods"></a><span data-ttu-id="d29ba-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d29ba-110">Methods</span></span>

<span data-ttu-id="d29ba-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="d29ba-111">Method</span></span> |<span data-ttu-id="d29ba-112">Type renvoyé</span><span class="sxs-lookup"><span data-stu-id="d29ba-112">Return Type</span></span> |<span data-ttu-id="d29ba-113">Description</span><span class="sxs-lookup"><span data-stu-id="d29ba-113">Description</span></span>
:---|:---|:---
[<span data-ttu-id="d29ba-114">Obtenir un score d'exposition</span><span class="sxs-lookup"><span data-stu-id="d29ba-114">Get exposure score</span></span>](get-exposure-score.md) | [<span data-ttu-id="d29ba-115">Score</span><span class="sxs-lookup"><span data-stu-id="d29ba-115">Score</span></span>](score.md) | <span data-ttu-id="d29ba-116">Obtenir le score d’exposition de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="d29ba-116">Get the organizational exposure score.</span></span>
[<span data-ttu-id="d29ba-117">Obtenir un score sécurisé d’appareil</span><span class="sxs-lookup"><span data-stu-id="d29ba-117">Get device secure score</span></span>](get-device-secure-score.md) | [<span data-ttu-id="d29ba-118">Score</span><span class="sxs-lookup"><span data-stu-id="d29ba-118">Score</span></span>](score.md) | <span data-ttu-id="d29ba-119">Obtenez le score de sécurité de l’appareil de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="d29ba-119">Get the organizational device secure score.</span></span>
[<span data-ttu-id="d29ba-120">Liste du score d’exposition par groupe d’appareils</span><span class="sxs-lookup"><span data-stu-id="d29ba-120">List exposure score by device group</span></span>](get-machine-group-exposure-score.md)| [<span data-ttu-id="d29ba-121">Score</span><span class="sxs-lookup"><span data-stu-id="d29ba-121">Score</span></span>](score.md) | <span data-ttu-id="d29ba-122">Liste des scores par groupe d’appareils.</span><span class="sxs-lookup"><span data-stu-id="d29ba-122">List scores by device group.</span></span>

## <a name="properties"></a><span data-ttu-id="d29ba-123">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d29ba-123">Properties</span></span>

<span data-ttu-id="d29ba-124">Propriété</span><span class="sxs-lookup"><span data-stu-id="d29ba-124">Property</span></span> |  <span data-ttu-id="d29ba-125">Type</span><span class="sxs-lookup"><span data-stu-id="d29ba-125">Type</span></span>    |   <span data-ttu-id="d29ba-126">Description</span><span class="sxs-lookup"><span data-stu-id="d29ba-126">Description</span></span>
:---|:---|:---
<span data-ttu-id="d29ba-127">Niveau</span><span class="sxs-lookup"><span data-stu-id="d29ba-127">Score</span></span> | <span data-ttu-id="d29ba-128">Double</span><span class="sxs-lookup"><span data-stu-id="d29ba-128">Double</span></span> | <span data-ttu-id="d29ba-129">Score actuel.</span><span class="sxs-lookup"><span data-stu-id="d29ba-129">The current score.</span></span>
<span data-ttu-id="d29ba-130">Temps</span><span class="sxs-lookup"><span data-stu-id="d29ba-130">Time</span></span> | <span data-ttu-id="d29ba-131">Date/heure</span><span class="sxs-lookup"><span data-stu-id="d29ba-131">DateTime</span></span> | <span data-ttu-id="d29ba-132">Date et heure à laquelle l’appel de cette API a été effectué.</span><span class="sxs-lookup"><span data-stu-id="d29ba-132">The date and time in which the call for this API was made.</span></span>
<span data-ttu-id="d29ba-133">RbacGroupName</span><span class="sxs-lookup"><span data-stu-id="d29ba-133">RbacGroupName</span></span> | <span data-ttu-id="d29ba-134">Chaîne</span><span class="sxs-lookup"><span data-stu-id="d29ba-134">String</span></span> | <span data-ttu-id="d29ba-135">Nom du groupe d’appareils.</span><span class="sxs-lookup"><span data-stu-id="d29ba-135">The device group name.</span></span>
