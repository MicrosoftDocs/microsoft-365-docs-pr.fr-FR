---
title: Type de ressource Investigation
description: Entité Microsoft Defender for Endpoint Investigation.
keywords: api, api de graphique, api pris en charge, obtenir, alertes, enquêtes
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
ms.collection:
- m365-security-compliance
- m365initiative-defender-endpoint
ms.topic: article
ms.technology: mde
ms.openlocfilehash: 3872976717a5b472ab8d471db7eff9975dbc2258
ms.sourcegitcommit: 987f70e44e406ab6b1dd35f336a9d0c228032794
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/05/2021
ms.locfileid: "51587682"
---
# <a name="investigation-resource-type"></a><span data-ttu-id="21749-104">Type de ressource Investigation</span><span class="sxs-lookup"><span data-stu-id="21749-104">Investigation resource type</span></span>

[!INCLUDE [Microsoft 365 Defender rebranding](../../includes/microsoft-defender.md)]

<span data-ttu-id="21749-105">**S’applique à :**</span><span class="sxs-lookup"><span data-stu-id="21749-105">**Applies to:**</span></span>
- [<span data-ttu-id="21749-106">Microsoft Defender pour point de terminaison</span><span class="sxs-lookup"><span data-stu-id="21749-106">Microsoft Defender for Endpoint</span></span>](https://go.microsoft.com/fwlink/p/?linkid=2154037)
- [<span data-ttu-id="21749-107">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="21749-107">Microsoft 365 Defender</span></span>](https://go.microsoft.com/fwlink/?linkid=2118804)

> <span data-ttu-id="21749-108">Vous souhaitez faire l’expérience de Defender pour point de terminaison ?</span><span class="sxs-lookup"><span data-stu-id="21749-108">Want to experience Defender for Endpoint?</span></span> [<span data-ttu-id="21749-109">Inscrivez-vous à un essai gratuit.</span><span class="sxs-lookup"><span data-stu-id="21749-109">Sign up for a free trial.</span></span>](https://www.microsoft.com/microsoft-365/windows/microsoft-defender-atp?ocid=docs-wdatp-exposedapis-abovefoldlink) 

[!include[Microsoft Defender for Endpoint API URIs for US Government](../../includes/microsoft-defender-api-usgov.md)]

[!include[Improve request performance](../../includes/improve-request-performance.md)]

<span data-ttu-id="21749-110">Représente une entité d’investigation automatisée dans Defender pour le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="21749-110">Represent an Automated Investigation entity in Defender for Endpoint.</span></span>
<br> <span data-ttu-id="21749-111">Pour plus [d’informations, voir Vue d’ensemble des enquêtes](automated-investigations.md) automatisées.</span><span class="sxs-lookup"><span data-stu-id="21749-111">See [Overview of automated investigations](automated-investigations.md) for more information.</span></span>

## <a name="methods"></a><span data-ttu-id="21749-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="21749-112">Methods</span></span>
<span data-ttu-id="21749-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="21749-113">Method</span></span>|<span data-ttu-id="21749-114">Type renvoyé</span><span class="sxs-lookup"><span data-stu-id="21749-114">Return Type</span></span> |<span data-ttu-id="21749-115">Description</span><span class="sxs-lookup"><span data-stu-id="21749-115">Description</span></span>
:---|:---|:---
[<span data-ttu-id="21749-116">Examens de liste</span><span class="sxs-lookup"><span data-stu-id="21749-116">List Investigations</span></span>](get-investigation-collection.md) | <span data-ttu-id="21749-117">Collection d’examens</span><span class="sxs-lookup"><span data-stu-id="21749-117">Investigation collection</span></span> | <span data-ttu-id="21749-118">Obtenir une collection d’examens</span><span class="sxs-lookup"><span data-stu-id="21749-118">Get collection of Investigation</span></span>
[<span data-ttu-id="21749-119">Obtenir un examen unique</span><span class="sxs-lookup"><span data-stu-id="21749-119">Get single Investigation</span></span>](get-investigation-object.md) | <span data-ttu-id="21749-120">Entité Investigation</span><span class="sxs-lookup"><span data-stu-id="21749-120">Investigation entity</span></span> | <span data-ttu-id="21749-121">Obtient une entité Investigation unique.</span><span class="sxs-lookup"><span data-stu-id="21749-121">Gets single Investigation entity.</span></span>
[<span data-ttu-id="21749-122">Démarrer l’examen</span><span class="sxs-lookup"><span data-stu-id="21749-122">Start Investigation</span></span>](initiate-autoir-investigation.md) | <span data-ttu-id="21749-123">Entité Investigation</span><span class="sxs-lookup"><span data-stu-id="21749-123">Investigation entity</span></span> | <span data-ttu-id="21749-124">Démarre l’examen sur un appareil.</span><span class="sxs-lookup"><span data-stu-id="21749-124">Starts Investigation on a device.</span></span>


## <a name="properties"></a><span data-ttu-id="21749-125">Propriétés</span><span class="sxs-lookup"><span data-stu-id="21749-125">Properties</span></span>
<span data-ttu-id="21749-126">Propriété</span><span class="sxs-lookup"><span data-stu-id="21749-126">Property</span></span> |  <span data-ttu-id="21749-127">Type</span><span class="sxs-lookup"><span data-stu-id="21749-127">Type</span></span>    |   <span data-ttu-id="21749-128">Description</span><span class="sxs-lookup"><span data-stu-id="21749-128">Description</span></span>
:---|:---|:---
<span data-ttu-id="21749-129">id</span><span class="sxs-lookup"><span data-stu-id="21749-129">id</span></span> | <span data-ttu-id="21749-130">Chaîne</span><span class="sxs-lookup"><span data-stu-id="21749-130">String</span></span> | <span data-ttu-id="21749-131">Identité de l’entité d’investigation.</span><span class="sxs-lookup"><span data-stu-id="21749-131">Identity of the investigation entity.</span></span> 
<span data-ttu-id="21749-132">startTime</span><span class="sxs-lookup"><span data-stu-id="21749-132">startTime</span></span> | <span data-ttu-id="21749-133">DateTime Nullable</span><span class="sxs-lookup"><span data-stu-id="21749-133">DateTime Nullable</span></span> | <span data-ttu-id="21749-134">Date et heure de création de l’enquête.</span><span class="sxs-lookup"><span data-stu-id="21749-134">The date and time when the investigation was created.</span></span> 
<span data-ttu-id="21749-135">endTime</span><span class="sxs-lookup"><span data-stu-id="21749-135">endTime</span></span> | <span data-ttu-id="21749-136">DateTime Nullable</span><span class="sxs-lookup"><span data-stu-id="21749-136">DateTime Nullable</span></span> | <span data-ttu-id="21749-137">Date et heure de fin de l’enquête.</span><span class="sxs-lookup"><span data-stu-id="21749-137">The date and time when the investigation was completed.</span></span> 
<span data-ttu-id="21749-138">cancelledBy</span><span class="sxs-lookup"><span data-stu-id="21749-138">cancelledBy</span></span> | <span data-ttu-id="21749-139">Chaîne</span><span class="sxs-lookup"><span data-stu-id="21749-139">String</span></span> | <span data-ttu-id="21749-140">ID de l’utilisateur/de l’application qui a annulé cet examen.</span><span class="sxs-lookup"><span data-stu-id="21749-140">The ID of the user/application that canceled that investigation.</span></span> 
<span data-ttu-id="21749-141">investigationState</span><span class="sxs-lookup"><span data-stu-id="21749-141">investigationState</span></span> | <span data-ttu-id="21749-142">Énum</span><span class="sxs-lookup"><span data-stu-id="21749-142">Enum</span></span> | <span data-ttu-id="21749-143">État actuel de l’enquête.</span><span class="sxs-lookup"><span data-stu-id="21749-143">The current state of the investigation.</span></span> <span data-ttu-id="21749-144">Les valeurs possibles sont : « Unknown » (inconnu), « Terminated » (terminé), « SuccessfullyRemediated », 'Suppress', 'Failed', 'PartiallyRemediated', 'Running', 'PendingApproval', 'PendingResource', 'PartiallySystemigated', 'TerminatedByUser', 'TerminatedBySystem', 'Queued', 'InnerFailure', 'PreexistingAlert', 'UnsupportedOs', 'UnsupportedAlertType', 'SuppressedAlert'.</span><span class="sxs-lookup"><span data-stu-id="21749-144">Possible values are: 'Unknown', 'Terminated', 'SuccessfullyRemediated', 'Benign', 'Failed', 'PartiallyRemediated', 'Running', 'PendingApproval', 'PendingResource', 'PartiallyInvestigated', 'TerminatedByUser', 'TerminatedBySystem', 'Queued', 'InnerFailure', 'PreexistingAlert', 'UnsupportedOs', 'UnsupportedAlertType', 'SuppressedAlert'.</span></span>
<span data-ttu-id="21749-145">statusDetails</span><span class="sxs-lookup"><span data-stu-id="21749-145">statusDetails</span></span> | <span data-ttu-id="21749-146">Chaîne</span><span class="sxs-lookup"><span data-stu-id="21749-146">String</span></span> | <span data-ttu-id="21749-147">Informations supplémentaires sur l’état de l’enquête.</span><span class="sxs-lookup"><span data-stu-id="21749-147">Additional information about the state of the investigation.</span></span>
<span data-ttu-id="21749-148">machineId</span><span class="sxs-lookup"><span data-stu-id="21749-148">machineId</span></span> | <span data-ttu-id="21749-149">Chaîne</span><span class="sxs-lookup"><span data-stu-id="21749-149">String</span></span> | <span data-ttu-id="21749-150">ID de l’appareil sur lequel l’enquête est exécutée.</span><span class="sxs-lookup"><span data-stu-id="21749-150">The ID of the device on which the investigation is executed.</span></span>
<span data-ttu-id="21749-151">computerDnsName</span><span class="sxs-lookup"><span data-stu-id="21749-151">computerDnsName</span></span> | <span data-ttu-id="21749-152">Chaîne</span><span class="sxs-lookup"><span data-stu-id="21749-152">String</span></span> | <span data-ttu-id="21749-153">Nom de l’appareil sur lequel l’enquête est exécutée.</span><span class="sxs-lookup"><span data-stu-id="21749-153">The name of the device on which the investigation is executed.</span></span>
<span data-ttu-id="21749-154">triggeringAlertId</span><span class="sxs-lookup"><span data-stu-id="21749-154">triggeringAlertId</span></span> | <span data-ttu-id="21749-155">Chaîne</span><span class="sxs-lookup"><span data-stu-id="21749-155">String</span></span> | <span data-ttu-id="21749-156">ID de l’alerte qui a déclenché l’enquête.</span><span class="sxs-lookup"><span data-stu-id="21749-156">The ID of the alert that triggered the investigation.</span></span>


## <a name="json-representation"></a><span data-ttu-id="21749-157">Représentation Json</span><span class="sxs-lookup"><span data-stu-id="21749-157">Json representation</span></span>

```json
{
    "id": "63004",
    "startTime": "2020-01-06T13:05:15Z",
    "endTime": null,
    "state": "Running",
    "cancelledBy": null,
    "statusDetails": null,
    "machineId": "e828a0624ed33f919db541065190d2f75e50a071",
    "computerDnsName": "desktop-test123",
    "triggeringAlertId": "da637139127150012465_1011995739"
}
```
