---
title: Méthodes et propriétés de score
description: Récupère le score d’exposition de votre organisation, le score de sécurisation de l’appareil et le score d’exposition par groupe d’appareils
keywords: api, api de graphique, api pris en charge, score, score d’exposition, score de sécurité de l’appareil, score d’exposition par groupe d’appareils
search.product: eADQiWindows 10XVcnh
ms.prod: m365-security
ms.mktglfcycl: deploy
ms.sitesec: library
ms.pagetype: security
ms.author: ellevin
author: levinec
localization_priority: Normal
manager: dansimp
audience: ITPro
ms.collection: M365-security-compliance
ms.topic: article
ms.technology: mde
ms.openlocfilehash: 72dacca8529b54b082590d911f03aaa86bfe9097
ms.sourcegitcommit: 956176ed7c8b8427fdc655abcd1709d86da9447e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2021
ms.locfileid: "51200160"
---
# <a name="score-resource-type"></a><span data-ttu-id="af7c6-104">Type de ressource Score</span><span class="sxs-lookup"><span data-stu-id="af7c6-104">Score resource type</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]


<span data-ttu-id="af7c6-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="af7c6-105">**Applies to:**</span></span>
- [<span data-ttu-id="af7c6-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="af7c6-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/?linkid=2154037)
- [<span data-ttu-id="af7c6-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="af7c6-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="af7c6-108">Vous souhaitez découvrir Microsoft Defender pour le point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="af7c6-108">Want to experience Microsoft Defender for Endpoint?</span></span> [<span data-ttu-id="af7c6-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="af7c6-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]


[!include[Prerelease information](../../includes/prerelease.md)]

## <a name="methods"></a><span data-ttu-id="af7c6-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="af7c6-110">Methods</span></span>

<span data-ttu-id="af7c6-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="af7c6-111">Method</span></span> |<span data-ttu-id="af7c6-112">Type renvoyé</span><span class="sxs-lookup"><span data-stu-id="af7c6-112">Return Type</span></span> |<span data-ttu-id="af7c6-113">Description</span><span class="sxs-lookup"><span data-stu-id="af7c6-113">Description</span></span>
:---|:---|:---
[<span data-ttu-id="af7c6-114">Obtenir le score d’exposition</span><span class="sxs-lookup"><span data-stu-id="af7c6-114">Get exposure score</span></span>](get-exposure-score.md) | [<span data-ttu-id="af7c6-115">Score</span><span class="sxs-lookup"><span data-stu-id="af7c6-115">Score</span></span>](score.md) | <span data-ttu-id="af7c6-116">Obtenir le score d’exposition de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="af7c6-116">Get the organizational exposure score.</span></span>
[<span data-ttu-id="af7c6-117">Obtenir le score de sécurité de l’appareil</span><span class="sxs-lookup"><span data-stu-id="af7c6-117">Get device secure score</span></span>](get-device-secure-score.md) | [<span data-ttu-id="af7c6-118">Score</span><span class="sxs-lookup"><span data-stu-id="af7c6-118">Score</span></span>](score.md) | <span data-ttu-id="af7c6-119">Obtenez le score de sécurité de l’appareil de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="af7c6-119">Get the organizational device secure score.</span></span>
[<span data-ttu-id="af7c6-120">Liste du score d’exposition par groupe d’appareils</span><span class="sxs-lookup"><span data-stu-id="af7c6-120">List exposure score by device group</span></span>](get-machine-group-exposure-score.md)| [<span data-ttu-id="af7c6-121">Score</span><span class="sxs-lookup"><span data-stu-id="af7c6-121">Score</span></span>](score.md) | <span data-ttu-id="af7c6-122">Liste des scores par groupe d’appareils.</span><span class="sxs-lookup"><span data-stu-id="af7c6-122">List scores by device group.</span></span>

## <a name="properties"></a><span data-ttu-id="af7c6-123">Propriétés</span><span class="sxs-lookup"><span data-stu-id="af7c6-123">Properties</span></span>

<span data-ttu-id="af7c6-124">Propriété</span><span class="sxs-lookup"><span data-stu-id="af7c6-124">Property</span></span> |  <span data-ttu-id="af7c6-125">Type</span><span class="sxs-lookup"><span data-stu-id="af7c6-125">Type</span></span>    |   <span data-ttu-id="af7c6-126">Description</span><span class="sxs-lookup"><span data-stu-id="af7c6-126">Description</span></span>
:---|:---|:---
<span data-ttu-id="af7c6-127">Niveau</span><span class="sxs-lookup"><span data-stu-id="af7c6-127">Score</span></span> | <span data-ttu-id="af7c6-128">Double</span><span class="sxs-lookup"><span data-stu-id="af7c6-128">Double</span></span> | <span data-ttu-id="af7c6-129">Score actuel.</span><span class="sxs-lookup"><span data-stu-id="af7c6-129">The current score.</span></span>
<span data-ttu-id="af7c6-130">Temps</span><span class="sxs-lookup"><span data-stu-id="af7c6-130">Time</span></span> | <span data-ttu-id="af7c6-131">Date/heure</span><span class="sxs-lookup"><span data-stu-id="af7c6-131">DateTime</span></span> | <span data-ttu-id="af7c6-132">Date et heure à laquelle l’appel de cette API a été effectué.</span><span class="sxs-lookup"><span data-stu-id="af7c6-132">The date and time in which the call for this API was made.</span></span>
<span data-ttu-id="af7c6-133">RbacGroupName</span><span class="sxs-lookup"><span data-stu-id="af7c6-133">RbacGroupName</span></span> | <span data-ttu-id="af7c6-134">Chaîne</span><span class="sxs-lookup"><span data-stu-id="af7c6-134">String</span></span> | <span data-ttu-id="af7c6-135">Nom du groupe d’appareils.</span><span class="sxs-lookup"><span data-stu-id="af7c6-135">The device group name.</span></span>
